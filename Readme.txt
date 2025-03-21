###############################################

This folder includes the code to plot the main figures in the paper "Interannual Variability of Tropical Cyclone Landfalls in the Eastern North Pacific: Environmental Drivers and Implications"

################################################

Figures 1, 2, 3 and 4 are done in Python and could be plotted using the Jupyter notebook named: "ENP_TC_Landfall_Figures.ipynb"

The Python environment employed by the authors utilizes the following versions of Python and its packages:
Python version: 3.10.6 (main, Oct 24 2022, 16:07:47) [GCC 11.2.0]
xarray version: 2023.8.0
pandas version: 1.4.4
geopandas version: 0.14.0
numpy version: 1.23.3
matplotlib version: 3.5.3
seaborn version: 0.12.2
cmocean version: 2.0

################################################

Original Data sources (IBTrACS and ERA5) are from:

Gahtan, J., Knapp, K. R., Schreck, C. J. I.m Diamon, H. J., Kossin, J. P., & Kruk, M. C. (2024). International Best Track Archive for Climate Stewardship (IBTrACS) project, version 4.01 EP supset [Dataset]. NOAA National Centers for Environmental Information. (Downloaded XCV format on 2025-02-20) doi: https://doi.org/10.25921/82ty-9e16

European Centre for Medium-Range Weather Forecasts (ECMWF). (2019). ERA5 reanalysis(monthly mean 0.25 degree latitude-longitude grid)(updated yearly) [Dataset]. Boulder CO: Research Data Archive at the National Center for Atmospheric Research, Computational and Information Systems Laboratory. doi: https://doi.org/10.5065/P8GT-0R61

The Post Processed data needed to plot the figures is the following:

############ Figure 1 ##########################

topography_data.nc: NetCDF file from ERA5 containing the topography of the basin (calculated using Geopotential). Coordinates longitude and latitude.

ep_filtered.nc: Processed IBTrACS for the Eastern North Pacific. Coordinate: index. Variables: SID (Storm ID), NAME, NATURE, ISO_TIME, LAT, LON, DIST2LAND, LANDFALL, USA_STATUS, USA_WIND, USA_PRES, USA_R34_NE, USA_R34_WE, USA_R34_NW, USA_R34_SW, STRONGEST_LANDFALL. The only new variable different from IBTrACS is the strongest landfall, a Boolean variable to describe the strongest landfall (when the value is 1) for storms that made multiple landfalls.
 
hlf_years.txt: list of high landfall years. The numbers are years after 1980; for example, 1 means 1981

llf_years.txt: list of low landfall years. The numbers are years after 1980; for example, 0 means 1980

monthly_landfalls.csv: Table with monthly landfalls for each year from 1980 to 2024.

monthly_genesis.csv: table with monthly genesis for each year from 1980 to 2024.


############ Figure 2 ##########################

central_america_states.geojson: Polygon data of the second-level administrative regions of Central America

mexico_states.json: Polygon data of the second-level administrative regions of Mexico. Including a column with the ranking based on the vulnerability index discussed in the main text.

muns_hlf_data.geojson: storm count of all second-level administrative regions affected by at least tropical storm intensity winds for the high landfall years. Obtained running the storm wind model described in the main text.

landfall_points_hlf.geojson: landfall location of all the storms during high landfall years.

muns_llf_data.geojson: storm count of all second-level administrative regions affected by at least tropical storm intensity winds for the low landfall years. Obtained running the storm wind model described in the main text.

landfall_points_llf.geojson: landfall location of all the storms during low landfall years.


############ Figure 3 ##########################

fig3a.csv: Table containing the value of the decomposition for June, August, September, and October. the DIFF column is the differences in landfalls for a given month between high and low landfall years.

fig3a_bserror.csv: Error for each of the terms of the decomposition obtained running a 1000 steps bootstrapping to the decomposition.

u_hlf.nc: NetCDF file containing the zonal winds during high landfall probability years in the Eastern North Pacific. The coordinates are time, latitude, and longitude.

v_hlf.nc: NetCDF file containing the meridional winds during high landfall probability years in the Eastern North Pacific. The coordinates are time, latitude, and longitude.


u_llf.nc: NetCDF file containing the zonal winds during low landfall probability years in the Eastern North Pacific. The coordinates are time, latitude, and longitude.


v_llf.nc: NetCDF file containing the meridional winds during low landfall probability years in the Eastern North Pacific. The coordinates are time, latitude, and longitude.


pprime_term.nc: NetCDF file containing the landfall probability anomaly term for June, August, September, and October. The coordinates are month, x (longitude), and y (latitude).

mean_lat_lon.csv: Table containing the mean genesis location (latitude, and longitude) for high and low landfall probability years.


############ Figure 4 ##########################

u_july_climo.nc: NetCDF file containing the climatological zonal winds during July for the Eastern North Pacific. The coordinates are latitude and longitude.

v_july_climo.nc: NetCDF file containing the climatological meridional winds during July for the Eastern North Pacific. The coordinates are latitude and longitude.

dns.txt: Climatological Dynamical Seasonality Index (DNS, see main text). The size of the array is 201 x 481 (latitude x longitude), spanning from 200W to 320W and -10S to 40N.

tp_hov_hlf.nc: NetCDF file containing the mean precipitation rate during high landfall years in the Monsoonal region (Green Box Figure 4a of main text). The coordinates are latitude and month.

tp_hov_llf.nc: NetCDF file containing the mean precipitation rate during low landfall years in the Monsoonal region (Green Box Figure 4a of main text). The coordinates are latitude and month.

fig4d_data.csv: Table containing the mean zonal winds for the Caribbean Low-Level Jet (black box) and the red box region of Figure 4a of main text.




 




