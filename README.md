# 🏅 Olympic Analytics Dashboard - Paris 2024 & Historical Analysis

A comprehensive interactive Power BI dashboard analyzing Olympic Games data from 1896 to 2024, featuring detailed insights into the Paris 2024 Olympics alongside 128 years of Olympic history.

## 🎯 Project Overview

This Power BI dashboard provides a complete analytical view of Olympic Games performance, combining current Paris 2024 data with extensive historical Olympic records. The project demonstrates advanced data visualization, DAX calculations, and interactive dashboard design principles.

![Olympic Dashboard Overview](screenshots/dashboard-overview.png)

## 🏆 Key Features & Insights

### Paris 2024 Olympics Analysis
- **Total Athletes**: 11,113 participants (5,658 male, 5,455 female)
- **Medal Distribution**: 329 Gold, 333 Silver, 390 Bronze medals
- **Global Participation**: 206 countries across 288 events
- **Gender Balance**: Near-perfect gender parity in participation

### Historical Olympic Trends (1896-2024)
- **Complete Historical Analysis**: 128 years of Olympic data
- **Medal Evolution**: 752 Gold, 760 Silver, 814 Bronze (historical totals)
- **Participation Growth**: From 43 events in 1896 to 288+ events in 2024
- **Country Performance**: Long-term performance tracking by nation

## 📊 Dashboard Pages

### 1. **Overview Page** 
- High-level tournament KPIs and medal summary
- Total participation statistics with gender breakdown
- Key highlights and tournament facts
- Interactive country filtering capabilities

### 2. **Medals by Athletes Page**
- Comprehensive athlete performance analysis  
- Country-wise medal distribution with visual medal icons
- Sport-specific medal comparisons (Athletics, Swimming, Wrestling, etc.)
- Gender-based performance metrics

### 3. **Athletes Demographics**
- Age category analysis (26-30, 21-25, 31-35, etc.)
- Gender distribution across age groups
- Visual podium representation for top performers
- Interactive demographic filtering

### 4. **Country Analysis**  
- Interactive world map with performance heat mapping
- Country selection panel with flag-based filtering
- Geographic medal distribution visualization
- Drill-down capabilities for detailed country insights

### 5. **Historical Trends**
- Olympic Games evolution from 1896-2024
- Medal trends over time with stacked visualizations
- Year-over-year participation growth patterns
- Historical milestone identification

## 🛠️ Technical Implementation

### **Tools & Technologies**
- **Power BI Desktop** - Primary dashboard development platform
- **Excel/Power Query** - Data cleaning and transformation
- **DAX** - Advanced calculations and custom measures
- **Power BI Service** - Dashboard publishing and sharing

### **Data Architecture**
```
Data Sources:
├── Paris 2024 Official Dataset
├── Historical Olympic Records (1896-2022)
├── Country & Flag Reference Data
└── Athlete Demographics Database
```

### **Key DAX Measures**
```dax
// Total Athletes Calculation
Total_Athletes = DISTINCTCOUNT(Olympics[Athlete_Name])

// Medal Count by Type
Gold_Medals = CALCULATE(COUNTA(Olympics[Medal]), Olympics[Medal] = "Gold")

// Gender Participation Rate  
Female_Participation_Rate = 
DIVIDE(
    CALCULATE(DISTINCTCOUNT(Olympics[Athlete_Name]), Olympics[Gender] = "Female"),
    [Total_Athletes], 0
) * 100

// Country Medal Ranking
Country_Ranking = RANKX(ALL(Olympics[Country]), [Total_Medals], , DESC)
```

### **Data Processing Pipeline**
1. **Data Collection**: Aggregated from multiple Olympic databases
2. **Data Cleaning**: Standardized country names, athlete records, medal classifications
3. **Data Modeling**: Created star schema with fact and dimension tables
4. **Validation**: Cross-verified medal counts with official Olympic records
5. **Performance Optimization**: Implemented efficient relationships and calculations

## 🔍 Key Analytical Insights

### **Performance Highlights**
- **USA Leadership**: Consistent top performer in total medal count
- **Gender Equality**: First Olympics achieving near-perfect gender balance
- **Global Representation**: Record 206 countries participating
- **Age Demographics**: Peak performance in 21-30 age category (65% of athletes)

### **Historical Trends**
- **Participation Growth**: 2,900% increase in athlete participation since 1896
- **Medal Expansion**: From 43 events to 288+ events over 128 years
- **Global Reach**: Expansion from 14 countries (1896) to 206 countries (2024)
- **Gender Evolution**: From male-only to equal gender representation

## 🚀 Dashboard Features

### **Interactive Elements**
- ✅ Multi-level filtering (Country, Year, Sport, Gender)
- ✅ Drill-through capabilities across all pages
- ✅ Dynamic tooltips with contextual information
- ✅ Cross-highlighting between visualizations
- ✅ Responsive design for multiple screen sizes

### **Visualization Types**
- 🗺️ **Geographic Heat Maps** - World map medal distribution
- 📊 **Stacked Bar Charts** - Medal counts by country and type  
- 🎂 **Age Demographics** - Histogram with gender breakdown
- 📈 **Time Series Analysis** - Historical trends and growth patterns
- 🏅 **Medal Icons** - Visual medal representations with actual counts

## 📁 Repository Structure

```
Olympic-Dashboard/
├── 📊 Dashboard/
│   ├── Olympic_Dashboard.pbix          # Main Power BI file
│   └── Olympic_Dashboard_Template.pbit  # Template version
├── 📂 Data/
│   ├── paris_2024_athletes.csv
│   ├── historical_olympics.csv
│   └── country_mapping.xlsx
├── 📸 Screenshots/
│   ├── overview-page.png
│   ├── athletes-demographics.png
│   ├── country-analysis.png
│   └── historical-trends.png
├── 📋 Documentation/
│   ├── data-dictionary.md
│   ├── dax-measures.md
│   └── methodology.md
└── 📖 README.md
```

## 🎮 How to Use

### **Prerequisites**
- Microsoft Power BI Desktop (latest version)
- Windows 10/11 or compatible system

### **Getting Started**
1. **Clone Repository**
   ```bash
   git clone https://github.com/1-RoushanKumar/Olympic-Dashboard.git
   cd Olympic-Dashboard
   ```

2. **Open Dashboard**
   - Launch Power BI Desktop
   - Open `Dashboard/Olympic_Dashboard.pbix`
   - Wait for data refresh (automatic)

3. **Navigate & Explore**
   - Use top navigation tabs to switch between analysis pages
   - Click on countries/filters to interact with visualizations
   - Hover over charts for detailed tooltips

## 📈 Sample Analysis Scenarios

### **Scenario 1: Country Performance Analysis**
- Select "Country" page → Choose USA from filter → Analyze medal distribution across sports
- **Insight**: USA excels in Swimming and Athletics with 40+ medals combined

### **Scenario 2: Historical Trend Analysis** 
- Navigate to "Historical" page → Select year range 1980-2024
- **Insight**: Exponential growth in participation post-1980s globalization

### **Scenario 3: Demographic Deep-dive**
- Go to "Athletes" page → Filter by age group 26-30 → Analyze gender split
- **Insight**: Peak performance age group shows balanced gender representation

## 🚀 Future Enhancements

- [ ] **Real-time Updates**: Live data integration during ongoing Olympics
- [ ] **Predictive Analytics**: ML models for medal prediction
- [ ] **Social Sentiment**: Integration with social media analytics  
- [ ] **Economic Analysis**: Cost-benefit analysis of hosting Olympics
- [ ] **Mobile Version**: Power BI mobile-optimized dashboard

## 🎓 Skills Demonstrated

### **Technical Skills**
- Advanced Power BI dashboard development
- DAX formula creation and optimization
- Data modeling and relationship management
- Power Query data transformation
- Interactive visualization design

### **Analytical Skills**
- Statistical analysis and trend identification
- Geographic data analysis
- Demographic segmentation analysis
- Historical pattern recognition
- KPI development and tracking

## 👨‍💻 About the Developer

**Roushan Kumar**
- 📧 Contact: [Add your email]
- 🔗 LinkedIn: [Add your LinkedIn]
- 🌐 Portfolio: [Add your portfolio website]

*Passionate about data analytics, business intelligence, and creating impactful visualizations that drive decision-making.*

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/1-RoushanKumar/Olympic-Dashboard/issues).

### **How to Contribute**
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **International Olympic Committee** - Official data sources
- **Paris 2024 Organizing Committee** - Current games data
- **Power BI Community** - Best practices and inspiration
- **Olympic Database Contributors** - Historical data compilation

---

⭐ **If you found this project helpful, please give it a star!**

📊 **Live Demo**: [View Interactive Dashboard](https://app.powerbi.com/view?r=your-dashboard-link) *(Add your published dashboard link)*

🎯 **Project Status**: ✅ Completed | 📈 Continuously Updated
