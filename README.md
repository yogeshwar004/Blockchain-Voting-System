
# 🗳️ Blockchain-Based Digital Voting System  

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![MySQL](https://img.shields.io/badge/mysql-8.0+-blue.svg)](https://www.mysql.com/)

A secure and transparent digital voting system built using **Blockchain technology**, designed to ensure vote integrity, prevent tampering, and enable trust in the voting process.  

---

## 📌 Project Overview  

This project implements a **decentralized voting mechanism** where each vote is stored as a block in a blockchain. The system ensures that once a vote is recorded, it cannot be modified or deleted.  

Additionally, a **MySQL database** is integrated to manage voter information and candidate data, while the blockchain ensures **data immutability and transparency**.  

---

## 🚀 Features  

- 🔐 Secure voting using blockchain technology  
- 🧾 Immutable vote records (tamper-proof)  
- 👤 Voter registration system  
- 🗳️ Candidate management  
- 📊 Real-time blockchain validation  
- 🌐 REST API using Flask  
- 💾 MySQL database integration  
- 🎯 Simple and beginner-friendly implementation  

---

## 🛠️ Tech Stack  

- **Backend:** Python, Flask  
- **Database:** MySQL  
- **Blockchain Logic:** Custom Python Implementation  
- **Frontend:** HTML, JavaScript  
- **Libraries:**  
  - Flask  
  - hashlib  
  - mysql-connector-python  

---

## 📂 Project Structure  


BlockchainVoting/
│── app.py # Main Flask application
│── blockchain.py # Blockchain logic
│── templates/
│ └── index.html # Frontend UI
│── static/ # CSS/JS files (optional)
│── README.md


---

## ⚙️ Installation & Setup  

### 1️⃣ Clone the Repository  

git clone https://github.com/your-username/blockchain-voting-system.git

cd blockchain-voting-system


---

### 2️⃣ Install Dependencies  

pip install flask mysql-connector-python


---

### 3️⃣ Setup MySQL Database  

Run the following SQL commands:  


CREATE DATABASE VotingSystem;

USE VotingSystem;

CREATE TABLE Voters (
voter_id VARCHAR(20) PRIMARY KEY,
name VARCHAR(100),
age INT
);

CREATE TABLE Candidates (
candidate_id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
party VARCHAR(100)
);

CREATE TABLE Votes (
vote_id INT AUTO_INCREMENT PRIMARY KEY,
voter_id VARCHAR(20),
candidate_id INT,
timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


---

### 4️⃣ Configure Database Connection  

Update your `app.py`:  


db = mysql.connector.connect(
host="localhost",
user="root",
password="your_password",
database="VotingSystem"
)


---

### 5️⃣ Run the Application  


python app.py


Open your browser and go to:  

http://127.0.0.1:5000/


---

## 🔗 API Endpoints  

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/register_voter` | POST | Register a new voter |
| `/candidates` | GET | Fetch candidate list |
| `/vote` | POST | Cast a vote |
| `/get_chain` | GET | View blockchain |
| `/is_valid` | GET | Validate blockchain |

---

## 🔐 How Blockchain Works in This Project  

- Each vote is stored as a **block**  
- Every block contains:  
  - Voter ID  
  - Candidate ID  
  - Timestamp  
  - Previous hash  
  - Current hash  
- Blocks are linked using cryptographic hashes (**SHA-256**)  
- Any attempt to modify a vote will break the chain  

---

## 📸 Future Enhancements  

- 🔑 User authentication & login system  
- 🧠 AI-based fraud detection  
- 🌍 Deployment on cloud (AWS / Render)  
- 📱 Improved UI with React or Bootstrap  
- 🔒 One-person-one-vote validation  

---

## 🎯 Learning Outcomes  

- Understanding of **Blockchain fundamentals**  
- Building **REST APIs using Flask**  
- Integration of **MySQL with Python**  
- Designing secure and transparent systems  

---

## 🤝 Contributing  

Contributions are welcome!  
Feel free to fork the repository and submit a pull request.  

---

## 📄 License  

This project is licensed under the **MIT License**.  

---

## 👨‍💻 Author  

**Yogeshwar N**  
- Aspiring Software Developer  
- Interested in Blockchain, AI & Full Stack Development  
