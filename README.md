# analytics_edge
Using machine learning and optimization for Wildfire Prediction and Management

# Summary
We use predictive analytics to help decision-makers in California counties with the challenge of allocating resources for wildfire management. We consider data on all wildfires on California from 1993-2015, and daily weather data in that same period. We provide a model that predicts at the time of discovery whether a fire will be big or small so that decision-makers can allocate appropriate resources. We define a “big” fire as burning >2 acres, and a “small” fire as burning ≤2 acres. We produce a boosted trees model that gives a test AUC of 0.6442 and misclassifies only 23% of big fires.  
To complement the reactive classification model, we provide a proactive survival analysis. We use survival regression to predict the expected number of days until the next fire in a county and the probability of fire on any given day based on past weather and fire data. Our Cox Proportional Hazard regression gives survival predictions with a 0.64 concordance index. With this model, decision-makers can allocate resources and advise county residents on their behavior based on daily fire risk.  
There is substantial evidence that predictive analytics can help to improve wildfire responses and reduce the negative financial, ecological, and health impacts that wildfires have.  

# Data
National Wildfire Coordinating Group  
The first dataset contains data for daily weather observations in different locations in California. https://fam.nwcg.gov/fam-web/weatherfirecd/fire_files.htm  
The second dataset contains fire observations. https://www.kaggle.com/rtatman/188-million-us-wildfires  
We have >30,000 observations of forest fires merged with weather data on the fire discovery date in the fire discovery location.   

# Method
1. Data processing  
2. Boosted Tree models (LightGBM)  
3. Cox Proportional Hazard model to perform survival regression  
