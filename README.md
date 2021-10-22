<h1>Analysis of Emergency Rental Assistance Program data set — 06/2021 to 10/2021</h1>

This repository contains data, analytic code, and findings on applications for the New York State Emergency Rental Assistance Program (ERAP) between 06/2021 and 10/2021, sourced via the New York State Office of Temporary and Disability Assistance. Please read that article, which contains important context and details, before proceeding.

<h2>Data</h2>
This analysis uses six spreadsheets.<br><br>
The spreadsheets come from the following sources:<P>
  
  <b>Name of source:</b>
<ul>
  <li><code>erap_data_full.xlsx</code>: Raw data of the Emergency Rental Assistance Program (ERAP)</li>
<li><code>Median_household_income.xlsx</code>: Raw data of Median Household Income by Zip Code, sourced via Data CC New York</li>
<li><code>race_data_1.xlsx</code>: Raw data on race, sourced from the Census Reporter which uses the latest available census and American Community Survey (ACS) data.</li>
<li><code>Language_data_1.xlsx</code>: Raw data on language spoken at home, sourced from the Census Reporter which uses the latest available census and American Community Survey (ACS) data.</li>
<li><code>population_total_acs2019_5yr_B01003_86000US10457.xlsx</code>: Raw data on population sourced from the Census.</li>
<li><code>Eviction_subset.xlsx</code>: Raw data of evictions executed in 2019 by Zip Code, sourced from Open Data.</li>
  </ul>
  
  This data was merged into one spreadsheet: <code>Erap_data_full</code>
  
  <h2>Methodology</h2>
  
  The notebook <a href=""><code>10-16 evictions dataset.ipynb</code></a> performs the following analyses:

  <h5>Part 1: Cleaning</h5>
  <ul>
<li>The dataset was initially cleaned using Google sheets, and income on median household income by zip code was merged with the dataset using v-lookup.
  </ul>
  
  <h5>Part 2: Merging</h5>
<ul>
  <li>Data on race and language spoken at home by ability to speak english were merged into the dataset using pandas (Jupyter Notebook for this merge is attached separately).</li>
  <li>Data on evictions executed in 2019 was filtered and sorted with a pivot table in excel and was merged with the dataset in Google Sheets using v-lookup. </li>
  </ul>
  
  <h5>Part 3: Analysis</h5>
<ul>
  <li>All data was analyzed using sort commands, average/median/max commands, and pivot tables in Google Sheets. Additional data analyses will be performed using pandas in a Jupyter Notebook, to be attached separately. </li>
  <li>Map of ERAP assistance applications by zip code was created via Datawrapper. </li>
  </ul>
  
  <h2>Outputs</h2>
  
  The notebooks output this spreadsheet which contains TKTK: <code>erap_data_final.xlsx</code>.
 
  <h2>Running the analysis yourself</h2>
You can run the analysis yourself. To do so, you'll need the following installed on your computer:
  
<ul>
  <li>Python 3</li>
  <li>The Python libraries specified in requirements.txt</li>
  </ul>
  
  <h2>Licensing</h2>
  
<p>All code in this repository is available under the Craig Newmark Graduate School of Journalism. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.</p>
  
  <h2>Feedback / Questions?</h2>
<p>Contact Anny Oberlink at anny.oberlink58@journalism.cuny.edu, Alexandra White alexandra.white86@journalism.cuny.edu or Audrey Carleton audrey.carleton34@journalism.cuny.edu.</p>

