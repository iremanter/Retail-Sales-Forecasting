# Retail-Sales-Forecasting

At the beginning of this analysis, information, types and descriptions of all attributes of this dataset have been examined by using necessary Python functions. Secondly, missing values of the sales dataset have been detected and the total count of missing values for each attribute has been checked. It was revealed that ‘ADDRESSLINE2’, ‘STATE’, and ‘TERRITORY’ attributes have missing values. These three attributes have no significant effect on sales amount so, instead of eliminating the whole records, these null values have been filled by writing ‘Unknown’, which is one of the appropriate methods to handle the missing values. Additionally, date format revision was required to make the type of all attributes in the dataset numerical for linear regression models.
After overall analysis of the dataset, it appeared that there are many categorical attributes in this dataset.

To analyze the correlation between independent variables and the target variable and then in order to develop a linear regression model, the attributes of the dataset must consist of only numerical values. Therefore, the elimination of the categorical values have been performed in the exploratory data analysis part, which is the next step after the data preprocessing part.

**Exploratory Data Analysis (EDA):**

After the annual bar chart of sales amount has been plotted, it was obtained that the maximum sales occurred in 2004, while the minimum sales occurred in 2005.

According to the bar chart of ‘Sales by Country’, it is shown that most of the sales occurred in the USA, while the lowest sales were recorded in Ireland.

To investigate the distribution of sales amount in each order, a histogram was plotted. Interpreting this histogram, it shows that smaller sales amounts occur more frequently than larger sales amounts.

Categorical variables related to date, status, address, and some demographic information have been eliminated in order to create a correlation matrix. After performing the correlation matrix, the correlations between the target variable, which is “Sales”, and other attributes have been examined more specifically.

The correlation matrix has been created. It can be interpreted such that if the correlations between attributes are more than 0.5, these variables have a significant effect on the target variable. To clearly see this correlation, the correlation between the target variable (Sales Amount) and other attributes has been examined. It appears that the 'Quantity Ordered' and 'Price Each' attributes have the most significant effect on the sales amount. Therefore, scatter plot of these two attributes have been created to provide a better understanding.

The scatter plot shows the relationship between 'Quantity Ordered' and 'Price Each' using five different colors to represent 'Sales.' As the points get darker, the amount of sales increases. There is no linear relationship between 'Quantity Ordered' and 'Price Each.' The points are most dense where 'Price Each' ranges from 90-100 and 'Quantity Ordered' ranges from 20-40. This interception area indicates that the highest sales occur under these conditions.

‘Quantity Ordered’ and ‘Price Each’ attributes are plotted separately and these graphs show that there is a linear relationship between each attribute and sales amount.

**Model Development:**

Before developing a linear regression model, min-max scaling was performed to normalize the data. Min-max scaling, which improves the performance of the linear regression model, converts attributes into one specific scale. After that, the dataset was split into training and testing sets, with 80% of the data used for training and 20% for testing.

**Model Evaluation:**
To perform a model evaluation Mean Squared Error (MSE), R2 Score, and Mean Absolute Error (MAE) methods have been used. 
The interpretation of these performance metrics as follows:

- Mean Squared Error (MSE): 0.0039, indicating small average prediction errors.
- R2 Score: 0.75, suggesting that 75.2% of sales variance is explained by the model.
- Mean Absolute Error (MAE): 0.048, indicating small average deviation from actual sales.

A significant portion of sales variability has been captured by the Linear Regression model, but further improvements in data quality, feature selection, and model complexity could increase the accuracy.
In conclusion, while the Linear Regression model provides a reasonable estimate of sales, achieving an R2 score of 0.75, there are opportunities to improve its predictive performance, accuracy and reliability.




