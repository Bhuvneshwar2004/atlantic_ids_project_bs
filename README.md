🛡️ AI-Powered Intrusion Detection System (IDS)

Team Atlantic | Minor Project

📌 Project Overview

This project is a real-time Network Intrusion Detection System (IDS) built using Machine Learning to detect cyberattacks with high accuracy.
It is trained on the CICIDS-2017 Dataset and uses the XGBoost classifier to categorize network traffic as:

✅ Benign (Safe)

❌ Malicious (Attack)

The system includes a fully functional Streamlit Dashboard for real-time monitoring, bulk log auditing, and forensic-level packet analysis.

🚀 Key Features
🔴 Live Traffic Monitor

Captures real-time packets using Scapy and predicts threats instantly.

📂 Bulk File Scan (CSV / PCAP)
Upload and analyze full network logs for attacks.

🔬 Single Packet Forensics
Test individual packet attributes (ports, sizes, durations etc.) to simulate specific attack scenarios.

📊 Interactive Dashboard
Visualize threats using Plotly charts, attack statistics, and logs.

⚙️ Custom Sensitivity
Adjust AI confidence threshold for stricter or lenient detection.

🛠️ Technology Stack
| Category            | Tools                       |
| ------------------- | --------------------------- |
| **Language**        | Python 3.x                  |
| **UI / Dashboard**  | Streamlit                   |
| **ML Model**        | XGBoost                     |
| **Preprocessing**   | Scikit-Learn, Pandas, NumPy |
| **Packet Sniffing** | Scapy                       |
| **Visualization**   | Plotly, Matplotlib          |

📂 Project Structure
IIDS_Project/
│
├── app.py                # Main Streamlit Application
├── requirements.txt      # All Python Dependencies
├── README.md             # Project Documentation
│
├── xgb_model.pkl         # Trained XGBoost Model
├── scaler.pkl            # MinMaxScaler for feature scaling
├── label_encoder.pkl     # LabelEncoder for decoding attack labels
└── features.pkl          # List of model feature names (training order)

⚙️ Installation & Setup
Follow these steps to run the IDS locally:

1. Install Python
Download Python (3.8 or newer) from:
https://www.python.org/

2. Clone or Download the Project
Create a folder named IDS_Project and place all project files inside it.

3. Install Required Libraries
Open Terminal / CMD inside the project folder:
pip install -r requirements.txt

4. Run the Application
streamlit run app.py

📈 Model Performance (CICIDS-2017 Dataset)
| Model                | Accuracy   | Precision | Recall |
| -------------------- | ---------- | --------- | ------ |
| **XGBoost**          | **99.82%** | 0.99      | 0.99   |
| Random Forest        | 99.65%     | 0.99      | 0.99   |
| LSTM (Deep Learning) | 98.40%     | 0.97      | 0.98   |


🧪 Testing the IDS
✔️ You can test the system with:
1.Real-time captured packets

2.Uploaded CSV log files

3.PCAP files

4.Manually entered packet attributes

A sample CSV for testing is provided in the repository.

⚠️ Limitations
1.Encrypted traffic (HTTPS) cannot be inspected beyond headers.

2.The model is trained on CICIDS-2017, so new zero-day attacks may require re-training.

3.Real-time sniffing requires Admin / Root privileges.

👥 Contributors — Team Atlantic
| Name                 | Role                                       |
| -------------------- | ------------------------------------------ |
| **Bhuvneshwar Sahu** | AI Model Development & Backend Engineering |
| **Priyal Jain**      | UI/UX Design & Documentation               |
| **Abhinesh**         | Data Preprocessing & System Testing        |

