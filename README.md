# Embodied Task Generator

A prompt-driven workflow for converting spreadsheet-based task variants into standardized embodied AI task schemas and platform-ready import files.

## Overview

This project demonstrates a workflow for embodied AI data production. It standardizes task variants from spreadsheet inputs into structured task schemas, then maps them into a platform-ready import format.

The workflow covers:

- Variant task parsing
- Task schema standardization
- Environment normalization
- Label JSON generation
- Platform import template generation
- Basic duplicate detection logic

## Workflow

```text
Spreadsheet task variants
        ↓
Variant standardization prompt
        ↓
Standard task schema
        ↓
Platform import schema
        ↓
Upload-ready Excel / CSV
