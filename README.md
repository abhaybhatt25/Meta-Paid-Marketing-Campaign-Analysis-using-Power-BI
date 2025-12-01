# 📊 Meta Paid Marketing Campaign Analysis using Power BI

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Meta](https://img.shields.io/badge/Meta_Ads-0668E1?style=for-the-badge&logo=meta&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)

**Keywords:** Power BI | DAX | Meta Ads API | Business Intelligence | Data Visualization | ROI Optimization | Marketing Analytics | Ad Performance | Data Modeling

---

## 📌 Project Overview

End-to-end **interactive Power BI dashboard** analyzing Meta (Facebook/Instagram) advertising performance across campaigns, audiences, and channels. Built with **advanced DAX measures** for ROI tracking, CAC metrics, and dynamic time-intelligence. Designed to deliver **actionable insights for real-time decision-making** and budget optimization.

**Use Case:** Marketing teams, BI analysts, and performance marketers seeking to understand ad spend efficiency, audience performance, and campaign ROI through interactive, drill-through dashboards.

---

## ✨ Key Features

- 🎯 **Campaign Performance Tracking** – Real-time monitoring of campaign metrics across multiple ad accounts with drill-down from campaign → ad set → creative level
- 💰 **ROI & Budget Analysis** – Comprehensive ROAS (Return on Ad Spend), CPA (Cost Per Acquisition), and budget utilization metrics with variance analysis
- 👥 **Audience Insights** – Deep-dive analysis by demographics (age, gender, location), interests, behavioral segments, and device/platform performance
- 📈 **Trend Analysis** – Time-series visualizations with YoY, MoM, and custom date range comparisons for seasonal and performance trends
- 🔍 **Drill-Through Capabilities** – Interactive drill-down from campaign level to ad-set and creative performance with cross-filtering
- 📊 **Performance Benchmarking** – Industry benchmarks and competitor comparison metrics to contextualize campaign performance
- ⚡ **Dynamic Slicing** – Filter by date range, campaign status, audience segment, placement type (Feed, Stories, Reels), and cost metrics

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-------------|
| **BI Tool** | Microsoft Power BI Desktop |
| **Data Transformation** | Power Query (M Language), DAX (Data Analysis Expressions) |
| **Data Sources** | Meta Business Suite API, Excel/CSV exports |
| **Database** | SQL Server (optional for data warehousing) |
| **Version Control** | Git/GitHub |
| **DAX Functions** | CALCULATE, FILTER, SUMX, DIVIDE, TIME INTELLIGENCE |

---

## 📂 Dashboard Sections

### 1️⃣ Executive Summary
High-level KPIs and metrics:
- **Total ad spend, impressions, clicks, conversions** – campaign-level aggregates
- **Overall ROAS and CAC** – efficiency metrics
- **Top performing campaigns** – quick view of best performers
- **Budget vs. actual spend variance** – cost control indicator
- **Trend cards** – week-over-week, month-over-month changes

### 2️⃣ Campaign Deep-Dive
Granular campaign performance:
- Campaign-level metrics with custom KPI indicators
- Ad-set breakdown with dynamic filtering
- Creative performance comparison (by audience, placement, cost)
- Placement analysis (Feed, Stories, Reels, Instant Articles)
- Budget tracking and spend forecasting

### 3️⃣ Audience Analysis
Demographic and behavioral insights:
- Age, gender, and location breakdowns
- Interest-based segmentation with performance metrics
- Device and platform performance (Mobile, Desktop, Tablet)
- Connection type analysis (WiFi vs. Cellular)
- Audience overlap and redundancy detection

### 4️⃣ Trend Analysis & Forecasting
Temporal performance patterns:
- YoY and MoM comparisons with variance indicators
- Seasonal trends and anomaly detection
- Daily performance calendar heatmaps
- Custom date range comparisons
- Spend vs. conversion trend lines

### 5️⃣ ROI Optimization
Cost efficiency and budget allocation:
- ROAS by campaign, audience, and placement
- CAC (Cost Per Acquisition) analysis with benchmarking
- Budget allocation recommendations
- Top performers vs. bottom performers
- Cost per result by campaign objective

---

## 📊 DAX Measures & Formulas

### Core Metrics
```dax
-- ROAS (Return on Ad Spend)
ROAS = DIVIDE([Total_Revenue], [Total_AdSpend], 0)

-- CAC (Cost Per Acquisition)
CAC = DIVIDE([Total_AdSpend], [Total_Conversions], 0)

-- CTR (Click-Through Rate)
CTR = DIVIDE([Total_Clicks], [Total_Impressions], 0)

-- CPC (Cost Per Click)
CPC = DIVIDE([Total_AdSpend], [Total_Clicks], 0)

-- Conversion Rate
ConversionRate = DIVIDE([Total_Conversions], [Total_Clicks], 0)

-- YoY Growth
YoYGrowth = DIVIDE(
    [Current_Year_Metric] - [Prior_Year_Metric],
    [Prior_Year_Metric],
    0
)
```

### Time Intelligence
```dax
-- MTD (Month-to-Date) Spend
MTD_Spend = CALCULATE(
    [Total_AdSpend],
    DATESMTD(Calendar[Date])
)

-- Previous Month Comparison
Prior_Month_Spend = CALCULATE(
    [Total_AdSpend],
    DATEADD(DATESMTD(Calendar[Date]), -1, MONTH)
)
```

---

## 🚀 How to Use

1. **Connect Data Source**
   - Export Meta Ads Manager data (CSV) or connect via Meta Business Suite API
   - Load data into Power BI using Power Query

2. **Load the Dashboard**
   - Open the `.pbix` file in Power BI Desktop
   - Refresh the data connection to pull latest metrics

3. **Explore & Filter**
   - Use date range slicers for custom periods
   - Filter by campaign, audience segment, or placement type
   - Hover over visuals for detailed tooltips

4. **Drill-Through**
   - Right-click on campaign cards to drill to ad-set level
   - Explore creative-level performance

5. **Export Reports**
   - Use "Export to PowerPoint" for stakeholder presentations
   - Publish to Power BI Service for real-time sharing

---

## 📈 Business Impact

**Results Delivered:**
- ✅ **Real-time visibility** into campaign performance, reducing reporting time from manual updates to instant refresh
- ✅ **ROAS tracking** enabling data-driven budget reallocation across campaigns
- ✅ **Audience insights** identifying highest-performing segments for audience expansion
- ✅ **Anomaly detection** flagging underperforming placements and creatives for quick optimization
- ✅ **Executive dashboard** providing stakeholder-ready summaries for board reviews

---

## 🎓 Key Learnings & Techniques

✅ **Data Modeling** – Star schema design for dimensional analysis  
✅ **DAX Optimization** – Efficient measure calculation and context handling  
✅ **API Integration** – Connecting to Meta Business Suite for real-time data  
✅ **Advanced Visualizations** – KPI cards, combo charts, tree maps, and heatmaps  
✅ **Drill-Through Navigation** – Multi-level dashboard interactivity  
✅ **Time Intelligence** – YTD, MTD, and period-over-period comparisons  

---

## 📝 Getting Started

### Prerequisites
- Microsoft Power BI Desktop (latest version)
- Meta Business Suite account with ad account access
- CSV export from Meta Ads Manager or API credentials

### Installation
1. Clone this repository: `git clone https://github.com/abhaybhatt25/Meta-Paid-Marketing-Campaign-Analysis-using-Power-BI.git`
2. Open the `.pbix` file in Power BI Desktop
3. Update data source connections with your Meta Ads data
4. Refresh and publish to Power BI Service

---

## 🔗 Connect & Explore

- **GitHub Portfolio:** [abhaybhatt25](https://github.com/abhaybhatt25)
- **LinkedIn:** [Abhay Bhatt – Business Analyst](https://linkedin.com/in/abhay-bhatt-business-analyst/)
- **Email:** abhaybhatt25@outlook.com

---

## 📄 Documentation

For detailed documentation on data dictionary, DAX measures, and troubleshooting, refer to:
- `/docs/data_dictionary.md` – Field descriptions and data sources
- `/docs/dax_measures.md` – Complete DAX formula library
- `/docs/user_guide.md` – Step-by-step usage guide

---

## 📜 License

This project is open source and available for educational and portfolio purposes. Feel free to fork, modify, and use as reference for your own analytics projects.

---

## ⭐ If You Found This Useful

Please consider:
- ⭐ **Starring the repository** to show support
- 🔄 **Forking and customizing** for your own use cases
- 💬 **Contributing** with improvements or feature suggestions
- 🤝 **Sharing** with your analytics and marketing teams

---

## 💪 Dashboard Screenshots

### Meta Ad Performance Dashboard - Executive Summary
Interactive Power BI dashboard showing comprehensive Meta advertising performance metrics:
- **KPI Cards:** Real-time metrics (Impressions: 123.8K, Clicks: 14.7K, Shares: 682, Comments: 1.5K, Purchases: 708, Engagements: 16.8K)
- **Engagement Rates:** CTR 11.86%, Engagement Rate 13.60%, Conversion Rate 4.82%, Purchase Rate 0.57%
- **Budget Analysis:** Average Budget $50.7K per campaign, Total Budget $2.5M
- **Demographic Insights:** Shares by Gender (pie chart), Shares by Age (distribution), Geographic breakdown
- **Trend Analysis:** Weekly Shares Trend (stacked bar chart), Hourly Shares Trend (line chart)
- **Performance Matrix:** Analysis by Ad Type (Carousel, Stories, Image, Video) with JMPR, CLKS, CTR, PR, ER, CR metrics
- **Placement Analysis:** Day-by-day analysis calendar heatmap and country-level geographic visualization
- **Meta Platform Selector:** Dynamic dropdowns for platform selection (Facebook/Instagram), campaign filtering, and target interest segmentation

![Meta Ad Performance Dashboard - Executive Summary](./assets/meta_dashboard_executive.png)

---

### Meta Ad Performance Dashboard - Advanced Analytics
Second view showing alternative KPI layout and additional performance dimensions:
- **Updated KPI Distribution:** Impressions: 216.0K, Clicks: 25.4K, Shares: 1.3K, Comments: 2.6K, Purchases: 1.3K, Engagements: 29.3K
- **Refined Engagement Metrics:** CTR 11.76%, Engagement Rate 13.56%, Conversion Rate 5.21%, Purchase Rate 0.61%
- **Consistent Budget Tracking:** $50.7K average per campaign, $2.5M total budget
- **Enriched Demographic Analysis:** Updated gender and age distribution patterns
- **Enhanced Weekly & Hourly Trends:** Refined trend visualizations showing performance consistency
- **Ad Type Performance Matrix:** Stories (23.8K JMPR, 2.7K CLKS, 11.35% CTR), Image (16.8K, 1.9K, 11.23%), Carousel (15.9K, 1.8K, 11.08%), Video (15.1K, 1.8K, 11.78%)
- **Advanced Filtering:** Multi-select dropdowns for dynamic measure selection, campaign filtering, and target interest segmentation

![Meta Ad Performance Dashboard - Advanced Analytics](./assets/meta_dashboard_analytics.png)

---

**Key Dashboard Features:**
- 🔄 **Drill-Through Interactivity:** Click on campaigns to drill down to ad-set and creative level
- 🔍 **Cross-Filtering:** All visuals interconnected; selecting metrics filters others in real-time
- 📈 **Trend Comparison:** YoY and MoM analysis with variance indicators
- 🎉 **Multi-Platform Analysis:** Simultaneous Facebook and Instagram performance comparison
- 📊 **Export Ready:** Download as PowerPoint or export data to Excel
- 🔏 **Dynamic Slicing:** Filter by date, campaign, audience, and placement type

---

**Last Updated:** December 2025  
**Status:** Active & Maintained  
**Complexity Level:** Intermediate to Advanced

#PowerBI #DataAnalytics #MetaAds #BusinessIntelligence #DAX #MarketingAnalytics #ROAS #DataVisualization #Analytics
