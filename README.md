# Flats dataset cleaning
Cleaning data gathered with my otodom_scraper. I made the following changes and created the following variables:
*	Parsed numeric data out of salary 
* Shorten ID
* Got district names out of location attribute
*	Parsed numeric data out of price per m2 
* Parsed numeric data out of floor number
*	Parsed numeric data out of floor attribute
*	Parsed numeric data out of production year attribute
*	Parsed numeric data out of rent attribute
*	Parsed numeric data out of flat surface attribute
* Parsed categorical data out of building type
* Parsed categorical data out of finishi condition
* Put np.NaN into empty values
Then saved everything into csv file. Next I decided to get rows only with market == "pierwotny", means first owner

# Imputation
For this purpose I used MissForest algorithm for numerical data
```python
from missingpy import MissForest
```
And for categorical data, mode was used abd fillna() function
```python
df_imputed.district.fillna('Krzyki', inplace=True)
```
