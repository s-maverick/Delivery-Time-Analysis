# Analyzing Key Factors Influencing E-Commerce & Grocery Delivery Times


## **Project Overview**

This project investigates the complex variables influencing delivery times across major Indian e-commerce platforms, including **Blinkit**, **Swiggy Instamart**, and **JioMart**. By analyzing over **200,000 rows** of transactional data, the study explores how static factors (order value, platform type) and dynamic environmental variables (traffic density, weather conditions) impact operational efficiency and delivery delays.

## **Key Research Questions**

**Platform & Transactional Impact:** How do order value and specific platform attributes contribute to delivery speed? 

**Environmental Impact:** To what extent do real-time traffic density and weather anomalies cause measurable delivery delays? 


## **Hypotheses Tested**

**H1:** High-order values lead to longer delivery delays compared to low-value orders.

**H2:** Real-time traffic density and weather conditions significantly impact food and grocery delivery times.


## **Dataset & Methodology**
The analysis utilizes two distinct datasets representing the online grocery and food delivery ecosystem:

**Dataset 1:** Focuses on platform comparisons, order values, and customer feedback for Blinkit, Swiggy Instamart, and JioMart.

**Dataset 2:** Emphasizes time-sensitive environmental metrics, including GPS-based distance, weather conditions (Stormy, Sunny, Fog, etc.), and road traffic levels (Low, Medium, High, Jam).


### **Technical Stack**

**Language:** R 
**Libraries:** `tidyverse` (dplyr, ggplot2), `geosphere` (distHaversine), `stringr` 

**Models:** Multiple Linear Regression, Interaction Terms, AIC/BIC Model Selection 


## **Core Findings**

**Traffic is King:** Road traffic density is a much stronger predictor of delivery time than raw geographical distance. In "Jam" conditions, delivery times increase by approximately **3.94 minutes**.

**Platform Variance:** JioMart showed slightly higher average delivery times (~10 seconds longer) compared to Blinkit in the primary regression model.

**The Festival Effect:** Deliveries during festivals experience significant delays, increasing by an average of over **19 minutes**.

**Operational Efficiency:** Higher delivery person ratings and better vehicle conditions are strongly correlated with reduced delivery times.


## **Final Models Selected**

**Dataset 1 (h1_model2):** Selected for its balance of explanatory power and parsimony, capturing platform-specific patterns without overfitting.

**Dataset 2 (h2_model3):** Identified as the most robust model for predicting delays based on a comprehensive set of predictors including weather, traffic, and operational load.
