# 🏨 Hotel Booking Data Analysis

## 📌 Project Overview
This project explores and analyzes a **Hotel Booking dataset**.  
The aim is to clean, preprocess, and visualize the data to extract meaningful insights about booking patterns, customer behavior, and revenue-related metrics.

---

## 🛠️ Data Cleaning & Preprocessing
1. **Missing Values Handling**  
   - Replaced missing values in `company` and `agent` with 0.  
   - Filled missing `country` values with the most frequent country.  

2. **Column Renaming**  
   - Renamed columns for clarity and consistency (e.g., `arrival_date_clean`, `Arrival_Year`).  

3. **Data Type Conversion**  
   - Converted `reservation_status_date` and other date-related columns to `datetime`.  

4. **Feature Engineering**  
   - Created new column `total_nights = stays_in_weekend_nights + stays_in_week_nights`.  
   - Grouped countries into top 20 + "Other" (`country_grouped`).  

5. **Outlier Treatment**  
   - Detected outliers using IQR method.  
   - Capped `adr` (Average Daily Rate) at 1000 to handle extreme values.  

---

## 📊 Exploratory Data Analysis (EDA)
- **Univariate Analysis**  
  - Distribution plots for ADR, lead time, and total nights.  
  - Boxplots to visualize outliers.  

- **Bivariate/Multivariate Analysis**  
  - Scatter plots: `lead_time vs adr`, `total_nights vs adr`.  
  - Correlation heatmap for numerical variables.  
  - Pairplot to analyze relationships between features.  

- **Country Analysis**  
  - Aggregated bookings by top 20 countries.  
  - Visualized booking frequency and grouped "Other" countries.  

---

## 📈 Key Insights
- ADR distribution is skewed with several high outliers (capped at 1000).  
- Lead time shows a wide variance and includes extreme outliers.  
- Most bookings come from a few top countries, while others are grouped into "Other".  
- Feature engineering (`total_nights`, `country_grouped`) improved analysis granularity.  

---

## 📂 Technologies Used
- **Python** 🐍  
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn  

---

## 🚀 How to Run
```bash
# Clone the repository
git clone https://github.com/username/hotel-booking-analysis.git

# Install required packages
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook




