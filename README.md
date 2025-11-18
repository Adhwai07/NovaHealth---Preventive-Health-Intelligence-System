# NovaHealth---Preventive-Health-Intelligence-System
A system that cleans and analyzes medical, pharmaceutical, survey and environment data to predict regional health risks and generate alerts and interventional plans for better preventive healthcare.

Opus Workflow Link: https://app.opus.com/app/workflow/share/5df13efc-2cc5-47ed-94bc-6f0adf44c8a0

## Workflow Logic
### 1. File Input
Accepts CSV, Excel, or other tabular formats containing medical data such as diseases, risk indicators, region codes, and time-based case counts.
### 2. Data Relevancy Check
Evaluates whether the uploaded dataset is medically relevant.
- If relevant → proceed
- If not → produce an explanatory error message
### 3. Decision Gate (Medical Validation)
Routes the workflow based on the relevancy result:
- True Path: Continues with standardization, cleaning, and anonymization
- False Path: Generates and outputs the error message only
### 4. Data Standardization & Cleaning
Normalizes column names, formats, and structures. Removes identifiers and sensitive information.
### 5. Regional Categorization
Groups the data by region code to enable localized risk analysis.
### 6. Risk Matrix Generation
Produces a regional risk matrix with:
- Risk name
- Risk score
- Category (e.g., high / moderate / low)
- Summary and supporting evidence
Also extracts Top Regional Risks.
### 7. Key Analysis Nodes
- Forecast Generator: Predicts short-term regional health trends
- Intervention Planner: Creates tailored prevention and mitigation strategies
- Public Health Alert Generator: Issues region-specific alerts and warnings
### 8. Report Generation
Creates structured disease and risk reports per region, including forecasts, alerts, and interventions.
Also includes compliance and ethical review content.
### 9. Email Output Flow
A human task prompts the reviewer to enter a valid email address.
The system then:
- Generates a concise regional risk summary email
- Sends the summary and intervention plans to the provided email
### 10. Executive Summary Report
Produces a comprehensive, downloadable regional risk assessment report for decision-makers.

## Review Logic
- Review nodes are intentionally not used, as earlier tests showed they frequently did not complete execution.
- Instead, data validation and compliance checks are handled directly within automated logic nodes for reliability.

## Error Handling
- If the dataset is not medically relevant, the workflow triggers the False branch of the decision gate.
- An error-specific node generates a clear explanatory message.
- The workflow terminates by outputting the error message only.

## Output Export Path
The workflow provides:
### 1. Email Output
Sent to the email address entered in the human task node containing:
- Regional risk summary
- Intervention recommendations

### 2. Workflow Outputs
Displayed at the end of the run:
- Top regional risks
- Complete regional risk matrix
- Regional codes detected
- Ethical review findings
- Policy adherence checks
- A comprehensive regional risk assessment report
