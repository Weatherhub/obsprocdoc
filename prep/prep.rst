====
Prep
====

.. contents ::

Purpose
=======

* BUFR Format
* Generated on production machine in each network from conventional data dump files

    * adpsfc, adpupa, aircar, aircft, ascatw, atovs, goesnd, gpsipw, msonet, proflr, rassda, satwnd (except for GFS/GDAS), sfcshp, vadwnd, wndsat

* Network-specific parm cards control processing
* Structure defined by input PrepBUFR mnemonic table
* BUFR message types can include:

    * ADPUPA, AIRCAR, AIRCFT, SATWND, PROFLR, VADWND, SATEMP, ADPSFC, SFCSHP, SFCBOG, SPSSMI, SYNDAT, ERS1DA, GOESND, QKSWND, MSONET, GPSIPW, RASSDA, WDSATR, ASCATW (what is present depends on the network)
    * Each message type has its own BUFR structure as defined in the PrepBUFR mnemonic table

* In: /nwprod/com/NET/prod/RUN.yyyymmdd/MODEL.tcycz.prepbufr.tmMM, where:

    * **NET(RUN/MODEL)** is either: nam(nam/nam), nam(ndas/ndas), rap(rap/rap), rap(rap_p/rap_p), rtma(rtma/rtma)
    * **cyc** is cycle (hourly for NET=rap, rtma; 00, 06, 12, 18 all others)
    * **MM** is 00 for all types except RUN/MODEL=ndas/ndas where it can be 12, 09, 06 or 03


Prep Procedure
==============


Quality Marker Table
====================

Most of the observation types in the PREPBUFR file are associated with quality markers (e.g., mnemonics “PQM, “TQM”, “WQM”, etc.).  These are used by the various analyses to place a weight on the data based on its quality.
`Table 7 <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/table_7.htm>`_ contains the code table of quality markers.  These quality markers apply to all observation types in the PREPBUFR file.

