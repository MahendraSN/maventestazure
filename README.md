
# Creating Microsoft Azure Pipelines

## 📌 Overview
This project demonstrates how to set up and configure **Azure Pipelines** to automate the build, test, and deployment process for applications.  
It includes YAML pipeline configuration, screenshots, and step-by-step instructions for beginners.

---

## 🎯 Objectives
- Create and configure a new Azure Pipeline.
- Automate build and deployment workflows.
- Integrate version control with Azure Repos or GitHub.
- Learn YAML-based CI/CD pipeline creation.

---

## 🛠 Technologies Used
- **Microsoft Azure DevOps**
- **Azure Pipelines**
- **YAML**
- **GitHub / Azure Repos**

---

## 📂 Project Structure
```

azure-pipelines-demo/
│
├── README.md                   # Project documentation
├── azure-pipelines.yml         # YAML pipeline configuration
├── screenshots/                # Step-by-step screenshots
│   ├── step1\_create\_pipeline.png
│   ├── step2\_select\_repo.png
│   ├── step3\_add\_yml.png
│   ├── step4\_pipeline\_run.png
│
└── sample-app/                 # Sample application for pipeline demo

````

---

## 🚀 Steps to Create an Azure Pipeline

### 1️⃣ Create a New Project in Azure DevOps
1. Go to [Azure DevOps](https://dev.azure.com/).
2. Create a new project with version control (Git).

### 2️⃣ Connect Repository
- Link your project to **GitHub** or **Azure Repos**.

### 3️⃣ Create a New Pipeline
- Navigate to **Pipelines** → **Create Pipeline**.
- Choose the repository.
- Select **YAML** configuration.

### 4️⃣ Add YAML Configuration
Example `azure-pipelines.yml`:
```yaml
trigger:
  - main

pool:
  vmImage: 'ubuntu-latest'

steps:
  - task: UsePythonVersion@0
    inputs:
      versionSpec: '3.x'
  - script: pip install -r requirements.txt
    displayName: 'Install dependencies'
  - script: python main.py
    displayName: 'Run application'
````

### 5️⃣ Run and Verify

* Save and run the pipeline.
* Check build logs and output.

---

## 📸 Sample Screenshots

* **Step 1** – Create Pipeline
  ![Step 1](screenshots/step1_create_pipeline.png)
* **Step 2** – Select Repository
  ![Step 2](screenshots/step2_select_repo.png)
* **Step 3** – Add YAML File
  ![Step 3](screenshots/step3_add_yml.png)
* **Step 4** – Pipeline Run Success
  ![Step 4](screenshots/step4_pipeline_run.png)

---


---

If you want, I can also give you a **list of files, scripts, and screenshots** to include so your **Azure Pipelines project** on GitHub looks authentic and complete. Do you want me to prepare that?
```
