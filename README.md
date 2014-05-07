WRF_modified_modules
====================

My modified WRF/Polar WRF FORTRAN modules.

- dyn_em/module_initialize_real.F

In the module dyn_em/module_initialize_real.F of Polar WRF 3.4.1 the maximum snow albedo used for initialization is changed from 0.75 to 0.92. The value 0.92 has been derived from radiation measurements at Hansbreen glacier.

- phys/module_sf_noahlsm_glacial_only.F

In the module phys/module_sf_noahlsm_glacial_only.F of Polar WRF 3.4.1 snow water equivalent and snow depth can now reach values of 0 m. Changes in surface albedo and emissivity are now scaled by a fractional snow cover parameter as suggested by phys/module_sf_noahlsm.F. The subroutine SNFRAC() was also added but calculates the fractional snow cover parameter using a snow distribution shape parameter of 2.6 as suggested in GENPARM.TBL.
