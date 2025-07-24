# Project_web_scraping-
# Real Estate Data Scraping and Analysis – Oman Property Market

## Objectives

The primary goal of this project is to collect, clean, and analyze real estate listings data from major Omani property portals to build a structured and enriched dataset. This dataset can then be used for exploratory analysis and predictive modeling (e.g., price estimation), supporting better market insights and decision-making.

---

## Websites Used

- **Dubizzle Oman**: A leading online marketplace for properties for sale across Oman.  
- **HilalPRP**: A prominent Omani real estate listing platform featuring residential properties for sale.

---

## Data Collection and Cleaning

### Data Collection

- For **Dubizzle Oman**, data was scraped using Selenium WebDriver to automate browser interaction, enabling retrieval of multiple pages of listings and dynamically loaded content. Key property details such as title, location, price, rooms, bathrooms, and size were extracted.
  
- For **HilalPRP**, data was collected through HTTP requests and HTML parsing with BeautifulSoup. This included main listing details and additional property metadata from individual detail pages, such as location and garage availability.

### Data Cleaning

- Duplicate records were removed to ensure dataset integrity.
- Missing and inconsistent values in key fields (e.g., price, area, rooms) were handled using appropriate imputation strategies or record removal where critical data was absent.
- Textual data in numeric fields was cleaned by extracting numeric values.
- Data types were standardized across features to enable consistent analysis.
- Erroneous and outlier data points were identified and addressed to improve dataset quality.

---

## Feature Engineering Strategy

- **Derived Metrics**: Created meaningful features such as price per square meter (`price_per_sqm`) and total room count (sum of bedrooms and bathrooms) to better capture property characteristics.
- **Categorical Encoding**: Applied one-hot encoding to categorical variables like location and garage availability to enable machine learning algorithms to utilize this information.
- **Missing Value Imputation**: Used median values grouped by relevant categories (e.g., median area by location or room count) to fill missing entries and reduce data loss.
- **Scaling**: Standardized numeric features using scaling techniques to improve model convergence and performance.

---

## Modeling Approach

- The cleaned and feature-engineered datasets were split into training and testing sets for model development and evaluation.
- Several regression algorithms were employed, including Linear Regression, Decision Tree Regressor, and Random Forest Regressor.
- Model performance was assessed using metrics such as Mean Squared Error (MSE) and R-squared (R²).
- The approach aimed to accurately predict property prices based on the engineered features, with potential applications for market valuation and investment decision support.
- Combining datasets from multiple sources enhanced the volume and diversity of training data, improving model robustness and generalization.

---

This project establishes a solid foundation for advanced real estate market analytics in Oman by integrating multi-source data scraping, thorough cleaning, insightful feature engineering, and practical modeling.

---
