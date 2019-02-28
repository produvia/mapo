# Mapo

## About

Mapo AI is a virtual exploration assistant that manages your mineral exploration efforts. To learn more, check out the [Mapo Blog Post](https://blog.produvia.com/letter-to-the-mining-industry-298cf0a0c6a8) and [Mapo White Paper](https://docs.google.com/document/d/1Y5WQ_IpmxeAowbNVMdT7lOzStZruOqBy1_rQ0PUWCEk/view).

# Data

The `data` folder contains mineral occurence datasets for:

1. Canada > British Columbia
2. Canada > Alberta

## Canada > British Columbia

### 1. ARIS Mineral Assessment Report Index Dataset

`ariasdata.csv` and `arismetadata.csv`

- Number of data records: 35,898
- Date of last update: Unknown

### 2. MINFILE Mineral Occurrence Dataset

`MINFILE.csv`

- Number of records: 14,817
- Record last modified: 2018-11-27

To re-create `MINFILE.csv`, perform the following:

1. Go here: <http://apps.gov.bc.ca/pub/dwds/addProducts.do>
2. Search "MINFILE Mineral Occurrence Database"
3. Click `+` button to add database to order
4. Click "View Your Order" button
5. Slect "Geographic Long/Lat (dd)" under projection drop-down menu and "CSV" under format drop-down menu
6. Type your email address
7. Press "I accept the Terms and Conditions"
8. Press "Submit Order"
9. Receive email from <NRSApplications@gov.bc.ca> with the subject: "Your order XXXXXXX has been assembled"
10. Copy URL in the email body (i.e. <https://apps.gov.bc.ca/pub/dwds/initiateDownload.do?orderId=XXXXXXX>)
11. Paste URL into browser to download a ZIP file
12. Open ZIP file to extract contents
13. Open extracted folder
14. Open "MINFIL_MINERAL_FILE" folder
15. Use "MINFILE.csv" for data analysis

### 3. Mineral Resources Data System (MRDS) Dataset

`mrds.csv`

- Number of records: 244
- Record last modified: Unknown

To re-create `mrds.csv`, perform the following:

1. Go here: <https://mrdata.usgs.gov/mrds/geo-inventory.php>
2. Click the "North America" link
3. Click the "Canada" link
4. Select "CSV" under Format menu
5. Click "Download" button
6. Look for "British Columbia" rows under the "state" column

## Canada > Alberta

### 1. Metallic Mineral Occurrence Dataset

`Metallic_Mineral_Occurrence.csv`

- [Website](https://geology-ags-aer.opendata.arcgis.com/datasets/metallic-mineral-occurrence)
- Number of records: 385
- Record last modified: 2016-09-23

### 2. Mineral Resources Data System (MRDS) Dataset

`mrds.csv`

- Number of records: 24
- Record last modified: Unknown

To re-create `mrds.csv`, perform the following:

1. Go here: <https://mrdata.usgs.gov/mrds/geo-inventory.php>
2. Click the "North America" link
3. Click the "Canada" link
4. Select "CSV" under Format menu
5. Click "Download" button
6. Look for "Alberta" rows under the "state" column

# Run on Local Machine

1. Create environment using pipenv with python 3.6.*

    ```
    pipenv --python python3.6
    ```
2. Enter pipenv environment

    ```
    pipenv shell
    ```
3. Install packages (for development)

    ```
    pipenv install -d
    ```

# Perform Exploratory Data Analysis (EDA)

1. To explore the existing datasets, review the `eda` folder
2. To visualize mineral occurrence data on a map, look for: Latitude, Longitude, Depth, or Elevation values. Use the guide below to get started.

## British Columbia, Canada

`MINFILE.csv`

- Relevant columns: `DECIMAL_LATITUDE`, `DECIMAL_LONGITUDE`, `ELEVATION`, `COMMODITY_DESCRIPTION1`, `COMMODITY_DESCRIPTION2`, `COMMODITY_DESCRIPTION3`, `COMMODITY_DESCRIPTION4`, `COMMODITY_DESCRIPTION5`, `COMMODITY_DESCRIPTION6`, `COMMODITY_DESCRIPTION7`, `COMMODITY_DESCRIPTION8`
- Missing columns: year of discovery

`mrds.csv`

- Relevant columns: `latitude`, `longitude`, `commod1`, `commod2`, `commod3`, `disc_yr`
- Missing columns: depth or elevation of discovery

## Alberta, Canada

`Metallic_Mineral_Occurrence.csv`

- Relevant columns: `Long_NAD83`, `Lat_NAD83`, `Depth_m`, `Comm_1`, `Comm_2`, `Location`, `Ref_AGS`

`mrds.csv`

- Relevant columns: `latitude`, `longitude`, `commod1`, `commod2`, `commod3`, `disc_yr`
- Missing columns: depth or elevation of discovery