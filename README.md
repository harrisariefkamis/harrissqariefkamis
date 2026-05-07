# Haris Arief Kamis - Data Analyst Enthusiat

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=harisariefkamis&color=blue)
![GitHub followers](https://img.shields.io/github/followers/harisariefkamis?style=social)

**Data Analysis | Machine Learning | Data Science | Business Intelligence**

📍 Bogor Timur, Kota Bogor, 16144, Indonesia  
📧 [harisariefkamis16@gmail.com](mailto:harisariefkamis16@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/harisariefkamis) | [GitHub](https://github.com/harisariefkamis) | 📱 +6285282436796

</div>

---

## 🎯 About Me

Seorang **Data Analyst & Data Scientist** bersemangat dengan pengalaman dalam **data analysis, machine learning, dan business intelligence**. Memiliki keahlian dalam mengubah data mentah menjadi insights yang actionable untuk mendukung keputusan bisnis strategis.

Sedang menempuh **S1 Sains Data** di Universitas Insan Cita Indonesia (IPK: 3.69) dan telah menyelesaikan berbagai bootcamp intensif di bidang data science dan analytics. Passionate tentang **problem-solving, automation, dan continuous learning**.

---

## 🎓 Pendidikan

| Institusi | Program | Durasi | IPK | Status |
|-----------|---------|--------|-----|--------|
| **Universitas Insan Cita Indonesia (UICI)** | S1 Sains Data | April 2023 - 2025 | 3.69 | Aktif (Semester II) |
| **Global Science Institute (GSI)** | D1 Teknik Komputer | Agustus 2016 | 2.91 | Selesai |

---

## 📚 Sertifikasi & Pelatihan

### 🏆 Digital Talent Scholarship (DTS) Komdigi
- **Fundamental Data Science + Python** (31 JP) - 2025
  - Data Scraping, Explorasi Data, Data Cleansing, Data Annotation
  - Python Programming, NumPy, Pandas, Scikit-Learn
  - Model Building, Tuning & Evaluation
  
- **Intermediate Data Science** (20 JP) - 2025
  - Data Screening & Validation
  - Feature Selection & Data Construction
  - Model Strategy & Evaluation

### 🎯 DqLab Bootcamp Certificates
- **Data Analyst FullStack Intensive Bootcamp** (Batch #14) - Jan-Feb 2024
  - SQL, Python, Data Visualization
  - Data Formatting, Cleansing & Analysis
  
- **Mini Bootcamp DqLab** (Batch #10) - Feb 2026
  - Machine Learning & AI for Beginner
  - Data Analyst with SQL & Python

### 🌐 Kementerian Komunikasi dan Digital
- **Pengenalan Data Science dan Pemanfaatannya di Berbagai Sektor** - 2025

### 📖 Additional Training
- **TOEFL Preparation Bootcamp** - Juni-Juli 2024

---

## 💻 Technical Skills

### **🐍 Bahasa Pemrograman**

### **📊 Data Analysis & Visualization**
- **Libraries & Frameworks:**
  - `Pandas` - Data manipulation & cleaning
  - `NumPy` - Numerical computing
  - `Matplotlib` - Static visualizations
  - `Seaborn` - Statistical data visualization
  - `Plotly` - Interactive dashboards
  
- **Visualization Tools:**
  - Google Looker Studio
  - Google Sheets Advanced Analytics
  - Microsoft Power BI (Basic)

### **🤖 Machine Learning & Statistics**
- **Scikit-Learn:**
  - Supervised Learning (Regression, Classification)
  - Unsupervised Learning (Clustering, Dimensionality Reduction)
  - Model Selection & Hyperparameter Tuning
  - Pipeline Building
  
- **Statistical Methods:**
  - Exploratory Data Analysis (EDA)
  - Hypothesis Testing
  - Probability Distribution Analysis
  - Correlation & Regression Analysis
  - Time Series Analysis
  - Linear Algebra & Calculus Application

- **Predictive Modeling:**
  - Linear Regression
  - Logistic Regression
  - Decision Tree & Random Forest
  - Ensemble Methods
  - Model Evaluation & Metrics

### **🗄️ Database & Data Warehousing**
- PostgreSQL
- Google BigQuery
- Google Sheets
- Data Integration

### **📈 Business Intelligence & Reporting**
- Dashboard Design & Development
- KPI Tracking
- Data Storytelling
- Business Metrics Analysis
- Report Automation

### **🛠️ Development Tools**
- Google Colaboratory (Jupyter Notebooks)
- Jupyter Notebook
- Git & GitHub
- VS Code
- Google Cloud Platform (Basic)

### **🎨 Other Skills**
- Microsoft Office (Word, Excel, PowerPoint)
- Bahasa Indonesia (Native)
- Bahasa Inggris (Basic)
- Problem Solving & Analytical Thinking
- Team Collaboration

---

## 🔄 Data Science Workflow Expertise


---

## 🎯 Key Competencies

### **Data Analysis**
- ✅ Exploratory Data Analysis (EDA)
- ✅ Descriptive & Inferential Statistics
- ✅ Data Validation & Quality Assurance
- ✅ Trend Analysis & Pattern Recognition

### **Machine Learning**
- ✅ Supervised Learning Models
- ✅ Unsupervised Learning Models
- ✅ Model Performance Optimization
- ✅ Predictive Analytics

### **Business Intelligence**
- ✅ Dashboard Development
- ✅ KPI Monitoring
- ✅ Business Metrics Analysis
- ✅ Data-Driven Recommendations

### **Data Engineering (Basic)**
- ✅ ETL Processes
- ✅ Data Integration
- ✅ SQL Query Optimization
- ✅ Data Pipeline Automation

## 📊 Featured Projects

### **1. Flight Delay Analysis Dashboard**
**Technologies:** BigQuery SQL | Google Looker Studio | Data Analytics

**Project Overview:**
Comprehensive analysis of airline flight delay patterns using advanced SQL queries and interactive dashboard visualization.

**SQL Analysis Performed:**
- Data cleaning & validation with NULL checks and filtering
- Average delay calculation by airline (GROUP BY, AVG, WHERE)
- Time-of-day delay analysis using EXTRACT(HOUR) & CASE WHEN
- Airport performance comparison (origin-based analysis)
- Cancellation rate analysis by airline (SUM, COUNT aggregation)
- Dashboard summary combining multiple metrics

**Key Metrics Analyzed:**
- Total Airlines: 109
- On-Time Performance: 119 flights
- Average Delay: 3,045 minutes
- Cancellation Rate: 11 flights
- Delay Categories: Small (1-30m), Medium (31-60m), Major (>60m)

**Sample SQL Queries:**
```sql
-- Average Delay by Airline
SELECT airline, ROUND(AVG(departure_delay), 2) AS avg_delay
FROM `Data_Flight.data_flight`
WHERE cancelled = 0
GROUP BY airline
ORDER BY avg_delay DESC;

-- Delay by Time of Day
SELECT 
  CASE
    WHEN EXTRACT(HOUR FROM scheduled_departure) BETWEEN 5 AND 11 THEN 'Morning'
    WHEN EXTRACT(HOUR FROM scheduled_departure) BETWEEN 12 AND 17 THEN 'Afternoon'
    ELSE 'Evening'
  END AS time_of_day,
  ROUND(AVG(departure_delay), 2) AS avg_delay
FROM `Data_Flight.data_flight`
WHERE cancelled = 0
GROUP BY time_of_day
ORDER BY avg_delay DESC;

-- Cancellation Rate Summary
SELECT 
  airline,
  COUNT(*) AS total_flights,
  SUM(cancelled) AS total_cancelled,
  ROUND(SUM(cancelled) * 100.0 / COUNT(*), 2) AS cancel_rate_percent
FROM `Data_Flight.data_flight`
GROUP BY airline
ORDER BY cancel_rate_percent DESC;

┌─────────────────────────────────────────────────────┐
│  DATA COLLECTION                                    │
│  (BigQuery Datasets, SQL Databases)                 │
└────────────────┬────────────────────────────────────┘
                 ▼
┌─────────────────────────────────────────────────────┐
│  DATA CLEANING & VALIDATION                         │
│  (NULL checks, Data type validation, Filtering)     │
└────────────────┬────────────────────────────────────┘
                 ▼
┌─────────────────────────────────────────────────────┐
│  EXPLORATORY DATA ANALYSIS (EDA)                    │
│  (Aggregation, Grouping, Statistical Analysis)     │
└────────────────┬────────────────────────────────────┘
                 ▼
┌─────────────────────────────────────────────────────┐
│  DATA TRANSFORMATION & FEATURE ENGINEERING          │
│  (CASE WHEN, EXTRACT, Window Functions)            │
└────────────────┬────────────────────────────────────┘
                 ▼
┌─────────────────────────────────────────────────────┐
│  VISUALIZATION & DASHBOARD DEVELOPMENT              │
│  (Looker Studio, Interactive Charts & KPIs)        │
└────────────────┬────────────────────────────────────┘
                 ▼
┌─────────────────────────────────────────────────────┐
│  INSIGHTS & RECOMMENDATIONS                         │
│  (Business Intelligence, Data-Driven Decisions)    │
└─────────────────────────────────────────────────────┘

---

## 👥 Pengalaman Organisasi

### 🏛️ Kepemimpinan & Organisasi
- **Anggota Pustaka Insani Institute (PII)** - 2025-2026
- **Wasekum Teknologi & Kreatif Digital** - HMI Komisariat Cakrawala UICI (2025-2026)
- **Ikatan Pelajar Mahasiswa Halmahera Timur (IPM-HT)** - 2022-2026
  - Anggota Bidang Pendidikan & Pengkaderan (2022-2023)
  - Ketua Panitia MUBES (22 Juli 2022 & 23-24 Agustus 2024)
  - Sekretaris Panitia SPO (24-26 Feb 2023 & 13-15 Feb 2022)
  - Koordinator Seksi HUMAS (02 November 2024)

### 🌍 Community & Environmental Impact
- **Delegasi Garuda Nusa Youth Action (GNYA#3)** - Jan 2022
  - Pengabdian ke Desa Adat Tenganan, Bali
  - Program: Recycling, Hydroponics, Eco-Enzyme, Education

- **Team Core World Cleanup Day (WCD)** - 18 September 2021
  - Koordinator WCD Kabupaten Halmahera Timur
  - Sosialisasi Lingkungan di Sekolah & Instansi Pemerintah

- **Founder Komunitas SODARA** - 11 Oktober 2020
  - Solidaritas Sadar Sampah Halmahera

---

## 📊 GitHub Statistics

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=harisariefkamis&show_icons=true&theme=radical&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=harisariefkamis&layout=compact&theme=radical)

</div>

---

## 🎓 Continuous Learning

Saat ini sedang fokus belajar:
- 🔄 Advanced Machine Learning Techniques
- 📈 Time Series Forecasting
- 🌐 Deep Learning & Neural Networks
- 🔧 Cloud Computing (Google Cloud, AWS)
- 📱 Data Engineering & Big Data
- 🤖 AI & Large Language Models

---

## 🚀 Current Focus

---

## 📬 Let's Connect!

<div align="center">

| Platform | Link |
|----------|------|
| 📧 **Email** | [harisariefkamis16@gmail.com](mailto:harisariefkamis16@gmail.com) |
| 💼 **LinkedIn** | [harisariefkamis](https://www.linkedin.com/in/harisariefkamis) |
| 💻 **GitHub** | [@harisariefkamis](https://github.com/harisariefkamis) |
| 📱 **WhatsApp** | +6285282436796 |

</div>

---

## 💡 Open To

- 🤝 Freelance Data Analysis Projects
- 📊 Machine Learning Collaborations
- 💼 Full-time Data Scientist/Analyst Roles
- 🎓 Knowledge Sharing & Mentoring
- 🔬 Research & Innovation Projects

---

<div align="center">

### ⭐ If you find my profile interesting, feel free to star my repositories and connect!

**Made with ❤️ by Haris Arief Kamis**

Last Updated: May 2026

</div>

