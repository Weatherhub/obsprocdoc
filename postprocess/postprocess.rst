===================
后处理
===================

.. contents ::

提取质控标识
==============

为了了解质控的步骤和结果，可以使用如下几种方法提取质控码：

1. 执行以下脚本::

    > find /home/zwtd/nwprod/com/rap/prod -name "rap.t??z.prepbufr.tm00" -exec python read_qcf.py -f {} \;

    提取的质控代码如下，如飞机观测::

.. code :: console

    CNCOVK1    116.47    29.60 2018-12-16 13:00:00 131 01
    PQM QQM TQM ZQM WQM NUL PWQ PMQ
    [2.0 -- 13.0 2.0 -- -- -- --]
    CNGOWP1    109.75    21.45 2018-12-16 13:00:00 131 01
    PQM QQM TQM ZQM WQM NUL PWQ PMQ
    [2.0 -- 13.0 2.0 -- -- -- --]
    CNGOWP1    109.28    21.77 2018-12-16 13:00:00 131 01
    PQM QQM TQM ZQM WQM NUL PWQ PMQ
    [2.0 -- 13.0 2.0 -- -- -- --]
    CNCOVK1    116.18    29.28 2018-12-16 13:00:00 131 01
    PQM QQM TQM ZQM WQM NUL PWQ PMQ
    [2.0 -- 13.0 2.0 -- -- -- --]
    CNFOSS1    117.90    29.45 2018-12-16 13:00:00 131 01
    PQM QQM TQM ZQM WQM NUL PWQ PMQ
    [2.0 -- 13.0 2.0 -- -- -- --]


2. 执行以下程序::

    > ln -fs  /nwprod/com/rap/prod/rap.20181216/rap.t12z.prepbufr.tm00 prepbufr
    > /nwprod/util/exec/bufrqc

.. note ::
    
     可以进入 :code:`/nwpprod/util/sorc/bufrqc.fd`，修改程序 :code:`prepbufr_decode_all_evn.f90` 以获得个性化输出。