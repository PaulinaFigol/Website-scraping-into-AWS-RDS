# Website scraping into AWS RDS

Objectives:
- create AWS RDS connection
- create a database named __postcodes__
- define and create a table with the following features:
          address VARCHAR(255), 
          propertyType VARCHAR(255),
          bedrooms INT(2), 
          bathrooms INT(2), 
          transactions_price VARCHAR(255), 
          transactions_date VARCHAR(255), 
          transactions_tenure VARCHAR(255), 
          lat VARCHAR(255), 
          lgt VARCHAR(255), 
          detailUrl VARCHAR(255), 
          transactions_date_dt DATE, 
          postcode VARCHAR(255)
- read csv with all 'AL' postcodes
- scrape RighMove properties sold during and after 2010 for each 'AL' postcode 
- append __postcodes__ table with the properties scraped from RightMove



__Reasoning for not using API:__
- limitation with the number of calls
- years needs to be extracted separately due to the aggregating method on Rightmove
  - if 2010 used as a maximum year the website will only include the most recent transactions truncating the oldest and loosing part of the data). This increases the number of calls that passes the daily API limit
          
