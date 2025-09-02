# Student Mental Health Analysis

This project analyzes student mental health data using a Random Forest classifier. The goal is to identify key factors influencing student well-being and provide actionable insights through visualizations.

---

## Project Structure

```shell
StudentMentalHealth/
│
├── data/
│ ├── Stress_Dataset.csv
│ └── StressLevelDataset.csv
├── excel/
├── notebooks/
│ └── RandomForest_Analysis.ipynb
├── reports/
│ ├── Report_Analysis.docx
│ └── Report_Analysis.pdf
├── powerbi/
│ └── Dashboards_PowerBI (prints or PBIX files)
├── src/
└── README.md
```

---

## Datasets

- **Stress_Dataset.csv** – Survey data containing features like anxiety, depression, sleep quality, blood pressure, social support, bullying, academic performance, teacher-student relationships, etc.
- **StressLevelDataset.csv** – Contains target variable (`0=Low, 1=Medium, 2=High`) and feature importance metrics.

---

## Methodology

1. Data uploaded and preprocessed in Google Colab using `files.upload()`.  
2. Features standardized and target defined.  
3. Class balance checked to ensure fairness.  
4. Dataset split into training (75%) and testing (25%) sets using `train_test_split`.  
5. Random Forest classifier trained with default parameters.  
6. Model evaluated using:  
   - Accuracy  
   - Precision  
   - Recall  
   - F1-score  
   - Confusion Matrix  
7. Feature importance analyzed to identify the most influential factors.  
8. Visualizations created in Power BI for interactive insights.

---

## Results

- **Global Accuracy:** 87%  
- **Classes balanced:** ~33% each (Low, Medium, High)  
- **Most important features:** Blood Pressure, Sleep Quality, Safety, Depression, Teacher-Student Relationship, Social Support

### Metrics by Class

| Class | Precision | Recall | F1-Score | Count |
|-------|----------|--------|----------|-------|
| Low Risk (0) | 0.89 | 0.85 | 0.87 | 93 |
| Medium Risk (1) | 0.88 | 0.90 | 0.89 | 90 |
| High Risk (2) | 0.85 | 0.87 | 0.86 | 92 |

### Confusion Matrix

|           | Predicted 0 | Predicted 1 | Predicted 2 |
|-----------|-------------|-------------|-------------|
| Actual 0  | 79          | 6           | 8           |
| Actual 1  | 3           | 81          | 6           |
| Actual 2  | 7           | 5           | 80          |

---

## Power BI Dashboards

Visualizations include:  
- Distribution of target variable  
- Relationship between sleep quality, academic performance, and target  
- Impact of bullying and social support  
- Feature importance ranking  

*(Insert screenshots or PBIX files in `powerbi/` folder)*

---

## How to Reproduce

1. Open `notebooks/RandomForest_Analysis.ipynb` in Google Colab.  
2. Ensure `data/` folder contains the CSV files.  
3. Run all cells to reproduce the analysis and generate reports.  
4. Optional: Open Power BI dashboards for visual exploration.

---

## Author

- **Your Name**  
- LinkedIn: https://www.linkedin.com/in/jo%C3%A3o-vitor-lucini-613900234/
- GitHub: https://github.com/LUC1NI 

---

## License

This project is for educational purposes.  
