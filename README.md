## 🧠 Customer Segmentation using RFMI and K-Means Clustering

### 📄 Overview

This project focuses on **customer segmentation** using the **RFMI (Recency–Frequency–Monetary–Interval)** model combined with **K-Means clustering**.
The main objective is to categorize customers based on purchasing patterns to help businesses design **targeted marketing strategies**, improve **customer retention**, and boost **sales performance**.

---

### 🧩 Table of Contents

1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Project Workflow](#project-workflow)
4. [RFMI Analysis](#rfmi-analysis)
5. [Clustering using K-Means](#clustering-using-k-means)
6. [Visualizations](#visualizations)
7. [Results](#results)
8. [Key Insights & Recommendations](#key-insights--recommendations)
9. [Tech Stack](#tech-stack)
10. [How to Run the Project](#how-to-run-the-project)
11. [Future Enhancements](#future-enhancements)
12. [Author](#author)

---

### 🧠 Introduction

Customer segmentation helps businesses identify customer groups with similar characteristics and behaviors.
In this project, customers are segmented using the **RFMI** model:

* **R (Recency):** How recently a customer made a purchase
* **F (Frequency):** How often the customer makes purchases
* **M (Monetary):** How much money the customer spends
* **I (Interval):** The average time gap between two purchases

Combining RFMI features with **K-Means Clustering** allows us to identify valuable customer groups for strategic marketing actions.

---

### 📊 Dataset Description
* **Dataset link:** https://drive.google.com/file/d/1YpIVltTaiWhksWBcjuWUOOozdv7I3b_0/view?usp=sharing
* **Source:** Online Retail dataset (UK-based non-store online retailer)
* **Duration:** 01/12/2010 – 09/12/2011
* **Attributes:**

  * `InvoiceNo` – Unique identifier for each transaction
  * `StockCode` – Product code
  * `Description` – Product name
  * `Quantity` – Units purchased
  * `InvoiceDate` – Transaction date
  * `UnitPrice` – Price per item
  * `CustomerID` – Unique customer identifier
  * `Country` – Customer’s country

---

### 🔄 Project Workflow

#### 1. Data Preprocessing

* Removed missing and duplicate values
* Filtered cancellations and negative quantities
* Converted date columns into datetime format
* Calculated total purchase value per invoice

#### 2. Exploratory Data Analysis (EDA)

* Identified sales trends and seasonal patterns
* Analyzed customer distribution across countries
* Visualized top-selling products and top customers

#### 3. RFMI Calculation

* **Recency:** Days since last purchase
* **Frequency:** Total number of transactions
* **Monetary:** Total amount spent
* **Interval:** Average gap between purchases

#### 4. Feature Scaling

* Standardized RFMI values using `StandardScaler` for clustering

#### 5. Clustering

* Applied **K-Means clustering**
* Determined optimal K using **Elbow method** and **Silhouette score**
* Clustered customers into meaningful groups

#### 6. Evaluation

* Visualized clusters in 2D and 3D plots
* Interpreted cluster characteristics

---

### 📈 RFMI Analysis

* **Recency:** Recent customers are more likely to purchase again
* **Frequency:** Frequent shoppers are loyal customers
* **Monetary:** High spenders contribute to majority of revenue
* **Interval:** Shorter intervals indicate consistent engagement

---

### 🌀 Clustering using K-Means

K-Means algorithm grouped customers into **N clusters** (based on Elbow & Silhouette scores).
Each cluster represents a unique customer segment such as:

* 🟢 **Loyal High Spenders**
* 🔵 **Frequent Moderate Buyers**
* 🟠 **Recent but Low-Value Customers**
* 🔴 **Inactive or Lost Customers**

---

### 📊 Visualizations

* Customer distribution by country
* Sales trend over time
* 3D scatter plot of K-Means clusters
* Heatmaps showing RFMI correlations

---

### 🧾 Results

* RFMI-based segmentation successfully identified distinct customer groups.
* Businesses can target each segment differently:

  * Offer loyalty rewards to high-value customers
  * Provide discounts to re-engage inactive users
  * Encourage frequent moderate buyers with personalized promotions

---

### 💡 Key Insights & Recommendations

* Retain **high-value loyal customers** through rewards and personalized campaigns.
* Re-engage **dormant customers** via email reminders or special offers.
* Identify **emerging customers** showing increasing frequency and monetary value.
* Reduce churn by monitoring customers with **long purchase intervals**.

---

### 🛠️ Tech Stack

* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:**

  * `pandas`, `numpy` – Data manipulation
  * `matplotlib`, `seaborn` – Visualization
  * `scikit-learn` – Clustering, scaling, evaluation
  * `datetime`, `mpl_toolkits` – Feature engineering & plotting

---

### ▶️ How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/Customer_Segmentation_RFMI.git
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:

   ```bash
   jupyter notebook "Customer_Segmentation_RPI_RFM_Final Interval.ipynb"
   ```
4. Run all cells sequentially to reproduce results.

---

### 🚀 Future Enhancements

* Integrate **hierarchical clustering** for comparison.
* Develop a **web dashboard (Flask/Streamlit)** for interactive segmentation visualization.
* Incorporate **time-based segmentation** and **predictive customer lifetime value (CLV)** modeling.
* Automate report generation for business decision-making.

---

### 👩‍💻 Author

**Developed by:** [Anusha Bikkina](https://github.com/AnushaBikkina)
**Project Type:** Machine Learning | Customer Analytics | Clustering

---


