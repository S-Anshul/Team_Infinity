✈️ United Airlines Flight Difficulty Analysis
Team Infinity
Introduction
Customer: “My flight to Brussels got delayed again! Is this route always this chaotic?”
Aditya (Future UA Employee): “It’s not just bad luck — some flights are naturally harder to manage. Too many transfers, tight schedules, or special requests can make them tricky.”
Customer: “So… you can actually measure how difficult a flight is?”
Anshul (Future UA Employee): “That’s what we’re trying to figure out.”

This project was born from that very question — can we quantify flight difficulty?

Project Overview
United Airlines operates thousands of flights every day, each with varying levels of operational complexity.
This project introduces the Flight Difficulty Score (FDS) — a composite metric that measures how challenging a flight is to operate, based on multiple real-world parameters like:

Delays and ground time
Passenger and baggage load
Special Service Requests (SSRs)
Transfer-to-checked bag ratios
By analyzing these factors, we classify each flight as Easy, Medium, or Difficult — helping airlines optimize operations, resource allocation, and scheduling.

Dataset Description
All datasets used are stored in the Data/ folder.

Dataset	Description
Airports Data	Airport and country codes
Bags Data	Transfer and checked baggage details
Flights Data	Flight schedules, delays, fleet, and carrier
PNR Flight Data	Passenger details (children, lap infants, etc.)
PNR Remark Data	Special Service Requests (SSRs) linked to each passenger
Analysis Pipeline
Data Loading & Cleaning

Imported and merged all datasets
Converted date/time columns
Handled missing and inconsistent data
Feature Engineering

Calculated new features: delay duration, passenger ratios, ground time flags, SSR counts
Computed a custom Flight Difficulty Score (FDS)
Difficulty Classification

Ranked flights by daily FDS
Top 20% → Difficult
Middle 60% → Medium
Bottom 20% → Easy
Exploratory Data Analysis (EDA)

Distribution of FDS
Top 10 most difficult flights
Difficult destinations
Correlation Analysis

Found relationships between FDS and features like passenger count, delay, SSRs, and baggage ratios
Visualizations
Histograms showing FDS distribution
Bar charts for Top 10 Difficult Flights and Destinations
Correlation heatmaps for operational insights
Key Insights
Most flights have low difficulty scores, with few highly difficult outliers
Certain destinations consistently have higher average difficulty
Strong correlation observed between:
Passenger count and difficulty
Tight ground time and delay rate
SSR count and overall complexity
Tech Stack
Python
pandas, numpy, matplotlib, seaborn
Jupyter Notebook
Usage
Clone this repository:
git clone https://github.com/<your-username>/United_airline_TEAM_INFINITY.git
