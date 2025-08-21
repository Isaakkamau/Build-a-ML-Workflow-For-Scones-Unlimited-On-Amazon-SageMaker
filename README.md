# ML Workflow for Scones Unlimited

## Problem Statement

Scones Unlimited, a food delivery platform, wants to automate the process of identifying and categorizing delivery images. The company receives large amounts of image data daily, and manually handling this data is slow, error-prone, and costly.

The challenge:

- **Efficiently stage raw image data** into the cloud.
- **Train and deploy a machine learning model** that can classify delivery images.
- **Automate workflows** using AWS Step Functions and Lambda.
- **Evaluate and monitor** the system for accuracy and reliability.

---

## Solution Overview

This project implements an **end-to-end ML workflow** on **AWS SageMaker** integrated with **Step Functions** and **Lambda**.

**Key Steps in the Workflow:**

1. **Data Staging** → Images are uploaded and stored in S3.
2. **Model Training & Deployment** → SageMaker is used to train and deploy an image classification model.
3. **Step Function Orchestration** → AWS Step Functions automate the workflow, from input data → model inference → classification output.
4. **Lambda Functions** → Custom logic for preprocessing and integration.
5. **Testing & Evaluation** → Model performance is validated, and results are logged.

This system provides a scalable, serverless pipeline for image classification in real-world production workflows.

---

## Project Structure

```
├── solution.ipynb              # Notebook with end-to-end workflow implementation
├── lambda.py                   # Lambda function for Step Functions integration
├── step_function.json           # AWS Step Function definition
├── screenshot_step_function.png # Proof of working state machine
├── README.md                    # Project documentation
```

---

## Setup Instructions

### Prerequisites

- AWS account with access to **S3, SageMaker, Lambda, Step Functions**
- Python 3.8+
- boto3 & sagemaker SDK installed

### Steps

1. Clone this repository:

   ```bash
   git clone https://github.com/Isaakkamau/Build-a-ML-Workflow-For-Scones-Unlimited-On-Amazon-SageMaker
   cd scones-ml-project
   ```

2. Open `solution.ipynb` in **SageMaker Studio** or Jupyter.
3. Run through the notebook to:

   - Stage data into S3
   - Train and deploy the model
   - Trigger inference via the deployed endpoint

4. Deploy **Lambda function** (`lambda.py`) and create the **Step Function** workflow using `step_function.json`.
5. Test the pipeline end-to-end with sample data.

---

## Results

- Successfully deployed a SageMaker image classification model.
- Automated data → inference workflow using Step Functions.
- Achieved scalable orchestration without manual intervention.

---

## Future Improvements

- Add CI/CD for ML pipelines.
- Integrate model monitoring for data drift detection.
- Expand classification to multi-class, real-world scenarios.
