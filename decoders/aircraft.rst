========
Aircraft
========

.. contents ::

Directory structure
===================

The Aircraft data is organized as MICAPS files every 12 hours ::

    >  tree -L 1 UPAR_CHN_MUL_FTM
    UPAR_CHN_MUL_FTM
    ├── 201807040000.xml
    ├── 201807041200.xml
    ├── 201807050000.xml
    ├── 201807051200.xml
    ├── 201807060000.xml
    ├── 201807061200.xml
    ├── 201807070000.xml
    ├── 201807071200.xml
    ├── 201807080000.xml
    ├── 201807081200.xml
    ├── 201807090000.xml
    ├── 201807091200.xml
    ├── 201807100000.xml
    ├── 201807101200.xml
    ├── 201807110000.xml
    ├── 201807111200.xml
    ├── 201807120000.xml
    ├── 201807121200.xml
    ......


Data format
===========

MICAPS format data is looks like ::

    diamond  31  AMDAR���� 
    	23323
     C_CCCC		C_LY		C_LM		C_LD		C_LH		C01006		V04001		V04002		V04003		V_OHM		V05001		V06001		V08004		V02061		V07002		V12001		V11001		V11002		V11041		V11031		F07002		F12001		F11001		F11002		F11041		F11031
     RKSL				2018				9				12				2				HL8236				2018				9				12				0200				33.445				126.36				0			0			740				20				179				1				9999			9999			0			0			0			0			0			0
     RKSL				2018				9				12				2				HL8236				2018				9				12				0201				33.4666				126.405				0			0			475				21.5				104				9.8				9999			9999			0			0			0			0			0			0
     RKSL				2018				9				12				2				HL8236				2018				9				12				0202				33.485				126.445				0			0			255				19.5				90				10.3				9999			9999			0			0			0			0			0			0
     RKSL				2018				9				12				2				HL8236				2018				9				12				0203				33.505				126.4816				0			0			45				21.5				82				7.2				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0200				25.2116				55.7				0			0			2588				18.5				358				6.2				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0009				2018				9				12				0202				22.2883				115.44				0			0			6294				-6.7				94				13.9				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0200				25.2166				55.675				0			0			2557				18.5				348				6.2				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0200				25.2183				55.6466				0			0			2527				18.5				346				6.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0201				25.225				55.6216				0			0			2496				19				347				7.2				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0201				25.2316				55.595				0			0			2487				19				345				6.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0200				21.5016				113.7266				0			0			5060				-1.2				56				11.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0201				25.2333				55.57				0			0			2487				19				345				6.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0200				21.525				113.7366				0			0			4877				-0.2				53				10.8				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0202				25.235				55.5416				0			0			2478				19				345				6.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0200				21.55				113.7466				0			0			4706				0.7				57				10.8				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0202				25.235				55.515				0			0			2365				19.7				352				7.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0201				21.575				113.7566				0			0			4535				2				55				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0028				2018				9				12				0202				25.235				55.4883				0			0			2274				20.7				353				7.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0201				21.6				113.7666				0			0			4386				3.2				40				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0201				21.6216				113.7766				0			0			4249				4.2				40				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0202				21.645				113.7866				0			0			4100				5.5				47				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0202				21.6683				113.7966				0			0			3959				6.7				50				9.8				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0202				21.6916				113.8066				0			0			3862				7.2				53				11.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0029				2018				9				12				0203				21.715				113.8166				0			0			3749				8.2				56				11.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0201				22.125				119.335				0			0			4868				0				133				8.2				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0201				22.1216				119.3716				0			0			4691				1.2				127				8.7				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0201				22.1166				119.4066				0			0			4499				1.7				136				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0202				22.115				119.445				0			0			4304				2.7				143				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0202				22.1083				119.48				0			0			4124				4.2				146				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0202				22.1016				119.515				0			0			3926				6				141				10.8				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0203				22.1				119.55				0			0			3749				7				138				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0203				22.095				119.585				0			0			3606				8				145				9.8				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0203				22.0916				119.62				0			0			3441				8.5				153				10.3				9999			9999			0			0			0			0			0			0			
     VHHH				2018				9				12				2				HK0039				2018				9				12				0204				22.085				119.6516				0			0			3185				10				160				10.8				9999			9999			0			0			0			0			0			0			
     EGRR				2018				9				12				2				EU8135				2018				9				12				0206				24.4011				-55.8833				0			0			11278				-50				339				8.8				9999			9999			0			0			0			0			0			0			
     EGRR				2018				9				12				2				EU8110				2018				9				12				0206				19.8502				6.7				0			0			11857				-52.2				57				14.4				9999			9999			0			0			0			0			0			0			
     CWAO				2018				9				12				2								2018				9				12				0200				45.3083				-75.6333				0			0			9999			17.05				290				2.6				9999			9999			0			0			0			0			0			0			
     CWAO				2018				9				12				2								2018				9				12				0200				45.6516				-73.4516				0			0			9999			11.55				274				3.1				9999			9999			0			0			0			0			0			0			
     CWAO				2018				9				12				2								2018				9				12				0201				45.6316				-73.5366				0			0			9999			13.55				314				3.1				9999			9999			0			0			0			0			0			0			
     CWAO				2018				9				12				2								2018				9				12				0202				45.5916				-73.5933				0			0			9999			13.35				317				3.6				9999			9999			0			0			0			0			0			0			

.. warning::

    The *CWAO* data may miss the flight ID

MICAPS extractor
================

A python code is used to extract the desired information from this MICAPS file::

    > python read_micaps_amdar.py > micaps_amdar_data

The information we want to extract from MICAPS is.
::

    print '{:>8}'.format(flightID), year, month, day, hour, minute, lat, lon, height, temperature, wdir, wspd, vv, turb

the content of **micaps_amdar_data** is::

    > less micaps_amdar_data
      HL8236 2018 9 12 2 0 33.445 126.36 740.0 20.0 179.0 1.0 9999.0 9999.0
      HL8236 2018 9 12 2 1 33.4666 126.405 475.0 21.5 104.0 9.8 9999.0 9999.0
      HL8236 2018 9 12 2 2 33.485 126.445 255.0 19.5 90.0 10.3 9999.0 9999.0
      HL8236 2018 9 12 2 3 33.505 126.4816 45.0 21.5 82.0 7.2 9999.0 9999.0
      HK0028 2018 9 12 2 0 25.2116 55.7 2588.0 18.5 358.0 6.2 9999.0 9999.0
      HK0009 2018 9 12 2 2 22.2883 115.44 6294.0 -6.7 94.0 13.9 9999.0 9999.0
      HK0028 2018 9 12 2 0 25.2166 55.675 2557.0 18.5 348.0 6.2 9999.0 9999.0
      HK0028 2018 9 12 2 0 25.2183 55.6466 2527.0 18.5 346.0 6.7 9999.0 9999.0
      HK0028 2018 9 12 2 1 25.225 55.6216 2496.0 19.0 347.0 7.2 9999.0 9999.0
      HK0028 2018 9 12 2 1 25.2316 55.595 2487.0 19.0 345.0 6.7 9999.0 9999.0
      HK0029 2018 9 12 2 0 21.5016 113.7266 5060.0 -1.2 56.0 11.3 9999.0 9999.0
      HK0028 2018 9 12 2 1 25.2333 55.57 2487.0 19.0 345.0 6.7 9999.0 9999.0
      HK0029 2018 9 12 2 0 21.525 113.7366 4877.0 -0.2 53.0 10.8 9999.0 9999.0
      HK0028 2018 9 12 2 2 25.235 55.5416 2478.0 19.0 345.0 6.7 9999.0 9999.0
      HK0029 2018 9 12 2 0 21.55 113.7466 4706.0 0.7 57.0 10.8 9999.0 9999.0
      HK0028 2018 9 12 2 2 25.235 55.515 2365.0 19.7 352.0 7.7 9999.0 9999.0
      HK0029 2018 9 12 2 1 21.575 113.7566 4535.0 2.0 55.0 10.3 9999.0 9999.0
      HK0028 2018 9 12 2 2 25.235 55.4883 2274.0 20.7 353.0 7.7 9999.0 9999.0
      HK0029 2018 9 12 2 1 21.6 113.7666 4386.0 3.2 40.0 10.3 9999.0 9999.0
      HK0029 2018 9 12 2 1 21.6216 113.7766 4249.0 4.2 40.0 10.3 9999.0 9999.0
      HK0029 2018 9 12 2 2 21.645 113.7866 4100.0 5.5 47.0 10.3 9999.0 9999.0
      HK0029 2018 9 12 2 2 21.6683 113.7966 3959.0 6.7 50.0 9.8 9999.0 9999.0
      HK0029 2018 9 12 2 2 21.6916 113.8066 3862.0 7.2 53.0 11.3 9999.0 9999.0
      HK0029 2018 9 12 2 3 21.715 113.8166 3749.0 8.2 56.0 11.3 9999.0 9999.0
      HK0039 2018 9 12 2 1 22.125 119.335 4868.0 0.0 133.0 8.2 9999.0 9999.0
      HK0039 2018 9 12 2 1 22.1216 119.3716 4691.0 1.2 127.0 8.7 9999.0 9999.0
      HK0039 2018 9 12 2 1 22.1166 119.4066 4499.0 1.7 136.0 10.3 9999.0 9999.0
      HK0039 2018 9 12 2 2 22.115 119.445 4304.0 2.7 143.0 10.3 9999.0 9999.0
      HK0039 2018 9 12 2 2 22.1083 119.48 4124.0 4.2 146.0 10.3 9999.0 9999.0
      HK0039 2018 9 12 2 2 22.1016 119.515 3926.0 6.0 141.0 10.8 9999.0 9999.0
      HK0039 2018 9 12 2 3 22.1 119.55 3749.0 7.0 138.0 10.3 9999.0 9999.0
      HK0039 2018 9 12 2 3 22.095 119.585 3606.0 8.0 145.0 9.8 9999.0 9999.0
      HK0039 2018 9 12 2 3 22.0916 119.62 3441.0 8.5 153.0 10.3 9999.0 9999.0
      HK0039 2018 9 12 2 4 22.085 119.6516 3185.0 10.0 160.0 10.8 9999.0 9999.0
      EU8135 2018 9 12 2 6 24.4011 -55.8833 11278.0 -50.0 339.0 8.8 9999.0 9999.0
      EU8110 2018 9 12 2 6 19.8502 6.7 11857.0 -52.2 57.0 14.4 9999.0 9999.0
       99999 2018 9 12 2 0 45.3083 -75.6333 9999.0 17.05 290.0 2.6 9999.0 9999.0
       99999 2018 9 12 2 0 45.6516 -73.4516 9999.0 11.55 274.0 3.1 9999.0 9999.0
       99999 2018 9 12 2 1 45.6316 -73.5366 9999.0 13.55 314.0 3.1 9999.0 9999.0
       99999 2018 9 12 2 2 45.5916 -73.5933 9999.0 13.35 317.0 3.6 9999.0 9999.0
     SQXIOYZA 2018 9 12 2 0 33.308 -111.69 2185.0 20.85 237.0 7.7 9999.0 9999.0


Source code
===========

1. Source code directory::

    > cd /nwprod/decoders/decod_dcmicapsamdar_v3.0.0/sorc

2. Subroutines to decode Aircraft data

    * afdcod.f

.. note::

    * The *pirep.tbl*,  *airep.tbl* are not used, although they are required as arguments and read in.
    * The path and file name of *micaps_amdar_data* file are hard coded in the subroutines.

4. Compile the code
::

    > make

Decode and convert to BUFR format
=================================

1.  enter into the exec directory
::

    > cd /nwprod/decoders/decod_dcmicapsamdar/exec
    > ls -la
    total 1944
    drwxr-xr-x  9 xinzhang  staff     288 Sep 25 21:24 .
    drwxr-xr-x  5 xinzhang  staff     160 Sep 21 18:45 ..
    lrwxr-xr-x  1 xinzhang  staff      25 Sep 21 18:45 airep.tbl -> ../dictionaries/airep.tbl
    lrwxr-xr-x  1 xinzhang  staff      34 Sep 21 18:45 bufrtab.004 -> ../../decod_shared/fix/bufrtab.004
    -rwxr-xr-x  1 xinzhang  staff  985984 Sep 21 18:45 decod_dcmicapsadmar
    -rw-r--r--  1 xinzhang  staff     470 Sep 21 18:45 decod_dcmicapsadmar.log
    lrwxr-xr-x  1 xinzhang  staff      25 Sep 21 18:45 pirep.tbl -> ../dictionaries/pirep.tbl
    -rwxr-xr-x  1 xinzhang  staff     410 Sep 21 18:45 run.ksh
    drwxr-xr-x  3 xinzhang  staff      96 Sep 21 18:45 tmp


2. run the decoder script
::

    > run.ksh

    > cat run.ksh
    #!/bin/bash
    export DBNBUFRT=120
    export TRANJB=/nwprod/ush/tranjb
    export tank_dir=/nwprod/dcom/us007003
    export SCREEN="OFF"
    export DBNROOT=`pwd`
    rm tmp/*
    rm decod_dcmicapsadmar.log
    ./decod_dcmicapsadmar -v 4 -d decod_dcmicapsadmar.log  -b 240 -c 180912/0200 pirep.tbl airep.tbl bufrtab.004
    ls -la tmp/*

    BUFR_FILES=$(echo tmp/BUFR*)
    echo ${BUFR_FILES}

    for file in ${BUFR_FILES}
    do
      ${TRANJB} ${tank_dir} ${file}
    done

.. note::

    * -c 180912/0200 : Set the **current time** (201809120200) used to calculate the time departures of the obs. data.
    * -b 240 : Number of hours to decode prior to "current" time (default)
    * The observations with date/time between **current time** - 240 hours and  **current time** + 3 are **kept**.

 3. The generated BUFR format file will be saved at
 ::

    > ls -la tmp/BUFR.0.aircraft.1.1933.1537419287.73 
    -rw-r--r--  1 xinzhang  staff  1806552 Sep 21 18:45 tmp/BUFR.0.aircraft.1.1933.1537419287.73


Transfer bufr data to BUFR Tanks
================================
* put data in BUFR **tanks**::

    > /nwprod/ush/tranjb /nwprod/dcom/us007003 tmp/BUFR.0.aircraft.1.1933.1537419287.73

    > ls -al /nwprod/dcom/us007003/20180912/b004/xx003
    -rw-r--r-- 1 vagrant vagrant 1828720 Sep 19 22:54 /nwprod/dcom/us007003/20180912/b004/xx003

.. note::

    * if environmental variable **SCREEN=ON** :
        * Define **Run Time** is the system time when the tranjb is running.
        * Only observations with date/time between **Run Time** - 10 days and **Run Time** + 12 hours are kept.
    * for retrospective run, set **SCREEN=OFF**
    * /nwprod/dcom/us007003/yyyymmdd/bmmm/xxsss (where mmm is WMO BUFR message type and xxx is local BUFR message subtype)
    * 004.003 (in dump group mnemonic aircft): AMDAR format aircraft data from ASDAR/ACARS reporting systems
    * BUFR format
    * Arranged by UTC day and continuously grow throughout the day, if you run decoders many time, the content of the file will grow
    * No QC (other than rudimentary checks inside decoders)
    * No duplicate checking
    * Interested users can use utility *debufr* to check the content of the bufr file::

        > /nwprod/util/execdebufr /nwprod/dcom/us007003/20180912/b004/xx003

      the output is in *debufr.out*.


PrepBUFR Processing
===================

Please refer to :

    * `Data Processing at NCEP <http://www.emc.ncep.noaa.gov/?data_processing=data_processing>`_ and `Overview talk by Keyser <https://dtcenter.org/com-GSI/users/docs/presentations/2013_tutorial/Tue_L1_Keyser_ObsProcessing.pdf>`_
    * `PREPBUFR Processing at NCEP <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/document.htm>`_
    * `PREPBUFR Report Types used by RAP analyses <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/table_5.htm>`_
    * `PREPBUFR Report Types used by Global GFS and GDAS GSI analyses <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/table_2.htm>`_
