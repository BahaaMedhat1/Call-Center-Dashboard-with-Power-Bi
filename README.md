# Call Center Dashboard

## Overview
This repository showcases a **Call Center Dashboard** developed using **Power BI**. The dashboard provides insights into call center performance through key metrics, charts, and detailed call records, enabling effective monitoring and decision-making.

---

## Dashboard Overview
### Home: KPIs and Charts  
![Call Center Dashboard](CallDash.png)

### Grid: Detailed Data Table  
![Call Center Grid](GridDash.png)

---

## Key Metrics and Visualizations
The dashboard is designed to track and analyze key performance indicators (KPIs) and call center metrics. It includes:

1. **Key Metrics**
   - Total Number of Calls
   - Total Call Duration (Hours and Minutes)
   - Average Call Duration
   - Response Time Percentage

2. **Visualizations**
   - Total Calls by Sentiment
   - Total Calls by Reason
   - Total Calls by Day
   - Total Calls by State
   - Total Calls by Call Centers

3. **Data Table View**
   A detailed table displaying individual call data, including customer information, channel, state, call reason, response time, city, and duration.

---

## DAX Calculations
Here are some of the DAX calculations used in this project:

1. **Average Call Duration in Minutes:**
   ```DAX
   Avg call Duration in mins = AVERAGE('Call Center'[Call Duration In Minutes])
   ```
   Calculates the average duration of calls in minutes.

2. **Response Time Percentage:**
   ```DAX
   Response Time % = COUNTX(
                        FILTER('Call Center', 
                        'Call Center'[Response Time] = "Above SLA" || 'Call Center'[Response Time]= "Within SLA"),
                        'Call Center'[Id]
                        ) / [Total Calls]
   ```
   Computes the percentage of calls that met or exceeded SLA response times.

3. **Total Call Duration in Hours:**
   ```DAX
   Total Call Duration in Hrs = [Total Call duration in mins] / 60
   ```
   Converts the total call duration from minutes to hours.

4. **Total Call Duration in Minutes:**
   ```DAX
   Total Call duration in mins = SUM('Call Center'[Call Duration In Minutes])
   ```
   Calculates the total duration of all calls in minutes.

---

## How to Use
1. Open the **Call Center Dashboard.pbix** file in **Power BI Desktop**.
2. Load or update the call center data from **Call center data.csv**.
3. Explore the interactive visuals on both pages:
   - **Home**: KPIs and charts.
   - **Grid**: Detailed call records table.

---

## Contact
For questions, feedback, or collaboration:

- **Name:** Bahaa Medhat Wanas  
- **Email:** [bahaamedhat2022@gmail.com](mailto:bahaamedhat2022@gmail.com)  
- **LinkedIn:** [Bahaa Wanas](https://www.linkedin.com/in/bahaa-wanas-9797b923a)  

---
