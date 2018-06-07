GEWEX Atmospheric Boundary Layer Study (GABLS)
==============================================
`Javier Sanz Rodrigo, CENER <mailto:jsrodrigo@cener.com>`_

16 June 2016

Background
~~~~~~~~~~
The GEWEX Atmospheric Boundary Layer Study (GABLS) series of benchmarks have been developed to improve the representation of the atmospheric boundary layer in regional and large-scale atmospheric models. The model intercomparison studies have been organized for single-column models (SCM) and large-eddy simulation models (LES). The cases are based on observations over flat terrain in the Artic, Kansas (USA), Cabauw (The Netherlands) and Dome C (Antarctica).

GABLS1 simulated a quasi-steady stable boundary layer resulting from 9 hours of uniform surface cooling [1][2][3]. GABLS2 simulated a diurnal cycle, still with idealized forcing, by simplifying measurements from the CASES-99 experiment in Kansas [4][5]. GABLS3 simulated a real diurnal case with a strong nocturnal low-level jet (LLJ) at the Cabauw met tower in the Netherlands [6][7][8][9][10]. In GABLS4, the aim is to study the interaction of a boundary layer with strong stability in relatively simple surface coupling characteristics.

Challenges
~~~~~~~~~~
The challenges of stable boundary layers and diurnal cycles are reviewed by Hotlslag et al. [11], notably: the relation between enhanced mixing in operational weather models performance, investigate the role of land-surface heterogeneity in the coupling with the atmosphere, develop LES models with interactive land-surface schemes, create a climatology of boundary-layer parameters (stability classes, boundary-layer depth, and surface fluxes) and develop parameterizations for the very stable boundary layer when turbulence is not the dominant driver. These challenges are ultimately shared by wind energy applications that are embeded in atmospheric models.

Benchmarks
~~~~~~~~~~
The GABLS benchmarks are revisited in Windbench as baseline for the design of microscale wind farm flow models that progressively incorporate more complex atmospheric physics. Wind energy specific quantities of interest are used in order to focus the model evaluation on the application of interest.

The GABLS activities are coordinated within the `GEWEX <http://www.gewex.org/>`_ Modelling and Prediction Panel (GMPP). The cases have been throughly documented in the literature and in the following websites:

* GABLS1: `SCM <http://turbulencia.uib.es/gabls/>`__, `LES <http://gabls.metoffice.com/>`__
* `GABLS2 <http://www.misu.su.se/~gunilla/gabls>`__
* GABLS3: `SCM <http://projects.knmi.nl/gabls/>`__, `LES <http://www4.ncsu.edu/~sbasu5/GABLS3/>`__
* `GABLS4 <http://www.cnrm-game-meteo.fr/aladin/meshtml/GABLS4/GABLS4.html>`__

In the context of developing a downscaling methodology to link mesoscale wind climate processes and microscale wind farm flow models, the GABLS3 case is particularly relevant. GABLS 1 and 2 can be considered as precursor cases dealing with turbulence modelling of the atmospheric boundary layer under idealized forcing conditions. These cases are suitable for the design of RANS-based SCMs by comparison with LES simulations, that have shown high consistency [3][5]. 

GABLS3 incorporates realistic forcing by using mesoscale model simulations and synoptic stations [6][7][8][9][10]. This benchmark has been revisited by the wind energy community in the context of the `NEWA <http://www.neweuropeanwindatlas.eu>`_ project to develop meso-micro methodologies for wind resource assessment applications:

.. toctree::
   :glob:
   :maxdepth: 1

   gabls3.rst

References 
~~~~~~~~~~
[1] Holtslag AAM (2006) GEWEX Atmospheric Boundary-Layer Study (GABLS) on stable boundary layers. Boundary-Layer Meteorol 118: 243-246

[2] Cuxart J, Holtslag AAM, Beare RJ, Bazile E, Beljaars A, Cheng A, Conangla L, Ek M, Freedman F, Hamdi R, Kerstein A, Kitagawa H, Lenderink G, Lewellen D, Mailhot J, Mauritsen T, Perov V, Schayes G, Steeneveld G-J, Svensson G, Taylor P, Weng W, Wunsch S (2006) Single-column model intercomparison for a stably stratified atmospheric boundary layer. Boundary-Layer Meteorol 118:273–303
Beare RJ, Macvean MK, Holtslag AAM, Cuxart J, Esau I, Golaz J-C, Jimenez MA, Khairoutdinov M, Kosovic B, Lewellen D, et al. (2006) An intercomparison of large-eddy simulations of the stable boundary layer. Bound-Layer Meteorol118 247–272. doi:10.1007/s10546-004-2820-6.

[3] Svensson G, Holtslag AAM, Kumar V, Mauritsen T, Steeneveld GJ, Angevine WM, Bazile E, Beljaars A, de Bruijn EIF, et al. (2011) Evaluation of the diurnal cycle in the atmospheric boundary layer over land as represented by a variety of single column models—the second GABLS experiment. Bound-Layer Meteorol 140 177–206. doi:10.1007/s10546-011-9611-7

[4] Kumar V, Svensson G, Holtslag AAM, Parlange MB, Meneveau C (2010) Impact of surface flux formulations and geostrophic forcing on large-eddy simulations of the diurnal atmospheric boundary layer flow. J Meteorol Climatol 49:1496–1516, doi:10.1175/2010JAMC2145.1

[5] Bass P, Bosveld FC, Lenderink G, van Meijgaard E and Holtslag AAM (2010) How to design single-column model experiments for comparison with observed nocturnal low-level jets. Q J R Meteorol Soc 136 671-684

[6] Holtslag AAM (2014) Introduction to the Third GEWEX Atmospheric Boundary Layer Study (GABLS3). Boundary-Layer Meteorol152 127-132. doi: 10.1007/s10546-014-9931-5Bosveld FC, Baas P, vanMeijgaard E, de Bruijn EIF, Steeneveld GJ and Holtslag AAM 2014 The third GABLS intercomparison case for evaluation studies of boundary-layer models, Part A: case selection and set-up. Boundary-Layer Meteorol 152 133-156, doi: 10.1007/s10546-014-9917-3

[7] Bosveld FC, Baas P, vanMeijgaard E, de Bruijn EIF, Steeneveld GJ and Holtslag AAM (2014) The third GABLS intercomparison case for evaluation studies of boundary-layer models, Part A: case selection and set-up. Boundary-Layer Meteorol 152 133-156, doi: 10.1007/s10546-014-9917-3

[8] Bosveld FC, Bass P, Steevenveld G-J, Holtslag AAM, Angevine WM, Bazile E, de Bruin EIF, Deacu D, Edwards JM, Ek M, Larson VE, Pleim JE, Raschendorfer M, Svensson G (2014) The third GABLS Intercomparison case for evaluation studies of Boundary-Layer Models Part B: Results and Process Understanding. Boundary–Layer Meteorol 152 157-187, doi: 10.1007/s10546-014-9919-1

[9] Basu S, Holtslag AAM, Bosveld FC (2011) GABLS3-LES Intercomparison Study. ECMWF GABLS Workshop on Diurnal cycles and the stable boundary layer, Reading, U.K., 7-10 November 2011

[10] Holtslag AAM, Svensson G, Baas P, Basu S, Beare B, Beljaars ACM, Bosveld FC, Cuxart J, Lindvall J, Steeneveld GJ, et al. (2013) Stable atmospheric boundary layers and diurnal cycles—challenges for weather and climate models. Bull Am Meteorol Soc 94 1691–1706, doi:10.1175/bams-d-11-00187.1
van Ulden AP, Wieringa J (1996) Atmospheric boundary layer research at Cabauw. Boundary-Layer Meteorol 78 39–69
