### Airbnb Listings EDA Project: New York 2024  

---

## Project Overview
This project explores 20,000+ Airbnb listings in New York City (2024) using Python-based data analysis to uncover trends in pricing, availability, and guest behavior. By applying Exploratory Data Analysis (EDA), feature engineering, and visualization techniques, we provide data-driven insights for hosts, travelers, and investors to optimize Airbnb strategies.

![](https://github.com/najirh/Python-Project-P2-New-York-AirBnb-Listing-2024/blob/main/New-York-City-Brooklyn-Bridge-Panorama-Juergen-Roth-2.jpg)

---

## Key Objective
The goal of this project is to:
1. Analyze pricing trends across different boroughs.
2. Explore host behavior and listing availability.
3. Detect outliers and identify high-value investments.
4. Understand guest preferences through review and booking patterns.

---

## Technologies Used
1. Python (Pandas, NumPy) for large-scale data processing.
2. Matplotlib, Seaborn for visualizing trends and correlations.
3. Feature Engineering (Price per Bed, Availability Metrics).
4. Outlier Analysis to detect extreme pricing patterns.
5. Heatmaps & Geospatial Mapping for neighborhood insights.

## Dataset
The dataset used in this project is a [freely available dataset from Kaggle](https://www.kaggle.com/datasets/vrindakallu/new-york-dataset), making it accessible for analysis, research, and visualization without any restrictions.
The dataset contains **20,765 entries and 22 features**, including:
- **id**: Unique identifier for each listing  
- **name**: Title of the Airbnb listing  
- **host_name**: Name of the host  
- **neighborhood_group**: Group (borough) where the listing is located  
- **latitude/longitude**: Geolocation of listings  
- **price**: Nightly rental price  
- **room_type**: Type of accommodation (e.g., entire home, private room)  
- **reviews_per_month**: Average monthly reviews for the listing  
- **availability_365**: Number of available days in the year  

---

## Steps and Workflow

### 1. Data Cleaning
- **Handle missing data**: `price`, `neighborhood`, and `beds` columns had null values.
- **Fix data types**: Converted `last_review` to a **datetime** object.
- **Remove outliers**: Listings with prices > $1,000 were capped to avoid skewed visualizations.

### 2. EDA (Exploratory Data Analysis)
1. **Room type distribution**: 
   - Visualized the count of each room type using **bar plots**.
   - Identified **Entire home/apt** as the most common room type.

2. **Neighborhood group insights**:
   - Analyzed **price variations by boroughs**.
   - Manhattan had the **highest average prices**.

3. **Availability trends**:
   - Used **heatmaps** to show correlations among `price`, `availability_365`, `number_of_reviews`, and `beds`.

4. **Price distribution**:
   - Used **histograms** to show the distribution of prices.
   - Majority of the listings were priced between **$50 - $300**.

5. **Host listings**:
   - Analyzed hosts with multiple listings using **boxplots** to identify key contributors.

6. **Review behavior**:
   - Used **pair plots** to show relationships between number of reviews, price, and availability.

### 3. Data Visualization
- **Pairplot**: To see correlations among `price`, `availability`, and `number of reviews`.
- **Heatmap**: Showing correlations among numerical features.
- **Histograms and Boxplots**: To detect outliers in `price`.
- **Bar Charts**: Displaying room types and neighborhood group distributions.

---

## Key Findings and Insights
1. **Price Trends**:  
   - **Manhattan** has the most expensive listings, followed by Brooklyn.  
   - **Entire homes/apartments** cost significantly more than private or shared rooms.  

2. **Room Type Distribution**:  
   - **Entire homes/apartments** are the most common, but **private rooms** offer budget-friendly options.

3. **Outliers in Price**:  
   - Few listings priced at **$10,000+** were detected, indicating the need to filter such extreme values.

4. **Availability Patterns**:  
   - Listings with **high availability** tend to have lower prices and more reviews, likely due to better guest experience.

5. **Host Behavior**:  
   - Some hosts manage **multiple listings**, indicating a trend toward professional hosting.

---

## How to Run This Project
1. Clone the repository:
   ```bash
   git clone https://github.com/najirh/Python-Project-P2-New-York-AirBnb-Listing-2024.git
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Run the **Jupyter notebook** or **Python script**:
   ```bash
   jupyter notebook day23_airbnb_eda.ipynb
   ```

---

## Recommendations
- **For Guests**: 
   - Look for listings with high availability and good reviews for a better experience.
   - **Private rooms** in Brooklyn offer affordable stays compared to Manhattan.

- **For Hosts**:  
   - Improve **availability** and **review response rates** to attract more bookings.
   - Manage pricing effectively to compete within the borough's market.

- **For Investors**:
   - Assess the most profitable neighborhoods by comparing occupancy rates, average prices, and return on investment (ROI).
   - Analyze the demand for different property types (entire homes, private rooms, shared spaces) to make informed investment decisions.

---

## Conclusion
This project offers valuable insights into the New York Airbnb market, helping both guests and hosts make informed decisions. By using **EDA techniques**, we identified key trends and developed actionable recommendations. Future improvements can involve advanced analytics and predictive modeling to further enhance the findings.
