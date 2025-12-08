Airline Performance Dashboard – Power BI

A comprehensive analytics project designed to analyze flight delays, cancellations, diversions, weather impacts, route performance, and operational efficiency using large-scale airline operational data.

This dashboard provides insights across 8+ report pages, helping users understand flight performance from multiple dimensions including airline, airport, time, route, seasonality, and delay causes.

Project Overview

This Power BI dashboard analyzes historical flight data to identify operational patterns and performance issues.

Key Questions Answered:

Which airlines perform best/worst?

What causes delays? (Carrier, NAS, Security, Late Aircraft)

What hours/days see maximum cancellations?

How weather impacts flight operations?

Which airports/routes are most efficient?

How many flights get diverted and why?

Dashboard Pages & Features
Overview Page

A high-level summary of overall airline operations.

KPIs

Total Flights

Total Delays

Total Cancellations

Total Diversions

On-Time Performance %

Avg Arrival & Departure Delay

Visuals

Delay Trend Over Time

Flights by Airline

Flights by Airport

Map – Flight activity distribution

2️⃣ Delay Analysis

Focus on identifying delay patterns by airline, route, time, and date.

KPIs

Avg Departure Delay

Avg Arrival Delay

% Delayed Flights

Longest Delay (Max)

Visuals

Delay by Airline

Delay by Hour

Weekend vs Weekday Delay

Distance vs Delay Scatter Plot

3️⃣ Cancellation Analysis

Understand why and when flights get cancelled.

KPIs

Total Cancellations

Cancellation Rate %

Peak Cancellation Hour

Cancellation by Reason Code (A, B, C, D)

Visuals

Cancellations by Airline

Cancellations by Hour

Pie: Distribution of Cancellation Codes

4️⃣ Divert Analysis

Shows diversion patterns across time.

KPIs

Total Diverted Flights

Diversions by Season

Diversion Rate %

Visuals

Divert Trend

Monthly Diversions

Airport/City-wise Diversions

5️⃣ Weather Impact Analysis

Measure how weather affects delays and operations.

KPIs

Weather Delay Minutes

% Operations Affected by Weather

Visuals

Monthly Weather Delay Trend

Weather Delay by Airline

Weather Impact by Airport

6️⃣ Route Analysis

Understand performance of specific flight routes.

KPIs

Top 10 Busiest Routes

Most Delayed Routes

Avg Delay per Route

Visuals

Chart: Route Performance

Table: Route Delay Summary

Map: Route-Based Delay Highlights

7️⃣ Airport/City Performance Analysis

Comparison of airports and cities where delays are common.

KPIs

Best/Worst Airports (Avg Delay)

Fastest vs Slowest Turnaround Airports

Visuals

Airport Delay Leaderboard

City-Wise Delay Heatmap

Airport Arrival vs Departure Delay

8️⃣ Delay Cause Breakdown (NAS, Carrier, Security, Late Aircraft)

Deep dive into reason behind delays.

KPIs

Carrier Delay %

Security Delay %

NAS Delay %

Late Aircraft Delay %

Visuals

100% Stacked Bar: Delay Cause by Month

Pie Chart: Contribution of Each Delay Type

Line Chart: Delay Cause Trend

9️⃣ Day/Night Analysis

Time-based performance insights.

KPIs

Day vs Night Delays

Day vs Night Cancellations

Day vs Night Diversions

Avg Delay per Time Bucket (Morning/Afternoon/Evening/Night)

Visuals

Column Chart: Day vs Night

Area Chart: Hourly Delay Trend

Time Bucket Analysis

🧮 Important DAX Measures Used
Total Flights
Total Flights = COUNT('Flights'[FlightNum])

Total Delayed Flights
Delayed Flights = CALCULATE(COUNT('Flights'[FlightNum]), 'Flights'[DepDelay] > 0)

Cancellation Rate %
Cancellation % = DIVIDE([Total Cancellations], [Total Flights], 0)

Delay Cause Measures
Carrier Delay = SUM('Flights'[CarrierDelay])
NAS Delay = SUM('Flights'[NASDelay])
Security Delay = SUM('Flights'[SecurityDelay])
Late Aircraft Delay = SUM('Flights'[LateAircraftDelay])


(More DAX formulas can be added if you want the full list.)

📁 Dataset

The dataset includes standard airline performance fields such as:

Date, Month, Year

Airline (Carrier)

Flight Number

Scheduled Departure & Arrival Time

Actual Departure & Arrival Delay

Cancellation Code

Delay Cause (Carrier, Security, NAS, Weather, Late Aircraft)

Diverted Indicator

Route Information (Origin–Destination)

🛠 Tools Used

Power BI Desktop

Power Query (Data Cleaning)

DAX (Measures & Calculated Columns)

Map Visuals, Slicers, Hierarchies, Tooltips

🚀 How to Use

Download the PBIX file from this repository.

Open in Power BI Desktop.

Use slicers (Airline, Route, City, Date, Delay Type) to explore the insights.

🤝 Contributions

Contributions, issues, and suggestions are welcome!
Feel free to open a PR or raise an issue.

⭐ If you liked this dashboard…

Give this repository a star ⭐ on GitHub — it helps a lot!
