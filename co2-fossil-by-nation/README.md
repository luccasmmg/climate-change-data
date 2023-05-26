Per Country CO2 Emissions from fossil-fuels annually since 1751 till 2014.

## Data
Data comes from the [Carbon Dioxide Information Analysis Center (CDIAC)][cdiac].
original csv: http://cdiac.ornl.gov/ftp/ndp030/CSV-FILES/nation.1751_2014.csv

<FlatUiTable url="https://raw.githubusercontent.com/luccasmmg/climate-change-data/main/co2-fossil-by-nation/data/fossil-fuel-co2-emissions-by-nation_csv.csv" />

## Changes over time in emissions by country(Top 10 Country)
<Vega spec={{
  "$schema": "https://vega.github.io/schema/vega-lite/v5.json",
  "data": {"url": "https://raw.githubusercontent.com/luccasmmg/climate-change-data/main/co2-fossil-by-nation/data/fossil-fuel-co2-emissions-by-nation_csv.csv"},
      "height": 500,
      "width": 500,
   "transform": [{ "filter": { "field": "Country", "oneOf": ["CHINA (MAINLAND)", "UNITED STATES OF AMERICA", "INDIA", "RUSSIAN FEDERATION", "JAPAN", "GERMANY", "ISLAMIC REPUBLIC OF IRAN", "SAUDI ARABIA", "REPUBLIC OF KOREA", "CANADA"]}}],
  "mark": "line",
  "encoding": {
    "x": {"field": "Year", "type": "temporal"},
    "y": {"field": "Total", "type": "quantitative"},
    "color": {"field": "Country", "type": "nominal"}
  }
}
} />


## Preparation
The data was prepared by the datahub.io project. You could find it here:  
https://datahub.io/core/co2-fossil-by-nation  

On the github (including the processing script):   
https://github.com/datasets/co2-emissions

[cdiac]: http://cdiac.esd.ornl.gov/

## Citation

Please cite as:

> Boden, T.A., G. Marland, and R.J. Andres. 2013. Global, Regional, and
> National Fossil-Fuel CO2 Emissions. Carbon Dioxide Information Analysis
> Center, Oak Ridge National Laboratory, U.S. Department of Energy, Oak Ridge,
> Tenn., U.S.A. doi 10.3334/CDIAC/00001_V2013

## License 
This Data Package is licensed by its maintainers under the Public Domain Dedication and License (PDDL).
