# Predicting Startup Acquisition and Success for Venture Capital Scoring 🚀

## 📊 Business Objective
The primary business objective is to provide **B2B investors and Venture Capitalists (VCs)** with a data-driven machine learning model to evaluate whether a startup is likely to **succeed, be acquired, or fail**. This helps optimize investment decisions and portfolio scoring.

---

## ⚙️ Machine Learning Task
* **Task Type:** Multi-class Classification.
* **Target Variable:** `Operating_Status` (Categorical: `Operating`, `Acquired`, `Closed`).

---

## 🗄️ Primary Dataset & Messiness Handling
* **Source:** Kaggle - [Startup Investments (Crunchbase)](https://www.kaggle.com/datasets/justinas/startup-investments)
* **Challenges & Preprocessing:**
  * **Massive Text Columns:** Processed using NLP techniques.
  * **Inconsistent Dates:** Cleaned and standardized funding dates.
  * **Parsing Funding Strings:** Extracted and parsed raw string formats (e.g., `'$50M'`) into numerical values for `Funding_Total_USD`.

---

## 🔌 API Integration Plan (Clearbit Company API)
* **API:** Clearbit Company API.
* **Implementation:** Query the API using the startup's website domain to fetch live, updated metadata such as:
  * Current exact employee count.
  * Tech stack utilized.
* **Data Cleaning:** Handled unmapped domains and standardized tech stack categories.

---

## 🕷️ Web Scraping Plan (Hiring Growth Rate)
* **Target Platforms:** LinkedIn Company Pages / Wellfound.
* **Implementation:** Scrape company profiles to extract the number of current **'Open Job Positions'**.
* **Feature Engineering:** Engineer a `Hiring_Growth_Rate` feature, as active mass hiring serves as a strong indicator of operational health and upcoming funding success.

---

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, BeautifulSoup / Selenium (Scraping), Requests (API), NLTK / SpaCy (NLP).