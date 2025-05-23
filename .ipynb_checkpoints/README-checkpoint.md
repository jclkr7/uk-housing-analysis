# uk-housing-analysis

# UK Housing Market Analysis: London's Affordability Crisis

This repository contains my final empirical project for BEE2041 – Data Science in Economics. The project presents a data-driven investigation into UK housing market trends, with particular focus on London's housing affordability compared to other UK regions. All analysis and visualisations have been produced using Python in Jupyter Notebook (eda.ipynb).

**GitHub Repository:** https://github.com/jclkr7/uk-housing-analysis

## Project Overview

This project employs several real-world datasets to empirically analyse trends in UK housing prices and affordability. The key objectives are to:

* **Examine House Price Trends** – Analyse overall national and regional differences in house price growth since 1995, with a special focus on London boroughs
* **Assess Housing Affordability** – Utilise price-to-earnings ratios to evaluate affordability across different regions of the UK
* **Compare Property Types** – Investigate price variations across different property types (detached, semi-detached, terraced, flats)
* **Analyse COVID-19 Impact** – Evaluate how the pandemic affected housing markets across different UK regions
* **Forecast Future Trends** – Employ predictive modelling to project housing price trajectories

The analysis addresses three main research questions:
1. How has housing affordability in London evolved over the past 25 years compared to the rest of England?
2. What factors contribute to the significant price-to-income ratio disparity between London and other regions?
3. How has the COVID-19 pandemic affected housing affordability across different UK regions?

This project employs linear regression modelling techniques from Unit 5 of the course to forecast future housing prices in London through 2030, demonstrating the application of predictive analytics to economic data. The time series analysis and forecasting methodology allows for robust projections based on historical trends while accounting for non-linear growth patterns.

## Version Control

This project uses git for version control. All development history is tracked in the repository, allowing for transparent documentation of the analysis process and changes made over time. The complete commit history demonstrates the progression of the analysis from data collection and cleaning through to visualisation and interpretation of findings.

## Repository Structure

The repository is structured as follows:

```
uk-housing-analysis
│   eda.ipynb                           # Main Jupyter notebook with all analysis
│   rightmove_borough_prices.png        # Visualisation of borough-level prices
│   rightmove_london_data.csv           # Scraped property data from Rightmove
│   README.md                           # Current File
│   rightmove_property_type_prices.png  # Visualisation of property type prices
│
└───data
    │   aff1ratioofhousepricetoworkplacebasedearnings2024.xlsx  # Data for Affordability
    │   UK-HPI-full-file-2025-01-1.csv  # House Price Index data - 1
    │   UK-HPI-full-file-2025-01-2.csv  # House Price Index data - 2
    │
    ├───figures
    │       avg_house_prices_by_region_tab20_manual.png
    │       covid_affordability_impact.png
    │       london_england_affordability_gap.png
    │       london_ftb_vs_foo.png
    │       london_price_predictions.png
    │       london_price_vs_affordability.png
    │       london_prices_by_property_type.png
    │       london_property_type_affordability.png
    │       london_property_type_trends.png
    │       yearly_growth_heatmap_boldlabels.png
    │
    └───processed
            key_regions_hpi_data.csv    # Processed HPI data for key regions
            key_regions_ratio_data.csv  # Processed affordability ratio data
            london_hpi_data.csv         # Processed London-specific HPI data
```

## Blog Post

The analysis is presented as a data-driven blog post titled "London's Housing Affordability Crisis: A Data-Driven Analysis of the UK Property Market". The post contains approximately 2,300 words and features 7 data visualisations, analysing trends in house prices, affordability ratios, and regional disparities from 1995 to 2025 with projections to 2030.

---

This project offers a comprehensive analysis of the UK housing market with a focus on London's affordability crisis, providing valuable insights for policymakers, researchers, and potential homebuyers interested in understanding historical trends and future projections of the housing market.

## Data Sources

The analysis uses the following datasets:

### UK House Price Index (HPI) Data
* `data/UK-HPI-full-file-2025-01-1.csv` and `data/UK-HPI-full-file-2025-01-2.csv`
* Contains detailed house price data by region and property type from 1968 to 2025
* Includes average prices, indices, monthly changes, yearly changes, and sales volumes
* The data covers all UK regions.

### Affordability Data
* `data/aff1ratioofhousepricetoworkplacebasedearnings2024.xlsx`
* Contains price-to-earnings ratios across different UK regions from 1997 to 2024
* Allows comparison of housing affordability over time and between regions

### Rightmove London Property Data
* `rightmove_london_data.csv`
* Contains property listings scraped from Rightmove for London boroughs
* Includes property prices, descriptions, property types, and borough information
* Used for more granular analysis of London's housing market

### Processed Data
* `data/processed/london_hpi_data.csv` - Filtered HPI data for London only
* `data/processed/key_regions_hpi_data.csv` - Filtered HPI data for key UK regions
* `data/processed/key_regions_ratio_data.csv` - Processed affordability ratio data for key regions

## Installation

To replicate this project, ensure that Python (version 3.8 or higher) is installed on your system. Install the required packages by running:

```bash
pip install pandas numpy matplotlib seaborn requests scikit-learn beautifulsoup4 lxml jupyter
```

Package Used:

* **pandas** 
* **numpy** 
* **matplotlib** 
* **seaborn** 
* **requests** 
* **scikit-learn**
* **beautifulsoup4**
* **lxml** – (not directly imported but used by BeautifulSoup)
* **jupyter**

Additionally, the following modules from the Python standard library are used:

* **datetime** 
* **re** 
* **random** 
* **time** 
* **warnings** 
* **sys** 
* **os** 

## Methodology

The analysis is divided into seven main parts:

1. **Data Loading and Cleaning**
   * Loading HPI data and affordability ratios
   * Handling missing values and formatting dates
   * Filtering relevant regions for comparison

2. **Exploratory Data Analysis**
   * Visualising house price trends from 1995-2025 across UK regions
   * Analysing London property prices by type (detached, semi-detached, terraced, flats)
   * Creating heatmaps of yearly price growth rates

3. **Web Scraping Rightmove**
   * Automated scraping of London property listings using BeautifulSoup and requests libraries
   * Extracting property details from 624 active listings including prices, types, and locations
   * Analysing borough-level price variations with structured data processing

4. **Predictive Modelling**
   * Time series analysis of London house prices
   * Building a linear regression model for price forecasting
   * Predicting future price trends (5-year projection to 2030)

5. **COVID-19 Impact Analysis**
   * Examining price changes before, during, and after the pandemic (2019-2023)
   * Comparing regional recoveries with visualisations
   * Analysing changes in affordability ratios post-COVID

6. **Affordability Crisis Analysis**
   * Tracking London's price-to-earnings ratio changes from approximately 4 in 1997 to around 11 in 2024
   * Comparing London to England average affordability (40-55% gap since 2015)
   * Analysing first-time buyers vs. existing homeowners price disparities

7. **Property Type Analysis**
   * Comparing affordability across property types in London
   * Calculating specific affordability ratios for each property type
   * Analysing price trends by property type from 2000-2024

## Replicating the Analysis

To replicate the analysis on your local machine, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/jclkr7/uk-housing-analysis.git
   cd uk-housing-analysis
   ```

2. **(Optional) Set Up a Virtual Environment:**
   ```bash
   # On macOS/Linux:
   python -m venv env
   source env/bin/activate

   # On Windows:
   python -m venv env
   env\Scripts\activate
   ```

3. **Install the Required Packages:**
   ```bash
   pip install pandas numpy matplotlib seaborn requests scikit-learn beautifulsoup4 lxml statsmodels jupyter datetime warnings
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Then, open the file `eda.ipynb`.

5. **Execute the Notebook Cells Sequentially:**
   Running through the notebook will:
   * Import and clean the datasets
   * Perform exploratory data analysis
   * Generate visualisations
   * Conduct statistical analyses
   * Create predictive models
   * Produce figures that are saved to the `data/figures` directory

## Key Findings

### Historical Price Trends
1. London house prices have grown significantly faster than any other region in England over the past 25 years
2. The average London property price increased from approximately £84,000 in 1990 to over £550,000 by 2025, representing more than a 550% increase
3. Detached properties in London have seen the most dramatic price increases, reaching an average of £1,150,000, compared to semi-detached (£710,000), terraced (£630,000), and flats (£450,000)

### Affordability Crisis
1. The price-to-earnings ratio in London has more than doubled since 1997, from around 4.9 to over 11 in 2024
2. London's affordability ratio has consistently been 40-55% higher than the England average over the past decade
3. First-time buyers face particularly challenging conditions, with the price-to-earnings ratio for entry-level properties reaching historic highs

### Regional Disparities
1. The North-South divide in housing affordability has widened significantly since 2000
2. The North East maintains the most affordable housing market in England, with price-to-earnings ratios consistently below 6
3. The South East and East of England have followed London's trend of decreasing affordability, though at a less severe rate

### COVID-19 Impact
1. The COVID-19 pandemic initially caused market uncertainty in 2020, followed by significant price increases across all regions in 2021-2022
2. London experienced a temporary dip in prices during the early pandemic, contrary to the growth seen in more rural areas
3. Post-pandemic recovery has been uneven, with London showing slower growth compared to other regions

### Future Projections
1. The predictive model suggests London house prices will continue to increase, potentially reaching an average of £800,000 by 2030
2. The affordability crisis is likely to persist unless significant policy interventions are implemented
3. The gap between first-time buyers and existing homeowners is projected to widen further

### Property Market Segmentation
1. The Rightmove data analysis shows significant price variation across London boroughs, with central areas commanding premium prices (ranging from £32,000,000 in Merton to under £1,100,000 in Lambeth)
2. Property type remains a major determinant of price, with detached houses typically costing more than twice as much as flats (affordability ratio of 27.8x for detached homes vs 11.1x for flats)
3. The gap between first-time buyers and existing homeowners has widened to approximately 44% in 2024, with first-time buyers paying around £485,000 and existing homeowners paying £700,000

## Policy Implications

Based on the analysis, several policy implications emerge:

1. Without intervention, housing will continue to be unaffordable for average earners in London, exacerbating inequality
2. Regional development policies may help reduce the North-South affordability divide
3. Specific support for first-time buyers remains critical to prevent further widening of the wealth gap between homeowners and non-homeowners

## Submission Contents

- Complete source code in `eda.ipynb`
- Raw data files in the `data` directory
- Processed data files in the `data/processed` directory  
- Generated visualisations in the `data/figures` directory and RightMove visualisations in 'uk-housing-analysis' directory.
- Comprehensive documentation in this README
- Blog post in PDF format and as a link in `blog.txt`
- Full git history in the `.git` directory

## Contact Information

Any errors or require further clarification:

* **GitHub Issues:** https://github.com/jclkr7/uk-housing-analysis/issues
