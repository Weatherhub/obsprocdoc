===================
后处理
===================

.. contents ::

提取质控标识
==============

为了了解质控的步骤和结果，可以使用如下几种方法提取质控码：

1. 执行以下脚本::

    > find /home/zwtd/nwprod/com/rap/prod -name "rap.t??z.prepbufr.tm00" -exec python read_qcf.py -f {} \;

2. 执行以下程序::

    > ln -fs  /nwprod/com/rap/prod/rap.20181216/rap.t12z.prepbufr.tm00 prepbufr
    > /nwprod/util/exec/bufrqc

.. note ::
    
     可以进入 :code:`/nwpprod/util/sorc/bufrqc.fd`，修改程序 :code:`prepbufr_decode_all_evn.f90` 以获得个性化输出。ss s