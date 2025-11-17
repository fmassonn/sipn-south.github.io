# Call for contributions

## Summer 2025-2026 sea ice prediction experiment

<p style="color: red;"> Submission deadline: Monday December 8th, 2025 </p>

### Overview and objectives

The Sea Ice Prediction Network South (SIPN South) is pleased to invite contributors to participate in the ninth coordinated sea-ice prediction experiment in the Southern Ocean. 

Over the past eight years, we have received more than 4000 forecasts from 29 unique contributors (institutions or individuals) across five continents. We warmly thank all contributors for their interests, efforts and feedbacks. An evaluation of the forecasts collected since 2017 is available in [Massonnet et al. (2023)](https://www.frontiersin.org/journals/marine-science/articles/10.3389/fmars.2023.1148899/full). All SIPN South contributors are automatically invited as co-authors on future papers.

Here, we outline the protocol for contributing to the summer 2025-2026 experiment. The protocol is the same as last year. All groups are invited to participate regardless of the approach they follow.

If the above schedule is too tight but a delayed contribution would still be possible, please do not hesitate to let us know and we will find a flexible solution that accommodates everyone.

### Diagnostics requested

Participants are invited to issue from one to five of the following diagnostics, ordered by descending priority. The submission process is described at the end of this page.
The diagnostics are:

**1. High priority**

<u>Diagnostic</u>: Antarctic (circumpolar) daily mean sea-ice area from December 1st 2025 to February 28th 2026 included (90 days).

<u>Format</u>: One text file with one row and 90 comma-separated values, each expressing daily sea-ice area for the 31 + 31 + 28 days of the December–February period.
Units must be 10⁶ km². Numbers must be rounded to four decimal digits, and trailing zeroes must be included.

<u>File name</u>: <`<group-name>_<forecast-id>_20251201-20260228_total-area.txt` where `<group-name>` is the name of the participating group (university, research center, institution) and `<forecast-id>` is a 3-digit identifier for the forecast (001, 002, ...).

<u>Remarks</u>: ensemble forecasts are welcome. Please keep one file per forecast and increment each time the `<forecast-id>` by one unit: `001` for the first forecast, `002` for the second, etc. If only one forecast is submitted, set `<forecast-id>` to `001`.

**2. Medium priority**

<u>Diagnostic</u>: February Antarctic daily mean sea-ice area per 10° longitude bin, from December 1st 2025 to February 28th 2026 included (90 days).

<u>Format</u>: One text file with 36 rows each displaying 90 comma-separated values following the same requirements as diagnostic 1.

Each row corresponds to a 10° longitude bin:

First row: 0° ≤ longitude < 10°

Second row: 10° ≤ longitude < 20°
...
36th row: 350° ≤ longitude < 360°


<u>File name</u>: `<group-name>_<forecast-id>_20251201-20260228_regional-area.txt`

<u>Remarks</u>: Same rules for ensemble forecast indexing as in diagnostic 1.


**3. Low priority**

<u>Diagnostic</u>: February Antarctic daily mean sea-ice concentration

<u>Format</u>: A NetCDF file with 90 timesteps (one per day from December 1st 2025 to February 28th 2026). Each timestep displays the spatial field of sea-ice concentration. The file format must follow CMIP6 conventions:
- Sea-ice concentration is defined as the fraction of the grid cell covered by sea ice, is named siconc, and is expressed in %.
- Longitude and latitude are reported under variables `longitude` and `latitude`.
- A land–sea mask is provided through the variable `sftof` (percentage of the grid cell covered by ocean, units %).
- Areas of grid cells are provided through the variable `areacello` (units m²).

<u>File name</u>: `<group-name>_<forecast-id>_20241201-20250228_concentration.nc`

<u>Remarks</u>: Same rules for ensemble forecast indexing as in diagnostic 1.

**4. Low priority**

<u>Diagnostic</u>: February Antarctic daily mean grid cell thickness (or equivalently: mean sea-ice volume per unit grid cell area, or actual sea-ice thickness × sea-ice concentration)

<u>Format</u>: A NetCDF file with 90 timesteps (one per day from December 1st 2025 to February 28th 2026). Each timestep displays the spatial field of mean grid cell thickness. The file format must follow CMIP6 conventions:
- Mean grid cell sea-ice thickness is calculated by dividing sea-ice volume by grid cell area, or multiplying actual sea-ice thickness by concentration.
- Following CMIP6 conventions, this variable is named `sivol` and has units of meters.
- Longitude and latitude are reported under the variables `longitude` and `latitude`.
- A land-sea mask is provided through the variable `sftof` (percentage of the grid cell covered by ocean, units %).
- Areas of grid cells are provided through the variable `areacello (units m²)`.

<u>File name</u>: `<group-name>_<forecast-id>_20251201-20251228_volume.nc`

<u>Remarks</u>: Same rules for ensemble forecast indexing as in diagnostic 1. 

**5. Low priority (long forecasts)**

<u>Diagnostic</u>:
Antarctic (circumpolar) monthly mean sea-ice area from forecasts initialized in 2024 (any date) and extended at least 6 months into 2025.

<u>Format</u>: One text file with one row and comma-separated monthly values. Units must be 10⁶ km². Numbers must be rounded to four decimal digits with trailing zeroes.

<u>File name</u>: `<group-name>_<forecast-id>_2025mm-2025MM_total-area-long-forecast.txt` where `<group-name>` is the name of the participating group, `<forecast-id>` is a 3-digit identifier (001, 002, ...), `mm` and `MM` are the first and last months of the forecasts, respectively.

<u>Remarks</u>: Same rules for ensemble forecast indexing as in diagnostic 1.


### Post-season forecast verification products

The forecasts will be assessed against two observational references:
- The Near-Real-Time DMSP SSMIS Daily Polar Gridded Sea-Ice Concentrations, Version 2 ([Data Set ID: NSIDC-0081](http://nsidc.org/data/nsidc-0081)).
- The OSI SAF SSMIS Sea-Ice Concentration Maps on 10 km Polar Stereographic Grid ([Data Set ID: OSI-401-d](https://osi-saf.eumetsat.int/products/osi-401-d)).
- 
Both data sets are publicly available. Sea ice areas will be computed directly from the sea ice concentration fields.

### Submission process

The submission of a forecast by a group is done in two steps. 

1.	First, the contributing group gathers the diagnostics (see “Diagnostics Requested” above) in an online archive of its choice. The archive must be accessible with a simple URL, so that the information can be retrieved simply. A Google Drive, a Dropbox archive, WeTransfer or a public FTP are all fine.
2.	Then, the groups fill [**this online form**](https://forms.gle/dq6eii8omJGA7uYj9) where they provide meta-data such as forecasting method, contact information but also the link where their data can be retrieved from. In case this information has not changed compared your submission last year, do not hesitate to indicate “see last year” in the fields.
Groups are invited to send an [e-mail to François Massonnet](mailto:francois.massonnet@uclouvain.be) upon completion of the submission process to ensure that the data and meta-data have been well received.

The deadline for submitting the online form (containing the link pointing towards the data) is the <p style="color: red;"> Monday December 8th, 2025 </p>.

### Timeline

- First processing of forecasts: 10-15th of December 2025.
- Post season report: 15 March 2026

### Open access statement
All forecast and verification data will be made publicly available, as for the previous exercises. [The SIPN South Github repository ](https://github.com/fmassonn/sipn-south-public)hosts all data collected up to now from the project.


### Interested in following SIPN South?
Please send an e-mail directly to [François Massonnet](mailto:francois.massonnet@uclouvain.be) to be added to the mailing list.

