# EEG-GPT

**EEG-GPT** is a framework that explores applying GPT-like architectures to EEG data. This repository contains the code necessary to reproduce the results reported in the *EEG-GPT* paper.

- **Paper**: [https://arxiv.org/abs/2401.18006]
- **Dataset**: [TUH EEG Corpus](https://isip.piconepress.com/projects/tuh_eeg/) (not included in this repository)

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [How to Cite](#how-to-cite)
7. [License](#license)

---

## Introduction

**Abstract**
Deep learning has the potential for advancing EEG analysis and interpretation, however widespread implementation has been constrained by the need for extensive labeled datasets and limited transparency. In contrast, generative pretrained transformer (GPT) architectures have enabled efficient learning of small datasets through fine-tuning and also offer verifiable chain-of-thought reasoning in agentic frameworks. Here, we present EEG-GPT, a framework for EEG classification fine-tuned on publicly available large-language models. We benchmark EEG-GPT on the Temple University Hospital (TUH) EEG corpus in a few-shot regime. Utilizing only 2\% of the training data, EEG-GPT classifies normal versus abnormal EEG recordings with AUROC of 0.86, comparable to state-of-the-art deep learning methods. In addition, EEG-GPT demonstrates the capability to be used as an artificial intelligence (AI) agent, orchestrating usage of specialized EEG tools while providing step-by-step verifiability of its reasoning steps. These results underscore GPTs potential to advance EEG analysis and interpretation, highlighting their efficient learning in small data regimes and their potential to automate EEG analysis in a verifiable manner.

Key goals of this repository:
- Preprocessing to convert raw EEG signals into a token-like representation suitable for transformer models.
- Provide scripts to train, validate, and visualize results of the EEG-GPT model.

---

## Features

- **Data Processing**: Includes data loaders and preprocessing scripts for the TUH EEG Corpus.
- **Training & Evaluation**: Provides training loops, evaluation metrics (e.g., AUROC), and logging.

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/EEG-GPT.git
   cd EEG-GPT
   ```
2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   # or
   venv\Scripts\activate  # Windows
   ```
3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   > Make sure to update `requirements.txt` with all necessary Python libraries (e.g., PyTorch, NumPy, Pandas, etc.).

---

## Usage

1. **Obtain the TUH EEG Corpus**  
   The EEG samples used in this project are available through the [TUH EEG Corpus](https://isip.piconepress.com/projects/tuh_eeg/). You must register and follow their guidelines to get access to the dataset.

2. **Preprocess the Data**  
   Use the provided preprocessing script to convert raw EEG files into model-ready inputs.  
   ```bash
   python scripts/preprocess_data.py \
       --data_path path/to/tuh_eeg_data \
       --output_path path/to/processed_data
   ```

3. **Train and Validate EEG-GPT Model**  
   Code provided in the Jupyter notebook
   
---

## How to Cite

If you use this repository or its code in your research, please cite our paper:

```
@article{kim2024eeg,
  title={EEG-GPT: exploring capabilities of large language models for EEG classification and interpretation},
  author={Kim, Jonathan W and Alaa, Ahmed and Bernardo, Danilo},
  journal={arXiv preprint arXiv:2401.18006},
  year={2024}
}
```

---

## License

This project is licensed under the Apache license 2.0.  
Please see the [TUH EEG Corpus website](https://isip.piconepress.com/projects/tuh_eeg/) for their data licensing and usage terms.

---

**Questions or feedback?**  
Feel free to open an [issue](https://github.com/dbernardo05/EEG-GPT/issues) or submit a pull request.  
We welcome contributions and collaboration to further develop **EEG-GPT**!
