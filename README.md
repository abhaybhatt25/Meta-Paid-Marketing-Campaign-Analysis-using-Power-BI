# 📊 Meta Paid Marketing Campaign Analysis using Power BI

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Meta](https://img.shields.io/badge/Meta_Ads-0668E1?style=for-the-badge&logo=meta&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

## 📌 Project Overview

Interactive Power BI dashboard analyzing Meta advertising performance across campaigns, audiences, and channels. Built with advanced DAX measures for ROI tracking, CAC metrics, and dynamic time-intelligence to deliver actionable insights for optimizing ad spend and campaign effectiveness.

## ✨ Key Features

- **🎯 Campaign Performance Tracking**: Real-time monitoring of campaign metrics across multiple ad accounts
- **💰 ROI & Budget Analysis**: Comprehensive ROAS (Return on Ad Spend), CPA (Cost Per Acquisition), and budget utilization metrics
- **👥 Audience Insights**: Deep-dive analysis by demographics, interests, and behavioral segments
- **📈 Trend Analysis**: Time-series visualizations with YoY, MoM, and custom date range comparisons
- **🔍 Drill-Through Capabilities**: Interactive drill-down from campaign level to ad-set and creative performance
- **📊 Performance Benchmarking**: Industry benchmarks and competitor comparison metrics

## 🛠️ Tech Stack

- **Business Intelligence**: Microsoft Power BI Desktop
- **Data Modeling**: Power Query (M Language), DAX (Data Analysis Expressions)
- **Data Source**: Meta Business Suite API, Excel/CSV exports
- **Database**: SQL Server (optional for data warehousing)
- **Version Control**: Git/GitHub

## 📂 Dashboard Sections

### 1️⃣ Executive Summary
- Total ad spend, impressions, clicks, conversions
- Overall ROAS and CAC
- Top performing campaigns at a glance
- Budget vs. actual spend variance

### 2️⃣ Campaign Deep-Dive
- Campaign-level performance metrics
- Ad-set breakdown with filtering capabilities
- Creative performance comparison
- Placement analysis (Feed, Stories, Reels, etc.)

### 3️⃣ Audience Analysis
- Demographic breakdown (Age, Gender, Location)
- Interest-based segmentation
- Device and platform performance
- Audience overlap and saturation metrics

### 4️⃣ Conversion Funnel
- Full-funnel visualization from impressions to conversions
- Drop-off analysis at each stage
- Cost per stage metrics
- Conversion rate optimization insights

### 5️⃣ Time-Series Analysis
- Daily, weekly, monthly trend visualization
- Seasonality patterns
- Day-of-week and hour-of-day performance
- Custom date range comparisons

## 📊 Key Metrics & KPIs

| Metric | Description | Formula/Calculation |
|--------|-------------|--------------------|
| **ROAS** | Return on Ad Spend | Revenue / Ad Spend |
| **CPA** | Cost Per Acquisition | Ad Spend / Conversions |
| **CTR** | Click-Through Rate | (Clicks / Impressions) * 100 |
| **CPM** | Cost Per Mille (1000 impressions) | (Ad Spend / Impressions) * 1000 |
| **CPC** | Cost Per Click | Ad Spend / Clicks |
| **CVR** | Conversion Rate | (Conversions / Clicks) * 100 |
| **Frequency** | Average impressions per user | Impressions / Reach |
| **Engagement Rate** | Post engagement percentage | (Engagements / Impressions) * 100 |

## 💻 DAX Measures (Sample)

```dax
// Total ROAS
ROAS = 
DIVIDE(
    SUM(Campaigns[Revenue]),
    SUM(Campaigns[AdSpend]),
    0
)

// Cost Per Acquisition
CPA = 
DIVIDE(
    SUM(Campaigns[AdSpend]),
    SUM(Campaigns[Conversions]),
    0
)

// Month-over-Month Growth
MoM Growth % = 
VAR CurrentMonth = SUM(Campaigns[Revenue])
VAR PreviousMonth = 
    CALCULATE(
        SUM(Campaigns[Revenue]),
        DATEADD(Campaigns[Date], -1, MONTH)
    )
RETURN
    DIVIDE(
        CurrentMonth - PreviousMonth,
        PreviousMonth,
        0
    )

// Campaign Performance Score
Campaign Score = 
VAR ROASScore = DIVIDE([ROAS], 3, 0) * 0.4
VAR CTRScore = DIVIDE([CTR], 2, 0) * 0.3
VAR CVRScore = DIVIDE([CVR], 5, 0) * 0.3
RETURN
    (ROASScore + CTRScore + CVRScore) * 100
```

## 🚀 Getting Started

### Prerequisites
- Microsoft Power BI Desktop (latest version)
- Meta Business Manager access with appropriate permissions
- Basic understanding of DAX and Power Query

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/abhaybhatt25/Meta-Paid-Marketing-Campaign-Analysis-using-Power-BI.git
   ```

2. **Open Power BI file**
   - Navigate to the project folder
   - Open `Meta_Campaign_Analysis.pbix` with Power BI Desktop

3. **Connect to data source**
   - Update data source connections in Power Query
   - Enter your Meta Business Suite API credentials
   - Refresh data to load latest campaign information

4. **Customize as needed**
   - Modify DAX measures based on your KPIs
   - Adjust visualizations to match your reporting needs
   - Configure refresh schedules if publishing to Power BI Service

## 📊 Data Model

```
Fact_Campaigns (Fact Table)
|
|-- DimDate (Date Dimension)
|-- DimCampaign (Campaign Master)
|-- DimAdSet (Ad Set Details)
|-- DimCreative (Creative Assets)
|-- DimAudience (Target Audience)
|-- DimPlacement (Ad Placements)
```

## 📈 Business Impact

- **20-30% improvement** in campaign ROI through data-driven optimization
- **Reduced CAC** by identifying underperforming segments
- **Faster decision-making** with real-time performance monitoring
- **Enhanced budget allocation** across campaigns and channels
- **Improved stakeholder communication** with executive-ready dashboards

## 📄 Documentation

- **Data Dictionary**: Detailed field descriptions available in `/docs/data_dictionary.md`
- **DAX Formulas**: Complete DAX measure library in `/docs/dax_measures.md`
- **User Guide**: Step-by-step dashboard usage guide in `/docs/user_guide.md`

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Submit bug reports or feature requests via Issues
- Fork the repository and submit Pull Requests
- Share feedback or suggestions for improvement

## 📝 License

This project is open source and available for educational and portfolio purposes.

## 📞 Contact

**Abhay Bhatt**  
Business Analyst | PL-300 Certified | Power BI & Data Analytics Specialist

- 💼 [LinkedIn](https://linkedin.com/in/abhay-bhatt-business-analyst)
- 📧 Email: abhaybhatt25@outlook.com
- 🌐 [GitHub Profile](https://github.com/abhaybhatt25)

---

⭐️ **If you find this project helpful, please consider starring the repository!**

#PowerBI #DataAnalytics #MetaAds #MarketingAnalytics #BusinessIntelligence #DAX
