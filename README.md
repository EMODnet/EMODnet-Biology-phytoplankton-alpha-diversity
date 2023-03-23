# Phytoplankton alpha diversity in the greater Baltic Sea area

## Introduction

Biodiversity loss due to human activities is an increasing threat for marine ecosystems and the services we obtain from them. As biodiversity is directly related to the resilience of ecosystems to temporary disturbance, biodiversity monitoring is a vital task for areas subjected to conservation goals. Environmental factors often control the community composition and biodiversity of marine microplankton, such as the pronounced salinity gradient in the Baltic Sea (e.g. Hu et al. 2016). Time series data of biodiversity can therefore provide an indication of changes in community composition due to environmental stressors, such as climate change or eutrophication.

As many biodiversity estimates are biased by sampling effort, caution must be taken when interpreting alpha diversity from microscopy phytoplankton counts. By rarefaction and evenness estimation, these biases can be reduced, but not ignored.

## Directory structure

```
EMODnet-Biology-phytoplankton-alpha-diversity/
├── analysis/
├── data/
│   ├── derived_data/
│   └── raw_data/
├── docs/
├── product/
│   ├── animations/
│   ├── maps/
│   │   ├── richness/
│   │   └── shannon/
│   └── plots/
└── scripts/
```

* **analysis** - Markdown or Jupyter notebooks
* **data** - Raw and derived data
* **docs** - Rendered reports
* **product** - Output product files
* **scripts** - Reusable code

## Data series

The raw data was accessed from GBIF, https://www.gbif.se/ipt/resource?r=smhi-phytoplankton-nat

```
https://www.gbif.se/ipt/archive.do?r=smhi-phytoplankton-nat&v=1.8
```

Alternatively, data can be accessed from EurOBIS, https://obis.org/dataset/1f15159f-6d35-4c3f-86e8-b3a89041ea33

```
http://geo.vliz.be/geoserver/Dataportal/ows?service=WFS&version=1.0.0&request=GetFeature&typeName=Dataportal:eurobis-obisenv_basic&&viewParams=where:datasetid=4659&maxFeatures=50&outputformat=csv
```

## Data product

We developed this product to assess how phytoplankton alpha diversity change over time in the greater Baltic sea area. Abundance data from the Swedish national phytoplankton monitoring are downloaded from [GBIF](https://www.gbif.org/) (data originating from [SHARKweb](https://sharkweb.smhi.se/)). Currently, only Swedish data are included as abundance is required for the calculations, and only between the time period between 2000-2021, as the sampling effort was more consistent during this time period (especially 2007-2021). Samples are rarified and Shannon diversity index and species richness (n taxa) are calculated for each monthly sample, and spatial data points are clustered together. Rarified monthly gamma diversity values are also calculated for the entire region, yet these values are highly biased by sampling effort (e.g. as there are less samples from the Gulf of Bothnia in wintertime). Maps with monthly alpha diversity values are produced using [EMODnetBiologyMaps](https://github.com/EMODnet/EMODnetBiologyMaps) R package (Fernández Bejarano & Schepers, 2020), and animated over time. Alpha diversity data are exported as NetCDF following Fernández-Bejarano (2022). 

https://user-images.githubusercontent.com/88311128/224287257-ad5b5979-eb90-4c99-9e6f-98396bad1fb7.mp4

Preview of Shannon diversity index between 2000-2021.

## More information:

### References

Fernández-Bejarano, S (2022). Create a EMODnet-Biology data product as NetCDF. Consulted online at https://github.com/EMODnet/EMODnet-Biology-products-erddap-demo on 2023-03-03.

Fernández Bejarano S, Schepers L (2020). _EMODnetBiologyMaps: Creates ggplot maps with the style of EMODnet_. R package version 0.0.1.0. Integrated data products
created under the European Marine Observation Data Network (EMODnet) Biology project (EASME/EMFF/2017/1.3.1.2/02/SI2.789013), funded by the by the European Union under
Regulation (EU) No 508/2014 of the European Parliament and of the Council of 15 May 2014 on the European Maritime and Fisheries Fund, 
https://github.com/EMODnet/EMODnetBiologyMaps.

Hu YO, Karlson B, Charvet S, Andersson AF. Diversity of Pico- to Mesoplankton along the 2000 km Salinity Gradient of the Baltic Sea. Front Microbiol. 2016 May 12;7:679. doi: 10.3389/fmicb.2016.00679.

### Code and methodology

The code, written in R, is distributed through GitHub:

[Link to repository](/../..)

### Citation and download link

This product should be cited as:

Torstensson A, Sundqvist L, Lindh M (2023) Phytoplankton alpha diversity in the greater Baltic Sea area. Integrated data products created under the European Marine Observation  Data Network (EMODnet) Biology project Phase IV (EMFF/2019/1.3.1.9/Lot  6/SI2.837974), funded by the by the European Union under Regulation (EU) No 508/2014 of the European Parliament and of the Council of 15 May 2014 on the European Maritime and Fisheries Fund.

Available to download in:

[Integrated Marine Information System (IMIS)](https://www.vliz.be/imis?dasid=8221)

and as zip:

[Link to zip](/../../archive/refs/heads/main.zip)

### Authors

Anders Torstensson, Lisa Sundqvist, Markus Lindh
