###############################################
This repository include the code to plot the main figures in the paper "Interannual Variability of Tropical Cyclone Landfalls in the Eastern North Pacific: Environmental Drivers and Implications"
################################################

Figures 1, 3 and 4 are done in Python and could be plotted using the Jupyter notebook named: "ENP_TC_Landfall_Figures.ipynb"

Figure 2 was made in R and could be plotted using the Rstudio Rmd file named "Figure2_Rcode.Rmd"

##############################################
The final data to be plotted is included under the subfolder named "data_plots" which include the following:

#####  fig1  #####

"df_melted_data.csv" is a pandas data frame that includes the monthly mean genesis needed for the seaborn package for plotting the climatology line in Fig 1b.
"df_total_landfall_data.csv" is a pandas data frame that includes the monthly mean landfalls needed for the seaborn package for plotting the climatology line in Fig 1d.
"ep_filtered_data.nc" is a NetCDF array of the IBTracs used after the filter described in the main text (all genesis and landfalls are derived from this one).
"gen_monthly_data.txt" is a matrix that counts the number of genesis storm during the period of analysis, with dimensions (years,months).
"hlf_years.txt" has the list of high landfall years.
"hplf_years.txt" has the list of high landfall probability years.
"lf_yearly_data.txt" has the number of landfalls per year during the period of analysis.
"llf_years.txt" has the list of low landfall years.
"lplf_years.txt" has the list of low landfall probability years.
"monthly_landfalls_full_data.csv" is pandas data frame that include the monthly landfalls for high and low landfall years (derived from df_total_landfall_data)

#####  fig2  #####

"mexico_states.json" is the geographic file with information about Mexican states for plotting.
"central_america_states.geojson" is the geographic file with information of all central America states for plotting.
"landfall_points_hlf.geojson" has the latitude and longitude points of the landfall locations from IBTrACS (ep_filtered_data above) for high landfall years.
"landfall_points_llf.geojson" has the latitude and longitude points of the landfall locations from IBTrACS (ep_filtered_data above) for low landfall years.
"muns_hlf_data.geojson" is a geographic table with the count of storms per second-level administrative divisions after using the parametric wind model described in the main text for the high landfall years.
"muns_llf_data.geojson" is a geographic table with the count of storms per second-level administrative divisions after using the parametric wind model described in the main text for the low landfall years.

#####  fig3  #####

"decomposition_data.nc" is a NetCDF file after containing the box analysis (landfall probabilities anomalies, genesis anomalies, and residual term) described in the main text for the 4 months revised in the manuscript.
"gen_lats_hlf.npz" is a numpy file listing all the latitude genesis locations for the 4 months analyzed in the manuscript during high landfall years.
"gen_lats_llf.npz" is a numpy file listing all the latitude genesis locations for the 4 months analyzed in the manuscript during low landfall years.
"gen_lons_hlf.npz" is a numpy file listing all the longitude genesis locations for the 4 months analyzed in the manuscript during high landfall years.
"gen_lons_llf.npz" is a numpy file listing all the longitude genesis locations for the 4 months analyzed in the manuscript during low landfall years.
"pprime_term.npz" is a numpy file listing all the matrices of numpy 2d histrograms for the landfalls probabilities anomalies for the 4 months analyzed in the manuscript.
"U_hlf_data.nc" has the zonal component of the steering wind (as described in the main text) for the high landfall years.
"U_llf_data.nc" has the zonal component of the steering wind (as described in the main text) for the low landfall years.
"V_hlf_data.nc" has the meridional component of the steering wind (as described in the main text) for the high landfall years.
"V_llf_data.nc" has the meridional component of the steering wind (as described in the main text) for the low landfall years.
"x_meshgrid.txt" has the horizontal grid spacing for the 5x5 box analysis needed for plotting.
"y_meshgrid.txt" has the vertical grid spacing for the 5x5 box analysis needed for plotting.

#####  fig4  #####

"dns.npy" is a numpy array with dimensions (longitude,latitude) on a 0.25 x 0.25 degree resolution of the dns (dynamical seasonality index, see main text) for the entire globe.
"precip_hlf_data.nc" NetCDF array with precipitation data during high landfall years.
"precip_llf_data.nc" NetCDF array with precipitation data during low landfall years.
"u_box_data.nc" NetCDF array with the zonal component of the wind inside the box of high landfall probabilities anomalies (red region, see main text)
"u_box_hlf_data.nc" NetCDF array with the zonal component of the wind inside the box of high landfall probabilities anomalies (red region, see main text), only during high landfall years.
"u_box_llf_data.nc" NetCDF array with the zonal component of the wind inside the box of high landfall probabilities anomalies (red region, see main text), only during low landfall years.
"u_cllj_data.nc" NetCDF array with the zonal component of the wind inside the box of the Caribbean low level jet (CLLJ).
"u_cllj_hlf_data.nc" NetCDF array with the zonal component of the wind inside the box of CLLJ only during high landfall years.
"u_cllj_llf_data.nc" NetCDF array with the zonal component of the wind inside the box of CLLJ only during low landfall years.
"u_enp_data.nc" zonal wind at 850 and 250hPa, used for plotting fig 3a.
"v_enp_data.nc" meridional wind at 850 and 250hPa, used for plotting fig 3a.
"us_hlf_data.nc" NetCDF array with the zonal steering winds during the high landfall years for the hovmoller diagram.
"us_llf_data.nc" NetCDF array with the zonal steering winds during the low landfall years for the hovmoller diagram.
"vs_hlf_data.nc" NetCDF array with the meridional steering winds during the high landfall years for the Hovmoller diagram.
"vs_llf_data.nc" NetCDF array with the meridional steering winds during the low landfall years for the Hovmoller diagram.










 




