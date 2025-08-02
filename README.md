# 💼 Employee Sentiment Analysis 📊

This project performs sentiment analysis on internal employee communications to measure engagement, rank employees, and identify potential flight risks. It uses NLP techniques and linear regression to derive insights from email message data.

---

## 📁 Dataset

The dataset (`test.csv`) includes the following fields:
- `subject`: Subject of the email
- `body`: Email message body
- `date`: Date of the message
- `from`: Sender's email address

The dataset is unlabeled, so the first step involves automatic sentiment labeling using TextBlob.

---

## 🧠 Project Objectives

1. **Sentiment Labeling**: Automatically tag messages as **Positive**, **Negative**, or **Neutral** using TextBlob.
2. **EDA**: Analyze sentiment distribution and monthly trends using visualizations.
3. **Employee Scoring**: Assign sentiment scores (+1, 0, -1) and compute monthly sentiment score per employee.
4. **Ranking**: Identify top 3 most and least positive employees per month.
5. **Flight Risk Detection**: Flag employees who sent 4+ negative messages within any rolling 30-day window.
6. **Predictive Modeling**: Use linear regression to predict sentiment scores based on message features.

---

## 📊 Sample Visualizations

- Sentiment distribution bar chart
- Monthly sentiment trend (stacked bar)
- True vs predicted sentiment score scatterplot (color-coded)
- Top ranked positive and negative employees

---

## 🧪 Technologies Used

- **Python 3.x**
- **Pandas, NumPy** – Data handling
- **Matplotlib, Seaborn** – Visualizations
- **TextBlob** – Rule-based sentiment analysis
- **Scikit-learn** – Linear regression and model evaluation
- **Jupyter Notebook** – Interactive analysis and documentation

---

## 🧾 Key Files

| File | Description |
|------|-------------|
| `Employee_Sentiment_Analysis.ipynb` | Main notebook with full implementation |
| `top_positive_employees.csv` | Top 3 most positive employees per month |
| `top_negative_employees.csv` | Top 3 most negative employees per month |
| `flight_risks.csv` | List of employees at risk of attrition |
| `visualization/` | Folder containing generated plots |
| `README.md` | Project overview and usage |

---

## 🛠️ How to Run

1. Clone the repo or download the ZIP.
2. Install required packages:
    ```bash
    pip install pandas numpy matplotlib seaborn textblob scikit-learn
    python -m textblob.download_corpora
    ```
3. Run the notebook:
    ```bash
    jupyter notebook Employee_Sentiment_Analysis.ipynb
    ```
4. Explore outputs and generated `.csv` files.

---

## ✅ Results Summary

- **Top Positive Employees**: Based on cumulative monthly sentiment scores.
- **Top Negative Employees**: Based on lowest monthly sentiment scores.
- **Flight Risks**: Employees sending 4+ negative emails in any 30-day period.
- **Regression Model**:
  - 📉 MSE: 3.6416377693387716
  - 📊 R² Score: 0.4221135463491611

---

## 📌 Future Improvements

- Replace TextBlob with transformer-based models (e.g., BERT) for better sentiment accuracy.
- Build a dashboard for live monitoring.
- Include receiver metadata and thread replies for richer context.

---

## 🧑‍💻 Author

**Kartik Sharma**  
 [GitHub](https://github.com/kartik10sharma)

---

> ⚠️ **Disclaimer**: This dataset is for academic use only. Do not publish or distribute the emails or content externally.
