# MNLI Logical Contradiction Classification

🤔 A natural language inference project using HuggingFace Transformers and the MNLI (Multi-Genre Natural Language Inference) dataset. This model predicts logical relationships between two sentences as **Entailment**, **Neutral**, or **Contradiction**.


## 💡 Project Overview
This project focuses on:
- Implementing a sequence classification model for natural language inference (NLI).
- Training and evaluating on the MNLI dataset with accuracy improvements using advanced techniques.
- Predicting logical relationships between two input sentences.

## 🔧 Key Skills and Tools
- HuggingFace Transformers
- MNLI Dataset
- Sequence Classification
- Overfitting Mitigation Techniques (Early Stopping, Learning Rate Scheduling)

## 🔄 Modifications and Solutions
### Observed Issue:
The model initially exhibited low accuracy on validation data, indicating overfitting and unstable training.

### Solutions:
- **Pretrained Model**: Switched to the pretrained **`bert-base-cased`** model for better performance.
- **Early Stopping**: Added **`EarlyStoppingCallback`** to halt training when no improvement is observed for 3 consecutive evaluations.
- **Learning Rate Scheduling**: Introduced **`lr_scheduler_type="linear"`** and **`warmup_steps=500`** for smoother convergence.

## 📊 Results
- **Validation Matched Accuracy**: **80.66%**  
  The model achieved **80.66% accuracy** on the validation_matched dataset.
- **Prediction Example**:  
  - Premise: *"A man is playing a guitar."*  
  - Hypothesis: *"A man is making music."*  
  - Predicted Relationship: **LABEL_0 (Entailment)** with **95.18% confidence**.

## 👤 Author
[Gyuhwan Choi](https://github.com/Choi0619)
