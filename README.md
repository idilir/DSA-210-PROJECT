
# DSA-210-PROJECT
## Coffee Preference, Sales, and Weather Analysis

**Title**: Analyzing the Impact of Weather on Coffee Sales

---

## 🧭 Motivation
Coffee shops often experience fluctuating sales due to weather conditions. This project explores how **temperature** and **rainfall** influence daily coffee sales at a café. The goal is to help small businesses optimize inventory and staffing based on weather forecasts.

---

## 📊 Data Sources
1. **Weather Data**
   - **Source**: https://www.ncei.noaa.gov/access/past-weather/
   - **Variables**: Daily temperature (°C), rainfall (mm), and date for New York City (Jan–Mar 2023).

2. **Coffee Sales Data**
   - **Source**: [Kaggle Coffee Sales Dataset](https://www.kaggle.com/datasets/ahmedabbas757/coffee-sales)
   - **Variables**: Daily sales ($), number of customers, date, location, coffee/tea preference.
   - **Enrichment**: Merged with weather data to analyze correlations.

---

## 🎯 Objectives
- Analyze correlations between weather (temperature, rainfall) and coffee sales.
- Identify patterns in coffee vs. tea preferences based on weather.
- Assess location-specific sales trends and time-of-day purchasing habits.
- Develop predictive insights for inventory and staffing optimization.

---

## 🔬 Hypotheses
### Temperature vs. Coffee Sales
- H₀: Temperature has no effect on coffee sales.
- H₁: Temperature significantly affects coffee sales.

### Rainfall vs. Coffee Sales
- H₀: Rainfall has no effect on coffee preference.
- H₁: Rainfall significantly affects coffee preference.

### Temperature-Rainfall Interaction
- H₀: No interaction between temperature and rainfall.
- H₁: A significant interaction exists.

### Location-Based Preferences
- H₀: No variation in preference by location.
- H₁: Preference varies significantly by location.

### Time-of-Day Influence
- H₀: Time of day has no impact.
- H₁: Time of day significantly influences sales/preference.

---

## 📈 Visual Insights and Commentary

### 1. Average Unit Price by Time of Day
![avg_price_time](avg_price_time.png)  
**Insight**: Higher prices in the morning suggest demand for premium beverages early in the day.

### 2. Coffee vs Tea Preference Over Time of Day
![coffee_tea_time](coffee_tea_time.png)  
**Insight**: Morning dominates in both coffee and tea sales, especially coffee.

### 3. Rainfall Distribution
![rain_dist](rain_dist.png)  
**Insight**: Most days are dry or have low rainfall, skewing distributions.

### 4. Coffee Categories on Rainy vs Dry Days
![coffee_cat_rain](coffee_cat_rain.png)  
**Insight**: Major categories remain dominant regardless of weather.

### 5. Correlation Heatmap
![corr_heatmap](corr_heatmap.png)  
**Insight**: Sales negatively correlate with temperature (-0.56), suggesting more sales in colder weather.

### 6. Coffee Sales by Location
![coffee_location](coffee_location.png)  
**Insight**: Hell’s Kitchen and Astoria lead sales, pointing to strong local demand.

### 7. Weekly Coffee Sales Trend
![weekly_trend](weekly_trend.png)  
**Insight**: Clear peak around week 25, followed by drop-off—seasonal or promotional effect likely.

### 8. Coffee Sales vs Temperature (Detailed)
![coffee_temp_detail](coffee_temp_detail.png)  
**Insight**: Strong cluster of lower temperatures with diverse price ranges—supports colder=more demand.

### 9. Tea Sales on Rainy vs Dry Days
![tea_rain](tea_rain.png)  
**Insight**: No strong change in tea pricing on rainy days.

### 10. Product Category vs Temperature
![cat_temp](cat_temp.png)  
**Insight**: "Cool" and "Cold" dominate coffee, tea, and bakery sales. Warm weather leads to drop.

### 11. Unit Price on Rainy vs Dry Days
![unit_rain_price](unit_rain_price.png)  
**Insight**: Rain has minimal effect on overall pricing.

### 12. Coffee vs Tea Preference by Rain
![rain_coffee_tea](rain_coffee_tea.png)  
**Insight**: Both coffee and tea see higher sales on rainy days—possibly due to comfort-seeking.

### 13. Store Location Sales Count
![location_sales](location_sales.png)  
**Insight**: Visual reconfirmation of Hell’s Kitchen and Astoria dominance.

### 14. Product Category Sales vs Temperature
![sales_temp_cat](sales_temp_cat.png)  
**Insight**: Cold and cool temperatures drive the majority of category sales.

### 15. Rainfall Effect by Product Category
![rain_mm_cat](rain_mm_cat.png)  
**Insight**: High rainfall doesn’t skew sales much—stable demand across weather.

---

## ✅ Conclusion
- ❄️ Cold weather clearly drives up coffee sales.
- ☔ Rain doesn't drastically affect pricing but nudges demand slightly.
- 📍 Location and time of day are strong predictors of sales volume.
- 📅 Weekly trends and weather together offer actionable insights for inventory planning.

---

