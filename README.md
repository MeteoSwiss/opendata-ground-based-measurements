# Automatic weather stations <!-- - Measurement values -->
The stations of the SwissMetNet ground monitoring network measure wind, radiation, pressure, humidity, precipitation, sunshine and temperature every 10 minutes.

If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [granularity](). Various [update frequencies]() (every 10 minutes to once a year) are available. 

We offer both
- the [current measured values of the main parameters of all stations in a single data file](..), and
- the [measured values of all parameters in a single file per station](..).


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
