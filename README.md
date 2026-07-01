# 🚖 RideIT Driver Engagement Analysis | Power BI Case Study

## 📌 Project Overview

This project analyzes driver engagement and operational performance for **RideIT**, a multi-service mobility platform offering ride-hailing, e-scooters, e-bikes, e-Vespas, and car-sharing services.

The objective of this case study is to help the **Supply Product Team** understand driver engagement, identify the factors influencing driver performance, and recommend business initiatives to improve platform efficiency.

---

## 🎯 Business Problem

The business wants to answer the following questions:

- Which KPIs should be monitored to measure driver engagement?
- Which factors are associated with better engagement?
- Which driver segments perform the best?
- What improvements can increase driver engagement and reduce cancellations?

---

## 📂 Dataset

This project uses two datasets.

### 1. Rideit_drivers

Contains driver profile information:

- Driver ID
- Registration Date
- Driver Rating
- Gold Level Count
- Receive Marketing (True/False)
- Country Code
- Service Type

### 2. Rideit_drivers_activity

Contains driver activity information:

- Driver ID
- Active Date
- Offers
- Bookings
- Driver Cancellations
- Passenger Cancellations
- Completed Rides

> **Note:** The original activity dataset is over 50 MB. A representative sample is included in this repository due to GitHub file upload limitations.

---

# 🏗 Data Model

A **Star Schema** was implemented.

```
Rideit_drivers
       │
       │ Driver ID
       │
Rideit_drivers_activity
```

Relationship

- One-to-Many
- Driver ID

---

# 📊 Dashboard Pages

## Executive Summary

KPIs

- Total Drivers
- Total Offers
- Total Bookings
- Total Rides
- Ride Completion %
- Cancellation Rate %
- Average Driver Rating
- Average Gold Level Count

Visuals

- KPI Cards
- Funnel Chart
- Donut Chart
- Line & Clustered Column Chart

---

## Driver Engagement

Visuals

- Ride Completion Trend
- Booking Trend
- Offer Acceptance Trend
- Running Total of Rides

KPIs

- Offer Acceptance Rate
- Ride Completion Rate
- Average Offers per Driver
- Average Rides per Driver

---

## Driver Performance

Visuals

- Scatter Chart
- Top Drivers
- Driver Performance Matrix

KPIs

- Driver Rating
- Gold Level Count
- Total Rides
- Total Bookings

---

## Cancellation Analysis

Visuals

- Driver vs Passenger Cancellation
- Monthly Cancellation Trend
- Cancellation Rate by Driver Rating

KPIs

- Driver Cancellation %
- Passenger Cancellation %
- Overall Cancellation %

---

## Marketing Analysis

Visuals

Comparison between

- Drivers Receiving Marketing
- Drivers Not Receiving Marketing

Measures

- Average Rides
- Average Bookings
- Ride Completion %

---

## Country & Service Type Analysis

Visuals

- Country Performance
- Service Type Comparison

KPIs

- Total Drivers
- Ride Completion %
- Cancellation Rate

---

# 📈 Key Metrics
### Total Completed Rides

```
SUM(rideit_drivers_activity[rides])
```

### Offer Acceptance Rate

```
Bookings / Offers
```

### Ride Completion Rate

```
Rides / Bookings
```

### Cancellation Rate

```
(Driver Cancellations + Passenger Cancellations)
/ Bookings
```

---

# 📌 Business Insights

✔ More than 25 million ride offers were analyzed.

✔ Ride completion rate remained above 80%.

✔ Passenger cancellations were higher than driver cancellations.

✔ Drivers with higher ratings generally completed more rides.

✔ Gold-level drivers demonstrated better engagement.

✔ Driver engagement varied across service types and countries.

---

# 💡 Business Recommendations

- Reward high-performing drivers through incentive programs.
- Reduce cancellations using driver education and targeted incentives.
- Expand personalized marketing campaigns for engaged drivers.
- Monitor engagement KPIs monthly using Power BI dashboards.
- Focus onboarding efforts on newly registered drivers to improve retention.

---

# 🛠 Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Microsoft Excel

---

# 📷 Dashboard Preview

Add screenshots in the **Images** folder and reference them below.

```
Images/
│
├── Executive_Summary.png
├── Driver_Engagement.png
├── Driver_Performance.png
├── Cancellation_Analysis.png
├── Marketing_Analysis.png
└── Country_Analysis.png
```


# 📁 Repository Structure

```
rideit-driver-engagement-analysis
│
├── README.md
├── Dataset
│   ├── Rideit_drivers.csv
│   └── Rideit_drivers_activity_sample.csv
│
├── PowerBI
│   └── RideIT_Driver_Engagement.pbix
│
├── Documentation
│   ├── Case_Study.pdf
│   └── Presentation.pdf
│
├── Images
│   ├── Executive_Summary.png
│   ├── Driver_Engagement.png
│   ├── Driver_Performance.png
│   ├── Cancellation_Analysis.png
│   ├── Marketing_Analysis.png
│   └── Country_Analysis.png
│
└── DAX
    └── DAX_Measures.md
```

---

# 👨‍💻 Author

**Gopala Krishna**

📧 Email: *Add your email here*

🔗 LinkedIn: *Add your LinkedIn profile*

🔗 GitHub: *Add your GitHub profile*

---

## ⭐ If you found this project helpful, please consider giving the repository a Star!
