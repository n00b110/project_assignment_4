# A Domain-Adapted AI Assistant for Operating Systems Question Answering

This project is our integrated GenAI system for Project Assignment 3 and serves as the foundation for Project Assignment 4. The goal of the project was to build a system that is more focused on a specific academic domain instead of only giving general responses.

The final system uses a Streamlit frontend, a FastAPI backend, a LoRA fine-tuning workflow, and support for evaluation, monitoring, and reproducibility.

## Team Members
- Ibrahim Alborno
- Immanuel Olaoye

## Overview

The system is designed to answer operating systems questions in a clearer and more structured way. We used an instruction-style dataset and LoRA fine-tuning to make the model more domain-focused.

The application also includes a Streamlit frontend for user interaction, a FastAPI backend for handling requests, and supporting files for evaluation and monitoring.

## Problem Statement

General-purpose AI systems often produce answers that are too broad or inconsistent for specific academic domains. In operating systems education, students benefit from answers that are more focused, structured, and relevant to technical concepts. This project addresses that problem by adapting an AI assistant to answer operating systems questions more effectively.

## Pipeline

Instruction Dataset → LoRA Fine-Tuning → Adapted Model → FastAPI Backend → Streamlit Frontend → Evaluation and Monitoring

## Main Features

- Streamlit frontend for user interaction
- FastAPI backend for handling requests
- Domain adaptation using LoRA fine-tuning
- Instruction-style dataset for operating systems questions
- Evaluation support
- Monitoring support
- Reproducibility and setup files

## Domain Task

The model is adapted to answer operating systems questions with clearer and more structured explanations. The purpose was to reduce generic responses and improve consistency for this domain.

## Dataset

The project uses an instruction-style dataset stored in:

- `dataset/instructions.json`

In the current repo version, the dataset contains a sample operating systems question-answer pair in the following format:

- instruction
- input
- output

The included sample focuses on explaining deadlock in operating systems.

## Adaptation Method

We used LoRA (Low-Rank Adaptation) with the PEFT library to fine-tune the model efficiently without retraining the full model.

Training script:
- `training/train_lora.py`

## Lab Integration

### Lab 6 - Integration
This phase contributed to combining project components into a more unified workflow.

### Lab 7 - Reproducibility
This phase focused on project organization, dependency setup, configuration support, and reproducibility.

### Lab 8 - Domain Adaptation
This phase focused on adapting the model using the instruction-style operating systems dataset and LoRA fine-tuning.

### Lab 9 - Application Enhancement
This phase improved the application through better frontend-backend communication, evaluation support, monitoring, and overall stability during testing.

## Installation and Setup

### Install dependencies
```bash
pip install -r requirements.txt
```

### Train the model
```bash
python training/train_lora.py
```

### Start the API
```bash
uvicorn app.api:app --reload
```

### Run Streamlit
```bash
streamlit run app/streamlit_app.py
```

## Demo Instructions

1. Install the dependencies.
2. Start the FastAPI backend.
3. Run the Streamlit frontend.
4. Open the Streamlit interface in your browser.
5. Enter an operating systems question.
6. Review the generated response.

Example question:
- What is deadlock in operating systems?

## Evaluation Summary

The project demonstrates a domain-focused question-answering workflow for operating systems topics. The current repo includes the full system structure for adaptation, frontend/backend interaction, evaluation, and monitoring, along with a sample instruction dataset for the domain.

## Reproducibility

To reproduce the project:

1. Clone the repository
2. Install dependencies from `requirements.txt`
3. Configure any required environment variables
4. Train or load the adapted model
5. Start the FastAPI backend
6. Launch the Streamlit frontend
7. Run test queries to confirm the system is working

## Repository Structure

- `app/` - frontend, backend, configuration, and utility functions
- `training/` - LoRA fine-tuning script
- `dataset/` - instruction dataset
- `evaluation/` - evaluation scripts
- `monitoring/` - metrics support
- `README.md` - main project documentation

## Demo Video

Add your public video link here once recorded.

## Poster

Add your poster PDF link here once finalized.

## Team Contributions

| Member | Contribution Description | Contribution % |
|--------|---------------------------|---------------:|
| Ibrahim Alborno | Worked on backend integration, model connection, monitoring, debugging API behavior, testing system performance, and helping make sure the pipeline worked correctly. | 50% |
| Immanuel Olaoye | Worked on the Streamlit interface, frontend flow, response formatting, testing for stability and consistency, and helping improve user interaction and evaluation. | 50% |

## Notes

This project shows how domain adaptation can be applied to a focused academic question-answering system using LoRA, a frontend/backend application structure, and supporting evaluation and monitoring components.
