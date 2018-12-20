===================
质量控制
===================

.. contents ::

Purpose
=======

* The "PREPBUFR" processing is the final step in preparing the majority of conventional observational data for assimilation into the various analyses.

* This step involves the execution of series of programs designed to assemble observations dumped from a number of on-line decoder databases:

    * encode information about the observational error for each data type as well the background (first guess) interpolated to each data location
    * perform both rudimentary multi-platform quality control and more complex platform-specific quality control
    * store the output in a monolithic BUFR file, known as PREPBUFR.

* Generated on production machine in each network from conventional data dump files

    * adpsfc, adpupa, aircar, aircft, ascatw, atovs, goesnd, gpsipw, msonet, proflr, rassda, satwnd (except for GFS/GDAS), sfcshp, vadwnd, wndsat

* Network-specific parm cards control processing
* Structure defined by input PrepBUFR mnemonic table
* BUFR message types can include:

    * ADPUPA, AIRCAR, AIRCFT, SATWND, PROFLR, VADWND, SATEMP, ADPSFC, SFCSHP, SFCBOG, SPSSMI, SYNDAT, ERS1DA, GOESND, QKSWND, MSONET, GPSIPW, RASSDA, WDSATR, ASCATW (what is present depends on the network)
    * Each message type has its own BUFR structure as defined in the PrepBUFR mnemonic table

* In :code:`/nwprod/com/NET/prod/RUN.yyyymmdd/MODEL.tcycz.prepbufr.tmMM`, where:

    * **NET(RUN/MODEL)** is either: nam(nam/nam), nam(ndas/ndas), rap(rap/rap), rap(rap_p/rap_p), rtma(rtma/rtma)
    * **cyc** is cycle (hourly for NET=rap, rtma; 00, 06, 12, 18 all others)
    * **MM** is 00 for all types except RUN/MODEL=ndas/ndas where it can be 12, 09, 06 or 03


质控步骤
==============

1. PREPDATA
^^^^^^^^^^^^
    * **总体质量控制**
    * 读入并合并从各个BUFR数据库中得到的各种观测资料，对数据进行初步检查，并按照气压值组织高空数据（降序)
    * *为气候模式分析准备观测资料不运行*
    * 执行名称为GBLEVENTS的多种质控任务:
        * 在每个观测位置插入的预报的背景场的值（第一次猜值场）
        * 向每个观测中添加观测误差（从查询表中读入）
        * 比照背景场对地面气压进行一些初步的质量控制检查
        * 对地面观测，将干球温度转换为虚温；由露点计算比湿 
    * 为中尺度分析准备观测资料，只执行第4项
    * 输出存储在名为PREPBUFR的BUFR文件中

2. GLERLADJ
^^^^^^^^^^^^^
    * **对大的水体周边观测的调整**
    * *仅在为中尺度分析模式准备观测资料时运行*
    * 对大面积江、湖地区陆地和海洋数据的调整
    * 目标是在大水体区域上创建一个平滑的风分析

3. PREVENTS 
^^^^^^^^^^^^^
    * *仅在为气候模式分析准备观测资料时运行*
    * 将预测背景场（来自气候模式本身的第一猜值场）插入到每个观测的位置
    * 将与每个观测相关联的观测误差（从查找表中读入）添加到PREPBUFR文件
    * 比照背景场，对地面气压进行一些粗略的质量控制检查
    * 对地面观测，将干球温度转换为虚温；由露点温度计算比湿

4. CQCBUFR
^^^^^^^^^^^^^
    * **对探空观测的质控**
    * 对探空观测的高度和温度记录进行复杂的质量控制，以识别或纠正由地理位置，记录或通信错误照成的错误记录。在适当的情况下，尝试纠正常见类型的错误
    * 标记无法纠正的错误数据，分析时不会考虑这些数据
    * 使用的质控检查包括:
        * 流体静力学检查
        * 增量检查
        * 水平统计
        * 垂直统计
        * 时间连续性检查（仅在为气候模式准备观测中使用）
        * 观测值范围基准检查
        * 垂直递减率检查
    * 以上检查基于与六小时全球资料同化系统预测（即背景初猜场）的差异
    * 对探空观测的高度和温度数据进行辐射校正。辐射校正是探空仪器类型，太阳角度和垂直压力水平的函数
    * 将探空观测的干球温度转换为虚温；由露点温度计算比湿

5. PROFCQC
^^^^^^^^^^^^^
    * **对飞机观测的质控**
    * *在中尺度分析中不运行*
    * 对风廓线仪和声学测深仪（SODAR）数据执行复杂的质量控制，以便识别错误数据并将其从分析中排除
    * 使用的检查是：
        * 增量检查
        * 垂直统计检查
        * 时间统计检查
        * 组合垂直 - 时间检查 
    * 这些质控也是基于与六小时全球资料同化系统预测的差异

6. PREPACQC
^^^^^^^^^^^^^
    * **对风廓线仪观测的质控**
    * 对常规AIREP，PIREP，AMDAR，TAMDAR和MDCRS的飞机风，温度，和水汽观测（若有）进行全面质量控制
    * 质控检查包括：
        * 重复记录检查
        * 极值检查
        * 无效报告
        * 卡住值（Stuck Value)
        * 总值（Gross Value)
        * 位置的一致性
        * 排序
        * 可疑数据
        * 黑名单检查
        * 详细的飞行轨道检查
    * 基本质量控制算法由Patricia Pauley博士在海军研究实验室（NRL）编写

7. OIQCBUFR
^^^^^^^^^^^^^
    * **Buddy Check**
    * 对PREPBUFR文件中的完整观测数据集执行基于最优插值的质量控制
    * 使用所有的观测来执行独立的质控检查：
        * 水平检查
        * 垂直检查
        * 地转平衡检查
    * 在每次检查中，使用除自身之外的所有观测对每个观测进行最优插值
    * 最终的质量决定（保持，抛弃或低置信度），将基于所有先前的质量控制的结果
    * 执行多变量地面风分析，并将分析得到的风向分配给SSM/I海洋风速观测，以便为这些数据产生风向量



Quality Marker Table
====================

Most of the observation types in the PREPBUFR file are associated with quality markers (e.g., mnemonics “PQM, “TQM”, “WQM”, etc.).  These are used by the various analyses to place a weight on the data based on its quality.
`质控标识表 <http://www.emc.ncep.noaa.gov/mmb/data_processing/prepbufr.doc/table_7.htm>`_ contains the code table of quality markers.  These quality markers apply to all observation types in the PREPBUFR file.