# ML-Pipeline-using-DVC

# 🚀 End-to-End Machine Learning Pipeline using DVC

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![DVC](https://img.shields.io/badge/DVC-Data_Version_Control-orange.svg)](https://dvc.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
This repository demonstrates a production-grade, end-to-end Machine Learning pipeline utilizing **Data Version Control (DVC)**. 

Moving beyond traditional Jupyter Notebook experimentation, this project is structured for **reproducibility, scalability, and MLOps best practices**. By tracking both the code (via Git) and the data/models (via DVC), this pipeline ensures that any model training process can be flawlessly reproduced across different environments.

### Key Objectives:
* Implement modular and scalable codebase architecture.
* Manage and version large datasets and model weights using DVC.
* Create a reproducible pipeline graph (`dvc.yaml`) for automated training and evaluation.
* Package the ML project as a clean, installable Python module using `setup.py`.

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
├── .dvcignore              # Files to be ignored by DVC
├── .gitignore              # Files to be ignored by Git
└── README.md               # Project documentation
