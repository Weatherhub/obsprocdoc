============
Installation
============

.. contents ::

Installing the Singularity
==========================

The whole system requires to be run with *Singularity*. To install Singualrity:

* please refer to `Singularity Homepage <https://www.sylabs.io/>`_

* shell into intel.simg::

    > singularity shell -B /Users/xinzhang/work/LR-App-Store/nwprod:/nwprod -e intel/intel.simg

.. note::
    make sure your local nwprod directory is mounted as /nwprod in Singualrity container.



Building the NCEP libraries
===========================

* enter into NCEP libraries' directory::

    > cd /nwprod/lib

* compile the libraries::

    > ./build1.bash

* If successfully compiled::

    > cpaessxinzhang-mpro:lib xinzhang$ tree -L 1
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

Building the gempak
===================

* enter into gempak directory::

    > cd /nwprod/gempak/NAWIPS

* setup the necessary environment variables::

    > . ./Gemenviron.profile

* compile

    > make everything

Building utilities
==================

* enter into directory::
    
    > cd /nwprod

* compile

    > ./build2.bash

Building obsproc
================

* enter into directory::

    > cd /nwprod

* compile::

    > ./build_obsproc.bash

