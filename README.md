[MeteoSwiss - Open Data](https://github.com/MeteoSwiss/opendata/blob/main/README.md) > [Understanding MeteoSwiss' Open Data products](https://github.com/MeteoSwiss/opendata/blob/main/README.md#understanding-meteoswiss-open-data-products) > A - Ground-based Measurements

# A - Ground-based Measurements
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

The following measurements (1-3; 5-7) and additional observations - manual recording of cloud cover (8) and vegetation development (9) - are available:

- A1 - [Automatic weather stations - Measured values](#a1---automatic-weather-stations---measured-values)
- A2 - [Automatic precipitation stations - Measured values](#a2---automatic-precipitation-stations---measured-values)
- A3 - [Automatic tower stations - Measured values](#a3---automatic-tower-stations---measured-values)
- A4 - [Automatic soil stations - Measured values](#a4---automatic-soil-stations---measured-values) *- not yet realised*
- A5 - [Manual precipitation stations - Measured values](#a5---manual-precipitation-stations---measured-values)
- A6 - [Totaliser precipitation stations - Measured values](#a6---totaliser-precipitation-stations---measured-values)
- A7 - [Pollen stations - Measured values](#a7---pollen-stations---measured-values)
- A8 - [Meteorological visual observations](#a8---meteorological-visual-observations)
- A9 - [Phenological observations](#a9---phenological-observations)

### General information
All MeteoSwiss surface stations have a name and an identfier consisting of three letters (e.g. `BER` for [Bern / Zollikofen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=BER&chart=hour) or `LUG` for [Lugano](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=LUG&chart=hour)). Data files use this station identifier (in lower case) in the file name throughout all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according 'station metadata' sections below.

> [!NOTE]
> If you require hourly, daily, monthly or annual values, we strongly recommend that you **download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#data-granularity)**. Various [update frequencies](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) (every 10 minutes to once a year) are available. 

---

## A1 - Automatic weather stations - Measured values
Around 160 stations of the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) SwissMetNet comprise a complete measurement programme. They deliver temperature, humidity, precipitation, wind, radiation, pressure and sunshine duration every ten minutes.

The network is supplemented by around 100 [automatic precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#2-automatic-precipitation-stations). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates 3 [automatic tower stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#3-automatic-tower-stations) at 150m to 230m above ground for boundary layer measurements.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 1.1. Data granularity, update frequency, format and volume
If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#data-granularity) `t`, `h`, `d`, `m`, `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

Time series can begin before the introduction of automatic measurements in the year 1981. Before 1981 at least three values per day were manually measured. They are stored as individual 10-minute values ([synoptic observations](https://community.wmo.int/en/observation-components-global-observing-system)).

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

See example data files for station `BAS` (set in lower case) for all granularities and update frequencies mentioned: [`ogd-smn_bas_(data granularity)_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn).

> [!NOTE]
> In addition we offer the [current measured values of the main parameters of all stations](..) *(URL to follow)* in a single data file, i.e. [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `t`. *The main parameters included are: ...*

### 1.2. Parameter metadata
See example parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`t`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-T.csv), [`h`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-H.csv), [`d`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-D.csv), [`m`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-M.csv) and [`y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-Y.csv).

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn_meta_parameters.csv`.

<!-- **Codes** -->
sremaxyv	1 	%	471 	Sonnenscheindauer; Verhältnis der Jahressumme zur maximal Möglichen
sremaxmv	1 	%	349 	Sonnenscheindauer; Verhältnis der Monatssumme zur maximal Möglichen
sremaxdv	1 	%	222 	Sonnenscheindauer; relativ zur absolut möglichen Tagessumme
<!-- ... -->

### 1.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn_meta_stations.csv`.

### 1.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en).

<br>

## A2 - Automatic precipitation stations - Measured values
As a meteorological parameter, precipitation exhibits a very high spatial variability and therefore requires a denser measurement network. In supplement to [1. Automatic weather stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#1-automatic-weather-stations) MeteoSwiss thus operates about 100 additional stations for the [automatic measurement of precipitation](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html).

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 2.1. Data granularity, update frequency, format and volume
If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#data-granularity) `t`, `h`, `d`, `m`, `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`).

Time series can begin before the introduction of automatic measurements in the year 1981. Before 1981 at least three values per day were manually measured. They are stored as individual 10-minute values ([synoptic observations](https://community.wmo.int/en/observation-components-global-observing-system)).

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

See example data files for station `AIR` (set in lower case) for all granularities and update frequencies mentioned: [`ogd-smn-precip_air_(data granularity)_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-precip).

### 2.2. Parameter metadata
For example parameter metadata files see [1.2. Parameter metadata](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#12-parameter-metadata) above.

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn-precip_meta_parameters.csv`.

<!-- *** Codes -->
<!-- ... -->

### 2.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn-precip_meta_stations.csv`.

### 2.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en).

<br>

## A3 - Automatic tower stations - Measured values
For boundary layer measurements MeteoSwis operates 3 automatic tower stations at 150m to 230m above ground. They deliver temperature, humidity, wind, radiation, pressure and sunshine duration every ten minutes.

### 3.1. Data granularity, update frequency, format and volume
If you require hourly, daily, monthly or annual values, we strongly recommend that you download the corresponding aggregated [data granularity](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#data-granularity) `t`, `h`, `d`, `m`, `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`),

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤5.3 MB per file.

See example data files for station `UEB` (set in lower case) for all granularities and update frequencies mentioned: [`ogd-smn-tower_ueb_(data granularity)_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-tower).

### 3.2. Parameter metadata
For example parameter metadata files see [1.2. Parameter metadata](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#12-parameter-metadata) above.

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-smn-tower_meta_parameters.csv`.

<!-- *** Codes -->
<!-- ... -->

### 3.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-smn-tower_meta_stations.csv`.

### 3.4. Data visualisation
*See ... .*

<br>

## A4 - Automatic soil stations - Measured values
*(not yet realised)*

<br>

## A5 - Manual precipitation stations - Measured values
In addition to its automatic precipitation measurements (see [1. Automatic weather stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#1-automatic-weather-stations), [2. Automatic precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#2-automatic-precipitation-stations) and [3. Automatic tower stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#3-automatic-tower-stations) above), MeteoSwiss operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html).

Measurements are taken once a day and transmitted to MeteoSwiss via SMS. The network comprises around 240 locations, about 190 stations measure rainfall and snow, and about 50 stations measure snow only. Due to their long-series measurements, they are of great climatological significance.

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

In mountainous areas that are difficult to access, the network is supplemented by around 60 totalisers which record the volume of precipitation for an entire year (see 5. [Totaliser precipitation stations](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#5-totaliser-precipitation-stations)).

### 5.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `d`, `m`, `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) daily (`recent`) or yearly (`historical`) for each station.

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤0.6 MB per file.

See example data files for station `PON` (set in lower case) for all granularities and update frequencies mentioned: [`ogd-nime_pon_(data granularity)_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-nime).

### 5.2. Parameter metadata
See example parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`d`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-D.csv), [`m`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-M.csv) and [`y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-Y.csv).

The productive version will provide a single parameter metadata file for all granularities; file name: `ogd-nime_meta_parameters.csv`.

<!-- **Codes** -->
<!-- ... -->

### 5.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-nime_meta_stations.csv`.

### 5.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false).

<br>

## A6 - Totaliser precipitation stations - Measured values
In supplement to [5. Manual precipitation stations – Measured values](https://github.com/MeteoSwiss/opendata-ground-based-measurements/blob/main/README.md#5-manual-precipitation-stations-measured-values) in mountainous areas that are difficult to access, MeteoSwiss operates around 60 totalisers which record the volume of precipitation for an entire year (see section "Totaliser monitoring network – annual readings" [here](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html).

> [!NOTE]
> For **climate analyses**, use the corresponding [homogeneous time series data](https://github.com/MeteoSwiss/opendata-climate-data/blob/main/README.md#d-climate-data) instead.

### 6.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) yearly (`historical`) for each station.

Data format of all files is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤0.6 MB per file.

See example data file for station `MGR` (set in lower case): [`ogd-tot_mgr_y_historical`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/manual-precipitation-stations-tot/tot_Y_MGR.csv).

### 6.2. Parameter metadata
See example parameter metadata file of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-tot-Y.csv).

The productive version will provide a parameter metadata file with the name: `ogd-tot_meta_parameters.csv`.

<!-- **Codes** -->
<!-- ... -->

### 6.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv).

The productive version will provide a station metadata file with the file name: `ogd-tot_meta_stations.csv`.

### 6.4. Data visualisation
See e.g. MeteoSwiss' [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false). 

<br>

## A7 - Pollen stations - Measured values
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). It consists of around 15 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies.  <!-- Daily average values are updated once a week and obtained from manual reference counts. -->

Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is operational: for the first time in the world, instead of daily averages being available after a week, airborne pollen concentrations (No/m³, number of grains per cubic metre of air) of Birch, Beech, Oak, Alder, Ash, Grasses and Hazel are available in real time at an hourly resolution.

### 7.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `h`, `d`, `m`, `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

> [!NOTE]
> The granularities `h` and `d` contain average pollen concentrations, while the granularities `m` and `y` contain pollen integrals.

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of 0.6 MB per file.

See example data files for station `PBS` (set in lower case) for granularities `h` and `d` and update frequencies `recent` and `historical`: [`ogd-pollen_pbs_(data granularity)_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/swiss-pollen-monitoring-stations-pollen).

### 7.2. Parameter metadata
See example parameter metadata files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`h`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-H.csv) and [`d`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-D.csv).

<!-- ### Codes -->
<!-- ... -->

### 7.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv).

### 7.4. Data visualisation
See e.g. MeteoSwiss' [POLLEN network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en&table=false&station=PLZ&chart=day).

<br>

## A8 - Meteorological visual observations
MeteoSwiss' data on current weather events is supplemented by [visual human observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html), which describe the atmospheric conditions around the observation sites in detail.

Meteorological observers make visual observations and take readings from measurement instruments between two and eight times per day every day of the year at around 20 locations in Switzerland. The following aspects are observed:
- Meteorological visibility
- Current weather: e.g. moderate rain showers, snowfall, fog with formation of hoarfrost
- Past weather: the main weather phenomena during the past 3, 6 or 12 hours, e.g. thunderstorms, drizzle, drifting snow
- Ground conditions: e.g. powder snow covering the entire ground surface; frozen; damp
- Clouds: extent of total cloud cover, type and shape of visible clouds, the altitude of the cloud base
- Mesurement of fresh and total snow depth

### 8.1. Data granularity, update frequency, format and volume
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `t` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) hourly (`now`), daily (`recent`) or yearly (`historical`) for each station.

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤0.04 MB per file.

See example data files for station `BAS` (set in lower case) for granularity `t` and update frequencies `now`, `recent` and `historical`: [`ogd-obs_bas_t_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/visual-observations-obs).

### 8.2. Parameter metadata
See example parameter metadata file of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`t`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-obs-T.csv).

<!-- ### Codes -->
<!-- ... -->

### 8.3. Station metadata
See example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-beobachtungen/ch.meteoschweiz.messnetz-beobachtungen_en.csv).

### 8.4. Data visualisation
See e.g. MeteoSwiss' [OBS network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-beobachtungen&lang=en&table=false).

<br>

## A9 - Phenological observations
The [Swiss Phenology Network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-phenology-network.html) consists of around 160 stations. Some 26 different plant species are observed in order to describe the vegetation development. On the basis of this information, it is possible to investigate the impact of climate change on the vegetation. The observations also serve to generate forecasting models for the start of flowering.

### 9.1. Data granularity, update frequency, format, volume and structure
There are files of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity) `y` and [update frequency](https://github.com/MeteoSwiss/opendata-download/blob/main/README.md#update-frequency) daily (`recent`) or yearly (`historical`) for each station.

Data format is [`CSV`](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#column-separators-decimal-dividers-and-missing-values) with an estimated volume of ≤7.1 MB per file.

Data structure conforms to the example data files for granularity `y` and update frequencies `recent` and `historical`: [`ogd-phenology_(station identifier)_y_(update frequency).csv`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/phenology).

| Variable name    | Description              | Datatype         | Note                                              |
| :---             | :---                     | :---             | :---                                              |
| *`param_id`*       | Parameter identification | `Number`         | see [Parameter metadata](#82-parameter-metadata)  |
| *`nat_abbr`*       | Station abbreviation     | `Text`           | see [Station metadata](#83-station-metadata)      |
| *`reference_year`* | Reference year           | `YYYY`           |                                                   |
| *`value`*          | Date of observation      | `YYYYMMDD`       |                                                   |
| *`doy`*            | Day of year              | `Number`         | `negative values`: Observation in the year preceding the reference year. <br> `values greater than 365`: Observation in the year following the reference year. <br> |

### 9.2. Parameter metadata
The available parameters are listed in the example parameter metadata file of [data granularity](https://github.com/MeteoSwiss/opendata-download?tab=readme-ov-file#data-granularity): [`y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-phenology-Y.csv).

| Variable name     | Description                                      | Datatype         | Example value                                   | Note                     |
| :---              | :---                                             | :---             | :---                                            | :---                     |
| *`param_id`*        | Parameter identification                         | `Number`         | `601`                                           |                          |
| *`param_shortname`* | Parameter shortname                              | `Integer`        | `maesh13d`                                      |                          |
| *`scientific name`* | Plant's scientific name + phenophase* in English | `String`         | `Aesculus hippocastanum - leaf unfolding (50%)` | *`phenophase`: An observable stage or phase in the annual life cycle of a plant that can be defined by a start and end point. <!-- Phenophases generally have a duration of a few days or weeks. Examples include the period over which newly emerging leaves are visible, or the period over which open flowers are present on a plant. --> |
| *`desc_english`*    | Plant's common name + phenophase* in English     | `String`         | `Horse chestnut - leaf unfolding (50%)`         |                          |
| *`desc_deutsch`*    | Plant's common name + phenophase* in German      | `String`         | `Rosskastanie - Blattentfaltung (50%)`          |                          |
| *`desc_italiano`*   | Plant's common name + phenophase* in Italian     | `String`         | `Ippocastano - spiegamento delle foglie (50%)`  |                          |
| *`desc_français`*   | Plant's common name + phenophase* in Italian     | `String`         | `Marronnier - déploiement des feuilles (50%)`   |                          |

<!-- #### Codes -->
<!-- ... -->

### 9.3. Station metadata
The available parameters are listed in the example [station metadata file](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-phaenologie/ch.meteoschweiz.messnetz-phaenologie_en.csv).

| Variable name     | Description                               | Datatype/Unit           | Example value       | Note                     |
| :---              | :---                                      | :---                    | :---                | :---                     |
| *`Station`*         | Station name                              | `Text`                  | `St. Gallen`        |                          |
| *`Abbr.`*           | Station abbreviation                      | `Text`                  | `STG`               |                          |
| *`WIGOS-ID`*        | WIGOS Station identifier (`WSI`)          | `4 Block Number`        | `0-20000-0-06681`   | [`WSI`](https://community.wmo.int/en/activity-areas/WIGOS/implementation-WIGOS/WIGOS-station-identifier) is used to register an observing station or platform in the [OSCAR/Surface database](https://space.oscar.wmo.int/). |
| *`Station type`*    | Station type                              | `Text`                  | `Phenology station` |                          |
| *`Data Owner`*      | Data Owner                                | `Text`                  | `MeteoSwiss`        |                          |
| *`Station height m a. sea level`* | Station height              | `Meter above sea level` | `711`               |                          |
| *`CoordinatesE`*    | [Swiss coordinates system LV95](https://www.swisstopo.admin.ch/en/the-swiss-coordinates-system), East      | `Number`          | `2746301`  |    |
| *`CoordinatesN`*    | [Swiss coordinates system LV95](https://www.swisstopo.admin.ch/en/the-swiss-coordinates-system), North     | `Number`          | `1255286`  |    |
| *`Latitude`*        | [Global WGS84 GPS coordinates](https://www.swisstopo.admin.ch/en/coordinates-conversion-navref), Latitude  | `Decimal degrees` | `47.432103`|    |
| *`Longitude`*       | [Global WGS84 GPS coordinates](https://www.swisstopo.admin.ch/en/coordinates-conversion-navref), Longitude | `Decimal degrees` | `9.378022` |    |
| *`Exposition`*      | *to be explained*                         | `Text`                  | `plain`             |                          |
| *`Canton`*          | Swiss canton abreviation                  | `Text`                  | `SG`                |                          |
| *`Measurements`*    | List of observed plants, scientific names | `Text`                  | `Aesculus hippocastanum, Fagus sylvatica, Acer pseudoplatanus, Sorbus aucuparia, Corylus avellana, Tilia platyphyllos, Sambucus nigra, Tilia cordata, Larix decidua, Picea abies, Robinia pseudoacacia, Betula pendula, Castanea sativa, Tussilago farfara, Anemone nemorosa, Dactylis glomerata, Taraxacum officinale, Cardamine pratensis, Leucanthemum vulgare, Colchicum autumnale, Prunus avium, Pyrus communis, Malus domestica, Hay` |    |
| *`Link`*            | More information about the station and the start date of observations (per plant) | `URL`                   | `https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-phaenologie&station=STG` |   |

### 9.4. Data visualisation
See e.g. MeteoSwiss' [PHENOLOGY network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-phaenologie&lang=en&table=false).

<br>
