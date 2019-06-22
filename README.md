# US Baby Names Example Dashboard

This dashboard expands the US Census Bureau's [US Baby Names dataset](https://datacatalog.worldbank.org/dataset/health-nutrition-and-population-statistics) 
(StateNames.csv) into a story about immigration policy and demographic trends. 

## Original Data

The original census data is in the files (on Git LFS) [`NationalNames.csv`](NationalNames.csv) and 
[`StateNames.csv`](StateNames.csv).

The first/last name/racial group data that is used to calculate the first name racial proportions that are used to map 
the baby first name data from first name to racial group is in [`wiki_name_race.csv`]. It comes from the 
[`ethnicolr`](https://github.com/appeler/ethnicolr/blob/master/ethnicolr/data/wiki/wiki_name_race.csv) Pypi module on
Github.

## Derived Data

The output of this project is the [`first_name_racial_proportions.csv`](first_name_racial_proportions.csv) file, which
contains first names, racial groups and counts. This can be joined to the US Baby Names data to infer the overall racial
proportion for each year's births, enabling a time series chart of the percentage change in these values. This chart
tells an interesting story about immigration and demographics.

## Jupyter Notebook

The Jupyter Notebook [`First Name to Origin Workbook.ipynb`](First Name to Origin Workbook.ipynb) contains the code that
performs the calculations for racial proportions for each first name using `pandas`.
