# GMD2019
This repository contains the WRF configuration files necessary to reproduce the simulations as described in Siedersleben et al. 2019

The file windturbinesGMD.txt contains the locations of all windturbines implemented in the simulations. The corresponding
attributes of each wind turbine type is described in the wind-turbine-xx.tbl. Be aware that all windturbines use the same 
power and thrust coefficients only the different hub heights and rotor diameters are taken into account as described in 
Siedersleben et al. (2019).

The namelist.input_nameOfSimulation files necessary to run the simulations are provided in this repository as well. You may 
notice that there are less namelist files than simulations. The simulations not using a TKE source use the same namelists as 
the ones with a TKE a source. However, the WRF model needs to be recompiled using the manipolated module_wind_fitch.F (you 
find this file in this repository). The sensitivity studies investigating the impact of the uncertainties in the power and 
thrust coefficients use the namelist of the control simulation CNTRb, but with manipulated wind-turbine-x_modMin/Max.tbl wind 
turbine files.
