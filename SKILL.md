---
name: embodied-task-generator
description: Transform spreadsheet-based task variants into standardized embodied AI task schemas and platform-ready import files.
---

# Embodied Task Generator
# 具身智能任务标准化工作流

## Overview | 项目简介

Embodied Task Generator is a prompt-driven workflow for converting spreadsheet-based task variants into standardized embodied AI task schemas.

Embodied Task Generator 是一个基于 Prompt 的任务标准化工作流，用于将 Excel 中的任务变体转换为标准化的具身智能任务 Schema，并生成平台可导入的数据格式。

The workflow focuses on:

- Task standardization
- Environment normalization
- Label generation
- Duplicate detection
- Structured export

主要解决：

- 任务标准化
- 环境归一化
- 标签生成
- 重复任务检测
- 平台导入格式生成

---

# Trigger Conditions
# 触发条件

Activate when:

- A spreadsheet containing task variants is provided
- The user requests task standardization
- The user requests batch task generation
- The user requests platform-ready task exports

满足以下情况时触发：

- 用户提供任务变体 Excel
- 用户要求任务标准化
- 用户要求批量任务生成
- 用户要求生成可导入平台的数据格式

---

# Core Principles
# 核心原则

## 1. One Variant = One Task
## 一个变体对应一个任务

Each task variant is converted into an independent task entry.

每条变体独立生成一个任务。

---

## 2. Description Preservation
## 保留原始描述

Task descriptions remain aligned with original variant instructions.

任务描述保持与原始变体指令一致。

---

## 3. Environment Normalization
## 环境归一化

Map user-defined environments into a standardized environment taxonomy.

将用户输入环境映射到统一环境体系。

Examples:

- home
- office
- retail
- healthcare
- hospitality
- logistics

例如：

- 家庭
- 办公
- 零售
- 医疗
- 酒店
- 仓储物流

---

## 4. Structured Task Schema
## 标准化任务结构

Each generated task contains:

每个任务包含：

- Task Name
- Description
- Goal
- Initial State
- Generalization Axes
- Task Type
- Environment
- Labels

即：

- 任务名称
- 描述
- 任务目标
- 初始状态
- 泛化方向
- 任务类型
- 环境
- 标签

---

## 5. Duplicate Prevention
## 查重机制

Detect duplicated or highly similar task variants before export.

导出前识别重复或高相似任务。

---

# Workflow
# 工作流程

Spreadsheet Task Variants

↓

Variant Parsing

↓

Task Standardization

↓

Environment Mapping

↓

Label Generation

↓

Duplicate Detection

↓

Platform-ready Export

对应中文：

Excel任务变体

↓

变体解析

↓

任务标准化

↓

环境归一化

↓

标签生成

↓

重复检测

↓

平台导出

---

# Input Format
# 输入格式

Expected spreadsheet fields:

标准输入字段：

| Field | Description |
|---------|---------|
| Task ID | Task Group ID |
| Task Name | Original Task Name |
| Variant Instruction | Task Variant |
| Generalization Reference | Generalization Hint |
| Materials | Required Objects |

---

# Output Format
# 输出格式

Generated structured task schema:

```json
{
  "task_name": "Restock Medicine-v01",
  "description": "...",
  "goal": "...",
  "initial_state": "...",
  "generalization_axes": "...",
  "task_type": "...",
  "environment": "...",
  "labels": {...}
}
```

# Key Features

## 核心能力

- Prompt-based task standardization
- Structured task schema generation
- Environment normalization
- Label JSON generation
- Duplicate detection support
- Batch task processing
- Platform-ready export

对应中文：

- Prompt驱动任务标准化
- 标准任务结构生成
- 环境归一化
- 标签生成
- 重复检测
- 批量任务处理
- 平台导出

---

# Repository Structure

```text
embodied-task-generator/
│
├── README.md
├── SKILL.md
├── config.example.json
│
├── prompts/
│   └── variant-standardizer.txt
│
├── examples/
│   ├── input_example.csv
│   └── output_example.csv
```

---

# Tech Stack

- Prompt Engineering
- Workflow Design
- JSON Schema Design
- Data Standardization
- Excel Processing

---

# License

MIT
