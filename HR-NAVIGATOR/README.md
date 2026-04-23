# 🧭 HR Navigator — Workforce Intelligence Platform

> The only HR platform that follows your employees from the day they applied to the day they leave.

---

## 📁 Project Structure

```
hr-navigator/
│
├── app.py                    ← Main entry point (run this)
│
├── pages/
│   ├── __init__.py
│   ├── home.py               ← Landing page & journey overview
│   ├── recruitment.py        ← Recruitment + Resume AI + Culture DNA
│   ├── retention.py          ← Attrition prediction + Life Events + Early Warning
│   ├── promotion.py          ← Promotion eligibility + Regret Score
│   └── analytics.py          ← Cross-module platform analytics
│
├── .streamlit/
│   └── config.toml           ← Theme & server config
│
├── requirements.txt          ← Python dependencies
├── .gitignore
└── README.md
```

---

## 🚀 How to Run Locally (Step by Step)

### Step 1 — Install Python
Make sure you have Python 3.10 or higher installed.
Download from: https://www.python.org/downloads/

Check your version:
```bash
python --version
```

### Step 2 — Clone or Download the Project
If using Git:
```bash
git clone https://github.com/YOUR_USERNAME/hr-navigator.git
cd hr-navigator
```

Or download the ZIP from GitHub and extract it, then open a terminal in the folder.

### Step 3 — Create a Virtual Environment (Recommended)
```bash
# Create the environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### Step 4 — Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 5 — Run the App
```bash
streamlit run app.py
```

The app will open automatically at: **http://localhost:8501**

---

## ☁️ Deploy to Streamlit Cloud (Free — Recommended)

This is the easiest way to share your app with anyone online.

### Step 1 — Push to GitHub

First, create a GitHub account at https://github.com if you don't have one.

Then create a new repository:
1. Go to https://github.com/new
2. Name it `hr-navigator`
3. Make it **Public**
4. Click **Create repository**

Then push your code:
```bash
# In your project folder
git init
git add .
git commit -m "Initial commit — HR Navigator Platform"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/hr-navigator.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### Step 2 — Deploy on Streamlit Cloud

1. Go to **https://share.streamlit.io**
2. Sign in with your GitHub account
3. Click **"New app"**
4. Fill in the form:
   - **Repository:** `YOUR_USERNAME/hr-navigator`
   - **Branch:** `main`
   - **Main file path:** `app.py`
5. Click **"Deploy!"**

Your app will be live at:
```
https://YOUR_USERNAME-hr-navigator-app-XXXXX.streamlit.app
```

Deployment takes about 2–3 minutes. That's it — free hosting, forever.

---

## 🗂️ What Dataset to Upload in Each Module

### Recruitment Module
Upload any CSV with these columns:
```
Age, Gender, EducationLevel, ExperienceYears, PreviousCompanies,
DistanceFromCompany, InterviewScore, SkillScore, RecruitmentStrategy,
HiringDecision (0 or 1), PersonalityScore
```
Sample dataset: https://www.kaggle.com/datasets/rabieelkharoua/predicting-hiring-decisions-in-recruitment-data

### Retention / Attrition Module
Upload IBM HR Analytics dataset with these columns:
```
Department, JobRole, MaritalStatus, OverTime, JobSatisfaction, Age,
Attrition (Yes/No)
```
Sample dataset: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

### Promotion Module
Upload HR promotion dataset with these columns:
```
employee_id, department, region, education, gender, recruitment_channel,
no_of_trainings, age, previous_year_rating, length_of_service,
awards_won, avg_training_score, is_promoted (0 or 1)
```
Sample dataset: https://www.kaggle.com/datasets/arashnic/hr-ana

---

## 🧠 Resume Screener — How to Use

The Resume Screener in the Recruitment module accepts **plain text (.txt) files**.

To test it:
1. Copy any resume text into a `.txt` file (e.g., `john_doe.txt`)
2. Upload it in the Resume Screener tab
3. Paste a job description in the text box
4. The AI will score and rank candidates automatically

### Example Resume TXT Format:
```
John Doe
5 years experience in data analysis
Skills: Python, SQL, Tableau, machine learning, communication, leadership
Education: Master of Science in Data Analytics
Previous companies: Google, Deloitte
```

---

## 🔑 Key Features Summary

| Feature | Module | What Makes It Unique |
|---|---|---|
| Culture DNA Matching | Recruitment | Matches candidates to your TOP performers, not just job descriptions |
| Resume AI Screener | Recruitment | Parses TXT resumes, extracts skills, ranks candidates automatically |
| Life Event Signals | Retention | Detects personal life triggers that cause attrition — missed by all other tools |
| Early Warning Dashboard | Retention | Team-level risk overview with manager-specific recommended actions |
| Promotion Regret Score | Promotion | Predicts 18-month post-promotion success, not just eligibility |
| Readiness Timeline | Promotion | Tells you exactly WHEN someone will be ready, not just IF |
| Platform Analytics | All | Cross-module insights — full employee lifecycle in one view |

---

## 🛠️ Tech Stack

- **Frontend:** Streamlit
- **ML Models:** scikit-learn (Random Forest, Gradient Boosting, Logistic Regression, Decision Tree, SVM)
- **Data:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **PDF Export:** fpdf
- **Deployment:** Streamlit Cloud (free)

---

## 📬 Questions?

Open an issue on GitHub or contact the maintainer.
