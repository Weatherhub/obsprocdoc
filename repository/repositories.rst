===========
源代码的管理
===========

.. contents ::

获取源代码
==========================

使用git版本管理系统，获取源代码

* 在 :code:`$HOME` 目录下建立克隆 :code:`obsproc` ::
    
    > git clone https://github.com/LongRunWeather/NCEP-obsproc.git nwprod

*  进入 :code:`nwprod` 目录::

    > cd nwprod

* 克隆 :code:`lib` ::

    > git clone https://github.com/LongRunWeather/NCEP-libs.git lib

* 克隆 :code:`util` ::

    > git clone https://github.com/LongRunWeather/NCEP-util.git util

* 克隆 :code:`rap` ::

    > git clone https://github.com/LongRunWeather/NCEP-rap.git rap.v4.0.2

* 克隆 :code:`decoders` ::

    > git clone https://github.com/LongRunWeather/NCEP-Decoders.git decoders

* 下载最新版本的 `gempak <https://www.unidata.ucar.edu/downloads/gempak/index.jsp/>`_ ::

    > wget https://www.unidata.ucar.edu/downloads/gempak/latest/gempak-7.4.3.tar.gz
    > mkdir -p gempak
    > cd gempak
    > tar -xvzf gempak-7.4.3.tar.gz
 
* 目录结构应该是::

    > tree -L 1 nwprod
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
