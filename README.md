# Tree cencus in NY
**How does the tree population in New-York city between 2005 et 2015 ?**
>
The 2 data set were obtained from the Open Data New York website. The first one correspond to [the 2005 cencus](https://data.cityofnewyork.us/Environment/2005-Street-Tree-Census/29bw-z7pj) and the second one to [the 2015 cencus](https://data.cityofnewyork.us/Environment/2015-Street-Tree-Census-Tree-Data/uvpi-gqnh). With each data set a pdf file is provided caintaining a description of the differents columns. Each of the data set contain around 600k rows and one row is equal to a tree. They contain information on the trees such as their diamater, the species, their health or even their location.
>
The first step was to get familiar with the data and to clean it in Python. Several observations were made :
  - A few of the columns were not interesting for us and were removed
  - A few columns (different ones in both dataset) contained missing values (NaN). They were replaced by appropriate value depending on the colummns.
  - A certain number of values for the tree and stump diamater were too high to be realistic : 364 in 2005 et 1921 in 2015. A threshold of 50 inches was choosed and all the tree/stump with a diamater higher than 50 inches were removed from the dataset.
