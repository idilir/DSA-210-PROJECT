# DSA-210-PROJECT
Coffee Preference,Sales and Weather Analysis

**Title**: Analyzing the Impact of Weather on Coffee Sales  

## Motivation  
Coffee shops often experience fluctuating sales due to weather conditions. This project explores how **temperature** and **rainfall** influence daily coffee sales at a café. The goal is to help small businesses optimize inventory and staffing based on weather forecasts.  

## Data Sources  
1. **Weather Data**  
   - **Source**: [https://www.ncei.noaa.gov/access/past-weather/)  
   - **Variables**: Daily temperature (°C), rainfall (mm), and date for New York City (Jan–Mar 2023).  
   - **Collection**: Downloaded directly from NOAA’s public database.  

2. **Coffee Sales Data**  
   - **Source**: [Kaggle Coffee Sales Dataset](https://www.kaggle.com/datasets/ahmedabbas757/coffee-sales) (simulated data).  
   - **Variables**: Daily sales ($), number of customers, date,location ,coffee tea preference.  
   - **Enrichment**: Merged with weather data to analyze correlations.
  
     
##  Objectives  
- Analyze correlations between weather (temperature, rainfall) and coffee sales.  
- Identify patterns in coffee vs. tea preferences based on weather.  
- Assess location-specific sales trends and time-of-day purchasing habits.  
- Develop predictive insights for inventory and staffing optimization.  



---

## Hypothesis   

### Temperature vs. Coffee Sales  
- **H₀**: Temperature has no effect on coffee preference/sales.  
- **H₁**: Temperature significantly affects coffee preference/sales.  

###  Rainfall vs. Coffee Sales  
- **H₀**: Rainfall has no effect on coffee preference.  
- **H₁**: Rainfall significantly affects coffee preference.  

### Temperature-Rainfall Interaction  
- **H₀**: No interaction effect between temperature and rainfall.  
- **H₁**: Significant interaction effect exists.  

### Location-Based Preferences  
- **H₀**: No variation in coffee preference by location.  
- **H₁**: Coffee preference varies significantly by location.  

### Quinary Hypothesis**: Time-of-Day Influence  
- **H₀**: Time of day has no impact on sales/preference.  
- **H₁**: Time of day significantly influences sales/preference.  


## 📊 Expected Insights  
1. Correlation between colder temperatures and higher coffee sales.  
2. Impact of rainy days on beverage preferences.  
3. Interaction effects of weather on peak sales periods.  
4. Location-specific trends (e.g., business vs. residential areas).  
5. Time-of-day sales patterns (morning coffee vs. evening tea).  

---

