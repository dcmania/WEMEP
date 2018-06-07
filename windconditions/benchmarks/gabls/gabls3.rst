GABLS3 Diurnal Cycle in Flat Terrain Leading to a Nocturnal Low-Level Jet
=========================================================================
`Javier Sanz Rodrigo, CENER <mailto:jsrodrigo@cener.com>`_

June 2017

Status
~~~~~~~~~~
The GABLS3 benchmark carried out jointly in the NEWA, Wakebench and MesoWake projects finished in June 2017. You can find the results and data open-access in the following links:

* Observational data: http://projects.knmi.nl/gabls/evaluation.html  
* Simulation data: http://doi.org/10.23728/b2share.f5d5a492d8aa4b7998b70abd68f5eae4
* Evaluation scripts and docker image: https://github.com/windbench/gabls3
* Journal paper: Sanz Rodrigo J, Allaerts D, Avila M, Barcons J, Cavar D, Chávez Arroyo R, Churchfield M, Kosović B, Lundquist JK, Meyers J, Muñoz Esparza D, Palma JMLM, Tomaszewski JM, Troldborg N, van der Laan MP, Veiga Rodrigues C (2017) Results of the GABLS3 diurnal cycle benchmark for wind energy applications. Journal of Physics: Conference Series, 854: 012037, http://iopscience.iop.org/article/10.1088/1742-6596/854/1/012037

Additionaly, you can also find individual evaluation results and data from CFDWind1D:

* Simulation data: http://doi.org/10.23728/b2share.22e419b663cb4ffca8107391b6716c1b
* Evaluation scripts: https://doi.org/10.5281/zenodo.834355 ; https://github.com/jsrodrigo/GABLS3-CFDWindSCM
* Journal paper: Sanz Rodrigo J, Churchfield M, Kosović B (2017) A methodology for the design and testing of atmospheric boundary layer models for wind energy applications. Wind Energ. Sci. 2: 1-20, doi:10.5194/wes-2-1-2017

Notebooks
~~~~~~~~~~~~~~~~~~~~
.. toctree::
   :glob:
   :maxdepth: 1

   notebooks/GABLS3DiurnalCycleBenchmarkForWindEnergy_2017.ipynb
   notebooks/GABLS3_CFDWind1D.ipynb

Scope
~~~~~~~~~~~~~~~~~~~~
The GABLS3 case has been selected in the NEWA project as a baseline exercise for the design of mesoscale-to-microscale methodologies for wind resource assessment. The case is suitable for the development of microscale wind farm models that incorporate realistic forcing, derived from a mesoscale model, along a typical diurnal case that leads to the development of a nocturnal low-level jet. Challenges of this case include: incorporating time- and height-dependent mesoscale forcing in microscale models, turbulence modeling at varying atmospheric stability conditions, defining suitable surface boundary conditions for momentum and heat and characterization of the wind profile in (non-logarithmic) LLJ conditions.  

Data Accessibility
~~~~~~~~~~~~~~~~~~~~
Data is provided open-access for registered participants. Observational data is available at the GABLS3-SCM `KNMI <http://projects.knmi.nl/gabls/>`__ website.

Objectives
~~~~~~~~~~~~~~~~~~~~
Wind-energy specific objectives of the benchmark include:

* Demonstrate the capability of wind energy ABL models to incorporate realistic mesoscale forcing
* Implement surface boundary conditions suitable for wind assessment studies using mesoscale simulation data and/or observations (typical of wind energy campaigns)
* Develop suitable model calibration strategies for wind energy applications or, in other words, how to best use available measurements (typical of wind energy campaigns) to correct meso-micro predictions
* Define suitable metrics for validation of ABL models based on wind energy quantities of interest

By "typical wind energy campaigns" we would like to encourage modellers to prioritize observations that are common place in wind resource assessment campaigns (80 masts with velocity and temperature measurements, lidar profilers measuring up to 400 m). 

Site Description
~~~~~~~~~~~~~~~~~~~~~~~
The GABLS3 set-up is described in Bosveld et al. [8]. The case analyzes the period from 12:00 UTC 1 July to 12:00 UTC 2 July 2006, at the KNMI-Cabauw Experimental Site for Atmospheric Research (`CESAR <http://www.cesar-observatory.nl/>`_), located in the Netherlands (51.971ºN, 4.927ºE), with a distance of 50 km to the North Sea at the WNW direction [12]. The elevation of the site is approximately -0.7 m, surrounded by relatively flat terrain characterized by grassland, fields and some scattered tree lines and villages (Figure 1). The mesoscale roughness length for the sector of interest (60º - 120º) is 15 cm.

.. image:: _static/Cabauw_landuse_30km.jpg
	:scale: 35%
	:align: center

Figure 1: Land-use map of a 30x30 km area around the Cabauw site (figure from `KNMI <http://projects.knmi.nl/hydra/index.html>`_'s HYDRA project website)

Measurement Campaign and Case Selection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The CESAR measurements are carried out at a 200-m tower, free of obstacles up to a few hundred meters in all directions. The measurements include 10-min averaged vertical profiles of wind speed, wind direction, temperature and humidity at heights 10, 20, 40, 80, 140 and 200 m, as well as surface radiation and energy budgets. Turbulence fluxes are also monitored at four heights: 3, 60, 100 and 180 m. A RASS profiler measures wind speed, wind direction and virtual temperature above 200 m.

The selection criteria for GABLS3 consisted on the following filters applied to a database of 6 years (2001 - 2006): stationary synoptic conditions, clear skies (net longwave cooling > 30 W m-2 at night), no fog, moderate geostrophic winds (5 to 19 m s-1, with less than 3 m s-1 variation at night) and small thermal advective tendencies. Out of the 9 diurnal cycles resulting from this filtering process, the one that seemed more suitable was finally selected: 12:00 UTC 1 July to 12:00 UTC 2 July 2006.

More information about the case background and set-up can be found in the official `GABLS3 <http://projects.knmi.nl/gabls/index.html>`_ website

Input data 
~~~~~~~~~~~~~~~~~~~~

The case set-up and input data of the original GABLS3 case can be found in the KNMI website. This is usefull if you want to compare with published results of the original SCM model intercomparison. In the original GABLS3 set-up, the simulated mesoscale tendencies are adjusted to produce a better match with the surface geostrophic wind obtained from a network of synoptic stations and the wind speed at 200-m measured at the Cabauw tower. Initial profiles are based on soundings measured near the Cabauw mast.

Alternatively, you can use inputs generated entirely from a WRF simulation, as described in [1][2]. Here, instead of using observed initial projiles and adjusted mesoscale forcings you can use initial profiles and forcing produced directly from a mesoscale simulation. This is more representative of a wind energy model-chain set-up, where the inputs of a microscale model are generated by a "wind atlas" methodology that doesn't normally include corrections with local measurements. Instead, local adjustments are allowed at the microscale level by incorporating onsite measurements as if these measurements were part of a typical wind resource assessment campaign.    

The WRF simulation is based on a one-way nesting configuration of three concentric square domains centered at the Cabauw site, of the same size 181x181, and at 9, 3 and 1 km horizontal resolution. The vertical grid, approximately 13 km high, is based on 46 terrain-following (eta) levels with 24 levels in the first 1000 m, the first level at approximately 13 m, a uniform spacing of 25 m over the first 300 m and then stretched to a uniform resolution of 600 m in the upper part. The U.S. Geological Survey (USGS) land-use surface data, that comes by default with the WRF model, is used together with the unified Noah land-surface model to define the boundary conditions at the surface. Other physical parameterizations used are: the rapid radiative transfer model (RRTM), the Dudhia radiation scheme and the Yonsei University (YSU) first-order PBL scheme. The simulation uses input data from ERA-Interim with a spin-up time of 24 hours. The WRF set-up follows the reference configuration of Kleczek et al [3], who run a sensitivity analysis of WRF showing reasonably good results at reproducing the nocturnal LLJ.

A NetCDF file is provided with the following information:

Site coordinates and Coriolis parameter
Time-height 2D arrays of velocity components (U,V,W) and potential temperature (Th)
Time-height 2D arrays of mesoscale forcings (tendencies): geostrophic wind (Ug, Vg), advective wind (Uadv, Vadv) and advective potential temperature (Thadv)
Time array of surface-layer quantities: friction velocity (ust), kinematic heat flux (wt), 2-m temperature (T2), skin temperature (TSK), surface pressure (Psfc)
Units, dimmensions and variables description are all provided in the NetCDF file. Momentum tendencies (Figure 2) are provided in [m s-1] and should be multiplied by the Coriolis parameter to obtain appropriate forces in [m s-2]. For convenience, we have ommitted information about humidity since the assumption of dry-atmosphere is typically adopted by wind energy flow models.

.. image:: _static/gabls3_tendencies.png
	:scale: 25%
	:align: center

Figure 2: Time-height contour plots of the longitudinal wind component U and momentum budget terms: Utend = Uadv + Ucor + Upg + Upbl. [1][2]

A python script is provided to show how to read the NetCDF input file and extract these variables.

Validation data
~~~~~~~~~~~~~~~~~~~~

The following quantities of interest (QoI) will be evaluated as described in [1][2], using a reference rotor size of 160 m diameter at a hub-height of 120 m (~ 7 MW turbine):

* Rotor equivalent wind speed (REWS)
* Hub-height wind direction (WDhub)
* Turbulence intensity at hub-height (TIhub)
* Wind shear (power-law exponent α) and wind veer (slope of linear fit to wind direction differences ψ) accross the rotor plane
* Surface-layer quantitites: T2, ust, wt and z/L

The evaluation consists on time-series plots of these QoIs along the diurnal cycle and mean-absolute error (MAE) integrated over the whole cycle. 

Model runs
~~~~~~~~~~
The benchmark is mainly developed for microscale models that make use of the input data described above. However, mesoscale or multi-scale (online meso-micro) simulations are also welcome. The following suggestions are provided to guide the model runs:

* We shall use the 2-m temperature (T2) as our most practical reference to deduce the potential temperature surface boundary conditions using Monin Obukhov similarity theory, since this variable is routinely measured in measurement campaigns and is part of the standard output of meteorological models.    
* Simulations may be based entirely on the mesoscale input data or incorporate measurements from the Cabauw mast. Priority should be given to measurements that can be found in "typical wind energy campaigns" (80 masts with velocity and temperature measurements, lidar profilers measuring up to 400 m).
* Sensitivity analysis of mesoscale models can be used to quantify the input uncertainty derived from the spread of the ensemble of simulations. 
* Online multi-scale simulations models can be used as a reference for microscale models that are coupled to mesoscale asyncronously through the input data. To allow this comparison multi-scale simulations should be also run with ERA-Interim input data.  
* Microscale models using Sogachev et al. (2012) k-ε turbulence model shall use this set of constants: κ = 0.4, Cε1 = 1.52, Cε2 = 1.833, σk = 2.95, σε = 2.95 and Cμ = 0.03 

If resources allow, please use a spin-up time of 24 hours as in the input data.

Output data
~~~~~~~~~~~
Data should be provided in a single NetCDF file as described in the python template. The following output variables are requested:

* Time-height 2D arrays of: velocity components, potential temperature and turbulent kinetic energy
* Time 1D array of surface-layer quantities: friction velocity (ust, at 3 m), kinematic heat flux (wt, at 3 m) and 2-m temperature (T2)
* Time in hours since 2006-07-01 12:00 UTC
* Heights in meters (please provide model levels at least up to 4000 m)

References
~~~~~~~~~~
[1] Sanz Rodrigo J, Churchfield M, Kosovic B (2016) A wind energy benchmark for ABL modelling of a diurnal cycle with a nocturnal low-level jet: GABLS3 revisited. J. Phys.: Conf. Ser. 753, 032024, doi: 10.1088/1742-6596/753/3/032024

[2] Sanz Rodrigo J, Churchfield M, Kosović B (2017) A methodology for the design and testing of atmospheric boundary layer models for wind energy applications. Wind Energ. Sci. 2: 1-20, doi:10.5194/wes-2-1-2017

[3] Kleczek MA, Steeveneveld GL and Holtslag AAM (2014) Evaluation of the Weather Research and Forecasting Mesoscale Model for GABLS3: Impact on Boundary-Layer Schemes, Boundary Conditions and Spin-Up. Boundary-Layer Meteorol 152 213-243, doi: 10.1007/s10546-014-9925-3

Acknowledgements
~~~~~~~~~~~~~~~~~~~~
This benchmark has been produced within a Marie Curie International Outgoing Fellowship, MesoWake project, with funding from the European Union’s Seventh Framework Programme for research, technological development and demonstration under grant agreement no 624562.



