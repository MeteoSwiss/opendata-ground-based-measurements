# A. Ground-based Measurements
...

1. [Automatic weather stations](#1-automatic-weather-stations)
2. [Automatic precipitation stations](#2-automatic-precipitation-stations)
3. [Automatic boundary layer stations](#3-automatic-boundary-layer-stations)
4. [Manual precipitation stations](#4-manual-precipitation-stations)
5. [Totaliser precipitation stations](#5-totaliser-precipitation-stations)
6. [Pollen stations](#6-pollen-stations)

---

## 1. Automatic weather stations 
The stations of the SwissMetNet ground monitoring network measure wind, radiation, pressure, humidity, precipitation, sunshine and temperature every 10 minutes.

If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/ogd-general/tree/main#data-granularity). Various [update frequencies](https://github.com/MeteoSwiss/ogd-general/tree/main#data-structure-and-update-cycle) (every 10 minutes to once a year) are available. 

We offer both
- the [current measured values of the main parameters of all stations in a single data file](..), and
- the [measured values of all parameters in a single file per station](..).

See [time stamps and intervals](https://github.com/MeteoSwiss/ogd-general/tree/main#time-stamps-and-time-intervals) as well as [column separators, decimal dividers and missing values](https://github.com/MeteoSwiss/ogd-general/tree/main#column-separators-decimal-dividers-and-missing-values).

...

### Parameter metadata
...

### Codes
...

### Station metadata
...

## 2. Automatic precipitation stations
...

## 3. Automatic boundary layer stations
...

## 4. Manual precipitation stations
...

## 5. Totaliser precipitation stations
...

## 6. Pollen stations
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). It consists of 14 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies. 

Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is operational: for the first time in the world, instead of daily averages being available after a week, information is available in real time at an hourly resolution.

### Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `H`, `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of 0.6 MB per file.

See (example!) data files: [`pollen`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/swiss-pollen-monitoring-stations-pollen).

### Parameter metadata
See (example!) parameter metadata files of [data granularities](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-H.csv) and [`D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-D.csv).

<!-- ### Codes -->
<!-- ... -->

### Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv).

### Data visualisation
See e.g. MeteoSwiss' [POLLEN network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en&table=false&station=PLZ&chart=day).

---
---

### 2.3. Surface data
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

All MeteoSwiss surface stations have a name and an identfier consisting of three letters (e.g. `BER` for [Bern / Zollikofen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=BER&chart=hour) or `LUG` for [Lugano](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=LUG&chart=hour)). Data files use this station identifier in the file name throughout all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according metadata section.


---
---

#### 2.3.1. Automatic weather stations (`smn`, `smn-precip`, `smn-tower`)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (`smn`). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (`smn-precip`). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (`smn-tower`). The time series can begin before the introduction of automatic measurements in 1981; the three manually measured values per day are stored as individual 10-minute values ("term values").

| *Dataset title*                | Measurement data from automatic weather stations |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example files: [`smn`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn), [`smn-precip`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-precip), [`smn-tower`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-tower) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `T`, `H`, `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤5.3 MB |
| *Visualisation*                | [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv) |
| *Parameter metadata*           | see parameter files: [`smn-T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-T.csv), [`smn-H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-H.csv), [`smn-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-D.csv), [`smn-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-M.csv) and [`smn-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-Y.csv)
| *Additional remarks*           | One file per station. |
