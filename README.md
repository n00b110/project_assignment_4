# Domain Adapted AI Assistant

This project demonstrates domain adaptation using LoRA fine-tuning to improve responses for domain-specific questions. The system extends a basic GenAI pipeline by adapting the model using an instruction dataset and improving usability, monitoring, and system stability.

---

## Pipeline

User → Streamlit → FastAPI → Fine-tuned Model

---

## Domain Task

The system is designed to answer computer science questions (mainly operating systems concepts) with clearer and more structured explanations. The goal is to reduce generic responses and improve consistency using domain-specific knowledge.

---

## Instruction Dataset

An instruction dataset was created using question-answer pairs related to operating systems topics. This dataset helps guide the model to produce more consistent and domain-specific responses.

File:
- instructions.json

---

## Adaptation Method

We used LoRA (Low-Rank Adaptation) with the PEFT library to fine-tune the model efficiently without retraining the entire model. This allows the system to adapt to the domain while keeping training cost low.

Training script:
- training/train_lora.py

---

## Application Enhancements

The Streamlit interface was improved to make the system easier to use and more interactive. Features such as better input handling, response formatting, and chat-style interaction were added.

The connection between Streamlit and FastAPI was also improved so requests are handled more consistently. This helped reduce delays and improved the overall user experience.

---

## Monitoring and Logging

A monitoring and logging system was added to track user queries, model responses, and performance metrics.

This includes:
- Logging requests and responses for debugging  
- Tracking inference time and system behavior  
- Recording evaluation results for performance analysis  

These improvements helped identify issues more easily and made the system more stable.

---

## Deployment and Stability

The system was improved for deployment using Docker and better configuration management.

This includes:
- Docker container setup for consistent environments  
- Error handling to prevent crashes  
- Health checks and stable API responses  
- Improved project structure for easier setup  

---

## Steps

### Install dependencies
pip install -r requirements.txt

### Train model
python training/train_lora.py

### Start API
uvicorn app.api:app --reload

### Run Streamlit
streamlit run app/streamlit_app.py

---

## Evaluation

The system was tested using multiple queries before and after adaptation.

Additional evaluation features include:
- Comparing baseline vs adapted model responses  
- Tracking response quality and consistency  
- Monitoring inference time and performance  

After applying domain adaptation and improvements:
- Responses became more structured  
- Answers were more relevant to operating systems topics  
- System responses were more consistent  
- Application runs more reliably during testing  

---

## Team Contributions

### Ibrahim Alborno (50%)
- Worked on improving how the FastAPI backend connects with the fine-tuned model  
- Added logging and monitoring for debugging and performance tracking  
- Tested system performance using multiple queries  
- Fixed API and response issues  
- Helped ensure the full pipeline runs correctly  

### Immanuel Olaoye (50%)
- Updated the Streamlit interface to improve usability and interaction  
- Improved response display and formatting  
- Helped organize frontend and backend communication  
- Tested the system for stability and consistency  
- Assisted with evaluation and user experience improvements  

---

## Notes

This project shows how domain adaptation can improve a GenAI system while keeping the training process efficient using LoRA. With added improvements in monitoring, logging, and deployment, the system is now closer to a production-ready application.
