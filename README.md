🔐 AI-Powered Intrusion Detection System (IDS):

This project implements an AI-powered Intrusion Detection System (IDS) that leverages machine learning to classify network traffic as either normal or malicious in real time. It is built using the UNSW-NB15 dataset, which contains labeled traffic data representing modern attack scenarios. The model is trained on selected features to optimize real-time performance and accuracy.

🧠 Key Features:

Machine Learning Model: Uses a Random Forest Classifier trained on key traffic features (proto, pkt_len, src_port, dst_port, flags) to detect intrusions.

Real-Time Integration Ready: Designed to work seamlessly with a GUI-based system or a real-time packet capture module.

Feature Engineering: Includes simulated real-time features such as pkt_len (packet length) and dummy values for ports and flags.

Label Encoding: Protocols (TCP, UDP, etc.) are encoded numerically for compatibility with ML models.

Model Persistence: The trained model is saved as a .pkl file (ids_model.pkl) for fast loading and prediction.

Extendable: Can be integrated into a broader network security system with live packet sniffing and threat visualization.


🗂 Dataset:
Source: UNSW-NB15

Description: Modern network intrusion dataset with various attack categories like Fuzzers, Analysis, DoS, Backdoors, Shellcode, Reconnaissance, etc.


⚙️ Tech Stack:

Python
scikit-learn
pandas
joblib
LabelEncoder & StandardScaler
Optional: GUI and real-time packet capture via scapy or socket

🚀 How It Works:

1.Model Training on Google Colab:
Open the train_model.py file or notebook in Google Colab.
Upload the UNSW_NB15_training-set.csv dataset to your Colab environment.
Run the script to preprocess the data, train the model using a Random Forest classifier, and export the trained model as a .pkl file (e.g., ids_model.pkl).
You can see the AI model word file for some help.

2.Download the Model File:
After training, download the generated ids_model.pkl file from Colab to your local machine.

3.Use the Model Locally:
Copy the path of the downloaded ids_model.pkl file.
Paste the path into your local script that performs real-time threat detection using this model.
Run the script on your local machine.

4.View Results:
Once the code is running, it will use the trained model to make predictions on incoming data.
Based on the output, the system can determine if a network flow is benign or malicious.

