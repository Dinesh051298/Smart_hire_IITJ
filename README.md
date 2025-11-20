# SmartHire - AI-Powered Resume Screening & Ranking System  
**by [Dinesh Periyasamy](https://github.com/Dinesh051298)**  

SmartHire is an **AI-driven web application** designed to revolutionize the recruitment process by automating **resume screening and candidate ranking** using **advanced NLP techniques**.  
It helps recruiters instantly identify top candidates by comparing resumes with job descriptions intelligently and efficiently.  

---

## Features 

| Category | Highlights |
|-----------|-------------|
| **Authentication** | Secure, role-based login for Applicants & Recruiters |
| **Resume Intelligence** | Upload and parse resumes (extracts skills, education, experience, and contact info) |
| **JD Management** | Upload, store, and manage Job Descriptions effortlessly |
| **AI-Powered Matching** | Uses **spaCy**, **NLTK**, and **TF-IDF / BERT embeddings** for semantic similarity |
| **Smart Ranking** | Automatically ranks resumes based on content and skill overlap |
| **Detailed Insights** | Displays matched and missing skills with confidence scores |
| **Dashboards** | Separate Recruiter and Applicant dashboards with easy navigation |

---

## Tech Stack Overview

| Layer | Technology |
|--------|-------------|
| **Frontend** | HTML5, CSS3, Bootstrap, Jinja2 Templates |
| **Backend** | Python, Flask |
| **AI/NLP** | spaCy, NLTK, scikit-learn |
| **Database** | MongoDB (NoSQL) |
| **Similarity Engine** | TF-IDF / BERT + Cosine Similarity |

---

---

## 🗂️ Project Structure

```
smart_hire/
├── app/
│ ├── templates/ # Jinja2 HTML templates (UI pages)
│ ├── static/ # CSS, JS, and image assets
│ ├── routes/ # Flask route definitions
│ ├── models/ # MongoDB model wrappers
│ ├── nlp/ # NLP resume-JD parsers & similarity modules
│ ├── forms/ # Flask-WTF form definitions
│ └── init.py # Flask app factory
├── requirements.txt # Python dependencies
├── init_db.py # MongoDB index initializer
├── run.py # Application entry point
└── README.md # Project documentation
```

---


---

## ⚙️ Installation Guide

### Prerequisites
Ensure you have the following installed:
- Python ≥ 3.8  
- MongoDB (Local / Atlas)
- `pip` package manager

---

### Setup Steps

### Clone the repository

```bash
git clone https://github.com/Dinesh051298/smart_hire_IITJ.git
```
```bash
cd smart_hire_IITJ
```


### Create virtual environment
```bash
python -m venv venv
```

```bash
venv\Scripts\activate     # (Windows)
```
```bash
#source venv/bin/activate  # (Linux/Mac)
```


### Install required dependencies
```bash
pip install -r requirements.txt
```

### Download NLP models
```bash
python -m spacy download en_core_web_sm
```


### ⚙️Configuration

Create a .env file in your project root:

```bash
SECRET_KEY=your_secret_key_here  Example: '8a2f1b3e8c9c4a8b7e6f0d3e5a4b1c8a3df2d9c2b4a6f8'
MONGO_URI=mongodb://localhost:27017/smart_hire
```



### Running the Application

### Start MongoDB (skip if already running)
```bash
mongod
```


### Run Flask app
```bash
python app.py
```


Visit the application at: 👉 http://localhost:5000

## 👨‍💻 User Guide

🧍‍♂️ For Applicants:
Register and log in

Upload your resume (.pdf or .docx)

View extracted resume insights



## 🧑‍💼 For Recruiters:
Register and log in

Upload job descriptions

Automatically view candidate rankings

Explore detailed skill and content match reports


## Resume–JD Matching Engine

SmartHire’s matching system uses a multi-layered AI approach:

### 🔍 Step-by-Step Process

| Step | Description |
|------|--------------|
| **Text Extraction** | Extracts key information such as keywords, skills, education, and work experience from both resumes and job descriptions. |
| **Preprocessing** | Cleans and prepares text data through tokenization, stop-word removal, and lemmatization. |
| **Vectorization** | Converts textual data into numerical vectors using **TF-IDF** or **BERT embeddings** for semantic understanding. |
| **Similarity Scoring** | Computes **Cosine Similarity** between resume and JD vectors to measure alignment. |
| **Result Generation** | Produces a **match score**, highlights **matched/missing skills**, and provides an **overall ranking** of candidates. |

---

## Block Diagram

<img width="7676" height="1038" alt="Untitled diagram-2025-11-20-123107" src="https://github.com/user-attachments/assets/74df0d6d-082b-4b77-b79d-7c2652eaabbd" />


## Output Screenshots

### Applicant dashboard
<img width="1603" height="956" alt="image" src="https://github.com/user-attachments/assets/cebf3427-73c9-4ed2-a52d-e669eba36464" />
<img width="1358" height="902" alt="image" src="https://github.com/user-attachments/assets/1668fbe1-b195-4a48-bf8c-4eff47ec6faf" />


### Recruiter dashoard
<img width="1401" height="898" alt="image" src="https://github.com/user-attachments/assets/e25fb1e0-4e14-45c7-9e9c-6821340fd3e9" />

<img width="1398" height="730" alt="image" src="https://github.com/user-attachments/assets/35e16be8-6f33-42cd-8d16-6bdddfb2198f" />



## Future Enhancements

GPT-based Resume Analysis & Feedback

Advanced Visualization Dashboards

Integration with ATS Systems

Real-time Job Recommendation Engine

## ❤️ Acknowledgements

Special thanks to **Dr. Md. Abu Talhamainuddin Ansary** for his constant guidance, support, and mentorship throughout this project.

Grateful to the **IIT Jodhpur Data Engineering Program** for providing academic direction.


 ## 📬Contact

Author: Dinesh Periyasamy

Email: dinesh.iot.developer@gmail.com

Website: www.dineshperiyasamy.com
