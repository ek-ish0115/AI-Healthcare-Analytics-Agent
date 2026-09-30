# AI Healthcare Analytics Agent

An AI-powered healthcare operations analytics system built using n8n, Microsoft SQL Server, Google Gemini, JavaScript, and Gmail.

The system allows users to ask natural-language questions about healthcare operations and automatically generates data-driven insights from the healthcare database.

---

## Project Overview

The AI Healthcare Analytics Agent is designed to automate healthcare operations analysis.

Instead of manually writing SQL queries and calculating KPIs, a user can submit a healthcare-related question through an n8n form.

The system then:

1. Understands the user's question
2. Generates the required SQL query
3. Retrieves data from Microsoft SQL Server
4. Calculates healthcare KPIs
5. Analyzes trends
6. Detects potential anomalies
7. Generates an AI-based healthcare operations insight
8. Sends the analysis through Gmail

The project focuses on healthcare operations and analytics, not medical diagnosis or treatment recommendations.

---

## Problem Statement

Healthcare organizations generate large amounts of operational data across patients, admissions, departments, billing, diagnoses, medications, procedures, and mortality records.

Manually analyzing this information can require:

- Writing SQL queries
- Calculating KPIs
- Comparing monthly trends
- Identifying unusual patterns
- Preparing management reports

This project automates these analytical steps using an AI-powered n8n workflow.

---

## Objectives

The main objectives of the project are:

- Automate healthcare operational analysis
- Enable natural-language data queries
- Reduce manual SQL analysis
- Calculate important healthcare KPIs
- Analyze patient volume trends
- Detect potential operational anomalies
- Generate easy-to-understand AI insights
- Automate healthcare analytics reporting through email

---

## System Architecture

```text
User
  |
  v
n8n Web Form
  |
  v
AI Query Planner
  |
  v
Microsoft SQL Server
  |
  v
Healthcare KPI Calculation
  |
  v
Trend Analysis
  |
  v
Anomaly Detection
  |
  v
Operational Analysis
  |
  v
Healthcare Insight Agent
  |
  v
Gmail Automated Report
