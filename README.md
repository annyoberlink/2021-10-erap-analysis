<h1>Analysis of Emergency Rental Assistance Program data set — 06/2021 to 10/2021</h1>

This repository contains data, analytic code, and findings on applications for the New York State Emergency Rental Assistance Program (ERAP) between 06/2021 and 10/2021, sourced via the New York State Office of Temporary and Disability Assistance. Please read that article, which contains important context and details, before proceeding.

<h1>Data</h1>
This analysis uses six spreadsheets.<p>
The spreadsheets come from the following sources:<P>
  
  <b>Name of source:</b>
<ul>
  <li>erap_data_full.xlsx: Raw data of the Emergency Rental Assistance Program (ERAP)</li>
<li>Median_household_income.xlsx: Raw data of Median Household Income by Zip Code, sourced via Data CC New York</li>
<li>race_data_1.xlsx: Raw data on race, sourced from the Census Reporter which uses the latest available census and American Community Survey (ACS) data.</li>
<li>Language_data_1.xlsx: Raw data on language spoken at home, sourced from the Census Reporter which uses the latest available census and American Community Survey (ACS) data.</li>
<li>population_total_acs2019_5yr_B01003_86000US10457.xlsx: Raw data on population sourced from the Census.</li>
<li>Eviction_subset.xlsx: Raw data of evictions executed in 2019 by Zip Code, sourced from Open Data.</li>
  </ul>
  
This data was merged into one spreadsheet:
Erap_data_full
Methodology
The notebook tktktktk.ipynb performs the following analyses:
Part 1: Cleaning
The dataset was initially cleaned using Google sheets, and income on median household income by zip code was merged with the dataset using v-lookup.
Part 2: Merging
Data on race and language spoken at home by ability to speak english were merged into the dataset using pandas (Jupyter Notebook for this merge is attached separately).
Data on evictions executed in 2019 was filtered and sorted with a pivot table in excel and was merged with the dataset in Google Sheets using v-lookup. 
Part 3: Analysis
All data was analyzed using sort commands, average/median/max commands, and pivot tables in Google Sheets. Additional data analyses will be performed using pandas in a Jupyter Notebook, to be attached separately. 
Map of ERAP assistance applications by zip code was created via Datawrapper.

Outputs
The notebooks output this spreadsheet which contains TKTK: output/tktktk.csv.
Running the analysis yourself
You can run the analysis yourself. To do so, you'll need the following installed on your computer:
Python 3
The Python libraries specified in requirements.txt
Licensing
All code in this repository is available under the Craig Newmark Graduate School of Journalism. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.
Feedback / Questions?
Contact Anny Oberlink at anny.oberlink58@journalism.cuny.edu, Alexandra White alexandra.white86@journalism.cuny.edu or Audrey Carleton audrey.carleton34@journalism.cuny.edu.

