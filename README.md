# uk-housing-analysis

# London’s Housing Affordability Crisis: A Data-Driven Analysis of the UK Property Market

**GitHub Repository:** https://github.com/jclkr7/uk-housing-analysis

**Blog Post** https://dataanalysisuk7.wordpress.com/2025/04/14/londons-housing-affordability-crisis-a-data-driven-analysis-of-the-uk-property-market/
(Total of 2,457 words)

## Project Overview
This project presents a comprehensive data-driven analysis of the UK housing market with a focus on London's affordability crisis compared to other regions. Using historical data from 1995-2025, the analysis reveals how London's housing market has evolved over three decades and examines the widening affordability gap that impacts millions of residents, particularly first-time buyers, providing valuable insights for policymakers, researchers, and potential homebuyers interested in understanding historical trends and future projections.

The project combines multiple data sources (UK House Price Index, ONS price-to-earnings ratios, Rightmove listings), diverse analytical approaches (historical trend analysis, web scraping, statistical modelling, etc.), and data visualisation techniques to create an evidence-based assessment of housing market dynamics with significant policy implications.

## Version Control

This project uses git for version control. All development history is tracked in the repository, allowing for transparent documentation of the analysis process and changes made over time. The complete commit history demonstrates the progression of the analysis from data collection and cleaning through to visualisation and interpretation of findings.

## Repository Structure

The repository is structured as follows:

```
uk-housing-analysis
│   eda.ipynb                           # Main Jupyter notebook with all analysis
│   rightmove_borough_prices.png        
│   rightmove_london_data.csv           
│   README.md                           # Current File
│   rightmove_property_type_prices.png  
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
    │       price_to_earnings_heatmap.png          
    │       year_over_year_growth_average.png      
    │       yearly_growth_heatmap_boldlabels.png
    │
    └───processed
            key_regions_hpi_data.csv    # Processed HPI data for key regions
            key_regions_ratio_data.csv  # Processed affordability ratio data
            london_hpi_data.csv         # Processed London-specific HPI data
```

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
* **Note on Web Scraping:** The scraping targeted the `/property-for-sale/find.html` path. According to Rightmove's `robots.txt` file (retrieved April 12, 2025, from [https://www.rightmove.co.uk/robots.txt]), this path was permitted for crawling by the general user agent (`User-agent: *`) at the time of data collection, as it lacked a specific Disallow rule.

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

2. **Install the Required Packages:**
   ```bash
   pip install pandas numpy matplotlib seaborn requests scikit-learn beautifulsoup4 lxml jupyter
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Then, open the file `eda.ipynb`.

4. **Execute the Notebook Cells Sequentially:**
   Running through the notebook will:
   * Import and clean the datasets
   * Perform exploratory data analysis
   * Generate visualisations
   * Conduct statistical analyses
   * Create predictive models
   * Produce figures that are saved to the `data/figures` and `uk-housing-analysis` folder  directory

## Submission Contents

- Complete source code in `eda.ipynb`
- Raw data files in the `data` directory
- Processed data files in the `data/processed` directory  
- Generated visualisations in the `data/figures` directory and RightMove visualisations in `uk-housing-analysis` folder directory.
- Comprehensive documentation in this README
- Blog post in PDF format and as a link in `blog.txt`
- Full git history in the `.git` directory

## Report Issues

* **GitHub Issues:** https://github.com/jclkr7/uk-housing-analysis/issues
