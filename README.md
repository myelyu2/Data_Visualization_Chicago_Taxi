# Data Visualization Chicago Taxi
🚕 Visualization of Taxi rides in Chicago using RStudio and ShinyApp. Using a NodeJS program designed to filter, process, and pre-generate CSV tables from a large dataset for visualization projects. This parser speeds up page load times and offers faster updates for visualization elements.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Data Conversion](#data-conversion)
- [Interesting Facts](#interesting-facts)

## Features
1. **Data Parsing & Filtering**: Efficiently parses large data sets and filters out necessary data objects.
2. **CSV Pre-Generation**: Pre-generates CSV tables for improved performance and memory usage.
3. **Matrix Data Format**: Saves all data in matrix format, ready for future CSV export.

## Installation

1. Ensure you have **NodeJS** installed in your system. If not, download and install it from [here](https://nodejs.org/en/download/).

2. Clone or download the source code from the repository:
   ```
   git clone https://github.com/nickparov/cs424_project3_ParserFilter
   ```

3. Download the original dataset file from the Chicago portal [here](https://data.cityofchicago.org/Transportation/Taxi-Trips-2019/h4cq-z3dy) and place the 7GB data file into the program's folder. Rename the file to `data.csv`.

4. Navigate to your program's folder and install all necessary dependencies using:
   ```
   npm install
   ```

## Usage

1. To start processing the data, run:
   ```
   node main.js
   ```
   The execution will take approximately 3-5 minutes, depending on your machine's specifications.

2. Upon successful execution, you'll find all necessary CSV files in the `csv` folder. Additionally, a `csv-HDMR_TO_FROM` folder will be generated, containing a smaller set of files specifically for the `hourDayMonthRidesToFrom` table used in the application.

## Data Conversion

### Miles to Kilometers
1. Open the CSV file `milageBinsTotalRides_table.csv` in Excel.
2. In a new column, use the function `=CONVERT(A2,"km","mi")`. Replace `A2` with the first cell containing mile data.
3. Drag the converted cell down to apply the conversion to the entire column.

### 24-hour Time to 12-hour Format
1. Open the CSV file `eachHourTotalRides_table.csv` in Excel.
2. Follow the provided steps to convert 24-hour time format to 12-hour.
3. Name the new columns as `hour_tw` and `ampm`.
4. Save the modified file or replace the old one if necessary.

## Interesting Facts

- A balanced distribution of people going out and returning to areas, with a roughly 50% average for rides to/from all Chicago community areas.
  
- Higher ride frequencies in areas like 'The North Side', 'The Loop', and 'New West Side', likely due to population density.

- A majority of taxi rides span distances of 0.4-0.6 miles, likely due to taxi pricing structures.

- The highest number of taxi rides recorded was in March, possibly due to factors like Spring break and favorable post-winter weather.

- Ride frequencies are higher on weekdays compared to weekends, with a peak during lunchtime at 1PM.
