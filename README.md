# A Domain-Adapted AI Assistant for Operating Systems Question Answering

This project was developed as our semester project for CS 5542 and submitted as part of Project Assignment 4 for the Research-A-Thon poster, video, and GitHub presentation. The goal of the project was to build an AI assistant that gives more focused and useful responses for operating systems questions instead of relying only on broad general-purpose outputs.

Our final system combines an operating systems instruction dataset, LoRA fine-tuning, a FastAPI backend, a Streamlit frontend, and support for evaluation and monitoring. The result is a domain-adapted application that can respond to operating systems questions in a more structured and relevant way.

## Team Members
- Ibrahim Alborno
- Immanuel Olaoye

## Project Overview

General-purpose AI tools can give answers that are too broad or inconsistent for technical academic subjects. In operating systems, students need answers that are clearer, more structured, and more connected to course concepts such as deadlock, scheduling, synchronization, paging, memory management, and process behavior.

This project addresses that problem by adapting an AI assistant to the operating systems domain. The system uses domain-focused data and model adaptation so that the final responses are more useful for students studying operating systems topics.

## Problem Statement

The goal of this project is to improve the quality of AI-generated answers for operating systems questions by building a domain-adapted question-answering system. Instead of using only a general model, the project applies fine-tuning and application integration so that answers are more domain-specific, consistent, and easier to understand.

## System Pipeline

Instruction Dataset → LoRA Fine-Tuning → Adapted Model → FastAPI Backend → Streamlit Frontend → Evaluation and Monitoring

## Main Features

- Streamlit frontend for user interaction
- FastAPI backend for request handling
- Operating systems instruction dataset
- Domain adaptation using LoRA fine-tuning
- Evaluation support
- Monitoring support
- Reproducibility through organized setup and documentation

## Dataset

The project uses an instruction-style dataset stored in:

- `dataset/instructions.json`

The dataset is focused on operating systems question-answer examples and is used to adapt the model toward more domain-specific responses.

## Adaptation Method

We used LoRA (Low-Rank Adaptation) with the PEFT library to fine-tune the model efficiently without retraining the full base model.

Training script:
- `training/train_lora.py`

The goal of adaptation was to make responses:
- more relevant to operating systems questions
- more structured
- more consistent
- less generic than standard baseline responses

## Application Structure

The system includes a FastAPI backend and a Streamlit frontend. The backend handles requests and model interaction, while the frontend provides a simple user interface where users can enter operating systems questions and view the generated responses.

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

### 3. Train or load the adapted model
```bash
python training/train_lora.py
```

### 4. Start the FastAPI backend
```bash
uvicorn app.api:app --reload
```

### 5. Run the Streamlit frontend
```bash
streamlit run app/streamlit_app.py
```

## Demo Instructions

1. Install the required dependencies.
2. Start the FastAPI backend.
3. Run the Streamlit frontend.
4. Open the Streamlit interface in your browser.
5. Enter an operating systems question.
6. Review the generated response.

Example questions:
- What is deadlock in operating systems?
- Explain round robin scheduling.
- What is paging in operating systems?
- What is the difference between a process and a thread?
- Explain mutual exclusion.

## Results Summary

The final system produced responses that were more structured, more relevant to operating systems topics, and more consistent than general baseline responses. The project also showed that combining a domain-adapted model with a working backend and frontend application can create a more useful academic AI assistant.

## Reproducibility

To reproduce the project:

1. Clone the repository
2. Install the dependencies from `requirements.txt`
3. Train or load the adapted model
4. Start the FastAPI backend
5. Launch the Streamlit frontend
6. Run test questions and evaluate the results

## Repository Structure

- `app/` - frontend, backend, configuration, and utility files
- `training/` - LoRA fine-tuning script
- `dataset/` - instruction dataset
- `evaluation/` - evaluation scripts and testing support
- `monitoring/` - monitoring and metrics support
- `README.md` - main project documentation
- 
## Demo Video

Add your public video link here.

## Poster

https://github.com/n00b110/project_assignment_4/blob/main/Project%20Assignment%204%20-%20Poster.pdf
