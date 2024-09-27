# Traffic Flow Prediction Project

## Overview

The **Traffic Flow Prediction Project** is designed to forecast traffic conditions based on historical vehicle data. This data includes the count of cars, bikes, buses, trucks, along with temporal data such as time of day and day of the week. The project aims to identify traffic patterns, predict congestion levels, and offer insights for urban traffic management. This model can help optimize traffic flow, reduce congestion, and contribute to sustainability goals by lowering emissions and fuel consumption through more efficient traffic control strategies.

This project is developed by [K.YUVA SHANKAR](https://www.linkedin.com/in/yuva-shankar-4ba786228?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app).

## Features of the Project
- **Traffic Prediction**: Predicts traffic flow based on vehicle counts and temporal data.
- **Actionable Insights**: Provides insights into peak traffic hours, vehicle distribution, and congestion periods.
- **Environmental Impact**: Helps in reducing traffic congestion, which in turn minimizes fuel consumption and emissions.
- **Sustainable Urban Mobility**: Assists city planners and traffic authorities in making real-time, data-driven decisions to optimize road usage and reduce traffic delays.

---

## Dataset Description

The dataset used in this project records traffic data over different timestamps, containing the following features:

### **Data Dictionary**:
- **Time**: Timestamp of the observation.
- **Date**: The specific date of the observation.
- **Day of the Week**: The day corresponding to the observation (e.g., Monday, Tuesday).
- **CarCount**: Number of cars counted at the observation point.
- **BikeCount**: Number of bikes counted at the observation point.
- **BusCount**: Number of buses counted at the observation point.
- **TruckCount**: Number of trucks counted at the observation point.
- **Total**: Total number of vehicles (sum of CarCount, BikeCount, BusCount, and TruckCount).
- **Traffic Situation**: Categorized traffic conditions based on congestion levels (e.g., low, medium, high traffic).

---

## Data Preprocessing

Data preprocessing is critical to ensure the model is accurate and reliable. The following steps were performed to clean and format the dataset:

1. **Time and Date Formatting**:
   - The **Time** and **Date** columns were converted to `datetime` format.
   - Additional features like **Hour**, **Month**, and **Day of the Week** were extracted to better capture temporal patterns.
   
2. **Handling Categorical Data**:
   - The categorical variables like **Day of the Week** and **Traffic Situation** were encoded numerically using label encoding to make them suitable for machine learning models.
   
3. **Handling Missing Values**:
   - Missing data was handled by replacing null values with the median values of their respective columns to ensure data completeness without distorting trends.

---

## Exploratory Data Analysis (EDA)

EDA was conducted to uncover hidden patterns and trends in traffic flow. Some key insights include:

### **Traffic Peak Hours**:
- **Morning Rush**: Spikes in traffic during the morning hours, with cars and bikes peaking between 7-9 AM.
- **Evening Rush**: Another peak observed during evening hours from 5-7 PM, showing similar car and bike traffic spikes.
- **Steady Truck Flow**: Trucks maintained a relatively stable count throughout the day compared to cars and bikes.

### **Vehicle Type Distribution**:
- **Car Dominance**: Cars accounted for the largest portion of total traffic, followed by bikes, buses, and trucks.
- **Truck Traffic and Congestion**: The volume of trucks was strongly associated with worsened traffic situations.

### **Day of the Week Influence**:
- There were no major variations in total traffic across different weekdays; however, certain days showed slight fluctuations in individual vehicle types.

---

## Model Building

### **Machine Learning Model: Random Forest Classifier**

A **Random Forest Classifier** was chosen as the primary model for predicting traffic situations. This model was selected for its robustness and ability to handle large datasets with multiple features.

- **Target Variable**: The target for prediction was the **Traffic Situation**, categorized into levels of congestion (e.g., low, medium, high).
- **Feature Set**: Key features for prediction included **CarCount**, **BikeCount**, **TruckCount**, **Day of the Week**, and **Hour of the Day**.
  
---

## Model Evaluation

### **Evaluation Metrics**:
The following metrics were used to assess the performance of the model:

- **Confusion Matrix**: Provided insight into true positives and prediction errors for each traffic category.
- **Classification Report**: Highlighted precision, recall, and F1-score for the different traffic situation categories.
- **Accuracy**: The overall accuracy of the model was satisfactory, particularly in predicting high-traffic periods.

### **Feature Importance**:
The features that had the most significant impact on traffic prediction included:

1. **CarCount**: Most critical in predicting traffic congestion.
2. **BikeCount**: Also a strong indicator of traffic situations.
3. **Day of the Week**: Contributed to identifying weekly traffic patterns.
4. **Hour of the Day**: Helped pinpoint peak traffic hours and predict congestion periods.

---

## Visualizations

Several visualizations were generated to enhance understanding of the traffic patterns:

- **Traffic Volume Over Time**: Cars and bikes dominate during peak hours, while trucks maintain a steady presence throughout the day.
- **Day-Wise Traffic Spread**: Vehicle traffic showed unique patterns across the week.
- **Pairwise Correlation**: There was a positive correlation between **CarCount** and **BikeCount**, while **TruckCount** negatively correlated with traffic conditions, indicating that increased truck traffic was linked with worse congestion.

---

## Conclusion

The **Traffic Flow Prediction Project** provides critical insights into traffic patterns, highlighting the significant influence of vehicle counts, time of day, and day of the week. By leveraging these insights, city planners and traffic authorities can:

- **Optimize Traffic Control**: Adjust traffic signals dynamically and plan road infrastructure more effectively.
- **Improve Public Transport Scheduling**: Enhance public transportation efficiency by adjusting routes and schedules based on predicted congestion.
- **Enhance Sustainability**: Reduce vehicle emissions and fuel consumption by managing traffic more efficiently, contributing to environmental goals.
- **Support Smart City Initiatives**: This project plays a vital role in integrating real-time data to build more efficient, sustainable, and smart cities.

## Future Work

Potential enhancements for this project include:

- **Real-Time Traffic Prediction**: Implementing real-time traffic updates using live data streams.
- **Integration with IoT Devices**: Collecting real-time data from road sensors, cameras, and IoT devices to improve traffic predictions.
- **Advanced ML Models**: Experimenting with deep learning models to further improve accuracy.
- **Traffic Control Optimization**: Building a traffic management dashboard for real-time decision-making.

---

This project is developed by [K.YUVA SHANKAR](https://www.linkedin.com/in/yuva-shankar-4ba786228?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app).
