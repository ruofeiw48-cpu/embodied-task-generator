# Embodied Task Generator

A prompt-driven workflow for transforming spreadsheet-based task variants into standardized embodied AI task schemas and platform-ready import files.

---

## Overview

Embodied AI data production often requires large volumes of task variants to be standardized before annotation, collection, or platform import.

This project demonstrates a lightweight workflow that converts raw task variants from spreadsheets into structured task definitions with normalized environments, standardized labels, and import-ready outputs.

The workflow is designed to improve consistency, reduce manual effort, and support scalable embodied AI data generation.

---

## Key Capabilities

- Variant task parsing
- Task schema standardization
- Environment normalization
- Label JSON generation
- Duplicate detection support
- Platform-ready template generation
- Batch processing for spreadsheet inputs

---

## Workflow

```text
Spreadsheet Task Variants
            │
            ▼
Variant Parsing
            │
            ▼
Task Standardization Prompt
            │
            ▼
Structured Task Schema
            │
            ▼
Environment Mapping
            │
            ▼
Label Generation
            │
            ▼
Duplicate Check
            │
            ▼
Platform Import Template
            │
            ▼
Upload-ready Excel / JSON
```

---

## Architecture

```text
┌─────────────────────┐
│ Raw Task Variants   │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Variant Parser      │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Standardization     │
│ Prompt              │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Schema Generator    │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Environment Mapper  │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Label Generator     │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Duplicate Checker   │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│ Platform Exporter   │
└─────────────────────┘
```

---

## Example Input

| Task Name | Variant |
|------------|------------|
| Restock Medicine | Move two medicine boxes from storage to shelf A |
| Restock Medicine | Move three medicine boxes from storage to shelf B |

Example spreadsheet:

```csv
Task ID,Task Name,Variant
t1,Restock Medicine,Move two medicine boxes from storage to shelf A
t1,Restock Medicine,Move three medicine boxes from storage to shelf B
```

---

## Example Output

```json
{
  "任务名称": "补充药品-v01",
  "描述": "从储药箱中取出2盒药品摆放至指定货架",
  "环境": "healthcare",
  "任务类型": "Gripper,Dexterous Hand",
  "标签": {
    "工具使用": false,
    "标准用时": "≤4min",
    "灵巧度等级": "非灵巧"
  }
}
```

---

## Repository Structure

```text
embodied-task-generator/
├── README.md
├── SKILL.md
├── config.example.json
├── prompts/
│   └── variant-standardizer.txt
├── examples/
│   ├── input_example.csv
│   └── output_example.csv
```

---

## Task Schema

Each generated task contains the following standardized fields:

| Field | Description |
|---------|---------|
| 任务名称 | Task title |
| 描述 | Variant instruction |
| 初始状态 | Initial world state |
| 任务目标 | Completion criteria |
| 泛化方向 | Generalization dimensions |
| 任务类型 | Manipulation capability |
| 灵巧度标签 | Dexterity level |
| 环境 | Standardized environment |
| 标准用时档位 | Estimated completion time |
| 工具使用 | Tool usage flag |
| 精细工具使用 | Fine-tool usage flag |
| SOP操作说明 | Step-by-step procedure |
| 项目 | Project identifier |

---

## Environment Normalization

Supported environment categories:

```text
home
retail
logistics
factory
office
healthcare
education
hospitality
outdoor
construction
transit
sports
service
other
```

---

## Duplicate Detection

The workflow supports duplicate checking by:

- Exact text matching
- Variant comparison within the same task group
- Duplicate candidate review before export

This helps reduce redundant task generation during large-scale data production.

---

## Tech Stack

- Prompt Engineering
- LLM Workflow Design
- JSON Schema Design
- Data Standardization
- Spreadsheet Processing
- Structured Data Generation

---

## Use Cases

- Embodied AI data generation
- Manipulation task standardization
- Synthetic task creation workflows
- Data annotation preparation
- Dataset production pipelines
- Structured task export

---

## Disclaimer

This repository contains a sanitized demonstration workflow for educational and portfolio purposes.

No proprietary datasets, internal tools, customer information, platform credentials, or production assets are included.

---

## License

MIT License
