# E-commerce Customer Behavior Analysis

## Overview
The rapid growth of e-commerce has led to an increased focus on understanding customer behavior to enhance satisfaction and retention. This project analyzes a dataset containing information about customer demographics, purchasing patterns, and satisfaction levels in an e-commerce platform. The primary objective is to address the business question: **"What factors influence customer satisfaction levels?"**

This analysis uses statistical methods and machine learning techniques to uncover key drivers of customer satisfaction and provide actionable recommendations for improving customer experiences.

---

## Dataset
The dataset used for this analysis is titled **"E-commerce Customer Behavior"** and contains **450 rows (customers)** and **11 columns (features)**. It includes the following attributes:

| Column Name            | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Customer ID            | Unique identifier for each customer.                                        |
| Gender                 | Gender of the customer (Male/Female).                                       |
| Age                    | Age of the customer.                                                        |
| City                   | City where the customer resides (e.g., New York, Los Angeles, Chicago, etc.).|
| Membership Type        | Type of membership (Gold, Silver, Bronze).                                  |
| Total Spend            | Total amount spent by the customer.                                         |
| Items Purchased        | Number of items purchased.                                                  |
| Average Rating         | Average rating given by the customer for their purchases.                   |
| Discount Applied       | Whether a discount was applied to their purchase (TRUE/FALSE).              |
| Days Since Last Purchase | Number of days since the customer’s last purchase.                        |
| Satisfaction Level     | Customer satisfaction level (Satisfied, Neutral, Unsatisfied).              |

This dataset provides valuable insights into consumer behavior and helps businesses make data-driven decisions.

---

## Methodology
The data analysis process followed in this project consists of several key steps:

### 1. Data Preprocessing
- Missing values in the **Satisfaction Level** column were filled with the default value "Neutral."
- Categorical variables such as **Gender**, **Discount Applied**, **Membership Type**, and **City** were encoded into numerical formats using label encoding and one-hot encoding.
- Irrelevant columns like **Customer ID** were removed to streamline the analysis.

### 2. Exploratory Data Analysis (EDA)
- Summary statistics (mean, median, standard deviation, etc.) were calculated for numerical variables.
- Visualizations such as count plots, box plots, and correlation heatmaps were created to explore relationships between variables.
- Key findings include:
  - Trends in customer spending across different cities and membership types.
  - Distribution of satisfaction levels (Satisfied, Neutral, Unsatisfied) across demographic groups.
  - Correlations between features such as **Total Spend** and **Satisfaction Level**.

### 3. Statistical Methods
- A **Random Forest Classifier** was trained to predict customer satisfaction levels using features such as **Total Spend**, **Age**, **Average Rating**, and others.
- The dataset was split into training (80%) and testing (20%) sets to evaluate model performance.
- Feature importance analysis was conducted to identify the most influential factors affecting satisfaction levels.

### 4. Visualization Tools
Visualizations were created using Python libraries such as **Matplotlib** and **Seaborn**. These tools enabled the creation of clear and informative charts, including bar graphs, heatmaps, and box plots.

---

## Results
Key findings from the analysis are summarized below:

### 1. Customer Satisfaction Distribution
Figure 1(a) shows the distribution of customer satisfaction levels across the three categories:
- Approximately **120 customers** are classified as **Satisfied**.
- Around **110 customers** are classified as **Neutral**.
- Roughly **115 customers** are classified as **Unsatisfied**.

This balanced distribution ensures that the analysis is not skewed toward any particular category.

### 2. Correlation Heatmap
Figure 1(b) presents a correlation heatmap that reveals relationships between different variables:
- A strong positive correlation (~0.97) between **Total Spend** and **Items Purchased**, indicating that customers who spend more tend to purchase more items.
- A high positive correlation (~0.94) between **Average Rating** and **Satisfaction Level**, confirming that higher ratings lead to greater satisfaction.
- A moderate negative correlation (~-0.42) between **Discount Applied** and **Days Since Last Purchase**, suggesting that discounts may delay repeat purchases.

### 3. Total Spend vs Satisfaction Level
Figure 1(c) illustrates the relationship between total spending and customer satisfaction levels:
- **Satisfied customers** tend to spend significantly more, with median values around **$1,200** and a range extending up to **$1,500**.
- **Neutral customers** exhibit moderate spending, with median values around **$450**.
- **Unsatisfied customers** spend the least, with median values around **$600**.

This suggests that higher spending is strongly associated with higher satisfaction levels.

### 4. Feature Importance
Figure 1(d) highlights the most important features influencing customer satisfaction based on the Random Forest model:
- **Days Since Last Purchase**: Recent activity plays a crucial role in determining satisfaction.
- **Total Spend**: Higher spending is a significant predictor of satisfaction.
- **Items Purchased**: The number of items purchased also contributes to satisfaction.

---

## Results

### 1. Customer Satisfaction Distribution
Figure 1(a) shows the distribution of customer satisfaction levels:
![Figure 1(a): Distribution of Satisfaction Levels](Visualizations/Distribution%20of%20Satisfaction%20Levels.png)

### 2. Correlation Heatmap
Figure 1(b) presents a correlation heatmap:
![Figure 1(b): Correlation Heatmap](Visualizations/Correlation%20Heatmap.png)

### 3. Total Spend vs Satisfaction Level
Figure 1(c) illustrates the relationship between total spending and satisfaction levels:
![Figure 1(c): Boxplot - Total Spend vs Satisfaction Level](Visualizations/Total%20Spend%20vs%20Satisfaction%20Level.png)

### 4. Feature Importance
Figure 1(d) highlights the most important features influencing customer satisfaction:
![Figure 1(d): Feature Importance Bar Chart](Visualizations/Feature%20Importance%20Bar%20Chart.png)

---

## Key Takeaways
- **Higher spending leads to higher satisfaction**: Encouraging customers to spend more could improve satisfaction.
- **Recent purchases matter**: Keeping customers engaged with frequent purchases is important.
- **Ratings are crucial**: Improving product quality or service can boost satisfaction.
- **Discounts need careful planning**: While discounts attract customers, they may reduce purchase frequency.

By addressing these factors, businesses can improve customer experiences, drive repeat business, and ultimately boost overall performance.

---

## Repository Structure
The repository is organized as follows:
    ├── README.md # This file
    ├── Assignment_1.pdf # Assignment in PDF format
    ├── Final_Report.pdf # Final report in PDF format
    ├── E-commerce_Customer_Behavior.csv # Dataset used for analysis
    ├── BIS_Assignment.ipynb # Jupyter Notebook containing the analysis code
    ├── requirements.txt # List of Python dependencies
    └── Visualizations/ # Folder containing generated visualizations

---

## How to Run the Code
1. **Clone the repository**:
    ```bash
    git clone https://github.com/kushantha-sajith/BIS_Assignment.git
    cd BIS_Assignment

2. **Install Dependencies**:
    Ensure you have Python 3.11 installed, then install the required libraries:
    ```bash
    pip install -r requirements.txt

3. **Run the Jupyter Notebook**:
    Open the notebook and execute the cells to reproduce the analysis:
    ```bash
    jupyter notebook BIS_Assignment.ipynb

---

## View the Report

The final report is available in the [`Final_Report.pdf`](Final_Report.pdf) file.