# 🛍️ Customer Segmentation using K-Means Clustering

## 📌 Project Overview

This project focuses on **customer segmentation using the K-Means clustering algorithm**.

The goal is to group customers into meaningful segments based on their demographic information, income, spending behavior, membership duration, purchasing frequency, and preferred product categories.

Customer segmentation can help businesses better understand their customers and develop targeted marketing strategies, personalized offers, and improved customer experiences.

---

## 🎯 Objectives

* Analyze customer purchasing behavior.
* Identify meaningful groups of customers.
* Apply **K-Means Clustering** for unsupervised learning.
* Preprocess numerical and categorical features.
* Standardize numerical features before clustering.
* Visualize customer patterns and clusters.
* Understand different customer segments based on their characteristics.

---

## 📊 Dataset

The project uses a customer dataset containing **1,000 records and 9 columns**.

### Dataset Features

| Feature                | Description                                    |
| ---------------------- | ---------------------------------------------- |
| `id`                   | Unique customer identifier                     |
| `age`                  | Customer age                                   |
| `gender`               | Customer gender                                |
| `income`               | Customer income                                |
| `spending_score`       | Customer spending score                        |
| `membership_years`     | Number of years the customer has been a member |
| `purchase_frequency`   | Customer purchase frequency                    |
| `preferred_category`   | Customer's preferred product category          |
| `last_purchase_amount` | Amount spent on the customer's last purchase   |

The dataset contains both numerical and categorical variables. The notebook separates these columns during preprocessing.

---

## 🧠 Machine Learning Algorithm

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** used to divide data points into a predefined number of clusters.

The algorithm works by:

1. Selecting initial cluster centroids.
2. Assigning each data point to the nearest centroid.
3. Recalculating the centroid of each cluster.
4. Reassigning data points based on the updated centroids.
5. Repeating the process until the clusters converge.

The resulting clusters represent groups of customers with similar characteristics.

---

## 🔧 Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* K-Means Clustering
* StandardScaler
* LabelEncoder

The notebook imports `StandardScaler`, `KMeans`, and `LabelEncoder` from Scikit-learn and uses Pandas, Matplotlib, and Seaborn for data analysis and visualization.

---

## ⚙️ Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Inspection
   ↓
Identify Numerical & Categorical Columns
   ↓
Data Preprocessing
   ↓
Feature Scaling / Encoding
   ↓
K-Means Clustering
   ↓
Cluster Analysis
   ↓
Visualization
   ↓
Customer Segmentation
```

---

## 🔍 Data Exploration

The dataset is loaded using Pandas:

```python
df = pd.read_csv('data.csv')
```

The dataset contains:

```text
1000 rows × 9 columns
```

The data includes **6 integer columns, 1 floating-point column, and 2 categorical/object columns**.

The numerical and categorical columns are identified separately:

```python
numeric_cols = [
    cols for cols in columns
    if df[cols].dtype in ['int64', 'float64']
]

cat_cols = [
    cols for cols in columns
    if df[cols].dtype == 'object'
]
```

---

## 📈 Exploratory Data Analysis

The project analyzes customer characteristics and purchasing behavior through data exploration and visualization.

Important variables include:

* Age
* Income
* Spending Score
* Membership Years
* Purchase Frequency
* Preferred Category
* Last Purchase Amount

These variables provide useful information for identifying similarities and differences between customers.

---

## 🧹 Data Preprocessing

Before applying K-Means clustering, the dataset requires preprocessing because K-Means works with numerical feature representations.

The project identifies:

### Numerical Features

* `id`
* `age`
* `income`
* `spending_score`
* `membership_years`
* `purchase_frequency`
* `last_purchase_amount`

### Categorical Features

* `gender`
* `preferred_category`

Categorical variables can be encoded using techniques such as `LabelEncoder`, while numerical variables can be standardized using `StandardScaler`.

---

## 🤖 K-Means Clustering

K-Means clustering is used to divide customers into groups based on their similarity.

Each customer is assigned to a cluster according to the distance between the customer's feature values and the cluster centroid.

The resulting groups can be interpreted as different customer profiles.

For example, clusters may represent customers such as:

* High-income, high-spending customers
* Low-income, low-spending customers
* Frequent purchasers
* Occasional purchasers
* Long-term members
* Newer customers

> **Note:** The exact interpretation and number of clusters should be based on the final clustering results generated by the notebook.

---

## 📊 Results

The final clustering results can be used to understand customer behavior and identify distinct customer segments.

These segments can support business decisions such as:

* Targeted marketing campaigns
* Personalized recommendations
* Customer retention strategies
* Loyalty program planning
* Promotional offers
* Identifying high-value customers

---

## 📁 Project Structure

```text
Customer-Segmentation-KMeans/
│
├── kmeans.ipynb
├── data.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Customer-Segmentation-KMeans.git
```

### 2. Navigate to the Project Folder

```bash
cd Customer-Segmentation-KMeans
```

### 3. Install Required Libraries

```bash
pip install pandas matplotlib seaborn scikit-learn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
kmeans.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and clustering.

---

## 💡 Applications

Customer segmentation using K-Means can be applied in:

* 🛒 E-commerce
* 🏪 Retail
* 📢 Marketing
* 💳 Banking
* 📦 Subscription businesses
* 🎯 Personalized recommendation systems
* 📈 Customer relationship management

---

## 🔮 Future Improvements

The project can be further improved by:

* Determining the optimal number of clusters using the **Elbow Method**.
* Evaluating clustering quality using the **Silhouette Score**.
* Comparing K-Means with other clustering algorithms.
* Performing dimensionality reduction using PCA.
* Building an interactive customer segmentation dashboard.
* Creating customer profiles for each cluster.
* Adding automated cluster interpretation.
* Deploying the segmentation model as a web application.

---

## 📚 Key Learning Outcomes

Through this project, the following concepts were explored:

* Unsupervised Machine Learning
* K-Means Clustering
* Data Preprocessing
* Feature Scaling
* Categorical Encoding
* Exploratory Data Analysis
* Data Visualization
* Customer Segmentation
* Cluster Interpretation

---

## 👨‍💻 Author

**Your Name**

GitHub: `https://github.com/your-username`

---

## ⭐ Conclusion

This project demonstrates how **K-Means clustering** can be used to segment customers based on their characteristics and purchasing behavior.

By identifying groups of customers with similar patterns, businesses can gain useful insights into their customer base and make more informed marketing and business decisions.

---

## 🏁 Project Status

**Completed ✅**

This project was developed as a machine learning practice project to understand and implement **K-Means Clustering for customer segmentation**.

If you found this project useful, consider giving the repository a ⭐.
