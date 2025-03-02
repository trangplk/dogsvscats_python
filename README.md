# dogsvscats_python

### Background

It has always been a great debate over whether dog or cat is more popular as a pet. In this workbook, we're going to analyze dogs vs cats ownership in UK and find out the answer

## Finding summary

1. Dogs are more popular than cats in all regions across the UK (Dogs per household is always higher than Cats per household on town/county/region level)
2. Pet ownership is higher in urban area than metropolitan area, possibly due to more favourable environment settings. South and South West areas have higher pets per household than other areas.
3. Population has a positive but not very strong relationship with pet ownership. This suggest that there might be other factors impacting pets ownership: eg. disposable income, culture, ... 
4. Meanwhile, population density does not have any impact on pet ownership. This suggests that space constraints might not be a big problem for pet ownership in the UK and that other factors play a more impactful role.

### The data

There are 5 datasets used in the workbook, which contain the data as follows below.

#### The `population_per_postal_code.csv` data contains these columns:

| Column | Description |
|---------|----------------------------------------|  
| `postal_code` | An identifier for each postal code area|
| `estimated_cat_population` | The estimated cat population for the postal code area |  
| `estimated_dog_population` | The estimated cat population for the postal code area |


#### The `avg_per_household.csv` data contains these columns:

| Column | Description |
|---------|----------------------------------------|  
| `postal_code` | An identifier for each postal code area|
| `cats_per_household` | The average number of cats per household in the postal code area |  
| `dog_per_household` | The average number of dogs per household in the postal code area |

#### The `postal_code_areas.csv` data contains these columns:

| Column | Description |
|---------|----------------------------------------|  
| `postal_code` | An identifier for each postal code area|
| `town` | The town/towns which are contained in the postal code area |  
| `county` | The UK county that the postal code area is located in |
| `population` | The population of people in each postal code area |
| `num_households` | The number of households in each postal code area |
| `uk_region` | The region in the UK which the postal code is located in |

#### The `ukpostcodes.csv` data contains these columns:
| Column | Description |
|---------|----------------------------------------|  
| `postcode` | An identifier for each postal code area|
| `longitude` | Longitude of the postal code area |  
| `latitude` | Latitude of the postal code area |

#### The `area` data contains these columns:
| Column | Description |
|---------|----------------------------------------|  
| `Rank` | Alphabetical ranking of districts |
| `District` | Districts within the postal code area | 
| `Area (km²)` | Land area of the district in square kilometers |
| `Area (mi²)` | Land area of the district in square miles |
| `Type` | Classification of the district |
| `Ceremonial county` | Ceremonial county in the UK where the postal code is located |
| `Region` | UK region where the postal code is situated |

***Acknowledgments**: 
Data has been assembled and modified from these sources: [Animal and Plant Health Agency](https://www.data.gov.uk/search?filters%5Bpublisher%5D=Animal+and+Plant+Health+Agency), [Postcodes](
https://ideal-postcodes.co.uk/guides/postcode-areas), [Free Map Tools](https://www.freemaptools.com/download-uk-postcode-lat-lng.htm), [Wikipedia](https://en.wikipedia.org/wiki/List_of_English_districts_by_area).


### Techniques
This workbook imports packages for data manipulation, visualization, statistical analysis, machine learning, and geospatial plotting, including pandas, numpy, seaborn, matplotlib, folium, shapely, plotly, scipy, and scikit-learn.

The data cleaning techniques implemented involve type casting string columns to float, filtering out rows with missing or implausible values, imputing missing values using estimations, and conducting a final diagnostic analysis to assess the distribution and correlation of variables in the dataset.

Folium polygons were utilized to map and examine regional trends in pet ownership, while Plotly was employed to visualize the data through bar charts for comparative analysis.

Linear and polynomial regression models were used to analyze the relationship between population size and pet population.
