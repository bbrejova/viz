---
title: Data files
---

This page contains data files used in the lectures and tutorials.

## Life expectancy

* [life_expectancy_years.csv](./life_expectancy_years.csv)
* The number of years a newborn would live if prevailing patterns of mortality at the time of its birth were to stay the same throughout its life.
* Based on FREE DATA FROM WORLD BANK VIA [GAPMINDER.ORG](https://www.gapminder.org/data/), CC-BY LICENSE (years 1900-2017) and [WORLD BANK](https://databank.worldbank.org/reports.aspx?source=2&series=SP.DYN.LE00.IN&country=#) directly (years 2018-2021)
* Downloaded on 2021-02-08 (gapminder) and 2024-02-17 (World bank)
* ISO3 codes from World bank, country names from Gapminder. Contains only countries listed in both databases.
* Removed 3 countries with missing values, as well as years before 1900.

## UNdata country population

* [Un_population.csv](./Un_population.csv)
* See https://data.un.org/
* Downloaded from 
https://data.un.org/_Docs/SYB/CSV/SYB65_1_202209_Population,%20Surface%20Area%20and%20Density.csv
* Provided free of charge by the United Nations https://data.un.org/Host.aspx?Content=UNdataUse


## Country indicators from World Bank

* [World_bank.csv](./World_bank.csv)
* Downloaded from [https://databank.worldbank.org/home](https://databank.worldbank.org/home) under CC BY 4.0 license.
* Country population, surface area in km squared, GDP per capita (in current US$), life expectancy at birth (years), fertility rate, total (births per woman); in years 2000, 2010, 2020.
* Downloaded on 2024-03-05
* Also country metadata, including ISO3 code, region and income group.

## Movies from Kaggle

* [Movies_small.csv](./Movies_small.csv), [Movies_genres_small.csv](./Movies_genres_small.csv)
* A table describing 2049 movies.
* The dataset was downloaded from [https://www.kaggle.com/rounakbanik/the-movies-dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset) and preprocessed, keeping only movies with at least 500 viewer votes.

## FSEV survey

* [fsev-responses.csv](./fsev-responses.csv)
* Responses from a survey among students of [FSEV UK](https://fses.uniba.sk/en/) and their friends in 2013, downloaded from [https://www.kaggle.com/miroslavsabo/young-people-survey](https://www.kaggle.com/miroslavsabo/young-people-survey)
* Description of the survey questions: [fsev-columns.txt](./fsev-columns.txt)

## Airports

* [airports.geojson](./airports.geojson) 
* The dataset of international airports of the world was [downloaded](https://datacatalog.worldbank.org/search/dataset/0038117/Global-Airports) from the World Bank under the CC-BY 4.0 license, and preprocessed. The number of seats is from unknown years, possibly not comparable between countries.
* Our preprocessed file is in Geojson format used for describing simple geographical features. It contains both location data and other attributes. 
* Each row of the table contains one airport, with its 3-letter code, name, country, 3-letter code of the country, the number of airplane seats per year and the location.

* [airport_pairs_svk.geojson](./airport_pairs_svk.geojson)
* International airline connections from Slovak airports (in an unknown year), also from World Bank, as above.
* Each connection is given by two airport codes, the number of airplane seats within a year, and geometry with a segment connecting the two airport locations.

## Country boundaries

* [country_boundaries.geojson](./country_boundaries.geojson)
* The dataset of countries from [Natural Earth](https://www.naturalearthdata.com/downloads/110m-cultural-vectors/110m-admin-0-countries/), in public domain.
* Our preprocessed file is in Geojson format containing selected columns from the original table.

## Piešťany weather

* [piestany-weather.csv](./piestany-weather.csv)
* Downloaded from https://www.ncdc.noaa.gov/cdo-web/

## Google trends

* [kapustnica-kapor.csv](./kapustnica-kapor.csv) and [lyze-vlek.csv](./lyze-vlek.csv)
* Downloaded from Google trends [kapustnice,kapor](https://trends.google.com/trends/explore?date=today%205-y&geo=SK&q=kapustnica,kapor&hl=en-GB) and [lyže,vlek](https://trends.google.com/trends/explore?date=all&geo=SK&q=ly%C5%BEe,vlek&hl=en-GB)
* Editted (simplified header, replaced "<1" with "0", removed start of 2023)

## Districts of Slovakia

* [districts.json](./districts.json)
* Downloaded from https://www.geoportal.sk/sk/zbgis_smd/na-stiahnutie/, CC-BY 4.0 GKÚ Bratislava

## Life expectancy in districts of Slovakia

* [districts_expectancy.csv](./districts_expectancy.csv)
* Life expectancy at brith for women in 2015-2019 in districts of Slovakia
* Downloaded from http://www.infostat.sk/vdc/sk/index.php?option=com_wrapper&view=wrapper&Itemid=54

