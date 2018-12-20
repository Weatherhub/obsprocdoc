===================
后处理
===================

.. contents ::

提取质控标识
==============

执行以下脚本::

> find /home/zwtd/nwprod/com/rap/prod -name "rap.t??z.prepbufr.tm00" -exec python read_qcf.py -f {} \;
