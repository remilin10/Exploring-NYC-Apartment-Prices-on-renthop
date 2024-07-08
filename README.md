# Exploring-NYC-Apartment-Prices-on-renthop

Overview
This project aims to scrape, clean, and analyze apartment rental prices in Manhattan, New York. The data is extracted from RentHop's website, processed, and analyzed to explore the relationship between apartment characteristics and their rental prices.

Table of Contents
Installation
Data Collection
Data Cleaning
Data Exploration
Data Pre-processing
Variable Transformation
Data Partitioning
LASSO Analysis
Results
Useage

# Installation
Clone the repository:
bash
Copy code
git clone <repository-url>
cd <repository-directory>
Install dependencies:
Copy code
pip install -r requirements.txt
Ensure you have chromedriver installed and correctly set up in your PATH.
# Data Collection
The script uses Selenium and BeautifulSoup to scrape apartment rental data from RentHop's Manhattan listings.
1.Setup:
URL: https://www.renthop.com/apartments-for-rent/manhattan-new-york-ny
Selenium WebDriver with ChromeDriver is used to navigate and scrape data.

2.Scraping Process:
The script navigates through multiple pages (defined by page_num) to collect data on location, price, apartment type, number of bathrooms, neighborhood, and district.

3.Saving Data:
Scraped data is saved into a CSV file named Apartment Info - New Data.csv.

# Data Cleaning
1.Load Data:
Load the CSV file into a pandas DataFrame.
Remove unnecessary columns and clean data (e.g., remove dollar signs and commas from price).

2.Initial Exploration:
Inspect unique values for categorical variables.
Handle missing values by dropping rows with missing data.

# Data Exploration
1.Variables Definition:
Categorical Variables: Apt Type, Neighborhood, District, Num of Bath
Numeric Variable: Price

2.Boxplots:
Visualize the distribution of rental prices across different categories (e.g., number of bathrooms, districts).

# Data Pre-processing
1.Missing Value Imputation:
Drop rows with missing values.

2.Variable Transformation:
Standardize numeric variables.
Convert categorical variables into dummy variables.

# Variable Transformation
1.Standardization:
Standardize the numeric variables for further analysis.

2.Dummy Coding:
Convert categorical variables into dummy variables and remove redundant ones.

# Data Partitioning
1.Train-Test Split:
Split the data into training and testing sets using an 80-20 split.

# LASSO Analysis
1.LASSO Regression:
Perform LASSO regression to identify important predictors.
Use cross-validation to find the optimal penalty level.

2.Model Evaluation:
Compare ASE (Average Squared Error) on training and test sets to evaluate model performance.

# Results
1.Coefficients:
Display the estimated coefficients from the final selected LASSO model.

2.ASE Comparison:
Compare ASE values between training and test sets to check for overfitting.


# Usage
1.Run the Script:
Ensure all dependencies are installed and chromedriver is set up.
Execute the script to start data collection, cleaning, and analysis.

2.Modify Parameters:
Adjust page_num to scrape more or fewer pages.
Modify file paths and URLs as necessary.
