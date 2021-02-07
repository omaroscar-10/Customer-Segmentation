# **Customer-Segmentation**

Used clustering techniques to segment a company's customer pool and identify the best customers based on Recency, Frequency and Monetary Value (RFM). 


# **1. Introduction**

Understanding customers (their similarities and their differences) is one of the most fundamental and important steps in quantifying the customers’ relationship with a product and the company.

Customer segmentation is a useful marketing tool for businesses that can help them/be used to improve their product or service, marketing strategy, and profitability.

Therefore, this analysis will segment customers so that a company can target them efficiently.


# **2. Data**

The original dataset is called *Online Retail II UCI* and was downloaded from Kaggle website [Online Retail II UCI](https://www.kaggle.com/mashlyn/online-retail-ii-uci). 

The dataset contains all the transactions of an online retail store between 01-12-2009 and 09-12-2011.


# **3. Modelling**

**Data Cleaning:** eliminate any problems from the dataset which would prevent further analysis.

**Data Exploration:** apply statistics and visualization techniques to gain a better understanding of the dataset.

**Feature Engineering:** select or create new features from the existing ones.

### **Recency, Frequency, Monetary Value (RFM)**

Recency, frequency, monetary value is a marketing analysis tool used to identify a firm's best clients, based on the nature of their spending habits. The RFM model is based on three quantitative factors:

**1. Recency:** How recently a customer has made a purchase

**2. Frequency:** How often a customer makes a purchase

**3. Monetary Value:** How much money a customer spends on purchases

**Consequently, I will segment the customers based on RFM so that the company can target its customers efficiently.**

**Modelling:** apply several clustering techniques to group similar observations and select the best performing model.


# **4. Results**

**K-means**

* Silhouette score with n_clusters=2: 0.5088

**Mini-Batch K-means**

* Silhouette score with n_clusters=2: 0.5065

**Hierarchical Clustering**

* Silhouette score with n_clusters=2 and linkage=ward: 0.5052

* Silhouette score with n_clusters=2 and linkage=complete: 0.4695

* Silhouette score with n_clusters=2 and linkage=average: 0.4618

**DBSCAN**

* Silhouette score with eps=1 and min_samples=27: 0.3729

* Silhouette score with eps=0.6 and min_samples=1: 0.2356

* Silhouette score with eps=0.6 and min_samples=27: 0.2786

**GMM**

* Silhouette score with n_components=2 and covariance_type=full: 0.3510

* Silhouette score with n_components=2 and covariance_type=tied: 0.4765

* Silhouette score with n_components=2 and covariance_type= 0.4007

* Silhouette score with n_components=2 and covariance_type= **0.5223**

The silhouette score of the GMM solution with n_components=2 and covariance_type=spherical is by far the highest among the clustering techniques applied.

As a result, this model is the top performer since it segments customers based Recency, Frequency and Monetary Value (RFM) better than the other models.

GMM identified two classes or groups of customers based on RFM.

One of those groups represent customers who have recently purchased from the company, buy more often and spend more. **These customers are more likely to buy again; they are also likely to buy more often and spend more money.**


# **5. Discussion & Recomendations**

From a marketing perspective, companies need to understand the characteristics and preferences of their best customers because they should target their marketing efforts towards prospects who resemble their best costumers’ characteristics. But, before they can start to understand their best customers, they first need to identify them. Therefore, from this unsupervised learning analysis, interested parties will be able to segment a customer pool and identify the best customers.

Once they have identified their customers based on their purchasing behavior (RFM); they could start to analyze the characteristics and purchasing behavior of this group and try to understand what distinguishes them from typical customers. As a result, understanding their customers will help them become more precise in targeting actual and potential customers.

The next steps I would take to expand this analysis would be to predict which customers are more likely to make purchases again in the future. I would use the available consumer spending data to estimate future behavior. This approach can be used by businesses to improve their marketing plan and target potential customers. 


# **References**

1. https://www.kaggle.com/mashlyn/online-retail-ii-uci
2. https://www.investopedia.com/terms/r/rfm-recency-frequency-monetary-value.asp
3. https://www.investopedia.com/terms/b/behavioral-modeling.asp



