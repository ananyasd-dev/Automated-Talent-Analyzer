# Automated Talent Analyzer 📝
The **Automated Talent Analyzer** is an intelligent web-based platform designed to help job seekers evaluate and enhance their resumes by comparing them directly against specific job descriptions. Leveraging advanced AI models, this tool simulates how Applicant Tracking Systems (ATS) and recruiters assess your resume for relevance, alignment, and suitability for a role. 

🚀 **[Click Here to View the Live Live Application!](https://streamlit.app)**

## 🔍 Key Engineering Features
### 1. Resume Text Extraction
Users upload resumes in PDF format, and the system automatically extracts the raw text for further analysis using `pdfminer`.

### 2. ATS Similarity Vector Scoring
Using Sentence Transformers (`all-mpnet-base-v2`), the tool calculates a precise cosine similarity score between the resume and the job description. This matches requirements typically scanned by corporate ATS software.

### 3. AI-Powered Resume Evaluation & Feedback
Powered by Groq's `llama-3.3-70b-versatile` LLM, the tool generates a detailed, human-readable evaluation report scoring skills and experience out of 5 with clear visual indicator indicators (✅, ❌, ⚠️).

### 4. Downloadable Reports
Users can export their complete text analysis report to a local text file with one click to track and implement the suggested changes.

### 5. Custom Added: Personalized Interview Practice Tips
An interactive, state-managed dashboard component that displays tailored behavioral and technical interview preparation frameworks based on the candidate's core profile metrics.

---

# ⚙️ Installation & Local Setup

Follow these steps to set up and run the system locally:

### 1️⃣ Clone the Repository
```bash
git clone https://github.com
cd Automated-Talent-Analyzer
```

### 2️⃣ Set Up a Virtual Environment
```bash
python -m venv myenv
./myenv/Scripts/activate
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Set Up Cloud Secrets (.env)
Create a `.env` file in your root folder (this file is hidden from public git pushes for security):
```text
GROQ_API_KEY=your_groq_api_key_here
```

### 5️⃣ Run the Streamlit App
```bash
streamlit run main.py
```

---

## 🛠️ Credits & Engineering Enhancements
This project was fork-engineered from the baseline AI Resume Analyzer open-source tutorial created by **Altoks-AI** ([Original Tutorial Video](https://youtu.be/XfoHr9GivCs)). 

To elevate the application into a custom production build, I performed a complete system migration and integrated several architectural enhancements:
* **Branding Refactor**: Re-engineered the UI layout, headers, and state structures to transition from a generic baseline into the *Automated Talent Analyzer*.
* **Feature Engineering**: Designed and implemented an interactive, state-managed **Personalized Interview Practice Tips** drop-down matrix component at the bottom of the reporting pipeline to increase user post-analysis value.
* **Security Hardening**: Fixed critical deployment risks by decoupling hardcoded production variables using a strict `.gitignore` layer to prevent private `GROQ_API_KEY` infrastructure leaks online.
* **Environment Synchronization**: Re-mapped system routes and fixed variable indentation conflicts (`StreamlitDuplicateElementId`) to enable seamless execution within native cloud pipelines.
* **Cloud Infrastructure Distribution**: Successfully deployed and routed the active production system natively via Streamlit Community Cloud.
