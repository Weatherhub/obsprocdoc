===================
质量控制
===================

.. contents ::

Purpose
=======

* The "PREPBUFR" processing is the final step in preparing the majority of conventional observational data for assimilation into the various analyses.

* This step involves the execution of series of programs designed to assemble observations dumped from a number of on-line decoder databases:

    * encode information about the observational error for each data type as well the background (first guess) interpolated to each data location
    * perform both rudimentary multi-platform quality control and more complex platform-specific quality control
    * store the output in a monolithic BUFR file, known as PREPBUFR.

* Generated on production machine in each network from conventional data dump files

    * adpsfc, adpupa, aircar, aircft, ascatw, atovs, goesnd, gpsipw, msonet, proflr, rassda, satwnd (except for GFS/GDAS), sfcshp, vadwnd, wndsat

* Network-specific parm cards control processing
* Structure defined by input PrepBUFR mnemonic table
* BUFR message types can include:

    * ADPUPA, AIRCAR, AIRCFT, SATWND, PROFLR, VADWND, SATEMP, ADPSFC, SFCSHP, SFCBOG, SPSSMI, SYNDAT, ERS1DA, GOESND, QKSWND, MSONET, GPSIPW, RASSDA, WDSATR, ASCATW (what is present depends on the network)
    * Each message type has its own BUFR structure as defined in the PrepBUFR mnemonic table

* In :code:`/nwprod/com/NET/prod/RUN.yyyymmdd/MODEL.tcycz.prepbufr.tmMM`, where:

    * **NET(RUN/MODEL)** is either: nam(nam/nam), nam(ndas/ndas), rap(rap/rap), rap(rap_p/rap_p), rtma(rtma/rtma)
    * **cyc** is cycle (hourly for NET=rap, rtma; 00, 06, 12, 18 all others)
    * **MM** is 00 for all types except RUN/MODEL=ndas/ndas where it can be 12, 09, 06 or 03


质控步骤
==============

1. PREPDATA
    总体质量控制

2. GLERLADJ
    对大的水体周边观测的调整

3. PREVENTS 
    针对气候模式使用的观测资料的质控

4. CQCBUFR
    对探空观测的质控

5. PROFCQC
    对飞机观测的质控

6. PREPACQC
    对风廓线仪挂册的质控
    
7. OIQCBUFR
    Buddy Check


Quality Marker Table
====================

Most of the observation types in the PREPBUFR file are associated with quality markers (e.g., mnemonics “PQM, “TQM”, “WQM”, etc.).  These are used by the various analyses to place a weight on the data based on its quality.
`质控标识表 <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/table_7.htm>`_ contains the code table of quality markers.  These quality markers apply to all observation types in the PREPBUFR file.