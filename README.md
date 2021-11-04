# Analysis of Emergency Rental Assistance Program data set — 06/2021 to 10/2021

This repository contains data, analytic code, and findings on applications for the New York State Emergency Rental Assistance Program (ERAP) between 06/2021 and 10/2021, sourced via the New York State Office of Temporary and Disability Assistance. Please read that article, which contains important context and details, before proceeding.

## Data
This analysis uses several datasets. The spreadsheets come from the following sources:

#### Sources
- `ERAP_Data_Zipcode_County.csv`: Summary data of the Emergency Rental Assistance Program (ERAP) by zip code and includes information around number of rental assistance applications through the month of September of 2021. This data was extracted from a PDF published by the city every month and  pared down to only include New York City-based zip codes. The original PDF is included in the data folder as `ERAP-Jurisdiction-Zip-Application-Counts-21-09-30.pdf`.
- `race-acs2019_5yr_B02001_86000US10457.csv`: Summary data on race, sourced from the [Census Reporter](https://censusreporter.org/) which uses the latest available American Community Survey (ACS) data.
- `Language_data_1.xlsx`: Summary data on languages spoken at home, sourced from the [Census Reporter](https://censusreporter.org/) which uses the latest available census and American Community Survey (ACS) data.
- `population_total_acs2019_5yr_B01003_86000US10457.xlsx`: Summary data on population sourced from the [Census Bureau](https://www.census.gov/data/developers/data-sets/acs-5year.html).
- `CCNY_Median Income.xlsx`: Summary data on median incomes for New York City by zip code.
- `Evictions_subset.csv`: Summary data of evictions executed in 2019 by Zip Code, sourced from [NYC Open Data](https://opendata.cityofnewyork.us/).


## Methodology

The notebook `10-16 evictions dataset.ipynb` performs the following analyses:

#### Part 1: Cleaning

The dataset was initially cleaned using Google sheets, and income on median household income by zip code was merged with the dataset using v-lookup.

#### Part 2: Merging

- Data on race and language spoken at home by ability to speak english were merged into the dataset using pandas. The notebook then output a file called `erap_full.csv`which was imported into another spreadsheet `erap_data_final.xlsx` file. There, in a sheet called `erap_data_full`, this data was further merged with income, population and eviction data using vlookup formulas in the columns `Population size`, `Household Income` and `2019 executed evictions`.

#### Part 3: Analysis

-  The data in the merged table was then analyzed using in the following ways:"
  - using the population count and number of rental arrears applications, we created  new columms called `Arrears applications per 100K people` and `Prospective Rent Applications per 100K people`.
  - we then sorted the sheet by highest rate of `Arrears applications per 100K people`.
- We then mapped the ERAP assistance applications by zip code was created via Datawrapper.


#### Outputs

The notebook and Excel sheet's analyses can be found in the spreadsheet titled `erap_data_final.xlsx` in the `output` folder in a sheet called `findings sheet`.

## Running the analysis yourself
You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in requirements.txt

## Licensing

All code in this repository is available under the Craig Newmark Graduate School of Journalism. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?
Contact Anny Oberlink at anny.oberlink58@journalism.cuny.edu, Alexandra White alexandra.white86@journalism.cuny.edu or Audrey Carleton audrey.carleton34@journalism.cuny.edu.
