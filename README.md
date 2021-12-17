# What Do Rich  *Ditch?* 
An attempt to answer if wealthier districts of Amsterdam produce more waste per capita / per household.

![alt text](https://vconsyst.com/storage/section/159/2dmWxgyZT9veY3O4M6qy.jpeg)

This project is a part of Ironhack Data Analytics Full Time Bootcamp course. 

## 1. Project Description

The Amsterdam City Council (*Gemeente Amsterdam*) has an immense directory of open-source datasets related to the city of Amsterdam. Two of these datasets are related to:
* Underground waste containers' pickups (ID of the container, amount of waste collected, date & time, location, type of waste, etc.)
  * 
* Each distericts' socio-economic data (population and number of households in each district, average personal / household income for each district)

By combining the two, it is possible to see the amount of waste produced per capita or per household in the function of average wealth.

## 2. Tools used

The main technologies used here are Python and Tableau Public. The raw data file has been imported and wrangled in Jupyter Lab notebook using Pandas, clean .csv files exported & imported & joined in Tableau for visualizations.

The Jupyter notebook includes the statistical hypothesis test based on the p-value of a one-sided test for a relation between the waste per capita/household and district's/personal level of income. Results vary depending on the approach.

## 3. Challenges identified

There have been three major challenges during this project:
* As with most raw data files, the waste pickups file is not free of issues. There has been a significant portion of data missing the attributes necessary for proper work, and given a time crunch, a decision has been made to remove them (approx. 25% of the data). 
   * It is theoretically possible to map-back some of the features (e.g. the district location) using the available geo-spatial data, but that would require some additional coding.
*  One of the Amsterdam districts (Amsterdam Centrum) is available in the dataset, but it has a particular feature - most of the actual waste pickups there do not go through the underground containers, but through a street pickups instead. 
   *  While the data has still been included in the project & visualized, an attempt has been made to exclude it during the hypothesis testing not to skew the results.
*  Combining two datasets: initially they have been joined on a row level using the district_id, but this led to a big duplication and redundancy of district data (citizens, household, income, etc) which was troublesome to work with in Tableau. 
   * The solution used was not merging the data on a row level in Python, but to create a relation between the two in Tableau directly.

## 4. How to use & install

The project is straightforward to install, use & modify:
* Fork & clone the entire repo on your hard-drive
* Download the main dataset from the Amsterdam City Council website (it is too large to fit in Github/LFS) and include it in the same folder as other files
   * https://api.data.amsterdam.nl/dcatd/datasets/j9-Ddad9JWYPrQ/purls/7
* Run the Jupyter notebook (.ipynb) in your preferred Python IDE
* Explore the Tableau visuals by visiting the public directory and/or use the provided Tableau .twbx files to play with the visualizations on your own
   * https://public.tableau.com/app/profile/arek.tarnawski/viz/WhatDoRichDitch/WhatDoRichDitch 

## 5. Copyright

While the data used & tools are free-to-use & open-source, I will appreciate if the below credits are mentioned if you find using my work & time devoted to this project useful, and you intend to share it in full/parts publicly:

* **Author:** Arek Tarnawski
* **LinkedIn:** https://www.linkedin.com/in/arek-tarnawski/
* **Github:** https://github.com/arektarnawski/

*Amsterdam, 2021*
