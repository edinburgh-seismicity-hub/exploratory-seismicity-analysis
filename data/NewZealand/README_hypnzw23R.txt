
New Zealand earthquake catalogue 2001-2011 relocated with 3-D velocity 
model nzwide2.3
----------------------------------------------------------------------
Eberhart-Philips, D. & Reyners, M., 2022. New Zealand earthquake 
catalogue 2001-2011 relocated with 3-D velocity model nzwide2.3[Data 
Set], Zenodo, doi:10.5281/zenodo.6604627
----------------------------------------------------------------------
This archive provides the results from the paper “A catalogue of 2001-
2011 New Zealand earthquakes relocated with a 3-D seismic velocity 
model and comparison to 2019-2020 auto-detected earthquakes in the 
sparsely instrumented southern South Island”, published in New Zealand 
Journal of Geology and Geophysics (Eberhart-Phillips and Reyners, 
2022).  

This uses P- and S-wave arrival times from earthquakes during 2001-
2011 as these were manually picked with assigned quality. The Simul 
program is used (Eberhart-Phillips et al., 2021), and the current 
version of the New Zealand wide 3-D velocity model, nzwide2.3 
(Eberhart-Phillips et al., 2022). The catalogue updates the nzwide1.0 
hypocentres presented in Reyners et al. (2011), and results are 
similar. On average, the nzwide2.3 events moved 0.25 km southeast, 0.1 
km deeper, and had 0.02 s reduction in rms residual. 

The hypocentre ‘xyze’ file includes various location quality 
parameters, and assigned letter quality codes as described in Table 1.

The location error computed in Simul is related to the diagonal of the 
covariance multiplied by a factor sig2, which should be related to the 
error in travel-time observations.  The travel-time error is related 
both the measurement accuracy and the phase uncertainty, which Simul 
uses as the input reading error (rderr) and wrms, related by an error 
coefficient (ercof).
       sig2 = rderr*rderr + ercof*wrms 
In this work, we assign rderr as 0.05 s, and use ercof of 0.5 to 
provide larger location uncertainty for poorly-fit travel-time data.  
Further we assign erz as 20 km for fixed depth relocations, and set 
the maximum erh and erz to 99 km. We also assign minimum erh and erz 
for qualities C, D and E; since some computed location errors may be 
unrealistically small, as it is easier to fit a small set of 
observations, although the other quality parameters point to poorer 
actual constraint.  For C quality, minimum erh is 1.0 and erz is 2.0.  
For D quality, minimum erh is 1.5 and erz is 3.0.  For E quality, 
minimum erh is 2.0 and erz is 4.0.

The New Zealand seismic network is sparse, with 100-km spacing, in 
some regions. Thus even the lower quality hypocentres contribute to 
understanding regional seismic potential.  
 
Table 1.  NZ-wide Assigned Quality Codes
 
parameter,A,B,C,D,E
nobs,? 15,? 12,? 8,? 6,? 4
ns,? 4,? 2,? 1,,
wrms (s),? 0.2,? 0.3,? 0.4,? 0.6,
gap (deg),? 140,? 180,? 240,? 270,
dmin (km),? 500,? 500,? 500,? 500,
rzdm(depth/dmin),? 0.5,? 0.3,? 0.1,,
erh (km),? 1.5,? 2.5,? 4,? 8,

Archived files are:

hypnzw23R2001_2011.xyze, the Simul hypocentre file with X,Y 
coordinates, error parameters and quality code. 
Table S1 shows a sample portion of this file. This can be read with 
the following fortran lines, where the file is assigned to fort.7.

      read(7,1631) iyr4,imo,idy,ihr,imin,sec,rlat,rlon,depth,rmag,
     2   nobs,wrmsr,x,y,gap,dmin,rzdm,np,ns,serot,serh,serz,qcode
 1631 format(i4.4,2(1x,2i2.2),f6.2,f9.4,f10.4,f7.2,f6.2,
     2 i5,f6.2,2f9.2,i5,i4,f5.1,2i4,3f6.2,2x,a1)

hypnzw23R2001_2011.sum, the Hypo71 summary format hypocentre file (Lee 
and Lahr, 1975).

aznzw23Ra......out files in the tar file azlist.tar.gz.  These are 
monthly output files in the Hypo71 list format that show the 
hypocentre solution, and stations travel-time, with remark, distance, 
azimuth, residual, and weight.

f4nzw23Ra.......out files in the tar file ttdata.tar.gz.  These Simul 
format travel-time data monthly output files provide the travel-times 
and phase remarks for each event.

References:
Eberhart-Philips, D., Bannister, S., Reyners, M. & Bourguignon, S., 
2022a. New Zealand Wide model 2.3 seismic velocity model for New 
Zealand (vlnzwide2.3) [Data Set], Zenodo, doi:10.5281/zenodo.6568301.

Eberhart-Philips, D. & Reyners, M., 2022. A catalogue of 2001-2011 New 
Zealand earthquakes relocated with a 3-D seismic velocity model and 
comparison to 2019-2020 auto-detected earthquakes in the sparsely 
instrumented southern South Island, New Zealand J. Geol. Geophys.

Eberhart-Phillips, D., Thurber, C., Rietbrock, A., Fry, B., Reyners, 
M. & Lanza, F., 2021c. Simul2017: a flexible program for inversion of 
earthquake data for 3-D velocity and hypocenters or 3-D Q, Zenodo, 
doi:10.5281/zenodo.5746047.

Lee, W.H. & Lahr, J.C., 1975. HYPO71 (revised); a computer program for 
determining hypocenter, magnitude, and first motion pattern of local 
earthquakes. in Open-File Report 75-311U. S. Geol. Surv., Menlo Park, 
Calif., doi:10.3133/ofr75311.

Reyners, M., Eberhart-Phillips, D. & Bannister, S., 2011. Tracking 
repeated subduction of the Hikurangi Plateau beneath New Zealand, 
Earth Planet Science Letters, 311, 165.
