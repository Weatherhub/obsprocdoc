===========
源代码的管理
===========

.. contents ::

获取源代码
==========================

使用git版本管理系统，获取源代码

* 在 :code:`$HOME` 目录下建立克隆obsproc::
    
    > git clone https://github.com/LongRunWeather/NCEP-obsproc.git nwprod

*  进入 :code:`nwprod` 目录::

    > cd nwprod

* 克隆lib::

    > git clone https://github.com/LongRunWeather/NCEP-libs.git lib

* 克隆util::

    > git clone https://github.com/LongRunWeather/NCEP-util.git util

* 克隆rap::

    > git clone https://github.com/LongRunWeather/NCEP-rap.git rap.v4.0.2

* 克隆decoders::

    > git clone https://github.com/LongRunWeather/NCEP-Decoders.git decoders

* 目录结构应该是::

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
