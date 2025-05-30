
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
Predicting Unit Price Using Machine Learning
Models & Results:
Model
R² Score
RMSE
MAE
CV R² Mean
Linear Regression
0.03
0.972
0.632
—
Random Forest
0.70
0.545
0.419
0.70

Visualization:
The scatter plot compares actual vs. predicted unit prices using the Random Forest model.
The red dashed line represents perfect predictions.
Most predictions fall close to the line, showing strong predictive power.
Takeaways:
Random Forest performed significantly better than Linear Regression.
The model achieved 70% of the variance explained (R² = 0.70), indicating a good fit.
This suggests unit price is partially predictable using features like product category, weather, and timing.
Further improvement may be possible by adding marketing or inventory features.









Machine Learning Results: Coffee vs Tea Prediction
 Model: Random Forest Classifier
Target: Classify transactions as Coffee (1) or Tea (0)
 Performance Metrics:
Metric
Tea (0)
Coffee (1)
Precision
0.44
0.56
Recall
0.19
0.81
F1-Score
0.27
0.66
Accuracy


0.54









The model correctly identifies Coffee purchases 81% of the time, but struggles with Tea (19% recall).
Overall accuracy is 54%, better than random guessing for unbalanced classes.
Precision for Coffee is higher, suggesting more confident classification in that category.
 Confusion Matrix Insight:
The model tends to overpredict Coffee, misclassifying many actual Tea purchases as Coffee.
Class imbalance may be affecting performance. Techniques like SMOTE or class weighting can improve this.
Top Features Influencing Prediction:
Rank
Feature
Description
1
hour
Time of transaction (strongest signal)
2
total_sales
Quantity × price per transaction
3
avg_temp_c
Temperature (°C)
4
transaction_qty
Number of items bought
5
unit_price
Price per item
6
rain_mm
Rainfall amount
7
month, day_of_week
Seasonality & weekday effects

Observation: Coffee is heavily consumed in the morning and during cooler days. Tea shows a more subtle pattern, often consumed in the afternoon or rainy days — harder for the model to detect.

CONCLUSION
This project aimed to examine whether environmental conditions—specifically weather (temperature and rainfall) and time of day—have a measurable influence on beverage sales patterns. Through extensive exploratory data analysis and machine learning experimentation, we arrived at several meaningful insights:
Cold weather strongly correlates with increased coffee sales, especially during morning hours. This supports the idea that consumers gravitate toward hot beverages like coffee to start their day in colder climates.
Tea sales tend to show a moderate increase during rainy and warmer afternoons, though this trend is not as strong or consistent as coffee in the morning. The relationship between rain and tea consumption appears to be more behavioral than causal.
Time of day emerged as a more significant driver of beverage choice than weather alone. Morning hours consistently saw the highest volume of coffee sales, regardless of weather conditions.
Weather does exert some influence, particularly in terms of temperature-driven demand for coffee. However, it is not a dominant factor in determining unit prices or exact sales quantities. Other factors such as marketing campaigns, customer demographics, or seasonal promotions may play a more important role.
Machine learning models, particularly regression algorithms, struggled to predict unit prices based on weather and time variables alone. Their performance (as reflected in R² scores close to zero) suggests that weather is not a sufficient predictor for pricing models.
Classification models fared slightly better when predicting product categories (coffee vs tea) but were still limited by class imbalance and weak feature predictability.
Business Implications:
Companies can benefit from aligning inventory and staffing with predictable time-of-day patterns (e.g., stocking more coffee for morning shifts).
Weather forecasts may help anticipate minor fluctuations in demand, particularly for tea on rainy afternoons or coffee during cold mornings.
However, for accurate forecasting and pricing, more granular data inputs—such as customer-level data, event schedules, or marketing activity—are likely required.




## ✅ Conclusion
- ❄️ Cold weather clearly drives up coffee sales.
- ☔ Rain doesn't drastically affect pricing but nudges demand slightly.
- 📍 Location and time of day are strong predictors of sales volume.
- 📅 Weekly trends and weather together offer actionable insights for inventory planning.

---

