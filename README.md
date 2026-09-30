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

---

## Database

The project uses Microsoft SQL Server.

Database: HealthcareDB

The database contains the following tables:

- Patients
- Departments
- Admissions
- Billing
- Diagnoses
- Medications
- Procedures
- Mortality

---

## Database Relationships

The main relationships are:

Patients
   |
   +---- Admissions
   |       |
   |       +---- Departments
   |       +---- Billing
   |       +---- Diagnoses
   |       +---- Medications
   |       +---- Procedures
   |       +---- Mortality

Important relationships include:

- Patients.patient_id → Admissions.patient_id
- Departments.department_id → Admissions.department_id
- Admissions.admission_id → Billing.admission_id
- Admissions.admission_id → Diagnoses.admission_id
- Admissions.admission_id → Medications.admission_id
- Admissions.admission_id → Procedures.admission_id
- Admissions.admission_id → Mortality.admission_id

---

## Healthcare Tables

### Patients

Stores basic patient information.

Main fields include:

- patient_id
- first_name
- last_name
- date_of_birth
- gender
- city
- insurance_provider

### Departments

Stores hospital department information.

Main fields include:

- department_id
- department_name
- location
- capacity
- department_head

### Admissions

Stores patient admission information.

Main fields include:

- admission_id
- patient_id
- department_id
- admission_date
- discharge_date
- admission_type
- length_of_stay
- readmission
- attending_physician
- insurance_provider
- admission_status

### Billing

Stores hospital billing information.

### Diagnoses

Stores diagnosis information associated with patients and admissions.

### Medications

Stores medication usage information.

### Procedures

Stores medical procedure information.

### Mortality

Stores mortality-related records associated with patients and admissions.

---

## Key Analytics

The system can analyze healthcare operational metrics such as:

- Patient volume
- Admission count
- Average length of stay
- Readmission count
- Readmission rate
- Hospital charges
- Insurance-covered amount
- Patient responsibility
- Medication usage
- Procedure volume
- Mortality count
- Monthly patient trends

---

## Example Questions

Users can ask questions such as:

- Which department had the highest patient volume?
- What is the average length of stay?
- Show monthly patient volume trends.
- Which month had the highest patient volume?
- Which department has the highest readmission rate?
- Give me a complete healthcare operational summary.
- What are the top healthcare operational insights?

---

## Trend Analysis

The workflow analyzes monthly admission data.

It can identify:

- Highest patient-volume month
- Lowest patient-volume month
- Month-over-month changes
- Historical average patient volume
- Potential unusual months

The system uses available historical data rather than assuming that a single month represents a long-term trend.

---

## Anomaly Detection

The anomaly detection component uses historical patient-volume data.

The workflow calculates:

- Historical average
- Standard deviation
- Lower threshold
- Upper threshold

Months outside the calculated thresholds can be flagged as potential anomalies.

An anomaly indicates an unusual data pattern and does not automatically explain its cause.

---

## AI Analysis

Google Gemini is used for natural-language understanding and insight generation.

The AI receives calculated healthcare analytics and produces a readable response.

The AI is instructed to:

- Use only the provided data
- Avoid inventing numbers
- Explain results clearly
- Distinguish patterns from causation
- Avoid medical diagnosis or treatment recommendations
- Answer the user's actual question first

---

## Automated Reporting

The generated healthcare analysis can be sent through Gmail.

Example report structure:

AI Healthcare Analytics Report

Healthcare Analysis

[Generated healthcare insight]

Key Insights

[Important findings]

Trend & Anomaly Insights

[Trend and anomaly information]

This report was generated automatically by the AI Healthcare Analytics Agent.

---

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Microsoft SQL Server | Healthcare data storage |
| Google Gemini | AI query planning and insight generation |
| JavaScript | KPI calculations and data processing |
| Gmail | Automated reporting |
| GitHub | Project documentation and version control |

---

## Running n8n Locally

The project uses a local n8n installation to connect with the local Microsoft SQL Server database.

Start n8n using:

n8n start

Then open:

http://localhost:5678

---

## How to Use

### Step 1

Open the n8n healthcare analytics form.

### Step 2

Enter a healthcare operations question.

Example:

Which department had the highest patient volume?

### Step 3

Submit the form.

### Step 4

The workflow automatically processes the request.

### Step 5

The AI-generated analysis is displayed and can also be sent through Gmail.

---

## Sample Tested Results

The project has been tested with healthcare operational queries.

Example results include:

Emergency Department
Patient Volume: 1,976

Highest monthly patient volume:
December 2025 — 556 patients

Lowest monthly patient volume:
June 2024 — 415 patients

Daily operational example for December 31, 2025:

Patient Volume: 27
Admissions: 27
Readmissions: 4
Average Length of Stay: 5.63
Hospital Charges: $220,780.82
Medication Usage: 43
Procedures: 23
Mortality: 1

---

## Project Scope

This project focuses on healthcare operations analytics.

It is designed for:

- Healthcare operations teams
- Hospital management
- Healthcare analysts
- Business analysts
- Data analysts
- Management reporting

The system is not designed to provide:

- Medical diagnosis
- Treatment recommendations
- Clinical decision-making
- Individual medical advice

---

## Future Scope

Future enhancements could include:

- Patient demand forecasting
- Department capacity planning
- Appointment no-show prediction
- Readmission risk analytics
- Automated healthcare anomaly alerts
- Power BI integration
- Enterprise healthcare system integration
- Automated operational workflows

---

## Project Resources

- [Project Presentation](./AI_Healthcare_Analytics_Agent_ppt.pptx)
- [User Guide](./AI_Healthcare_Analytics_Agent_User_Guide.pdf)
- [n8n Workflow](./AI_Healthcare_Analytics_Agent.json)
- [Workflow Diagram](./AI_Healthcare_Analytics_Agent_Workflow.png)
- [n8n Workflow Screenshot](./n8n_workflow_screenshot.png)

## Project Deliverables

- AI Healthcare Analytics Agent built in n8n
- Microsoft SQL Server healthcare database integration
- Google Gemini AI analysis
- Automated healthcare KPI and trend analysis
- Anomaly detection
- Automated Gmail reporting
- Project presentation and user documentation

---

## Conclusion

The AI Healthcare Analytics Agent demonstrates how AI, workflow automation, and SQL-based analytics can be combined to automate healthcare operational reporting.

The system allows users to ask natural-language questions and receive data-driven healthcare insights without manually performing every SQL and analytical step.

---

## Author

AI Healthcare Analytics Agent - Ekta Grewal

Built using n8n, Microsoft SQL Server, Google Gemini, JavaScript, and Gmail.
