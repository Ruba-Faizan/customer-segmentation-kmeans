# Customer Segmentation Using Unsupervised Learning

## Project Overview
Customer segmentation is an important technique used by businesses to understand customer behavior and improve marketing strategies. This project applies **unsupervised machine learning** techniques to group customers based on their **spending habits and annual income**.

Using the **Mall Customers Dataset**, the project implements **K-Means Clustering** to identify meaningful customer segments. To improve interpretability, dimensionality reduction techniques such as **Principal Component Analysis (PCA)** and **t-SNE** are used to visualize the clusters.

The insights obtained from this segmentation help businesses design **targeted marketing strategies** for different customer groups.

---

## Objectives

The main objectives of this project are:

- Perform **Exploratory Data Analysis (EDA)** to understand customer behavior.
- Apply **K-Means Clustering** to segment customers.
- Visualize clusters using **PCA and t-SNE**.
- Analyze cluster characteristics.
- Suggest **marketing strategies** for each customer segment.

---

## Dataset

Dataset used: **Mall Customers Dataset**

The dataset contains demographic and behavioral information about customers visiting a shopping mall.

### Dataset Features

| Feature | Description |
|-------|-------------|
| CustomerID | Unique identifier for each customer |
| Gender | Male or Female |
| Age | Age of the customer |
| Annual Income (k$) | Customer's yearly income |
| Spending Score (1–100) | Score assigned by the mall based on customer spending behavior |

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook  

---

## Project Workflow

### 1. Data Loading
The dataset is loaded using **Pandas** and inspected to understand its structure and data types.

### 2. Exploratory Data Analysis (EDA)
EDA is performed to explore patterns in customer behavior.

Key analyses include:

- Age distribution
- Income distribution
- Relationship between annual income and spending score
- Gender-based spending patterns

These visualizations help understand how customers behave in the mall environment.

---

### 3. Data Preprocessing

Before applying clustering algorithms:

- Relevant features are selected.
- Data is normalized using **StandardScaler**.
- Feature matrix is prepared for clustering.

Feature scaling ensures that each variable contributes equally to the clustering process.

---

### 4. K-Means Clustering

K-Means is an **unsupervised learning algorithm** used to group similar data points together.

Steps performed:

1. Determine optimal number of clusters using the **Elbow Method**.
2. Train the **K-Means model**.
3. Assign cluster labels to each customer.
4. Analyze characteristics of each cluster.

The model identifies **five distinct customer segments**.

---

## Cluster Visualization

### PCA Visualization

Principal Component Analysis (PCA) reduces the dataset into two dimensions for easier visualization.

```python
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

plt.figure(figsize=(8,6))
sns.scatterplot(x=X_pca[:,0], y=X_pca[:,1], hue=df['Cluster'], palette='Set2', s=100)
plt.title("Clusters visualized with PCA")
plt.xlabel("PCA 1")
plt.ylabel("PCA 2")
plt.legend(title="Cluster")
plt.show()


## t-SNE Visualization

t-SNE is another dimensionality reduction technique that helps visualize complex data relationships.

tsne = TSNE(n_components=2, random_state=42)
X_tsne = tsne.fit_transform(X_scaled)

plt.figure(figsize=(8,6))
sns.scatterplot(x=X_tsne[:,0], y=X_tsne[:,1], hue=df['Cluster'], palette='Set2', s=100)
plt.title("Clusters visualized with t-SNE")
plt.xlabel("t-SNE 1")
plt.ylabel("t-SNE 2")
plt.legend(title="Cluster")
plt.show()
```

---

# Customer Segments and Marketing Strategies

## Cluster 0 – Low Income, Low Spending
Customers with limited purchasing power.

### Marketing Strategy
- Discount offers  
- Loyalty programs  
- Budget-friendly promotions  

---

## Cluster 1 – High Income, High Spending
These customers are the most valuable for the business.

### Marketing Strategy
- Premium products  
- Exclusive memberships  
- Personalized services  

---

## Cluster 2 – Average Income, High Spending
Customers who actively spend despite moderate income.

### Marketing Strategy
- Upselling premium products  
- Cross-selling related items  
- Reward programs  

---

## Cluster 3 – Low Income, High Spending
Customers with lower income but high spending behavior.

### Marketing Strategy
- Bundle offers  
- Budget deals  
- Installment payment options  

---

## Cluster 4 – High Income, Low Spending
Customers with strong purchasing power but low engagement.

### Marketing Strategy
- Personalized promotions  
- Brand awareness campaigns  
- Premium product trials  

---

# Results

The clustering model successfully segmented customers into **five distinct groups** based on their **spending behavior and income**.

Visualization using **PCA and t-SNE** clearly shows the separation between clusters, making it easier to understand customer patterns.

These insights can help businesses design **data-driven marketing strategies**.

---

# Conclusion

Customer segmentation using **unsupervised machine learning** provides valuable insights into customer behavior. By identifying different customer groups, businesses can create targeted marketing campaigns, improve customer satisfaction, and increase revenue.

### Future Improvements
- Using larger datasets  
- Applying advanced clustering techniques  
- Incorporating additional behavioral features  

---

# Author

**Ruba Faizan**  
Data Science Student
