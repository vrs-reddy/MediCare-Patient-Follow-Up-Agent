🏥 MediCare – Agentic AI Patient Follow-up System

📌 Project Overview

MediCare is an Agentic AI-powered patient follow-up system designed to assist healthcare teams in monitoring patients with chronic diseases, identifying potential clinical risks, analysing missed appointments, and generating prioritised follow-up recommendations.

The system leverages GPT-OSS 120B through the Groq API and native LLM tool-calling capabilities to autonomously retrieve, analyse, and interpret structured patient data.

Unlike traditional rule-based healthcare applications, this solution enables an LLM to dynamically select appropriate tools, evaluate their outputs, and generate context-aware recommendations through an iterative agentic workflow.

🎯 Business Problem

Healthcare teams face several challenges in managing patients with chronic conditions:

- Missed appointments and delayed follow-ups.
- Abnormal laboratory results and vital signs.
- Manual review of patient records.
- Difficulty prioritising high-risk patients.
- Fragmented clinical information.
- Increased administrative workload.
- Potentially preventable hospital readmissions.

This project demonstrates how Agentic AI can support proactive patient care and reduce manual patient monitoring efforts.

🚀 Key Features

- Autonomous LLM-driven tool selection.
- Native function calling using Groq API.
- Iterative agentic reasoning workflow.
- Patient-specific clinical data retrieval.
- Laboratory result analysis.
- Vital signs assessment.
- Medication and clinical history analysis.
- Missed appointment identification.
- Risk-based patient prioritisation.
- Clinical note grounding and guardrails.
- Invalid blood pressure data detection.
- Interactive exploratory data visualisations.
- Human-in-the-loop clinical decision support.

⚙️ Technology Stack

Technology| Purpose
Python| Core application development
GPT-OSS 120B| Large language model
Groq API| LLM inference and native tool calling
Pandas| Data processing and analysis
Plotly| Interactive data visualisation
JSON| Structured tool inputs and outputs
Jupyter Notebook| Development and execution
Agentic AI| Autonomous tool orchestration
Prompt Engineering| Clinical reasoning and guardrails

📊 Dataset

The project uses a structured, anonymised healthcare dataset containing 100 patient records and 18 features.

The dataset includes information related to:

- Patient identifiers and demographics.
- Chronic disease diagnoses.
- Prescribed medications.
- Laboratory tests and results.
- Laboratory measurement units.
- Patient visit history.
- Missed appointment status.
- Vital signs.
- Clinical notes.

Dataset: "patient_data.csv"

🧠 Agentic AI Workflow

The agent operates through an iterative tool-calling mechanism rather than a predefined sequence of actions.

1. Receive a patient-related query.
2. Send the query and available tool definitions to the LLM.
3. Allow the LLM to determine which tools are required.
4. Execute the selected Python functions.
5. Return structured tool results to the LLM.
6. Allow the LLM to evaluate whether additional information is required.
7. Repeat tool execution when necessary.
8. Generate evidence-grounded clinical insights and follow-up recommendations.

This architecture allows the agent to dynamically determine the appropriate workflow based on the user's query.

🔧 Agent Tools

The system implements six Python-based tools supporting capabilities such as:

Capability| Description
Patient Information| Retrieve patient-specific information
Laboratory Analysis| Retrieve and assess laboratory results
Vital Signs Analysis| Evaluate available vital signs
Medication Analysis| Retrieve medication-related information
Clinical History| Analyse available clinical records and notes
Appointment Monitoring| Identify patients requiring appointment follow-up

The LLM autonomously determines which available tools to invoke based on the query and retrieved evidence.

📋 Implementation

The project is divided into five major tasks.

Task 1: Data Loading and Exploratory Data Analysis

- Load the patient dataset using Pandas.
- Understand dataset structure and feature distributions.
- Analyse chronic disease patterns.
- Identify missing or invalid clinical values.
- Analyse missed appointments.
- Generate interactive visualisations using Plotly.

Task 2: Agent Tool Development

- Implement six Python-based tools.
- Define structured tool descriptions and parameters.
- Enable patient-specific information retrieval.
- Return structured results for LLM interpretation.
- Handle unavailable or invalid patient information.

Task 3: Agentic Loop Implementation

- Integrate GPT-OSS 120B using the Groq API.
- Implement native LLM function calling.
- Dynamically execute requested tools.
- Maintain conversation and tool-response context.
- Support iterative, multi-step tool execution.
- Generate final evidence-grounded responses.

Task 4: Single Patient Analysis

Perform a comprehensive analysis of patient "P0001" using autonomous tool selection.

The agent retrieves relevant patient information, evaluates available clinical evidence, identifies potential risks, and generates follow-up recommendations.

The demonstrated execution uses five tools to collect supporting evidence before generating its response.

Task 5: Missed Appointment Follow-up

Identify patients who have missed appointments and generate prioritised follow-up recommendations.

The agent analyses relevant patient information to support risk-based prioritisation rather than relying exclusively on missed appointment status.

📈 Results and Achievements

Metric| Result
Patient records| 100
Dataset features| 18
Python agent tools| 6
Implementation tasks completed| 5/5
Tools invoked for P0001 analysis| 5
Unique missed-appointment patients identified| 15/15
Follow-up priority categories| 4
Executable code| 247 lines
LLM| GPT-OSS 120B
Inference provider| Groq

Key Outcomes

- Successfully implemented all five case study requirements.
- Demonstrated autonomous, multi-step LLM tool calling.
- Identified all 15 unique patients with missed appointments.
- Generated risk-based follow-up recommendations across four priority categories.
- Detected invalid blood pressure data.
- Incorporated clinical note grounding to reduce unsupported claims.
- Implemented the complete solution within the 250-line executable code constraint.

These results demonstrate functional performance on the supplied dataset and do not represent independently validated clinical accuracy.

🤖 Why Agentic AI?

Traditional Application| MediCare Agentic AI
Predefined execution flow| Dynamic execution flow
Hardcoded action selection| LLM-driven tool selection
Fixed response templates| Context-aware responses
Limited multi-step analysis| Iterative tool execution
Manual information retrieval| Autonomous information retrieval
Static recommendations| Evidence-based recommendations

💡 Design Decisions

Native Tool Calling

The project uses Groq's native LLM tool-calling capabilities without relying on external agent orchestration frameworks.

This provides:

- Greater control over agent execution.
- Reduced framework dependencies.
- Transparent tool execution.
- Simplified debugging.
- Lightweight implementation.

No LangChain or LangGraph

The agentic workflow is implemented directly in Python, demonstrating the underlying mechanics of LLM-based tool orchestration.

No RAG Required

Since the patient dataset is structured and can be queried directly using Python functions, vector databases, embeddings, and document retrieval pipelines are not required for this implementation.

No Model Training or Fine-Tuning

The solution uses a pretrained LLM with prompt engineering and structured tool calling rather than training or fine-tuning a custom model.

Cloud-Independent Implementation

The project does not require Azure OpenAI or additional Azure infrastructure. LLM inference is performed through the Groq API.

🛡️ Responsible AI and Clinical Guardrails

Healthcare AI applications require careful consideration of safety, reliability, and patient privacy.

The project incorporates the following principles:

- Ground recommendations in retrieved patient evidence.
- Avoid inventing unavailable clinical information.
- Identify invalid or missing clinical measurements.
- Distinguish available evidence from assumptions.
- Avoid autonomous medical diagnosis or treatment decisions.
- Require healthcare professional review of recommendations.
- Protect API credentials and patient information.

The system is designed as a clinical decision-support prototype, not a replacement for qualified healthcare professionals.

📂 Repository Structure

MediCare-Agentic-AI/
│
├── MediCare_Agent.ipynb
├── patient_data.csv
└── README.md

🛠️ Installation and Setup

1. Clone the Repository

git clone https://github.com/YOUR_USERNAME/MediCare-Agentic-AI.git

cd MediCare-Agentic-AI

2. Install Dependencies

pip install groq pandas plotly jupyter

3. Configure Groq API Key

Create an API key at:

https://console.groq.com/keys

Set the API key as an environment variable.

Windows PowerShell:

$env:GROQ_API_KEY="your_api_key"

Linux/macOS:

export GROQ_API_KEY="your_api_key"

Ensure the notebook reads the API key securely.

import os
from groq import Groq

client = Groq(
    api_key=os.environ["GROQ_API_KEY"]
)

Never commit API keys to GitHub.

4. Launch Jupyter Notebook

jupyter notebook

Open "MediCare_Agent.ipynb", ensure "patient_data.csv" is available in the same directory, and execute all cells sequentially.

💬 Example User Queries

What is your role as a patient follow-up agent?

Analyse patient P0001 and identify potential clinical risks.

Identify all patients who have missed their appointments.

Prioritise patients who require immediate follow-up based on
their available clinical information.

Generate follow-up recommendations based on patient history,
laboratory results and vital signs.

⚠️ Current Limitations

- Evaluated on a small dataset of 100 anonymised patient records.
- LLM-generated recommendations may contain inaccuracies.
- Clinical thresholds may require patient-specific interpretation.
- No integration with live electronic health record systems.
- No independent clinical validation.
- LLM inference requires external API connectivity.
- No production-grade authentication or monitoring infrastructure.

🔮 Future Enhancements

- Integration with Electronic Health Records (EHR).
- HL7 and FHIR-based healthcare interoperability.
- Multimodal RAG for medical reports and clinical documents.
- Medical guideline retrieval with source citations.
- Automated clinical risk scoring.
- Agent evaluation and hallucination monitoring.
- Human-in-the-loop approval workflows.
- FastAPI-based backend services.
- Streamlit-based healthcare dashboards.
- Automated appointment reminder workflows.
- Role-based access control and audit logging.
- Production-grade deployment and observability.

🎓 Skills Demonstrated

- Agentic AI Development
- Generative AI
- Large Language Model Integration
- Native LLM Function Calling
- Autonomous Tool Orchestration
- Prompt Engineering
- Structured Data Retrieval
- Multi-step Agent Execution
- Healthcare Data Analytics
- Exploratory Data Analysis
- Interactive Data Visualisation
- Data Quality Validation
- Responsible AI
- Clinical Decision Support

📝 Conclusion

MediCare demonstrates how Agentic AI can transform structured healthcare data into actionable patient follow-up insights through autonomous tool selection, iterative LLM execution, and evidence-grounded recommendations.

The project successfully implements all five case study requirements using GPT-OSS 120B, Groq API, and lightweight Python-based orchestration without requiring LangChain, LangGraph, RAG, or model fine-tuning.

The system provides a foundation for developing intelligent healthcare assistants capable of supporting proactive patient monitoring, reducing administrative workload, and improving follow-up prioritisation.

Further clinical validation, robust evaluation, privacy controls, and healthcare professional oversight are necessary before real-world clinical deployment.

⚕️ Disclaimer

This project is developed for educational, research, and technical demonstration purposes only. It is not a certified medical device and must not be used as a substitute for professional medical advice, diagnosis, or treatment.

All clinical recommendations require review by qualified healthcare professionals.

👨‍💻 Author

Rajasekhara Reddy

AI/ML | Generative AI | Agentic AI | Data Science

---

⭐ If you find this project useful, consider starring the repository.