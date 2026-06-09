
Each notebook corresponds to a stage in the MLOps lifecycle.

---

## 🔄 End-to-End Pipeline

### **1. Training (Notebook 02)**
- Loads training data  
- Trains a model using MLflow  
- Logs artifacts + metrics  
- Writes predictions to Unity Catalog tables  

### **2. Model Registration (Notebook 03)**
- Registers the model in Unity Catalog  
- Creates a new version  
- Promotes to `staging` alias  

### **3. Inference (Notebook 04)**
- Batch inference → Delta table  
- Real-time inference → Python client  
- Validates model signature  

### **4. Model Serving (Notebook 05)**
- Deploys a Databricks Model Serving endpoint  
- Supports REST API inference  

### **5. Drift Detection (Notebook 06)**
- Computes PSI + KS for features + predictions  
- Logs drift metrics to monitoring table  

### **6. Automated Retraining (Notebook 07)**
- Reads drift metrics  
- Compares against thresholds  
- Retrains model if drift detected  
- Registers + promotes new version  

### **7. Monitoring Dashboard (Notebook 08)**
- Lakeview dashboard for:  
  - PSI over time  
  - KS statistics  
  - Prediction distributions  
  - Model version history  

---

## 🔧 CI/CD Integration

CI/CD handles:

- Deploying notebooks to Databricks Repos  
- Deploying Jobs / Workflows  
- Deploying Model Serving configs  
- Promoting models across environments  
- Running tests and validations  
- Managing IaC (Databricks Bundles, Terraform, Bicep)

Retraining is triggered by **Databricks Jobs**, not CI/CD.

---

## 🧪 Testing Strategy

Recommended testing layers:

- Unit tests  
- Integration tests  
- Model performance tests  
- Data quality tests  

CI/CD runs these before deployment.

---

## 🚀 Getting Started

### Prerequisites
- Azure Databricks workspace  
- Unity Catalog enabled  
- MLflow permissions  
- GitHub or Azure DevOps repo  
- Databricks CLI or Repos integration  

### Run the Pipeline
1. Run `00_Config`  
2. Run `02_Train_and_Predict`  
3. Run `03_Register_Model`  
4. Run `04_Inference_Batch_and_Realtime`  
5. Run `05_Model_Serving`  
6. Run `06_Drift_Detection`  
7. Run `07_Automated_Retraining`  
8. Build Lakeview dashboard using `08_Lakeview_Dashboard`  

---

## 🤝 Contributing

Pull requests are welcome.  
For major changes, open an issue to discuss what you’d like to modify.

---

## 📄 License

This project is licensed under the MIT License.

