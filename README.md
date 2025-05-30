
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

## 🧪 Data Enrichment  
To understand the impact of environmental conditions on beverage sales, both datasets were **merged** based on the `date` field. Additional engineered features were created for deeper analysis:

- `avg_temp_c`: Daily average temperature (from weather data)  
- `rain_mm`: Daily total rainfall  
- `hour`: Extracted from transaction timestamps to analyze time-of-day effects  
- `day_of_week`, `month`: Temporal features derived from date  
- `transaction_qty`: Total number of items purchased per transaction  
- `unit_price`: Derived by dividing sales amount by quantity  
- `is_rainy`: Boolean feature indicating whether rainfall occurred  
- `beverage_type`: Binary label for machine learning (1 = Coffee, 0 = Tea)

This enrichment enabled correlation analysis, feature selection, and predictive modeling.

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

### Time-of-Day Influence
- H₀: Time of day has no impact.
- H₁: Time of day significantly influences sales/preference.
  
  ### Temperature-Beverage Preference
- H₀: No interaction between temperature and rainfall.
- H₁: A significant interaction exists.


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
---

## 🤖 Machine Learning: Predicting Unit Price

| Model             | R² Score | RMSE  | MAE   | CV R² Mean |
|------------------|----------|-------|-------|-------------|
| Linear Regression | 0.03     | 0.972 | 0.632 | —           |
| Random Forest     | 0.70     | 0.545 | 0.419 | 0.70        |
<img width="841" alt="Screenshot 2025-05-30 at 10 06 06" src="https://github.com/user-attachments/assets/0993bb9e-9c19-49a0-a148-61ebb7e3b555" />
<img width="841" alt="Screenshot 2025-05-30 at 10 06 14" src="https://github.com/user-attachments/assets/4ec2f476-2572-45b3-8ea9-5574db27c895" />


**Takeaways**:
- Random Forest performed significantly better  
- Weather and timing explain ~70% of price variance  
- More features (e.g., marketing, inventory) may improve accuracy

---

## 🤖 Machine Learning: Coffee vs Tea Classification

**Model**: Random Forest Classifier  
**Target**: Classify purchases as Coffee (1) or Tea (0)  

| Metric     | Tea (0) | Coffee (1) |
|------------|---------|------------|
| Precision  | 0.44    | 0.56       |
| Recall     | 0.19    | 0.81       |
| F1-Score   | 0.27    | 0.66       |

**Accuracy**: 54%
<img width="619" alt="Screenshot 2025-05-30 at 10 21 11" src="https://github.com/user-attachments/assets/9c416f45-bb13-4fa7-b7bb-5a29682b139b" />
<img width="987" alt="Screenshot 2025-05-30 at 10 21 31" src="https://github.com/user-attachments/assets/e5ec4755-796e-4035-ac7b-39704e5f418d" />

**Insights**:
- Coffee is detected with high recall  
- Model overpredicts coffee  
- Class imbalance affects performance  
- Consider SMOTE or class weighting  

**Top Features**:
1. `hour` – time of transaction  
2. `total_sales` – total amount spent  
3. `avg_temp_c` – temperature  
4. `transaction_qty` – item count  
5. `unit_price` – price per unit  
6. `rain_mm` – rainfall  
7. `month`, `day_of_week` – seasonal effects  

---

## 📌 Conclusion

This project analyzed how weather (temperature and rainfall) and time of day affect beverage sales. Key insights include:

- Cold mornings increase coffee sales  
- Tea consumption slightly rises on rainy afternoons  
- Time of day is a stronger predictor than weather  
- Weather does influence demand but not pricing significantly  
- Regression models struggle to predict unit price from weather  
- Classification models perform moderately well with class imbalance

**Business Implications**:
- Adjust inventory and staff for busy morning shifts  
- Use weather forecasts for minor demand shifts  
- For precise forecasting, integrate customer behavior and marketing data

---
