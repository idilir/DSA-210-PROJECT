
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

![Unknown-7](https://github.com/user-attachments/assets/66a267f2-097f-424e-a2ed-6d968709cd67)

**Insight**: Higher prices in the morning suggest demand for premium beverages early in the day.

### 2. Coffee vs Tea Preference Over Time of Day
![Unknown-8](https://github.com/user-attachments/assets/909507d8-23c0-471b-919a-340f4e653a36)

**Insight**: Morning dominates in both coffee and tea sales, especially coffee.

### 3. Rainfall Distribution
![Unknown-9](https://github.com/user-attachments/assets/06269ef9-9ec7-4fe9-b042-1c499539ef7b)

**Insight**: Most days are dry or have low rainfall, skewing distributions.

### 4. Coffee Categories on Rainy vs Dry Days
![Unknown-10](https://github.com/user-attachments/assets/a192dde6-1ded-45ae-a0a3-aa6fabb675ad)
 
**Insight**: Major categories remain dominant regardless of weather.

### 5. Correlation Heatmap
![Unknown-11](https://github.com/user-attachments/assets/c6cc531f-aa05-4200-96db-9ce62c144a1a)

**Insight**: Sales negatively correlate with temperature (-0.56), suggesting more sales in colder weather.

### 6. Coffee Sales by Location
![Unknown-4](https://github.com/user-attachments/assets/112d32d4-e5b0-44dd-9938-f3f4b5473e28)

**Insight**: Hell’s Kitchen and Astoria lead sales, pointing to strong local demand.

### 7. Weekly Coffee Sales Trend
![Unknown-13](https://github.com/user-attachments/assets/508176d9-d3da-4734-9fb4-2200d9bbe59a)

**Insight**: Clear peak around week 25, followed by drop-off—seasonal or promotional effect likely.

### 8. Coffee Sales vs Temperature (Detailed)
![Unknown-5](https://github.com/user-attachments/assets/efd2fa29-d277-4bc2-be7b-05a3127ef993)

**Insight**: Strong cluster of lower temperatures with diverse price ranges—supports colder=more demand.

### 9. Tea Sales on Rainy vs Dry Days
![Unknown-15](https://github.com/user-attachments/assets/14015bcf-99e3-4aad-b24f-849f49b1e364)
 
**Insight**: No strong change in tea pricing on rainy days.

### 10. Product Category vs Temperature
![Unknown](https://github.com/user-attachments/assets/fc81a652-6958-4747-9dc9-33a6957d3206)

**Insight**: "Cool" and "Cold" dominate coffee, tea, and bakery sales. Warm weather leads to drop.

### 11. Unit Price on Rainy vs Dry Days
![Unknown-2](https://github.com/user-attachments/assets/2740cc21-5ae9-4860-9e21-e3c4c68c1a06)

**Insight**: Rain has minimal effect on overall pricing.

### 12. Coffee vs Tea Preference by Rain
![Unknown-3](https://github.com/user-attachments/assets/ca8838c4-1700-401e-91f8-3d1b53ddfa67)

**Insight**: Both coffee and tea see higher sales on rainy days—possibly due to comfort-seeking.

### 15. Rainfall Effect by Product Category
![Unknown-6](https://github.com/user-attachments/assets/45cf3706-1956-4503-aa29-7dbea570fd28)

**Insight**: High rainfall doesn’t skew sales much—stable demand across weather.

---

## ✅ Conclusion
- ❄️ Cold weather clearly drives up coffee sales.
- ☔ Rain doesn't drastically affect pricing but nudges demand slightly.
- 📍 Location and time of day are strong predictors of sales volume.
- 📅 Weekly trends and weather together offer actionable insights for inventory planning.

---

