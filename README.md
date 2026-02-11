# 🌟 SafePayAI - BSc Student Project

**SafePayAI** is an AI-powered fraud detection and prevention software developed as a **partial completion project for a BSc in Computer Science / Software Engineering**.

It demonstrates practical application of **Generative Adversarial Networks (GANs)** for synthetic data generation and **Random Forest classifiers** for accurate real-time fraud detection in digital payment systems.

This project includes:

1. **Software**: Frontend (React) + Backend (Python Flask + AI models)
2. **Paperwork**: Project report, diagrams, and research documentation
3. **README.md**: Complete explanation, installation, workflow, and system architecture

---

# ⚙️ Key Features

## Frontend

* 🔒 Secure user authentication with Google Sign-In
* 📊 Transaction Dashboard: monitor history, alerts, and analytics
* 📱 Responsive interface for mobile and desktop
* 🎨 Smooth animations via Framer Motion

## Backend

* 🤖 AI-Powered Fraud Detection (GAN + Random Forest)
* ⚡ Real-time fraud prediction through API
* 🔄 Synthetic data generation to improve model performance
* 📂 Firebase integration for storing UPI IDs and transaction history

---

# 📦 Technology Stack

### Frontend

* React + Vite
* Tailwind CSS
* Framer Motion
* Radix UI

### Backend

* Python + Flask
* Firebase (Authentication + Database)
* GANs for synthetic transaction generation
* Random Forest classifier for fraud detection

---

# 🖼 User Interface Snapshots

**Dashboard UI**

```
+--------------------------------+
|        SafePayAI Dashboard      |
|--------------------------------|
| Transactions | Analytics | User |
|--------------------------------|
| Transaction 1: 1000 NGN        |
| Transaction 2: 500 NGN         |
| Transaction 3: Fraud Alert 🔴  |
+--------------------------------+
```

**Fraud Detection Warning UI**

```
+---------------------------+
| 🚨 Fraud Alert Detected!  |
| Recipient: 012345@bank    |
| Amount: 50,000 NGN        |
| Status: Blocked           |
+---------------------------+
```

**Recent Transactions UI**

```
+-------------------------------------+
| Recipient | Amount | Date | Status  |
|-------------------------------------|
| 012345@bank | 1000 | 11-02-2026 | ✅ |
| 678901@bank | 2000 | 10-02-2026 | ⚠️ |
| 543210@bank | 5000 | 09-02-2026 | ✅ |
+-------------------------------------+
```

---

# ⚙️ Installation & Setup

### Clone the repository

```bash
git clone https://github.com/Shabopp/FraudDetectionUsingGAN.git
cd FraudDetectionUsingGAN
```

### Frontend

```bash
cd fraudAI_Frontend_React
npm install
npm run dev
```

Open browser at `http://localhost:3000`.

### Backend

```bash
cd ../AI_model_server_Flask
pip install -r requirements.txt
```

* Ensure `best_rf_model.pkl` is present.
* Start Flask server:

```bash
python app.py
```

API available at `http://127.0.0.1:5000`.

---

# 📈 AI Model Workflow

1. **Data Preparation**

   * Load and preprocess dataset (fraud + non-fraud transactions).
   * Split dataset: 80% training / 20% testing.
   * Feature normalization and encoding.

2. **GAN Training**

   * Generator creates synthetic transactions.
   * Discriminator identifies real vs synthetic.
   * Train using Binary Cross-Entropy loss.

3. **Data Augmentation**

   * Generate synthetic transactions for balancing dataset.
   * Merge synthetic and real data.

4. **Random Forest Model**

   * Train classifier on augmented dataset.
   * Hyperparameter tuning and evaluation (Accuracy, F1-score, AUC-ROC).

5. **Fraud Prediction**

   * Preprocess input transactions.
   * Predict Fraud or Not Fraud.
   * Real-time results displayed on dashboard.

6. **Workflow Automation**

   * Modular scripts for preprocessing, GAN, and Random Forest
   * Seamless execution for real-time predictions

```
+---------------------------+
|        AI Model           |
|---------------------------|
| Input Transactions        |
| GAN Synthetic Data        |
| Random Forest Prediction  |
| Fraud/Not Fraud Output    |
+---------------------------+
```

---

# 🔗 API Endpoints

**Base URL:** `http://127.0.0.1:5000/`

### Home

```
GET /
```

Returns welcome message.

### Predict

```
POST /predict
```

**Request Body:**

```json
{
  "features": [value1, value2, ...]
}
```

**Response:**

```json
{
  "prediction": ["Fraud" or "Not Fraud"]
}
```

**Error Responses:** 400 = no data, 500 = server error

---

# 🏗 System Architecture

```
+----------------------+
|  Google Sign-In Auth |
+----------------------+
           |
           v
+----------------------+
|   Firebase UID       |
+----------------------+
           |
           v
+----------------------+
|  UPI ID Management   |
+----------------------+
           |
           v
+----------------------+
| Transaction Input    |
+----------------------+
           |
           v
+----------------------+
| Fraud Verification   |
+----------------------+
           |
           v
+----------------------+
| Transaction Exec     |
+----------------------+
           |
           v
+----------------------+
| History Storage      |
+----------------------+
```

---

# 📁 Project Structure

```
SafePayAI/
│
├── fraudAI_Frontend_React/      # React frontend
├── AI_model_server_Flask/       # Python Flask backend
│   ├── models/
│   │   └── best_rf_model.pkl
│   ├── app.py
│   ├── utils.py
│   └── requirements.txt
├── paperwork/                   # BSc project documents, diagrams, reports
│   └── placeholder.docx
└── README.md
```

---

# 📄 Nigerian BSc Student Project Context

* Partial BSc project in **Computer Science / Software Engineering**
* Focus: Fraud detection in digital payment systems for Nigerian context
* Includes **software + AI model + project paperwork**
* Designed for **evaluation, presentation, and portfolio showcase**

---

# 🔮 Future Improvements

* Integration with real Nigerian UPI systems
* Advanced behavioral analytics for Nigerian payment patterns
* Mobile app deployment
* Model explainability and compliance auditing

---

# 📜 License

Open-source under **MIT License**

```
```
