# Repo of Engineered Prompts for Copilot in a Fabric environment focusing on Power BI and Fabric Notebook usage. 
<img width="2502" height="268" alt="Copilot" src="https://github.com/user-attachments/assets/e99f1a2d-e3c5-401f-9829-cfac005b96a9" />
<img width="1244" height="1386" alt="Prompt Input" src="https://github.com/user-attachments/assets/958e0ce5-ab1c-48e7-bfb8-122b8d97bb33" />

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
