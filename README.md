 # 🛡️ Network Intrusion Detection System (NIDS)

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-SVM%2C%20KNN%2C%20Autoencoder-orange.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📖 Overview
**Network Intrusion Detection System (NIDS)** is a machine learning–based project that identifies malicious network activity by analyzing traffic patterns.  
It compares three algorithms — **SVM**, **KNN**, and **Autoencoder** — to detect intrusions and evaluates their accuracy.  
The system also includes an **email alert feature** that notifies administrators whenever a suspicious activity is detected.

---

## ⚙️ Features
- 🧠 **Multi-Algorithm Analysis:** SVM, KNN, and Autoencoder
- 📊 **Model Comparison:** Accuracy, precision, recall, and F1-score
- 📈 **Data Visualization:** Insight into network behavior
- 📬 **Email Notifications:** Automatic alerts for detected intrusions
- 🔍 **Anomaly Detection:** Autoencoder-based unsupervised detection

---

## 🧩 Tech Stack
| Category | Tools / Libraries |
|-----------|------------------|
| Language | Python |
| ML Libraries | scikit-learn, TensorFlow/Keras |
| Data Processing | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Email Alerts | smtplib |
| IDE | Jupyter Notebook / VS Code |

---

## 📊 Dataset
The project uses public intrusion detection datasets like:
- **NSL-KDD**
- **CICIDS 2017**
- or any similar network traffic dataset

Each record contains:
- Source/Destination IP
- Protocol type
- Packet size
- Connection duration
- Attack flag (normal or malicious)

---

## 🚀 Project Workflow
1. **Data Preprocessing:** Cleaning, encoding, and normalizing features  
2. **Model Training:** Train SVM, KNN, and Autoencoder  
3. **Performance Evaluation:** Compare models on test data  
4. **Detection:** Classify new incoming traffic as normal or intrusion  
5. **Email Alert:** Notify the admin when intrusion is detected  

---

## 📧 Email Alert System
When an intrusion is detected:
- The system automatically sends an email notification  
- Includes details like timestamp, IP address, and attack type  

```python
# Example (simplified)
import smtplib

def send_alert(message):
    server = smtplib.SMTP('smtp.gmail.com', 587)
    server.starttls()
    server.login("your_email@gmail.com", "app_password")
    server.sendmail("your_email@gmail.com", "receiver_email@gmail.com", message)
    server.quit()

