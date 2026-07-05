# 🤖 AI Impact on Students — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Viz-4C72B0?logo=python&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?logo=kaggle&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

An exploratory data analysis project examining how **Generative AI tools affect students' academic performance, anxiety levels, skill retention, and burnout risk** across various majors and years of study.

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Analysis Questions](#-analysis-questions)
- [Methodology](#-methodology)
- [Key Insights & Findings](#-key-insights--findings)
- [Visualizations](#-visualizations)
- [Libraries Used](#-libraries-used)
- [How to Run](#-how-to-run)
- [Recommendations](#-recommendations)
- [Future Work](#-future-work)
- [License](#-license)

---

## 🎯 About the Project

This project analyzes how artificial intelligence technology — particularly Generative AI tools — affects students' experiences, learning outcomes, and behavior. Using a dataset of student records, the analysis explores patterns in AI usage across different academic majors, year levels, and use cases, while also examining the relationship between AI engagement and indicators such as GPA change, exam anxiety, and burnout risk.

The goal is to provide data-driven insights that can inform educators, institutions, and students about the responsible and effective use of AI in academic settings.

---

## 📦 Dataset

| Attribute | Detail |
|---|---|
| **Source** | [Kaggle — AI Impact on Students](https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students) |
| **File** | `ai_student_impact_dataset.csv` |
| **Dimensions** | 1,000+ rows × 15 columns |
| **Missing Values** | None — dataset is clean |

### Column Reference

| Column | Type | Description |
|---|---|---|
| `Major_Category` | categorical | Student's field of study (STEM, Medical, Humanities, etc.) |
| `Year_of_Study` | categorical | Academic year (Freshman, Sophomore, Junior, Senior) |
| `Primary_Use_Case` | categorical | Main purpose for using GenAI (e.g., Debugging/Troubleshooting) |
| `Prompt_Engineering_Skill` | categorical | Self-rated skill level (Beginner, Intermediate, Advanced) |
| `Institutional_Policy` | categorical | Institution's AI usage policy |
| `Burnout_Risk_Level` | categorical | Assessed burnout level (Low, Medium, High) |
| `Weekly_GenAI_Hours` | numerical | Hours per week spent using Generative AI |
| `Pre_Semester_GPA` | numerical | GPA recorded before the semester |
| `Post_Semester_GPA` | numerical | GPA recorded after the semester |
| `Anxiety_Level_During_Exams` | numerical | Self-reported exam anxiety level |
| `Skill_Retention_Score` | numerical | Score measuring knowledge retention |

### Key Categorical Breakdowns

| Column | Dominant Category |
|---|---|
| Major Category | STEM — 15,059 students |
| Year of Study | Junior — 11,045 students |
| Primary Use Case | Debugging/Troubleshooting — 12,295 students |
| Prompt Engineering Skill | Beginner — 18,495 students |
| Institutional Policy | Allowed with Citation — 25,224 students |
| Burnout Risk Level | Medium — 21,144 students |

---

## 📁 Project Structure

```
ai-impact-on-students-eda/
│
├── ai-impact-on-students.ipynb     # Main analysis notebook
├── ai_student_impact_dataset.csv   # Raw dataset
└── README.md
```

---

## ❓ Analysis Questions

This EDA is structured around six core questions:

1. **Which major uses Generative AI the most?**
   Comparing average weekly GenAI hours across academic disciplines.

2. **Why do students use GenAI — and which use case is most time-intensive?**
   Grouping `Weekly_GenAI_Hours` by `Primary_Use_Case`.

3. **Which major has the highest pre- and post-semester GPA?**
   Examining academic performance before and after AI exposure.

4. **Which year of study reports the highest anxiety during exams?**
   Aggregating `Anxiety_Level_During_Exams` by `Year_of_Study`.

5. **Which year of study uses GenAI the most?**
   Understanding adoption rate across freshman to senior level.

6. **Does higher burnout risk correlate with higher exam anxiety?**
   Cross-tabulating `Burnout_Risk_Level` with `Anxiety_Level_During_Exams`.

---

## 🔬 Methodology

```
Raw Dataset (CSV)
       │
       ▼
[1] Dataset Overview
       • Shape, dtypes, memory usage
       • Sample rows (head, tail, random sample)
       • Dimensionality check
       │
       ▼
[2] Data Quality Check
       • Missing values analysis
       • Duplicate detection
       • Descriptive statistics (numerical & categorical)
       │
       ▼
[3] Univariate Analysis
       • Value counts per categorical column
       • Histograms for all numerical columns
       • Skewness & kurtosis
       │
       ▼
[4] Bivariate & Multivariate Analysis
       • Correlation matrix + heatmap
       • Covariance matrix
       • GroupBy aggregations (6 analytical questions)
       • Pairplot for key numerical variables
       │
       ▼
[5] Visualization Suite (10 chart types)
       • Bar charts, pie charts, boxplots
       • Scatterplots, countplots, pairplots
       • Missing value heatmap
       │
       ▼
[6] Insights, Conclusions & Recommendations
```

---

## 📊 Key Insights & Findings

1. **STEM students are the heaviest GenAI users**, averaging **10.49 hours/week**, while Humanities students average the least at **6.77 hours/week**.

2. **Debugging & Troubleshooting is the most time-intensive use case** for Generative AI among students.

3. **Medical students have the highest average Pre-Semester GPA**, indicating a higher academic baseline entering the semester.

4. **STEM students achieve the highest average Post-Semester GPA**, suggesting GenAI usage may contribute to academic improvement in technical fields.

5. **Sophomore students report the highest anxiety levels during exams**, potentially reflecting the transition from introductory to more demanding coursework.

6. **Senior students spend the most time using Generative AI**, likely due to thesis work, research, and complex project requirements.

7. **High burnout risk is strongly associated with high exam anxiety**, pointing to a compounding effect between workload stress and academic pressure.

8. **Most numerical variables show slight positive skewness**, indicating a small number of students with notably high values driving the distribution.

9. **Covariance matrix reveals positive relationships** between several academic performance variables, especially between pre- and post-semester GPA.

10. **No missing values were found**, confirming the dataset is clean and ready for downstream machine learning modeling.

---

## 📈 Visualizations

The notebook produces **20+ visualizations** across 10 chart types:

| Chart Type | Variables | Purpose |
|---|---|---|
| Correlation heatmap | All numerical columns | Identify relationships between variables |
| Bar charts | `Major_Category`, `Year_of_Study`, `Primary_Use_Case` | Distribution of categorical variables |
| Histograms | All numerical columns | Frequency distribution per variable |
| Boxplots | All numerical columns | Outlier detection and spread |
| Scatterplots | Pre vs Post GPA · GenAI Hours vs Anxiety · GenAI Hours vs Skill Retention | Bivariate relationships |
| Countplots | `Burnout_Risk_Level`, `Institutional_Policy`, `Prompt_Engineering_Skill` | Count per category |
| Pie charts | `Major_Category`, `Burnout_Risk_Level` | Proportion per group |
| Pairplot | GPA (pre/post), Weekly GenAI Hours, Skill Retention Score | Multivariate overview |
| Missing value heatmap | All columns | Data completeness check |
| GroupBy aggregations | Multiple combinations | Answering specific analytical questions |

---

## 📚 Libraries Used

```python
pandas        # Data manipulation and aggregation
numpy         # Numerical computation
matplotlib    # Static visualizations
seaborn       # Statistical visualizations
warnings      # Suppress runtime warnings
```

Install all dependencies at once:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## ▶️ How to Run

### On Kaggle (Recommended)

1. Open the notebook on Kaggle: [Link to Notebook](#) *(replace with your notebook URL)*
2. Add the dataset: [AI Impact on Students](https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students)
3. Click **Run All** — all libraries are pre-installed in the Kaggle environment

### Locally

```bash
# Clone the repository
git clone https://github.com/username/ai-impact-on-students-eda.git
cd ai-impact-on-students-eda

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook ai-impact-on-students.ipynb
```

> **Note:** Update the dataset path in the first code cell from `/kaggle/input/...` to your local path, e.g. `./ai_student_impact_dataset.csv`.

---

## 💡 Recommendations

Based on the findings, the following actions are recommended for institutions and educators:

1. **Encourage balanced GenAI usage** — promote responsible use without over-reliance on AI tools.
2. **Introduce AI literacy programs** — help students use AI effectively and ethically across all disciplines.
3. **Support high-burnout students** — implement counseling and wellness programs targeting students identified as high burnout risk.
4. **Reframe AI as a learning assistant** — emphasize that AI should complement, not replace, critical thinking.
5. **Blend traditional and AI-assisted study methods** — encourage students to maintain conventional study habits alongside AI usage.
6. **Develop institution-level AI policies** — standardize guidelines for ethical and academic AI use.
7. **Conduct longitudinal assessments** — measure the long-term impact of GenAI adoption on learning outcomes over multiple semesters.

---

## 🔮 Future Work

- Apply machine learning models (e.g., logistic regression, random forest) to predict burnout risk or GPA change based on GenAI usage patterns
- Perform clustering to identify student personas based on AI behavior and academic performance
- Conduct sentiment analysis if open-ended survey responses are available
- Expand the dataset to include more institutions and geographic regions for broader generalizability

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

The dataset is sourced from Kaggle and used for educational and non-commercial analytical purposes.

---

<div align="center">
  <p>Built with ❤️ using Python & Jupyter Notebook</p>
  <p>⭐ If you found this project helpful, consider leaving a star!</p>
</div>
