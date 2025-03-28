# Western Europe Military Expenditure Analysis

A Google Colab notebook for processing, visualizing, and analyzing military expenditure data for 17 Western European countries from 1993 to 2023, using the SIPRI Military Expenditure dataset.

## Description

This Google Colab notebook provides a comprehensive analysis of military spending trends across Western European nations. The notebook processes the SIPRI Military Expenditure Excel file, extracts data for Western European countries, performs data quality checks, and generates various visualizations to identify patterns and trends in defense spending over time.

## Project Structure

```
western-europe-military-expenditure-analyzer/
├── README.md                                  				# Project documentation
├── LICENSE                                    				# MIT License file
├── west_europe_military_expenditure_analyzer.ipynb 			# Main Google Colab notebook
├── data/
│   ├── raw/                                   				# Directory for original SIPRI data files
│   │   └── SIPRI-Milex-data-1993-2024.xlsx    				# Original data file (to be uploaded)
│   └── processed/                             				# Directory for processed data files
│       └── SIPRI-Milex-data-1993-2024_western_europe_clean.csv 	# Processed data output
```

## Notebook Structure

The notebook is organized into sections:
1. **Setup & Imports**: Imports required libraries and sets up the environment
2. **Data Loading Functions**: Functions to upload and load the SIPRI Excel file
3. **Data Processing Functions**: Functions to extract and process Western European data
4. **Data Quality Check Functions**: Functions to validate data completeness and integrity
5. **Visualization Functions**: Functions for creating trend charts, bar charts, and heatmaps
6. **Additional Analysis Functions**: Functions for calculating metrics like CAGR and volatility
7. **Analysis Steps**: Sequential execution of the analysis pipeline
8. **Custom Analysis**: Examples of customized visualizations and analyses

## Features

- **Interactive File Upload**: Uses Google Colab's file upload functionality
- **Data Processing**: Extracts and processes military expenditure data for 17 Western European countries
- **Data Quality Assessment**: Identifies duplicates, missing values, and calculates data completeness
- **Interactive Visualizations**:
  - Line charts of military spending trends with historical event annotations (9/11, Financial Crisis, Crimea Crisis, COVID-19)
  - Bar charts showing spending rankings by country
  - Heatmap of year-over-year percentage changes
- **Metrics Calculation**: 
  - 10-year Compound Annual Growth Rate (CAGR)
  - 5-year average spending
  - Spending volatility (standard deviation of annual changes)
- **Data Export**: Downloads processed data as CSV directly through the Colab interface

## Countries Included

The analysis covers the following Western European countries:
- Austria
- Belgium
- Denmark
- Finland
- France
- Germany
- Greece
- Ireland
- Italy
- Luxembourg
- Netherlands
- Norway
- Portugal
- Spain
- Sweden
- Switzerland
- United Kingdom

## Requirements

- Google Colab account
- Internet connection for accessing Google Colab
- SIPRI Military Expenditure Excel file

All required Python libraries are automatically imported in the notebook:
- pandas
- numpy
- matplotlib
- seaborn
- warnings
- google.colab

## How to Use

1. **Open in Google Colab**:
   - Upload the `.ipynb` file to Google Drive
   - Open with Google Colab
   - Alternatively, use the "Open in Colab" button if hosted on GitHub

2. **Run the Notebook**:
   - Click "Runtime" > "Run all" to execute all cells, or
   - Run cells sequentially using Shift+Enter

3. **File Upload**:
   - When prompted, upload the SIPRI Military Expenditure Excel file
   - The notebook will process the data automatically

4. **View Results**:
   - Visualizations will appear directly in the notebook
   - Processed data can be downloaded as CSV

## Custom Analysis Examples

The notebook includes examples for customized analysis:

```python
# Compare specific countries
countries_to_compare = ["France", "Germany", "Italy"]
plot_spending_trends(df, selected_countries=countries_to_compare)

# Focus on a specific time period
plot_spending_trends(df, year_range=(2010, 2023))

# Analyze a specific year
plot_current_spending(df, year=2015)
```

## Analysis Process

The notebook performs analysis in the following sequence:

1. **Data Loading**: Upload the SIPRI Excel file
2. **Data Processing**: 
   - Extract data for Western European countries
   - Process and clean the data
3. **Data Quality Checks**: 
   - Check for duplicates, missing values, empty rows/columns
   - Calculate data completeness percentage
4. **Data Export**:
   - Save processed data as CSV
   - Download directly through Colab interface
5. **Additional Metrics Calculation**:
   - Calculate growth rates, averages, and volatility
6. **Visualizations**:
   - Create multiple visualizations to analyze spending patterns
   - Add contextual annotations for significant historical events

## Data Output

The notebook produces:
- A cleaned CSV file with processed Western European military expenditure data
- Console output with data quality statistics
- Interactive visualizations within the notebook
- Statistical metrics for comparative analysis

## Notes

- The notebook is specifically designed for Google Colab environment
- Data processing assumes a specific Excel sheet format ("Current US$")
- All monetary values are in millions of USD (not adjusted for inflation)
- The notebook includes error handling to manage various data format issues

## Data Source

This notebook is designed to work with the Stockholm International Peace Research Institute (SIPRI) Military Expenditure dataset, available at [SIPRI's website](https://www.sipri.org/databases/milex).

## License

[MIT License](LICENSE)

---

*For research and educational purposes only.*