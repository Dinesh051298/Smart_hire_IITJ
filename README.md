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

# Clone the repository

```bash
git clone https://github.com/Dinesh051298/smart_hire_IITJ.git
```
```bash
cd smart_hire_IITJ
```


# Create virtual environment
```bash
python -m venv venv
```

```bash
venv\Scripts\activate     # (Windows)
```
```bash
#source venv/bin/activate  # (Linux/Mac)
```


# Install required dependencies
```bash
pip install -r requirements.txt
```

# Download NLP models
```bash
python -m spacy download en_core_web_sm
```


# ⚙️Configuration

Create a .env file in your project root:

```bash
SECRET_KEY=your_secret_key_here  Example: '8a2f1b3e8c9c4a8b7e6f0d3e5a4b1c8a3df2d9c2b4a6f8'
MONGO_URI=mongodb://localhost:27017/smart_hire
```



# Running the Application

### Start MongoDB (skip if already running)
```bash
mongod
```


# Run Flask app
```bash
python run.py
```


Visit the application at: 👉 http://localhost:5000

## 👨‍💻 User Guide

🧍‍♂️ For Applicants:
Register and log in

Upload your resume (.pdf or .docx)

View extracted resume insights

Get job recommendations based on your profile



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






## 🧑‍💻Developer Notes

Built with Flask Blueprints for modular routing

Designed with Bootstrap 5 responsive UI

Integrates MongoDB Atlas for cloud-ready deployment

Easily extensible to include BERT, Sentence Transformers, or LLMs for advanced semantic understanding

## Future Enhancements

GPT-based Resume Analysis & Feedback

Advanced Visualization Dashboards

Integration with ATS Systems

Real-time Job Recommendation Engine

 ##  ❤️Acknowledgements

Special thanks to the IIT Jodhpur Data Engineering Program for academic guidance and the open-source AI community for enabling innovation.

 ## 📬Contact

Author: Dinesh Periyasamy

Email: dinesh.iot.developer@gmail.com

Website: www.dineshperiyasamy.com
