=====
Dump
=====

.. contents ::

Purpose
=======

* BUFR format

* Generated from “tanks” at each network data cutoff time

* Time-windowed

    * NET=rap : +/- 1.0 hour

* Geographically filtered

    * environmental variable "**LALO=0*" is used to turn off the filter

* Duplicate checked

* QC: SDM purge (or keep) flags, reject list flags

    * /nwprod/dcom/us007003/sdmedit can be used to filtered out specific reports

* The product is :code:`/nwprod/com/NET/prod/RUN.yyyymmdd/MODEL.tcycz.TYPE.tmMM.bufr_d`, where:

    * **NET(RUN/MODEL)** is either: cdas(cdas/cdas), cfs(cdas/cdas1),dump(dump/dump), gfs(gdas/gdas1), gfs(gfs/gfs), nam(nam/nam), nam(ndas/ndas), rap(rap/rap), rap(rap_p/rap_p), rtma(rtma/rtma)
    * **cyc** is cycle (hourly for NET=dump, rap, rtma; 00, 06, 12, 18 all others)
    * **MM** is 00 for all types except RUN/MODEL=ndas/ndas where it can be 12, 09, 06 or 03
    * **TYPE** is either: 1bamua, 1bamub, 1bhrs3, 1bhrs4, 1bmhs, adpsfc, adpupa, aircar, aircft, airsev, ascatt, ascatw, atms, atovs, avcsam, avcspm, bathy, cris, esamua, esamub, eshrs3, esmhs, geoimr, goesfv, goesnd, gome, gpsipw, gpsro, lghtng, lgycld, mls, msonet, mtiasi, nexrad, omi, osbuv8, proflr, radwnd, rassda, satwnd, sevcsr, sfcshp, sptrmm, ssmisu, tesac, trkob, trmm, vadwnd, wdsatr, wndsat (types actually dumped depend upon the network)



Dump Procedure
===============

For each type of observation, the following steps are followed:

1. 

