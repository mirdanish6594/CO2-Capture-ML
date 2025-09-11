# In Silico Descriptor-Based High-Throughput Screening of Amine-Based Solvents for CO₂ Capture

> A machine learning project to replicate, extend, and explain the prediction of CO₂ absorption in chemical solvents, designed for execution in Google Colab.

---

## 📝 Abstract

This project addresses the critical need for efficient carbon capture technologies by developing a robust machine learning framework. We first aim to replicate the findings of Masoumi et al. (2024), who used Artificial Neural Networks to predict CO₂ mass flux in alkanolamine solutions based on operational parameters. Subsequently, we will extend this work by curating a larger, more diverse dataset and engineering a richer feature set that includes *in silico* molecular descriptors. By training and systematically tuning advanced models like XGBoost and analyzing them with Explainable AI (XAI) techniques like SHAP, we seek to not only achieve superior predictive accuracy but also to uncover the key physicochemical drivers of CO₂ absorption.

---

## 🎯 Project Objectives

1.  **Replicate:** To successfully reproduce the modeling results of the reference paper to establish a validated performance baseline.
2.  **Extend:** To build a more robust model by expanding the dataset and incorporating molecular-level features (descriptors).
3.  **Innovate:** To apply and tune state-of-the-art machine learning models (e.g., XGBoost, LightGBM) to achieve higher predictive accuracy.
4.  **Explain:** To use XAI techniques to interpret the model's behavior and identify the most influential parameters driving CO₂ capture.

---

## 👥 Team Members & Roles

* **Danish Mir:** Technical Lead (Programming, Modeling, XAI Analysis)
* **Ifra:** Research & Documentation Lead (Literature Review, Data Sourcing, Report Writing)
* **Tajamul:** Project Management & Presentation Lead (Progress Tracking, Weekly Updates, Presentation Design)

---

## 🛠️ Key Technologies

* **Environment:** Google Colab
* **Core Libraries:** Pandas, Scikit-learn, TensorFlow, XGBoost, RDKit, SHAP
* **Collaboration:** GitHub, Google Drive

---

## 📂 Repository Structure

* `README.md`: You are here! The main guide to the project.
* `requirements.txt`: A list of all necessary Python packages for the project.
* `colab_setup.ipynb`: A utility notebook to mount Drive and install dependencies.
* `data/`: Contains all datasets, split into `raw/` and `processed/`.
* `notebooks/`: Contains the Jupyter notebooks for each stage of the research workflow.
* `src/`: Contains reusable Python scripts and helper functions.
* `reports/`: For all written materials, including weekly updates, the final manuscript, and figures.
* `references/`: Contains downloaded research papers and other reference materials.

---

## 🚀 Getting Started: Step-by-Step Setup

Follow these instructions carefully to set up your environment for the first time.

### **Prerequisites**
1.  A Google Account.
2.  Access to the team's shared Google Drive folder for this project.

### **Step 1: Set Up Google Drive**
For Colab to find our project files, you must add a shortcut to the shared folder in your personal "My Drive". This is a one-time action.

1.  Navigate to the shared project folder in Google Drive.
2.  Right-click on the folder (e.g., `CO2-Capture-ML-Project`).
3.  Select **"Add shortcut to Drive"**.
4.  Choose **"My Drive"** as the location and click **"Add shortcut"**.

This ensures that when you mount your drive, Colab can see the project folder.

### **Step 2: Clone the Repository (First Time Only)**
You only need to do this once to get the project into the shared drive.

1.  Open a new, temporary Google Colab notebook.
2.  Mount your Google Drive with the following code:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```
3.  Navigate to the directory where you want to store the project:
    ```python
    %cd /content/drive/MyDrive/ # Or any other path
    ```
4.  Clone the repository from GitHub:
    ```python
    !git clone <your-github-repo-url>
    ```
Now the entire project structure is inside your Google Drive and accessible to all team members.

### **Step 3: Run the Setup Notebook**
Now you're ready to start working.

1.  Navigate to the project folder in your Google Drive.
2.  Open the `colab_setup.ipynb` notebook.
3.  Run the cells in the notebook. This will:
    * Mount your Google Drive.
    * Change the working directory to the project folder.
    * Install all packages listed in `requirements.txt`.
    * Add the `src/` folder to the system path, allowing you to import custom scripts.

---

## 🔄 Daily Workflow

1.  Open a project notebook you want to work on (e.g., `notebooks/01-replication-data-exploration.ipynb`).
2.  Run the initial setup cells (copied from `colab_setup.ipynb`) at the top of the notebook to mount your drive and install packages.
3.  Perform your work. All files will be saved directly to the shared Google Drive.
4.  When you're finished, commit your changes back to GitHub. You can do this from a cell in your notebook:
    ```python
    # Check the status of your changes
    !git status

    # Add your changes
    !git add notebooks/your_notebook.ipynb

    # Commit with a descriptive message
    !git commit -m "feat: Added initial data exploration and plots"

    # Push to the remote repository
    !git push
    ```