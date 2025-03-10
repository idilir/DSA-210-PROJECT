# DSA-210-PROJECT
Coffee Sales and Weather Analysis

**Title**: Analyzing the Impact of Weather on Coffee Sales  

## Motivation  
Coffee shops often experience fluctuating sales due to weather conditions. This project explores how **temperature** and **rainfall** influence daily coffee sales at a café. The goal is to help small businesses optimize inventory and staffing based on weather forecasts.  

## Data Sources  
1. **Weather Data**  
   - **Source**: [NOAA Climate Data](https://www.ncdc.noaa.gov/cdo-web/)  
   - **Variables**: Daily temperature (°C), rainfall (mm), and date for New York City (Jan–Mar 2023).  
   - **Collection**: Downloaded directly from NOAA’s public database.  

2. **Coffee Sales Data**  
   - **Source**: [Kaggle Coffee Sales Dataset](https://www.kaggle.com/datasets/ahmedabbas757/coffee-sales) (simulated data).  
   - **Variables**: Daily sales ($), number of customers, date,location ,coffee tea preference.  
   - **Enrichment**: Merged with weather data to analyze correlations.  


---

## Hypothesis Questions  
1. **Primary Hypothesis**:  
   - *Does temperature significantly influence daily coffe preference and sales?*  
     - **Null Hypothesis (H₀)**: Temperature has no significant effect on coffe preference and sales.  
     - **Alternative Hypothesis (H₁)**: Temperature significantly affects coffe preference and sales.  

2. **Secondary Hypothesis**:  
   - *Does rainfall significantly influence daily coffee preference and sales?*  
     - **Null Hypothesis (H₀)**: Rainfall has no significant effect on coffee preference.  
     - **Alternative Hypothesis (H₁)**: Rainfall significantly affects coffee preference.  

3. **Tertiary Hypothesis**:  
   - *Is there an interaction effect between temperature and rainfall on coffe preference and sales?*  
     - **Null Hypothesis (H₀)**: There is no interaction effect between temperature and rainfall on coffe preference and sales.  
     - **Alternative Hypothesis (H₁)**: There is a significant interaction effect between temperature and rainfall on coffe preference and sales.  

---

## Expected Insights  
- Identify whether colder or warmer temperatures drive higher coffee sales.  
- Determine if rainy days lead to increased or decreased sales.  
- Provide actionable recommendations for inventory and staffing based on weather forecasts.  

---
