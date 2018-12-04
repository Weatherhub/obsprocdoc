=======
详细设计
=======

.. contents ::

Installing Singularity
==========================

The whole system requires to be run with *Singularity*. To install Singualrity:

* please refer to `Singularity Homepage <https://www.sylabs.io/>`_

* shell into intel.simg::

    > singularity shell -B /Users/xinzhang/work/LR-App-Store/nwprod:/nwprod -e intel/intel.simg

.. note::
    make sure your local nwprod directory is mounted as /nwprod in Singualrity container.

* the directory structure is::

    > cpaessxinzhang-mpro:LR-App-Store xinzhang$ tree -L 1 nwprod
    nwprod
    ├── build2.bash
    ├── build_obsproc.bash
    ├── com
    ├── comGSIv3.6_EnKFv1.2
    ├── dcom
    ├── decoders
    ├── doc
    ├── exec
    ├── fix -> /nwprod/decoders/decod_shared/fix
    ├── gempak
    ├── lib
    ├── obsproc_dump.v3.2.1
    ├── obsproc_dump_post.v3.1.0
    ├── obsproc_global.v3.1.1
    ├── obsproc_prep.v5.0.0
    ├── obsproc_prep_post.v3.0.0
    ├── obsproc_rap.v3.0.0
    ├── obsproc_shared
    ├── run_rap_obsproc.bash
    ├── sorc
    ├── tmpprod
    ├── ush
    ├── util
    └── versions


Building NCEP libraries
===========================

* enter into NCEP libraries' directory::

    > cd /nwprod/lib

* compile the libraries::

    > ./build1.bash

* If successfully compiled::

    > tree -L 1
    .
    ├── build1.bash
    ├── clean.bash
    ├── graphics
    ├── incmod
    ├── libCRTM_2.0.5.a
    ├── libCRTM_2.0.6.a
    ├── libCRTM_2.1.3.a
    ├── libbacio_4.a
    ├── libbacio_8.a
    ├── libbufr_11.1.0_4_64.a
    ├── libbufr_11.1.0_4_64_DA.a
    ├── libbufr_11.1.0_8_64.a
    ├── libbufr_11.1.0_8_64_DA.a
    ├── libbufr_11.1.0_d_64.a
    ├── libbufr_11.1.0_d_64_DA.a
    ├── libbufr_11.1.0_s_64.a
    ├── libbufr_v10.2.5_4_64.a
    ├── libbufr_v10.2.5_8_64.a
    ├── libbufr_v10.2.5_d_64.a
    ├── libbufr_v10.2.5_s_64.a
    ├── libg2_4.a
    ├── libg2_d.a
    ├── libg2tmpl.a
    ├── libgfsio_4.a
    ├── libip_4.a
    ├── libip_8.a
    ├── libip_d.a
    ├── libnemsio_v2.2.2.a
    ├── libsfcio_big_4.a
    ├── libsigio_v2.0.1.a
    ├── libsp_v2.0.2_4.a
    ├── libsp_v2.0.2_8.a
    ├── libsp_v2.0.2_d.a
    ├── libtransutil_4.a
    ├── libtransutil_8.a
    ├── libtransutil_d.a
    ├── libw3emc_4.a
    ├── libw3emc_8.a
    ├── libw3emc_d.a
    ├── libw3nco_4.a
    ├── libw3nco_8.a
    ├── libw3nco_d.a
    ├── libxmlparse.a
    ├── make.log
    ├── progress.stat
    └── sorc

Building `gempak <https://www.unidata.ucar.edu/software/gempak/>`_
==================================================================

* enter into gempak directory::

    > cd /nwprod/gempak/NAWIPS

* setup the necessary environment variables::

    > . ./Gemenviron.profile

* compile::

    > make everything

* it makes lots of libs which will be used by decoders::

    > tree -L 1 os/linux64
    os/linux64
    ├── bin
    ├── include
    ├── lib
    └── share

Building utilities
==================

* enter into directory::

    > cd /nwprod

* compile::

    > ./build2.bash

* it compiles some utilities related to the grib file operators::

    > tree -L 1 util/exec/
    util/exec/
    ├── cnvgrib
    ├── copygb
    ├── copygb2
    ├── cwordsh
    ├── debufr
    ├── grb2index
    ├── grbindex
    ├── ndate
    ├── nhour
    ├── tocgrib
    ├── tocgrib2
    ├── wgrib
    └── wgrib2

Building obsproc
================

* enter into directory::

    > cd /nwprod

* compile::

    > ./build_obsproc.bash

* it compiles all the obsproc executables::

    > tree -L 1 obsproc_*/exec
    obsproc_dump.v3.2.1/exec
    ├── bufr_chkbfr
    ├── bufr_combfr
    ├── bufr_dcodwindsat
    ├── bufr_dumpmd
    ├── bufr_dupair
    ├── bufr_dupcor
    ├── bufr_dupmar
    ├── bufr_dupmrg
    ├── bufr_duprad
    ├── bufr_dupsat
    ├── bufr_dupshp
    ├── bufr_dupsst
    ├── bufr_edtbfr
    ├── bufr_geofil
    ├── bufr_quipc
    ├── bufr_raddate
    ├── bufr_supertmi
    ├── prepobs_prepssmi
    └── wave_dcodquikscat
    obsproc_dump_post.v3.1.0/exec
    ├── bufr_datacount
    └── bufr_listdumps
    obsproc_prep.v5.0.0/exec
    ├── prepobs_cqcbufr
    ├── prepobs_cqcvad
    ├── prepobs_glerladj
    ├── prepobs_listheaders
    ├── prepobs_monoprepbufr
    ├── prepobs_mpcopybufr
    ├── prepobs_oiqcbufr
    ├── prepobs_prepacpf
    ├── prepobs_prepacqc
    ├── prepobs_prepanow
    ├── prepobs_prepdata
    ├── prepobs_prevents
    ├── prepobs_profcqc
    └── syndat_syndata
    obsproc_prep_post.v3.0.0/exec
    ├── gdascounts_ave
    ├── global_postevents
    └── timetwin

Building decoders
=================

* enter into directory::

    > cd /nwprod/decoders/decod_shared

* compile::

    > ./build.bash

* it compiles the decoders for different type obs.::

    > tree -L 1 -I "tmp|*tbl|*headers|*log|fort*|*ksh|bufrtab*" decoders/decod_*/exec
    decoders/decod_dcacft/exec
    └── decod_dcacft
    decoders/decod_dcacft_v3.3.0/exec
    └── decod_dcacft
    decoders/decod_dcaxbt/exec
    └── decod_dcaxbt
    decoders/decod_dcaxbt_v3.0.0/exec
    └── decod_dcaxbt
    decoders/decod_dcbthy/exec
    └── decod_dcbthy
    decoders/decod_dcbthy_v3.0.0/exec
    └── decod_dcbthy
    decoders/decod_dccgrd/exec
    └── decod_dccgrd
    decoders/decod_dccgrd_v3.0.0/exec
    └── decod_dccgrd
    decoders/decod_dccimiss/exec
    └── decod_dccimiss
    decoders/decod_dccimiss_v3.0.0/exec
    └── decod_dccimiss
    decoders/decod_dccimissupr/exec
    ├── decod_dccmissupr
    └── decod_dcusnd
    decoders/decod_dccoop/exec
    decoders/decod_dccoop_v3.0.0/exec
    decoders/decod_dccrn/exec
    decoders/decod_dccrn_v3.0.0/exec
    decoders/decod_dccsev/exec
    └── decod_dccsev
    decoders/decod_dccsev_v3.0.0/exec
    └── decod_dccsev
    decoders/decod_dccsjp/exec
    decoders/decod_dccsjp_v3.0.0/exec
    decoders/decod_dcdrbu/exec
    └── decod_dcdrbu
    decoders/decod_dcdrbu_v3.0.0/exec
    └── decod_dcdrbu
    decoders/decod_dcelrw/exec
    └── decod_dcelrw
    decoders/decod_dcelrw_v3.0.0/exec
    └── decod_dcelrw
    decoders/decod_dcepfl/exec
    └── decod_dcepfl
    decoders/decod_dcepfl_v3.0.0/exec
    └── decod_dcepfl
    decoders/decod_dcgpsw/exec
    └── decod_dcgpsw
    decoders/decod_dcgpsw_v3.0.0/exec
    └── decod_dcgpsw
    decoders/decod_dchydr/exec
    decoders/decod_dchydr_v3.0.0/exec
    decoders/decod_dcigdr/exec
    └── decod_dcigdr
    decoders/decod_dcigdr_v3.0.0/exec
    └── decod_dcigdr
    decoders/decod_dcjpfl/exec
    └── decod_dcjpfl
    decoders/decod_dcjpfl_v3.0.0/exec
    └── decod_dcjpfl
    decoders/decod_dckora/exec
    └── decod_dckora
    decoders/decod_dckora_v3.0.0/exec
    └── decod_dckora
    decoders/decod_dclsfc/exec
    └── decod_dccimiss
    decoders/decod_dclsfc_v3.0.0/exec
    └── decod_dccimiss
    decoders/decod_dcmap/exec
    decoders/decod_dcmap_v3.0.0/exec
    decoders/decod_dcmeso/exec
    decoders/decod_dcmeso_v3.0.0/exec
    decoders/decod_dcmetr/exec
    └── decod_dcmetr
    decoders/decod_dcmetr_v3.1.0/exec
    └── decod_dcmetr
    decoders/decod_dcmopf/exec
    └── decod_dcmopf
    decoders/decod_dcmopf_v3.0.0/exec
    └── decod_dcmopf
    decoders/decod_dcmssf/exec
    └── decod_dcmssf
    decoders/decod_dcmssf_v3.0.0/exec
    └── decod_dcmssf
    decoders/decod_dcnxrd/exec
    └── decod_dcnxrd
    decoders/decod_dcnxrd_v3.0.0/exec
    └── decod_dcnxrd
    decoders/decod_dcozon/exec
    └── decod_dcozon
    decoders/decod_dcozon_v3.0.0/exec
    └── decod_dcozon
    decoders/decod_dcp3rd/exec
    └── decod_dcp3rd
    decoders/decod_dcp3rd_v3.0.0/exec
    └── decod_dcp3rd
    decoders/decod_dcpflr/exec
    └── decod_dcpflr
    decoders/decod_dcpflr_v3.0.0/exec
    └── decod_dcpflr
    decoders/decod_dcrast/exec
    └── decod_dcrast
    decoders/decod_dcrast_v3.0.0/exec
    └── decod_dcrast
    decoders/decod_dcrocc/exec
    └── decod_dcrocc
    decoders/decod_dcrocc_v3.0.0/exec
    └── decod_dcrocc
    decoders/decod_dcscd/exec
    └── decod_dcscd
    decoders/decod_dcscd_v3.0.0/exec
    └── decod_dcscd
    decoders/decod_dcsynp/exec
    └── decod_dcsynp
    decoders/decod_dcsynp_v3.7.0/exec
    └── decod_dcsynp
    decoders/decod_dctama/exec
    decoders/decod_dctama_v3.0.0/exec
    decoders/decod_dctidg/exec
    └── decod_dctidg
    decoders/decod_dctidg_v3.0.0/exec
    └── decod_dctidg
    decoders/decod_dcusnd/exec
    ├── decod_dccmissupr
    └── decod_dcusnd
    decoders/decod_dcusnd_v3.0.0/exec
    ├── decod_dccmissupr
    └── decod_dcusnd
    decoders/decod_dczsfc/exec
    └── decod_dczsfc
