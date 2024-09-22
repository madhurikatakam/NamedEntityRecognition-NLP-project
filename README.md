# Named Entity Recognition (NER) on Resume Data

This project implements a Named Entity Recognition (NER) model using spaCy to extract key information from resumes. The dataset consists of annotated resumes, and the model is trained to recognize entities like names, skills, education, and experience details.

## Requirements

Before running the code, ensure you have the following dependencies installed:

- Python 3.x
- spaCy (>=3.x)
- NumPy (numpy)
- Pandas (pandas)
- JSON (json)

## Project Details

### Dataset
- Resume Entities for NER  
  Source: [Kaggle - Resume Entities for NER Dataset]
- The dataset contains 220 annotated resumes.
- Training Set: 200 resumes  
- Test Set: 20 resumes

### Preprocessing
- Removed extra whitespaces, tabs, and newlines.
- Handled overlapping entities to ensure non-overlapping spans for spaCy training.
- Converted the data into a spaCy-compatible format for training.

### Model Training
- Framework: Python, spaCy
- Loaded a blank English model and added an NER component.
- Used a custom training loop to update the model weights based on annotated examples from the training set.
- The model learns to identify and classify entities from resumes effectively.

### Predictions
- The model was tested on 20 resumes.
- Predicted and summarized the entity recognition results, including name, education, skills, and work experience.

## Challenges & Solutions

### Challenge 1: Overlapping Entities
- Problem: spaCy does not support overlapping entities during model training.
- Solution: Implemented a function to handle overlapping entities by removing or consolidating conflicting spans, ensuring each span is unique and valid for training.

### Challenge 2: Data Formatting and Model Tuning
- Problem: Ensuring the data was formatted correctly for spaCy's NER model and adjusting the model to handle diverse resume data.
- Solution: Verified the annotation format and eliminated inconsistencies. Set up evaluation checkpoints during training to monitor and adjust model performance as needed.
