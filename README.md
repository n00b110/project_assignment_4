# Domain-Adapted AI Assistant

This project is our integrated GenAI system for Project 3. It combines work from Project 2 and Labs 6 through 9 into one final application. The goal of the project was to build a system that is more stable, more useful, and more focused on a specific domain instead of only giving general responses.

The final system uses a Streamlit frontend, a FastAPI backend, a fine-tuned model, and added support for logging, evaluation, reproducibility, and better overall system behavior.

## Overview

The system is designed to answer computer science questions, mainly operating systems topics, in a clearer and more structured way. We used an instruction dataset and LoRA fine-tuning so the model could give more consistent and domain-focused answers.

This project also includes improvements to the application itself, such as better frontend-backend communication, logging, monitoring, evaluation support, and setup organization.

## Pipeline

**Data Source / Dataset → Preprocessing and Setup → Snowflake + Analytics Layer → AI Agent and Tools → Domain-Adapted Model → FastAPI Backend → Streamlit Frontend → Evaluation and Logging**

## Main Features

* Streamlit frontend for user interaction
* FastAPI backend for handling requests
* Domain adaptation using LoRA fine-tuning
* Instruction dataset for operating systems questions
* AI agent and tool-based workflow
* Logging and monitoring support
* Evaluation support
* Docker and setup improvements for stability and reproducibility

## Project Foundation

The earlier phase of the project provided the main foundation for the system. This included working with Toyota stock price data, loading and querying data through Snowflake, and using a Streamlit interface for user interaction. That phase helped establish the data pipeline, warehouse support, analytics flow, and application layer that later improvements were built on.

## Domain Task

The model is adapted to answer computer science questions, mainly operating systems concepts, with clearer and more structured explanations. The purpose was to reduce generic responses and improve consistency for the selected domain.

## Dataset

An instruction dataset was created using question-answer pairs related to operating systems topics.

File used:

* `dataset/instructions.json`

## Adaptation Method

We used LoRA (Low-Rank Adaptation) with the PEFT library to fine-tune the model efficiently without retraining the full model.

Training script:

* `training/train_lora.py`

## Lab Integration

### Lab 6 - Agent Integration

Lab 6 added an AI agent layer so the system could interpret user questions, choose the correct tool, and return structured results.

### Lab 7 - Reproducibility

Lab 7 focused on reproducibility through better project organization, dependency setup, configuration support, scripts, and testing structure. We used **Claude** and **ChatGPT** during debugging and setup to help check dependencies, fix environment issues, and improve configuration.

### Lab 8 - Domain Adaptation

Lab 8 focused on adapting the model using an instruction dataset and LoRA fine-tuning. After adaptation, responses became more structured, more relevant to operating systems topics, and more consistent.

### Lab 9 - Application Enhancement

Lab 9 improved the application through better Streamlit and FastAPI communication, stronger logging and monitoring support, evaluation support, and better stability during testing.

## Installation and Setup

### Install dependencies

```
pip install -r requirements.txt
```

### Train the model

```
python training/train_lora.py
```

### Start the API

```
uvicorn app.api:app --reload
```

### Run Streamlit

```
streamlit run app/streamlit_app.py
```

## Evaluation Summary

The system was tested using multiple queries before and after adaptation. After applying domain adaptation and application improvements, responses became more structured, more relevant to operating systems topics, and more consistent. The application also ran more reliably during testing.

## Reproducibility

To reproduce the project:

1. Clone the repository
2. Install dependencies from the requirements file
3. Configure any required environment variables or credentials
4. Train or load the adapted model
5. Start the FastAPI backend
6. Launch the Streamlit frontend
7. Run evaluation or test queries to confirm the system is working

## Team Contributions

| Member          | Contribution Description                                                                                                                                                           | Contribution % |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: |
| Ibrahim Alborno | Worked on backend integration, model connection, logging, monitoring, debugging API behavior, testing system performance, and helping make sure the full pipeline worked correctly |            50% |
| Immanuel Olaoye | Worked on the Streamlit interface, frontend flow, response formatting, testing for stability and consistency, and helping improve user interaction and evaluation                  |            50% |

## Notes

This project shows how domain adaptation can improve a GenAI system while keeping the training process efficient through LoRA. With added improvements in monitoring, logging, reproducibility, and application stability, the system became more complete and closer to a real integrated application.
