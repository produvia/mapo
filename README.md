# Mapo

## About

Mapo AI is a virtual exploration assistant that manages your mineral exploration efforts. To learn more, check out the [Mapo Blog Post](https://blog.produvia.com/letter-to-the-mining-industry-298cf0a0c6a8) and [Mapo White Paper](https://docs.google.com/document/d/1Y5WQ_IpmxeAowbNVMdT7lOzStZruOqBy1_rQ0PUWCEk/view).

# Data

The `data` folder contains two datasets:

# 1. ARIS Mineral Assessment Report Index Dataset

- Files: ariasdata.csv and ariasdata.csv
- Number of data records: 35,898
- Date of last update: Unknown
- Source of Data: Unknown

# 2. MINFILE Mineral Occurrence Dataset

## MINFILE.csv

- Number of records: 14,817
- Record last modified: 2018-11-27

## MINFILE_Minerals.csv

- Number of data records: 14,646
- Record last modified: 2017-12-24

## Manual Access via Web App

### Method 1

Method 1 creates `MINFILE.csv` (see above).

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

### Method 2

Method 2 creates `MINFILE_Minerals.csv` (see above).

1. Go here: <https://catalogue.data.gov.bc.ca/dataset/minfile-mineral-occurrence-database/resource/120d5ee6-bff5-4cbe-b106-e419c790c395>
2. Click "Access / Download" button
3. Use `minfile_mineral.csv` for data analysis

## Programmatic Access via API

1. Visit BC Data Catalogue API here: <https://catalogue.data.gov.bc.ca/dataset/bc-data-catalogue-api>
2. Create a script to access the "MINFILE Mineral Occurrence Database" via API

## Run it on local host
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