[MeteoSwiss - Open Data](https://github.com/MeteoSwiss/opendata/blob/main/README.md) > [Understanding MeteoSwiss' Open Data products](https://github.com/MeteoSwiss/opendata/blob/main/README.md#understanding-meteoswiss-open-data-products) > A. Ground-based Measurements

# A. Ground-based Measurements
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

The following measurements (1-6) and additional observations - manual recording of cloud cover (7) and vegetation development (8) - are available:

1. [Automatic weather stations](#1-automatic-weather-stations) :yellow_circle: *in review by surface data team*
2. [Automatic precipitation stations](#2-automatic-precipitation-stations) :yellow_circle: *in review by surface data team*
3. [Automatic tower stations](#3-automatic-tower-stations) :yellow_circle: *in review by surface data team*
4. [Manual precipitation stations](#4-manual-precipitation-stations) :yellow_circle: *in review by surface data team*
5. [Totaliser precipitation stations](#5-totaliser-precipitation-stations) :yellow_circle: *in review by surface data team*
6. [Pollen stations](#6-pollen-stations) :yellow_circle: *in review by surface data team*
7. [Meteorological visual observations](#7-meteorological-visual-observations)
8. [Phenological observations](#8-phenological-observations)

### General information
All MeteoSwiss surface stations have a name and an identfier consisting of three letters (e.g. `BER` for [Bern / Zollikofen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=BER&chart=hour) or `LUG` for [Lugano](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=LUG&chart=hour)). Data files use this station identifier in the file name throughout all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according 'station metadata' sections below.

If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/ogd-general/tree/main#data-granularity). Various [update frequencies](https://github.com/MeteoSwiss/ogd-general/tree/main#data-structure-and-update-cycle) (every 10 minutes to once a year) are available. 

---

## 1. Automatic weather stations
Around 160 stations of the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) SwissMetNet comprise a complete measurement programme. They deliver temperature, humidity, precipitation, wind, radiation, pressure and sunshine duration every ten minutes.

The network is supplemented by around 100 [automatic precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#2-automatic-precipitation-stations). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates 3 [automatic tower stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#3-automatic-tower-stations) at 150m to 230m above ground for boundary layer measurements.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 1.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `T`, `H`, `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

Time series can begin before the introduction of automatic measurements in the year 1981; the three manually measured values per day are stored as individual 10-minute values (synoptic observations).

See (example!) data files for station `BAS` for all granularities and update frequencies mentioned: [`ogd-smn_BAS_(granularity code)_(update frequency code)`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn).

In addition we offer the [current measured values of the main parameters of all stations](..) in a single data file, i.e. [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `T`. *The main parameters included are: ...*

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

### 1.2. Parameter metadata
See (example!) parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-T.csv), [`H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-H.csv), [`D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-D.csv), [`M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-M.csv) and [`Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-Y.csv).

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn_meta_parameters.csv`.

<!-- **Codes** -->
<!-- ... -->

### 1.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn_meta_stations.csv`.

### 1.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en).

<br>

## 2. Automatic precipitation stations
As a meteorological parameter, precipitation exhibits a very high spatial variability and requires therefore a denser measurement network. In supplement to [1. Automatic weather stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#1-automatic-weather-stations) MeteoSwiss thus operates about 100 additional stations for the [automatic measurement of precipitation](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html).

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 2.1. Data granularity, update frequency, format and volume
If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/ogd-general/tree/main#data-granularity) `T`, `H`, `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`).

Time series can begin before the introduction of automatic measurements in the year 1981; the three manually measured values per day are stored as individual 10-minute values ("term values").

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

See (example!) data files for station `AIR` for all granularities and update frequencies mentioned: [`ogd-smn-precip_AIR_(granularity code)_(update frequency code)`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-precip).

### 2.2. Parameter metadata
For (example!) parameter metadata files see [1.2. Parameter metadata](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#12-parameter-metadata) above.

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn-precip_meta_parameters.csv`.

<!-- *** Codes -->
<!-- ... -->

### 2.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn-precip_meta_stations.csv`.

### 2.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en).

<br>

## 3. Automatic tower stations
For boundary layer measurements MeteoSwis operates 3 automatic tower stations at 150m to 230m above ground. They deliver data every ten minutes.

### 3.1. Data granularity, update frequency, format and volume
If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/ogd-general/tree/main#data-granularity) `T`, `H`, `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`),

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

See (example!) data files for station `UEB` for all granularities and update frequencies mentioned: [`ogd-smn-tower_UEB_(granularity code)_(update frequency code)`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-tower).

### 3.2. Parameter metadata
For (example!) parameter metadata files see [1.2. Parameter metadata](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#12-parameter-metadata) above.

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn-tower_meta_parameters.csv`.

<!-- *** Codes -->
<!-- ... -->

### 3.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn-tower_meta_stations.csv`.

### 3.4. Data visualisation
*See ... .*

<br>

## 4. Manual precipitation stations
In addition to its automatic precipitation measurements (see [1. Automatic weather stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#1-automatic-weather-stations), [2. Automatic precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#2-automatic-precipitation-stations) and [3. Automatic tower stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#3-automatic-tower-stations) above), MeteoSwiss operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html).

Measurements are taken once a day and transmitted to MeteoSwiss via SMS. The network comprises 243 locations, 190 stations measure rainfall and snow, and 53 stations measure snow only. Due to their long-series measurements, they are of great climatological significance.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

In mountainous areas that are difficult to access, the network is supplemented by around 57 totalisers which record the volume of precipitation for an entire year (see 5. [Totaliser precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#5-totaliser-precipitation-stations)).

### 4.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) daily (`recent`) or yearly (`historical`) for each station.

See (example!) data files for station `PON` for all granularities and update frequencies mentioned: [`ogd-nime_PON_(granularity code)_(update frequency code)`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-nime).

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤0.6 MB per file.

### 4.2. Parameter metadata
See (example!) parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-D.csv), [`M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-M.csv) and [`Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-Y.csv).

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-nime_meta_parameters.csv`.

<!-- **Codes** -->
<!-- ... -->

### 4.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-nime_meta_stations.csv`.

### 4.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false).

<br>

## 5. Totaliser precipitation stations
In supplement to [4. Manual precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#4-manual-precipitation-stations) in mountainous areas that are difficult to access, MeteoSwiss operates around 57 totalisers which record the volume of precipitation for an entire year.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 5.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) yearly (`historical`) for each station.

See (example!) data file for station `MGR`: [`ogd-tot_MGR_(granularity code)_(update frequency code)`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/manual-precipitation-stations-tot/tot_Y_MGR.csv).

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤0.6 MB per file.

### 5.2. Parameter metadata
See (example!) parameter metadata file of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-tot-Y.csv).

The productive version will provide a parameter metadata file with the name: `ogd-tot_meta_parameters.csv`.

<!-- **Codes** -->
<!-- ... -->

### 5.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-tot_meta_stations.csv`.

### 5.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false). 

<br>

## 6. Pollen stations
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). It consists of 14 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies. 

Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is operational: for the first time in the world, instead of daily averages being available after a week, information is available in real time at an hourly resolution.

*The networks measure ...*

### 6.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `H`, `D`, `M`, `Y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of 0.6 MB per file.

See (example!) data files: [`pollen`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/swiss-pollen-monitoring-stations-pollen).

### 6.2. Parameter metadata
See (example!) parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-H.csv) and [`D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-D.csv).

<!-- ### Codes -->
<!-- ... -->

### 6.3. Station metadata
See (example!) [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv).

### 6.4. Data visualisation
See e.g. MeteoSwiss' [POLLEN network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en&table=false&station=PLZ&chart=day).

## 7. Meteorological visual observations
... 

<br>

## 8. Phenological observations
... 

<brt>
