# ** Exploratory Data Analysis (EDA) **

This project performs an Exploratory Data Analysis (EDA) on a retail sales dataset containing customer transaction information. The dataset includes key fields such as transaction ID, date, customer demographics (age, gender), product category, quantity, price per unit, and total amount. The goal is to uncover patterns, trends, anomalies, and customer segments to derive actionable business insights using Python libraries like Pandas, Matplotlib, and Seaborn.

---

## **Step 1 – Data Loading and Initial Inspection**

**Key Actions:**

* Imported the dataset using Pandas.
* Used `.info()` to check data types and completeness.
* Used `.describe()` to view statistical summaries.
* Used `.isnull().sum()` to find missing values.
* Used `.value_counts()` to explore categorical data.

**Insights:**

* The dataset contains several thousand transactions with no missing critical fields in most columns.
* Age, Quantity, Price per Unit, and Total Amount are numeric and suitable for statistical analysis.
* Date column is stored as text and needs conversion for time-based analysis.
* Gender and Product Category are categorical variables useful for customer segmentation.

---

##  **Step 2 – Handling Missing Data**

**Key Actions:**

* Visualized missing data using `sns.heatmap()`.
* Used 'df.isnull().sum()' to check for missing values in the dataset.
* Decided to fill missing values where possible or ignore based on relevance.
* No missing values found.

**Insights:**

* All columns have 0 missing values, meaning the dataset is clean and reliable.
* No imputation or data cleaning is needed before further analysis.
* This makes it easier to proceed with statistical modeling and visualization, as the absence of missing data ensures consistency and accuracy.

---

##  **Step 3 – Distribution of Key Variables**

**Key Actions:**

* Plotted histograms for Age and Total Amount.
* Observed distribution patterns and skewness.

**Insights:**

* The majority of customers are aged between 25–40 years, indicating that this segment is the core audience.
* The distribution of Total Amount is highly right-skewed, suggesting the presence of bulk or high-value purchases.
* Log transformations can be applied to normalize skewed distributions for advanced modeling.

---

##  **Step 4 – Outlier Detection Using Boxplots**

**Key Actions:**

* Created boxplots to identify outliers in Total Amount grouped by Gender.
* Detected extreme values.

**Insights:**

* Several high-value transactions exist, likely due to corporate orders or seasonal spikes.
* Both male and female customers show outliers, implying that large purchases are spread across demographics.

---

##  **Step 5 – Frequency Analysis of Categorical Features**

**Key Actions:**

* Used `value_counts()` and countplots to analyze Gender and Product Category distributions.

**Insights:**

* Some product categories are overwhelmingly popular, while others are niche.
* Gender distribution is balanced, meaning marketing strategies should be tailored to both segments.

---

##  **Step 6 – Correlation Analysis**

**Key Actions:**

* Filtered numeric columns and calculated correlations using `.corr()`.
* Visualized relationships using `sns.heatmap()`.

**Insights:**

* Quantity and Total Amount show a strong positive correlation, confirming that larger orders naturally lead to higher revenue.
* Price per Unit has weaker correlation, indicating varied pricing structures across products.
* Other numeric features show little correlation, suggesting they might not directly influence each other.

---

##  **Step 7 – Grouping and Aggregation**

**Key Actions:**

* Grouped data by Product Category to find patterns in sales.
* Summed total amounts by category.

**Insights:**

* Electronics product categories consistently generate higher revenue, suggesting where inventory focus should be placed.

---

##  **Step 8 – Skewness & Transformations**

**Key Actions:**

* Measured skewness using `.skew()`.
* Applied `np.log1p()` transformation to reduce skewness.

**Insights:**

* Total Amount’s skewness value confirms data is not normally distributed.
* Applying logarithmic transformations smooths data for further analysis and modeling without losing critical patterns.

---

##  **Step 9 – Final Business Insights**

**Conclusion:**
✔ The dataset reveals that the majority of sales are driven by customers aged 25–40.
✔ High-value transactions, although rare, suggest opportunities for targeted premium offers.
✔ Product category segmentation shows clear favorites, helping optimize stock and marketing efforts.
✔ The correlation between Quantity and Total Amount confirms expected patterns and can be used to forecast future demand.
✔ Skewed data distribution was addressed with transformations, ensuring more accurate statistical analysis.

---
