===================
运行步骤
===================

1. 信息的提取
    
    请参考 :doc:`Decoders <radiosonde>` 。

2. 解码
    
    请参考

3. 运行 **dump** 和 **obsproc**

.. code-block :: bash

    > cd /nwpprod
    > ./run_obsproc.py -s 2018120100 -e 2018121512

:code:`run_obsproc.py` 调用 :code:`run_rap_obsproc.bash`, :code:`run_rap_obsproc.bash` 的内容如下:

.. code-block :: bash

    > cat run_rap_obsproc.bash 
    #!/bin/bash -e

    ulimit -s unlimited

    if [[ $# -eq 0 ]]; then
      echo "No cycle is given"
      echo "Usage:: run_rap_obsproc.bash 00"
      exit
    fi

    # Common setting
    export ROOT_DIR=/nwprod
    export NWROOT=${ROOT_DIR}
    export DATAROOT=${ROOT_DIR}/tmpprod
    export COMIN_ROOT=${ROOT_DIR}/com
    export COMROOT=${ROOT_DIR}/com

    # default root directory path to $TANK, $EPRM and $QPRM
    export DCOMROOT=${ROOT_DIR}/dcom

    # Where is the utility scripts
    export UTILROOT=${ROOT_DIR}/util
    export utilscript=${ROOT_DIR}/util/ush

    export NDATE=${UTILROOT}/exec/ndate
    export NHOUR=${UTILROOT}/exec/nhour

    export grib_util_ver=1.0.5

    # Run locally and background threads
    export sys_tp="local"
    export launcher="background"

    # root directory tree for the path to temporary work files
    export TMPDIR=/tmp

    # Geographical filtering of the data
    export LALO=0

    # 
    export RUN_ENVIR="nco"
    export envir="prod"

    export KEEPDATA="NO"
    export LOUD="off"

    ############################################
    # SENDCOM  - Copy files to $COMOUT directory
    # SENDECF  - Flag Events on ECFLOW
    # SENDDBN  - Alert output file to TOC
    ############################################
    export SENDCOM=YES
    export SENDECF=NO
    export SENDDBN=NO

    export PROCESS_GRIBFLDS="NO"
    export PROCESS_REMOREST="NO"

    # Only conventional data being processed
    export JOB_NUMBER=1

    # Which group will be processed
    export DUMP_group2="YES"
    export DUMP_group3="YES"
    export DUMP_group4="NO"
    export DUMP_group5="NO"

    export MPMD=NO
    export CHGRP_RSTPROD=NO

    export POE="NO"

    export NET="rap"
    export cyc=$1
    export job=${NET}_dump_${cyc}

    . ${ROOT_DIR}/versions/obsproc_rap.ver
    ${ROOT_DIR}/obsproc_rap.v3.0.0/jobs/JRAP_DUMP
    ${ROOT_DIR}/obsproc_rap.v3.0.0/jobs/JRAP_DUMP_POST

    export GETGUESS="YES"
    export NEMSIO_IN=.true.
    export job=${NET}_obsproc_${cyc}
    export GESROOT=/nwprod/com/gfs
    ${ROOT_DIR}/obsproc_rap.v3.0.0/jobs/JRAP_PREP

4. 检查运行结果

.. code :: bash

    > find /nwprod/com/rap -name rap.t??z.prepbufr.tm00 -exec ls -la {} \;
    -rw-r--r--. 1 zwtd zwtd 142960 Dec 17 17:17 /nwprod/com/rap/prod/rap.20180706/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 102472 Dec 17 13:19 /nwprod/com/rap/prod/rap.20180430/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 114824 Dec 17 16:32 /nwprod/com/rap/prod/rap.20180430/rap.t12z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 125584 Dec 17 16:33 /nwprod/com/rap/prod/rap.20180501/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 159824 Dec 17 16:33 /nwprod/com/rap/prod/rap.20180501/rap.t12z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 130096 Dec 17 16:34 /nwprod/com/rap/prod/rap.20180502/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 166208 Dec 17 16:34 /nwprod/com/rap/prod/rap.20180502/rap.t12z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 163704 Dec 17 16:35 /nwprod/com/rap/prod/rap.20180503/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 171776 Dec 17 16:35 /nwprod/com/rap/prod/rap.20180503/rap.t12z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 152832 Dec 17 16:36 /nwprod/com/rap/prod/rap.20180504/rap.t00z.prepbufr.tm00
    -rw-r--r--. 1 zwtd zwtd 159344 Dec 17 16:37 /nwprod/com/rap/prod/rap.20180504/rap.t12z.prepbufr.tm00
    ...
    ...
