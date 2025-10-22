# DS Project Template

A lightweight and reusable data science project template designed to help you start new projects quickly and consistently.
This repository provides a clear structure, setup instructions, and guidance for environment management and reproducibility.

---

## Repository Structure

```
├── .env                  # Optional environment variables file
├── .gitignore            # Specifies files ignored by Git
├── EDA.ipynb             # Example exploratory data analysis notebook
├── LICENSE               # License information
├── README.md             # Project documentation and navigation guide
├── column_names.md       # Description or documentation of dataset columns
├── requirements.txt      # List of Python dependencies
└── data/                 # Folder for raw and processed datasets
```

---

## Requirements

* pyenv
* Python 3.11.3
* pip (latest version recommended)
* Node.js (required for Plotly in Jupyter Lab)

---

## Setup Instructions

Follow these steps to set up your environment and install dependencies.
Select the commands appropriate for your operating system.

### macOS

```bash
# Step 1: Install Node.js (if not installed)
brew update
brew install node

# Step 2: Set Python version and create virtual environment
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate

# Step 3: Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)

```bash
# Step 1: Install Node.js (if not installed)
choco upgrade chocolatey
choco install nodejs

# Step 2: Set Python version and create virtual environment
pyenv local 3.11.3
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/Scripts/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

---


## Reproducibility

To ensure others can recreate your environment, generate a requirements file after installing dependencies:

```bash
pip freeze > requirements.txt
```

Note: On systems such as macOS M1, some compiled libraries (for example, SciPy) may require additional setup or system libraries.

---

## Repository Navigation

* **EDA.ipynb** – Explore and visualize your dataset.
* **data/** – Store raw and processed data.
* **column_names.md** – Reference for dataset fields and naming conventions.
* **requirements.txt** – List of dependencies for consistent environments.
* **.env** – (Optional) Store environment variables or API keys securely.

---

## License

This project is distributed under the terms of the MIT License.
See the [LICENSE](LICENSE) file for details.

---

## About This Project

First Project – Data Analysis: King County Housing Data

This project focuses on exploratory data analysis (EDA) and the presentation of findings to a client.
The dataset contains information on home sales in King County, USA, and is accessed via the eda schema in the shared database (DBeaver). The CSV file should be stored locally in the data/ directory.

The goal is to explore the data, perform statistical and geographical analysis, and derive meaningful insights and actionable recommendations.
Students are expected to:
Explore the dataset and join the relevant tables.
Conduct EDA to identify at least three insights, including one geographical insight.
Provide at least three client recommendations, taking the perspective of either a buyer or a seller.

Column name descriptions are provided in column_names.md. Some names may be ambiguous, simulating real-world data interpretation challenges. When in doubt, perform additional research or make reasoned assumptions, clearly stated in the analysis.
