# 🧠 AI Resume Skill Analyzer

An intelligent resume analysis tool built with Python and Gradio that automatically detects skills from a PDF resume, predicts suitable job roles, and provides direct job application links — all within a clean, mobile and desktop compatible web interface.

---

##  Demo
<img width="932" height="440" alt="image" src="https://github.com/user-attachments/assets/e15ebbd8-c0bf-4dfb-8dad-fb74a4139d13" />

## ✨ Features

- 📄 **PDF Resume Parsing** — Extracts raw text from any standard PDF resume using PyMuPDF
- 🔍 **Skill Detection** — Matches resume content against a curated skill database across 9 tech domains
- 🎯 **Job Role Prediction** — Scores and ranks the most suitable job roles based on detected skills
- 🔗 **Job Application Links** — Provides direct LinkedIn job search links for each matched role
- 📱 **Mobile + Desktop Compatible** — Fully responsive UI powered by Gradio
- ☁️ **Google Colab Ready** — Runs entirely in the browser, no local setup needed

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| [Gradio](https://gradio.app/) | Web UI framework |
| [PyMuPDF (fitz)](https://pymupdf.readthedocs.io/) | PDF text extraction |
| `re` | Text cleaning with regex |
| `pandas` | Data handling |
| Google Colab | Cloud notebook environment |

---

## 🚀 Getting Started

### Option 1 — Run on Google Colab (Recommended)

1. Open the notebook `AI_Resume_Skill_Analyzer_.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Click **Runtime → Run All**
3. Wait for the Gradio public link to appear (e.g. `https://xxxxxx.gradio.live`)
4. Open the link and upload your PDF resume

### Option 2 — Run Locally

**Prerequisites:** Python 3.8+

```bash
# Clone the repository
git clone https://github.com/your-username/ai-resume-skill-analyzer.git
cd ai-resume-skill-analyzer

# Install dependencies
pip install gradio pymupdf pandas

# Run the notebook or convert to script and run
jupyter notebook AI_Resume_Skill_Analyzer_.ipynb
```

---

## 📂 Project Structure

```
ai-resume-skill-analyzer/
│
├── AI_Resume_Skill_Analyzer_.ipynb   # Main project notebook
├── README.md                          # Project documentation
└── resume_analyzer.mp4                # Demo video
```

---

## 🧩 How It Works

```
PDF Resume Uploaded
        ↓
Text Extracted (PyMuPDF)
        ↓
Text Cleaned (regex normalization)
        ↓
Skills Detected (keyword matching against role database)
        ↓
Job Roles Scored & Ranked (by number of skill matches)
        ↓
Results Displayed with LinkedIn Job Links
```

### Step-by-Step Breakdown

| Step | Description |
|---|---|
| 1 | Install `gradio` and `pymupdf` |
| 2 | Import all required libraries |
| 3 | Define skill database for 9 job roles |
| 4 | Define LinkedIn job search links per role |
| 5 | Extract text from uploaded PDF using PyMuPDF |
| 6 | Clean text using regex (remove special characters, normalize whitespace) |
| 7 | Detect skills by matching cleaned text against the skill database |
| 8 | Score and rank job roles by number of matching skills |
| 9 | Build formatted output with skills, roles, scores, and links |
| 10 | Launch Gradio web interface |

---

## 💼 Supported Job Roles & Skills

| Job Role | Skills Detected |
|---|---|
| Frontend Developer | HTML, CSS, JavaScript, React, Bootstrap, Tailwind, UI |
| Backend Developer | Python, Java, PHP, Node.js, MySQL, API, Django, Flask |
| Data Analyst | Python, Excel, SQL, Power BI, Tableau, Pandas, NumPy |
| Database Analyst | SQL, MySQL, Oracle, MongoDB, PostgreSQL |
| System Analyst | System Analysis, UML, Testing, Documentation, Requirement Analysis |
| Machine Learning Engineer | Machine Learning, TensorFlow, Keras, Scikit-learn, CNN, Deep Learning, OpenCV |
| Cyber Security Analyst | Network Security, Ethical Hacking, Linux, Firewall, Kali Linux |
| Android Developer | Android, Kotlin, Java, Android Studio, Firebase |
| Cloud Engineer | AWS, Azure, Google Cloud, Docker |

---

## 🖥️ UI Preview

The Gradio interface includes:
- A **PDF file upload** button (mobile and desktop friendly)
- A **text output box** (30 lines) showing:
  - Detected skills list
  - Ranked job roles with match scores
  - Direct LinkedIn apply links

---

## 📊 Sample Output

```
==================================
 DETECTED SKILLS
==================================

• Python
• Pandas
• Numpy
• Sql
• Tableau
• Excel


==================================
 SUITABLE JOB ROLES
==================================

Data Analyst
Match Score: 6
Apply Here:
https://www.linkedin.com/jobs/data-analyst-jobs/

--------------------------

Backend Developer
Match Score: 2
Apply Here:
https://www.linkedin.com/jobs/backend-developer-jobs/
```

---

## ⚠️ Limitations

- Skill detection is keyword-based — context-aware matching is not yet implemented
- Only PDF format is supported (no `.docx` or image-based resumes)
- The Gradio public share link expires after **1 week** when run via Colab
- Skills database is limited to the 9 predefined roles above

---

## 🔮 Future Improvements

- [ ] Add support for `.docx` and image-based resumes (OCR)
- [ ] Integrate Claude/GPT API for contextual skill extraction
- [ ] Expand job role database to cover more domains
- [ ] Add skill gap analysis (what skills to learn for a target role)
- [ ] Deploy permanently on Hugging Face Spaces

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Fork the repository
- Add new job roles or skills to the database
- Improve the text extraction logic
- Submit a pull request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

Built with ❤️ using Python, Gradio, and PyMuPDF.

> ⭐ If you found this project helpful, please give it a star on GitHub!
