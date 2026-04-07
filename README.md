# A Domain-Adapted AI Assistant for Operating Systems Question Answering

This project is a fully integrated AI system developed for CS 5542 Project Assignment 3 and used as the foundation for Project Assignment 4. The goal of the project was to build a domain-focused AI assistant for operating systems education by combining dataset construction, preprocessing, retrieval support, model adaptation, backend/frontend integration, evaluation, monitoring, and reproducibility into one complete system.

The final system uses an operating systems instruction dataset, preprocessing and knowledge construction support, retrieval and embedding components, LoRA fine-tuning, an AI agent workflow, a FastAPI backend, a Streamlit frontend, Snowflake integration, and evaluation and monitoring tools.

## Team Members
- Ibrahim Alborno
- Immanuel Olaoye

## Project Overview

General-purpose AI systems often produce answers that are too broad or inconsistent for specific academic subjects. In operating systems education, students benefit from answers that are structured, technically relevant, and aligned with core concepts such as deadlock, process scheduling, synchronization, paging, and memory management.

This project addresses that problem by building a domain-adapted AI assistant for operating systems question answering. Instead of relying only on a general-purpose model, the system combines retrieval support, domain adaptation, and an application workflow so that answers are more focused and useful in the target domain.

## Problem Statement

The project aims to improve the quality of AI-generated responses for operating systems questions by integrating:
- an operating systems knowledge source,
- preprocessing and retrieval support,
- domain adaptation through LoRA fine-tuning,
- an AI agent reasoning layer,
- a backend/frontend application interface,
- Snowflake integration for structured data access,
- evaluation and monitoring support,
- reproducibility and setup documentation.

## Final System Pipeline

Instruction Dataset → Preprocessing / Knowledge Construction → Retrieval and Embeddings → LoRA-Adapted Model → AI Agent Reasoning Layer → FastAPI Backend → Streamlit Frontend → Evaluation, Monitoring, and Snowflake Support

## Main Features

- Streamlit frontend for user interaction
- FastAPI backend for request handling
- Instruction-style operating systems dataset
- Data ingestion and preprocessing support
- Retrieval pipeline and embedding-based context support
- Domain adaptation using LoRA fine-tuning
- AI agent reasoning and tool orchestration
- Snowflake integration for structured data access
- Evaluation scripts and response testing support
- Monitoring support
- Reproducibility and setup files

## Domain Task

The system is designed to answer operating systems questions with clearer, more structured, and more domain-relevant explanations. It focuses on reducing generic answers and improving consistency for technical educational questions.

Example domain topics include:
- deadlock
- process scheduling
- synchronization
- memory management
- paging
- resource allocation

## Dataset

The project uses an instruction-style operating systems dataset stored in:

- `dataset/instructions.json`

The dataset follows an instruction-based format with fields such as:
- instruction
- input
- output

The dataset is used for domain adaptation and supports operating systems question-answering behavior in the final system.

## Data Ingestion and Preprocessing

The system includes preprocessing and knowledge construction support for preparing operating systems content for downstream use. These components help clean, structure, and organize the domain information before it is used in retrieval or adaptation workflows.

Typical preprocessing responsibilities include:
- formatting data into instruction style
- organizing knowledge for retrieval
- preparing content for embeddings
- supporting domain-specific question-answer tasks

## Retrieval and Embedding Support

The project includes a retrieval pipeline that supports searching relevant operating systems content when additional context is needed. Embedding-based retrieval helps the system locate useful domain information and improve the relevance of generated responses.

This retrieval workflow is integrated into the overall application so that the system can combine model generation with retrieved context.

## Adaptation Method

We used LoRA (Low-Rank Adaptation) with the PEFT library to fine-tune the model efficiently without retraining the full base model.

Training script:
- `training/train_lora.py`

The purpose of domain adaptation is to make responses:
- more relevant to operating systems questions,
- more structured,
- more consistent,
- less generic than a baseline general response.

## AI Agent Workflow

The project includes an AI agent reasoning layer that helps route user requests through the system. Depending on the type of query, the agent can use different components such as retrieval, structured lookup, or response generation in order to produce a more useful final answer.

This makes the application more flexible than a simple one-path question-answering script.

## Snowflake Integration

The system includes Snowflake integration for structured data access and warehouse-style support. This component helps demonstrate how an AI application can connect to an external structured data layer as part of a larger integrated architecture.

## Lab Integration

### Lab 6 - AI Agent Integration
Lab 6 contributed the agent-style reasoning workflow and support for more dynamic query handling and tool usage.

### Lab 7 - Reproducibility
Lab 7 focused on project organization, dependency setup, environment support, and reproducibility.

### Lab 8 - Domain Adaptation
Lab 8 focused on adapting the model to operating systems question answering using an instruction dataset and LoRA fine-tuning.

### Lab 9 - Application Enhancement
Lab 9 improved the application through better frontend-backend communication, evaluation support, monitoring, and overall system stability.

## Installation and Setup

### 1. Clone the repository
```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure environment variables
Set any required API keys, model settings, or Snowflake connection credentials before running the system.

### 4. Run preprocessing / knowledge setup
Run the ingestion or preprocessing scripts if needed to prepare the knowledge base and retrieval resources.

### 5. Train or load the adapted model
```bash
python training/train_lora.py
```

### 6. Start the FastAPI backend
```bash
uvicorn app.api:app --reload
```

### 7. Run the Streamlit frontend
```bash
streamlit run app/streamlit_app.py
```

## Demo Instructions

1. Install the dependencies.
2. Configure the required environment variables.
3. Run preprocessing or retrieval setup if needed.
4. Start the FastAPI backend.
5. Run the Streamlit frontend.
6. Open the Streamlit interface in your browser.
7. Enter an operating systems question.
8. Review the generated response and any retrieved context or tool-supported behavior.

Example questions:
- What is deadlock in operating systems?
- Explain round robin scheduling.
- What is paging in operating systems?
- What is the difference between a process and a thread?
- Explain mutual exclusion.

## Evaluation Summary

The final system was evaluated from multiple perspectives, including:
- response relevance,
- response structure,
- domain specificity,
- application stability,
- retrieval usefulness,
- end-to-end interaction quality.

The integrated workflow showed that domain adaptation and retrieval support improved the usefulness of responses for operating systems questions. The addition of backend/frontend coordination, evaluation support, monitoring, and tool-based reasoning also made the application more stable and complete.

## Reproducibility

To reproduce the project:

1. Clone the repository.
2. Install dependencies from `requirements.txt`.
3. Configure required environment variables and credentials.
4. Run preprocessing and knowledge setup scripts.
5. Build or load retrieval resources and embeddings.
6. Configure Snowflake access if needed.
7. Train or load the adapted model.
8. Start the FastAPI backend.
9. Launch the Streamlit frontend.
10. Run evaluation scripts and test queries.

## Repository Structure

- `app/` - frontend, backend, configuration, and utility functions
- `training/` - LoRA fine-tuning scripts
- `dataset/` - operating systems instruction dataset
- `evaluation/` - evaluation scripts and testing support
- `monitoring/` - monitoring and metrics support
- `README.md` - main project documentation

You may also include additional folders such as:
- `preprocessing/` - ingestion and preprocessing scripts
- `retrieval/` - retrieval and embedding modules
- `agent/` - agent reasoning and tool orchestration
- `snowflake/` - Snowflake connection and query scripts
- `docs/` - architecture diagram and additional documentation

## System Architecture Diagram

Add your architecture diagram image or link here once finalized.

## Demo Video

Add your public video link here once recorded.

## Poster

Add your poster PDF link here once finalized.

## Team Contributions

| Member | Contribution Description | Contribution % |
|--------|---------------------------|---------------:|
| Ibrahim Alborno | Worked on backend integration, model connection, monitoring, debugging API behavior, evaluation support, documentation alignment, and helping make sure the full integrated pipeline worked correctly. | 50% |
| Immanuel Olaoye | Worked on the Streamlit interface, frontend flow, response formatting, testing for stability and consistency, user interaction improvements, and support for evaluation and application integration. | 50% |

## Notes

This project demonstrates how a domain-focused AI application can be built by combining data preparation, retrieval, model adaptation, agent reasoning, backend/frontend interaction, monitoring, evaluation, and reproducibility into one integrated system. The final result is an operating systems question-answering assistant designed to be more useful and more technically relevant than a generic baseline system.
