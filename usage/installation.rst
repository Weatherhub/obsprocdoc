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
