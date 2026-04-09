# 🌏 Asia Development Pulse — Power BI Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![World Bank](https://img.shields.io/badge/World%20Bank-WDI-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> A 6-page interactive Power BI dashboard analysing economic, social, and environmental development across **Asian countries** using World Bank WDI data (1990–2022).

---

## 📊 Dashboard Preview

### Cover Page
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160208" src="https://github.com/user-attachments/assets/2920a556-3833-426a-914c-c14e7e1f2383" />


### Page 1 — Executive Overview
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160440" src="https://github.com/user-attachments/assets/11a998b0-c4c8-4bcf-9b37-1fab00791116" />

### Page 2 — Economic Growth
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160505" src="https://github.com/user-attachments/assets/c0b4614d-a0b0-4264-b821-b0349dab60a1" />

### Page 3 — Social Development
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160529" src="https://github.com/user-attachments/assets/ac43e914-0d99-4e47-804f-e91271eaf48f" />

### Page 4 — Environment & Infrastructure
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160546" src="https://github.com/user-attachments/assets/536eb874-d1ab-45ef-9b45-8fb921eb6cc8" />

### Page 5 — Country Deep Dive
<img width="1920" height="1080" alt="Screenshot 2026-04-09 160603" src="https://github.com/user-attachments/assets/2a2d42a2-076f-48c2-9fb9-b03d85890238" />

---

## 🎯 Project Overview

| Attribute | Details |
|---|---|
| **Tool** | Microsoft Power BI Desktop |
| **Dataset** | World Bank — World Development Indicators (WDI) |
| **Scope** | Asian Countries |
| **Indicators** | 14 Key WDI Indicators |
| **Time Period** | 1990–2022 |
| **Pages** | 6 Report Pages |
| **DAX Measures** | 15+ Custom Measures |
| **Data Model** | Star Schema |

---

## 📁 Project Structure

```
Asia-Development-Pulse-PowerBI/
│
├── SaimMulani_Asia_Development_Pulse.pbix    # Power BI file
├── SaimMulani_Asia_Development_Pulse.pdf     # Exported PDF
├── README.md                                 # Project documentation
│
└── screenshots/
    ├── cover.png
    ├── page1_executive_overview.png
    ├── page2_economic_growth.png
    ├── page3_social_development.png
    ├── page4_environment.png
    └── page5_country_deep_dive.png
```

---

## 📋 Dashboard Pages

### 🏠 Cover Page
- Dark themed professional cover
- Project title, subtitle, author name and LinkedIn

### 📌 Page 1 — Executive Overview
- **ArcGIS Bubble Map** — GDP per Capita by country with custom report page tooltips
- **4 KPI Cards** — Total Population (4bn), GDP per Capita, Life Expectancy, Internet Users %
- **Bar Chart** — Top 10 economies by GDP in Billions
- **Donut Chart** — Countries by Income Group distribution
- **Year Range Slicer** — 1990 to 2022

### 📈 Page 2 — Economic Growth
- **Treemap** — Asia GDP distribution by country
- **Line Chart** — GDP per Capita trend (1990–2022) across 6 countries
- **Animated Scatter Plot** — Trade Openness vs FDI Inflows with Play Axis animation
- **Column Chart** — Inflation Rate by Country with conditional formatting

### 🏥 Page 3 — Social Development
- **Line Chart** — Life Expectancy Over Time across 6 countries
- **Line Chart** — Child Mortality decline with trend line
- **100% Stacked Bar** — School Enrollment by Income Group
- **Area Chart** — Internet Adoption (1990–2022)
- **4 KPI Cards** — Life Expectancy, Child Mortality, School Enrollment, Internet %

### 🌿 Page 4 — Environment & Infrastructure
- **Column Chart** — CO2 per Capita by Country with conditional formatting
- **Gauge Chart** — Asia Electricity Access (99.77/100) 
- **Line Chart** — CO2 Emissions Trend (1990–2022)
- **Scatter Chart** — Urbanization vs CO2 Emissions
- **Waterfall Chart** — Electricity Access improvement by country

### 🔍 Page 5 — Country Deep Dive
- **Country Slicer** — Single country selection
- **5 KPI Cards** — GDP, Life Expectancy, Unemployment, Internet %, CO2
- **Normalized Line Chart** — Key trends on 0–100 scale
- **Dynamic Country Info Card** — Region, Income Group
- **Indicator Slicer** — Select any WDI indicator dynamically
- **Dynamic Line Chart** — Selected indicator trend for chosen country
- **Radar Chart** — Development profile across 5 dimensions

---

## 🔢 DAX Measures

| Measure | Description |
|---|---|
| `Latest Value` | Most recent year value for any indicator |
| `Avg Value` | Average across selected context |
| `YoY Change %` | Year-over-year percentage change |
| `GDP Current USD` | GDP in current US dollars |
| `GDP per Capita` | GDP per capita |
| `GDP in Billions` | GDP divided by 1 billion |
| `Life Expectancy` | Average life expectancy at birth |
| `Under5 Mortality` | Under-5 mortality rate |
| `School Enrollment %` | Primary school enrollment rate |
| `Internet Users %` | Internet users as % of population |
| `Unemployment %` | Unemployment rate |
| `Inflation %` | Consumer price inflation (annual %) |
| `FDI Net Inflows % GDP` | Foreign direct investment inflows |
| `Exports % GDP` | Exports as % of GDP |
| `Electricity Access %` | Access to electricity (% of population) |
| `Urban Population %` | Urban population as % of total |
| `CO2 per Capita` | CO2 emissions per capita |
| `Total Population` | Total population (sum) |
| `Selected Indicator Value` | Dynamic measure for Country Deep Dive |
| `Economy Score` | Normalized GDP score (0–100) |
| `Health Score` | Normalized life expectancy score (0–100) |
| `Education Score` | School enrollment score |
| `Environment Score` | Inverted CO2 score |
| `Connectivity Score` | Internet users score |
| `Country Info` | Dynamic country description text |
| `GDP Normalized` | GDP normalized to 0–100 scale |
| `Life Expectancy Normalized` | Life expectancy normalized to 0–100 |
| `Internet Normalized` | Internet % normalized to 0–100 |

---

## 🗄️ Data Model

```
                    DimCountry
                        |
                        | (Many to One)
                        |
DimSeries --------  FactWDI  -------- DimYear
(Many to One)     (Fact Table)      (Many to One)

Unconnected: DimFootNote, DimCountrySeries, DimSeriesTime
```

### Tables:
| Table | Type | Description |
|---|---|---|
| `FactWDI` | Fact | Main data table (~400K rows, long format) |
| `DimCountry` | Dimension | Country metadata (name, region, income group) |
| `DimYear` | Dimension | Year dimension (1990–2022) |
| `DimSeries` | Dimension | Indicator metadata |
| `DimFootNote` | Reference | Data quality annotations (unconnected) |
| `_Measures` | Measure Table | All DAX measures |

---

## 🌐 WDI Indicators Used

| Indicator | Code |
|---|---|
| GDP (current US$) | NY.GDP.MKTP.CD |
| GDP per capita | NY.GDP.PCAP.CD |
| Population total | SP.POP.TOTL |
| Life expectancy at birth | SP.DYN.LE00.IN |
| Under-5 mortality rate | SH.DYN.MORT |
| School enrollment primary | SE.PRM.ENRR |
| Internet users % | IT.NET.USER.ZS |
| Unemployment % | SL.UEM.TOTL.ZS |
| Inflation consumer prices | FP.CPI.TOTL.ZG |
| FDI net inflows % GDP | BX.KLT.DINV.WD.GD.ZS |
| Exports % GDP | NE.EXP.GNFS.ZS |
| Electricity access % | EG.ELC.ACCS.ZS |
| Urban population % | SP.URB.TOTL.IN.ZS |
| CO2 per capita | EN.GHG.CO2.PC.CE.AR5 |

---

## ✨ Key Features

- 🗺️ **ArcGIS Mapping** with custom report page tooltips
- 🎬 **Animated Scatter Plot** with Play Axis (1990–2022)
- 🕸️ **Radar Chart** development profiling across 5 dimensions
- 🔄 **Dynamic Country Deep Dive** — fully interactive single-country analysis
- 📊 **Normalized Multi-Line Chart** — GDP, Life Expectancy, Internet on same scale
- 🎯 **Conditional Formatting** — Red/Green on CO2 and inflation charts
- 🔗 **Synced Slicers** across all pages
- 💡 **Report Page Tooltips** on ArcGIS map

---

## 💡 Key Insights

1. **China & India** together account for ~60% of Asia's GDP growth since 1990
2. **Life expectancy convergence** — low-income Asian countries closed the gap by ~12 years
3. **Digital leapfrog** — Internet adoption in South/Southeast Asia grew from <5% (2000) to >60% (2022)
4. **CO2 divergence** — East Asia emissions rising while Southeast Asia moderates
5. **Child mortality success** — Under-5 mortality fell by >70% across most of Asia
6. **Energy access** — Asia achieved 99.77% electricity access by 2022

---

## 🛠️ Tools & Technologies

- Microsoft Power BI Desktop
- Power Query (M Language)
- DAX (Data Analysis Expressions)
- ArcGIS Maps for Power BI
- World Bank WDI Dataset

---

## 👤 Author    

**Saim Mulani**
- 🔗 LinkedIn: [linkedin.com/in/saimmulani-data](https://linkedin.com/in/saimmulani-data)
- 💻 GitHub: [github.com/saim5010](https://github.com/saim5010)

---

*Built as a portfolio project demonstrating Power BI, DAX, and data storytelling capabilities using World Bank WDI data.*
