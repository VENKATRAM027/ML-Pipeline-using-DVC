# 🚀 End-to-End Machine Learning Pipeline using DVC

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![DVC](https://img.shields.io/badge/DVC-Data_Version_Control-orange.svg)](https://dvc.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview

This repository demonstrates a production-grade, end-to-end Machine Learning pipeline utilizing **Data Version Control (DVC)**. 

Moving beyond traditional Jupyter Notebook experimentation, this project is structured for **reproducibility, scalability, and MLOps best practices**. By tracking both the code (via Git) and the data/models (via DVC), this pipeline ensures that any model training process can be flawlessly reproduced across different environments.

### Key Features:
* **Data & Model Versioning:** Large datasets and model artifacts are tracked using DVC, keeping the Git repository lightweight.
* **Modular Codebase:** Clean separation of concerns (data ingestion, transformation, model training) for scalability.
* **Reproducible Pipeline:** Automated pipeline execution defined in `dvc.yaml`.
* **Custom Logging & Exception Handling:** Robust tracking of the pipeline's execution state.
* **Installable Package:** Structured as a standard Python module using `setup.py`.

---

## 🏗️ Repository Structure

```text
ML-Pipeline-using-DVC/
│
├── .dvc/                   # DVC configuration and cache
├── data/                   # Raw and processed datasets (Tracked by DVC)
├── Notebook/               # Jupyter notebooks for initial EDA and experimentation
├── src/                    # Source code for pipeline components
│   ├── components/         # Data ingestion, transformation, and model training scripts
│   ├── pipeline/           # Training and prediction pipeline logic
│   └── logger.py           # Custom logging configuration
│
├── dvc.yaml                # DVC pipeline stages and dependencies
├── dvc.lock                # Locked states of DVC pipeline to ensure reproducibility
├── main.py                 # Entry point to trigger the pipeline execution
├── setup.py                # Python package configuration
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation

⚙️ Prerequisites
Before running the pipeline, ensure you have the following installed:

Python 3.8 or higher

Git

DVC (pip install dvc)

🚀 How to Run the Project
1. Clone the repository
Bash
git clone [https://github.com/VENKATRAM027/ML-Pipeline-using-DVC.git](https://github.com/VENKATRAM027/ML-Pipeline-using-DVC.git)
cd ML-Pipeline-using-DVC

2. Create a virtual environment and install dependencies
Bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt

3. Initialize and Pull DVC Data
(Note: If you are using remote storage like AWS S3 or Google Drive for DVC, configure it here. Otherwise, local DVC cache will be used.)

Bash
dvc pull

4. Execute the Pipeline
To run the entire machine learning pipeline (data ingestion -> transformation -> training) simply execute:

Bash
dvc repro
Alternatively, you can trigger the pipeline via the main script:

Bash
python main.py


👨‍💻 Author
Venkat Ram

LinkedIn: www.linkedin.com/in/
venkat-ram-106867403


GitHub: @VENKATRAM027
