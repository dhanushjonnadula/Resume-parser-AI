# 🎯 AI Resume Job Role Matcher

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.1.3-green)](https://flask.palletsprojects.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📄 Overview
AI Resume Job Role Matcher is a **Flask web application** that analyzes uploaded resumes (PDF, DOCX, TXT) and predicts the **top matching job roles** using TF-IDF vectorization and cosine similarity. It matches against a dataset of resumes categorized by job roles (e.g., Data Scientist, HR, etc.).

**Live Demo**: Run locally at `http://127.0.0.1:5000`

## ✨ Features
- ✅ Upload resumes in **PDF, DOCX, TXT** formats
- ✅ **NLP-powered** parsing with NLTK (tokenization, stopwords removal)
- ✅ **TF-IDF + Cosine Similarity** for accurate job role matching
- ✅ **Top 10 matches** with confidence scores
- ✅ **Responsive UI** with clean design (upload form + results table)
- ✅ **No ML training needed** - zero-shot matching on pre-built dataset
- ✅ Easy deployment (Flask app)

## 🎨 Screenshots
### Home Page
![Home](screenshots/home.png) *(Add your screenshot here)*

### Results Page
![Results](screenshots/results.png) *(Add your screenshot here)*

## 🚀 Quick Start
```bash
# Clone the repo
git clone <your-repo-url>
cd parser-project

# Create virtual environment (recommended)
python -m venv venv
# On Windows: venv\\Scripts\\activate
# On macOS/Linux: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
```
Open `http://127.0.0.1:5000` in your browser!

## 📝 Usage
1. **Upload** your resume via the home page form.
2. **Analyze** - AI extracts text, preprocesses it, and computes matches.
3. **View Results** - Top 10 job categories with match scores (0-10).

**Example Output**:
| Category          | Score |
|-------------------|-------|
| Data Science      | 8.7   |
| Machine Learning  | 7.9   |
| Python Developer  | 6.5   |

## 🛠 How It Works
```
Resume Upload → Text Extraction (pdfplumber/docx) 
→ Preprocessing (NLTK) → TF-IDF Vectorization (sklearn)
→ Cosine Similarity vs Resume.csv Dataset → Top Matches
```
- **Dataset**: `Resume.csv` (job categories + resume texts)
- **Model**: Unsupervised similarity matching (no training required)

## 📁 File Structure
```
d:/parser project/
├── app.py              # Flask app (routes)
├── model.py            # Core matching logic
├── requirements.txt    # Dependencies
├── Resume.csv          # Job role dataset
├── templates/          # HTML templates
│   ├── index.html      # Upload form
│   └── result.html     # Results table
├── static/             # CSS styles
│   └── style.css
├── uploads/            # Temp uploads
├── TODO.md             # Task progress
└── README.md           # This file!
```

## 🐛 Dependencies
See [requirements.txt](requirements.txt). Key libs:
- Flask (web framework)
- NLTK, scikit-learn (NLP/ML)
- pdfplumber, python-docx (parsing)

## 🔧 Contributing
1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push (`git push origin feature/amazing-feature`)
5. Open a Pull Request

**Issues?** Open one [here](https://github.com/yourusername/parser-project/issues)!

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙌 Acknowledgments
- Dataset inspired by [Joblib](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)
- Built with ❤️ using Flask & scikit-learn

---

⭐ **Star the repo if you found it useful!** 🚀
