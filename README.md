# Repo of Engineered Prompts for Copilot in a Fabric environment focusing on Power BI and Fabric Notebook usage. 

# All prompts are stored in markdown files like the following and are named according to their intended tasks that the prompts will address. 

---
title: Suggested Tables
description: “Identify which tables you need based on business requirements”
tags: [data‑modeling, tables]
version: 1.0
---

**Input Variables**  
- `{{business_context}}`  
- `{{source_systems}}`

**Prompt**  
> “You are a data architect designing a Power BI semantic model for {{business_context}}.  
> Given these source systems: {{source_systems}}, list the top 5 tables you would include,  
> explain each table’s grain, and note any relationships you’d define.”

**Example Usage**  
```shell
copilot invoke --prompt-file prompts/data-modeling/suggested_tables.md \
               --var business_context="retail sales analysis" \
               --var source_systems="ERP, CRM"
