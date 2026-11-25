# MediCare-Patient-Follow-Up-Agent

The MediCare Patient Follow-Up Agent demonstrates an Agentic AI approach to clinical follow-up prioritization using GPT-OSS 120B through the Groq API.

The prototype integrates six reusable Python tools with a custom autonomous LLM-driven execution loop using native function calling, without relying on external agent orchestration frameworks such as LangChain or LangGraph.

The agent dynamically selects relevant tools, retrieves patient-specific clinical information, interprets available evidence, identifies potential risks and generates prioritized follow-up recommendations for healthcare professionals.

### Key Achievements

- Analysed 100 anonymised patient records across 18 features using Pandas and Plotly.
- Implemented six reusable clinical data retrieval tools.
- Enabled autonomous LLM tool selection, dynamic function execution and iterative evidence retrieval.
- Successfully executed all five relevant clinical tools for comprehensive single-patient assessment.
- Implemented a clinical notes retrieval completeness guardrail.
- Identified and assessed all 15 patients with missed appointments.
- Achieved 100% patient coverage with no missing or duplicate patient rows.
- Generated prioritized follow-up plans using four provisional risk categories: Critical, High, Moderate and Low.
- Implemented clinical data quality checks and identified an inconsistent blood pressure measurement.
- Incorporated execution tracing, error handling, iteration limits and clinical safety instructions.

### Final Execution Results

| Evaluation Metric | Result |
|---|---|
| Total patient records | 100 |
| Clinical features | 18 |
| Clinical retrieval tools | 6 |
| Single-patient tool coverage | 5/5 |
| Missed-appointment patients | 15 |
| Patients included in follow-up report | 15 |
| Patient coverage | 100% |
| Missing patient rows | 0 |
| Duplicate patient rows | 0 |
| Critical-priority patients | 3 |
| High-priority patients | 7 |
| Moderate-priority patients | 4 |
| Low-priority patients | 1 |

The risk distribution represents the provisional LLM-generated classifications from the final notebook execution and should not be interpreted as clinically validated risk assessments.

### Limitations

- The dataset contains historical clinical snapshots rather than longitudinal patient records, limiting the ability to identify clinical trends or determine current patient status.
- LLM-generated risk assessments and follow-up recommendations are not clinically validated.
- Hallucinations, unsupported clinical details and inconsistent risk classifications remain possible.
- Prompt-based safety instructions do not guarantee complete adherence to clinical constraints.
- Abnormal or inconsistent source measurements require verification by healthcare professionals.
- Patient coverage validation ensures completeness but does not establish clinical accuracy.
- The clinical notes completeness guardrail verifies tool invocation rather than successful retrieval of all required evidence.
- The prototype does not replace professional medical judgment.

### Future Enhancements

- Schema-validated structured JSON outputs for reliable downstream processing.
- Automated clinical evidence verification against source patient records.
- Integration with approved clinical guidelines and standardized risk assessment criteria.
- Improved evidence completeness validation and hallucination detection.
- Human-in-the-loop approval workflows for clinical recommendations.
- Evaluation against clinician-labelled risk assessments using appropriate performance metrics.
- Persistent audit logging, monitoring and robust API error handling.
- Secure integration with electronic health record systems and healthcare data privacy controls.

### Final Outcome

The prototype successfully demonstrates the feasibility of using Agentic AI for autonomous clinical data retrieval, evidence-based patient assessment and prioritized follow-up planning.

The solution is intended exclusively as a clinical decision-support prototype, with all generated risk assessments and follow-up recommendations subject to healthcare professional verification, review and approval.
