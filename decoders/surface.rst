=======
Surface
=======

.. contents ::

Directory structure
===================

The Surface data is organized as xml files every 15 minutes ::

    > tree -L 1 SURF_CHN_MAIN_MIN|more
    SURF_CHN_MAIN_MIN
    ├── 201807032000.xml
    ├── 201807032015.xml
    ├── 201807032030.xml
    ├── 201807032045.xml
    ├── 201807032100.xml
    ├── 201807032115.xml
    ├── 201807032130.xml
    ├── 201807032145.xml
    ├── 201807032200.xml
    ├── 201807032215.xml
    ├── 201807032230.xml
    ├── 201807032245.xml
    ├── 201807032300.xml
    ├── 201807032315.xml
    ├── 201807032330.xml
    ├── 201807032345.xml
    ├── 201807040000.xml
    ├── 201807040015.xml
    ......


Data format
===========

xml format data is looks like 
::

<?xml version="1.0" encoding="UTF-8"?>
<DS returnCode="0" returnMessage="Query Succeed" rowCount="48599" colCount="44" requestParams="times=20180901160000&amp;datacode=SURF_CHN_MAIN_MIN&amp;elements=Station_Name,Country,Province,City,Cnty,Town,Station_Id_C,Station_Id_d,Lat,Lon,Alti,PRS_Sensor_Alti,Station_Type,Station_levl,Admin_Code_CHN,Year,Mon,Day,Hour,Min,PRS,TEM,RHU,WIN_D_Avg_1mi,WIN_S_Avg_1mi,LGST,GST,GST_5cm,GST_10cm,GST_15cm,GST_20cm,GST_40Cm,Q_PRS,Q_TEM,Q_RHU,Q_WIN_D_Avg_1mi,Q_WIN_S_Avg_1mi,Q_LGST,Q_GST,Q_GST_5cm,Q_GST_10cm,Q_GST_15cm,Q_GST_20cm,Q_GST_40Cm" requestTime="2018-09-01 16:15:32" responseTime="2018-09-01 16:15:47" takeTime="14.888" fieldNames="站名 国家 省份 地市 区县 乡镇 区站号(字符) 区站号(数字) 纬度 经度 测站高度 气压传感器海拔高度 测站类型 测站级别 行政区代码 年 月 日 时 分 气压 温度/气温 相对湿度 1分钟平均风向 1分钟平均风速 草面(雪面)温度 地面温度 5cm地温 10cm地温 15cm地温 20cm地温 40cm地温 气压质控码 温度/气温质控码 相对湿度质控码 1分钟平均风向质控码 1分钟平均风速质控码 草面(雪面)温度质控码 地面温度质控码 5cm地温质控码 10cm地温质控码 15cm地温质控码 20cm地温质控码 40cm地温质控码" fieldUnits="- - - - - - - - 度 度 米 米 - - - 年 月 日 时 分钟 百帕 摄氏度(℃) 百分率 度 米/秒 摄氏度(℃) 摄氏度(℃) 摄氏度(℃) 摄氏度(℃) 摄氏度(℃) 摄氏度(℃) 摄氏度(℃) - - - - - - - - - - - -">
<R Station_Name="嫩洼" Country="中国" Province="四川省" City="阿坝藏族羌族自治州" Cnty="若尔盖县" Town="" Station_Id_C="56076" Station_Id_d="56076" Lat="33.85" Lon="102.6333" Alti="3429" PRS_Sensor_Alti="3430.5" Station_Type="0" Station_levl="999999" Admin_Code_CHN="513232" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="674.7" TEM="10.8" RHU="97" WIN_D_Avg_1mi="149" WIN_S_Avg_1mi="3.4" LGST="11.2" GST="11.4" GST_5cm="12.5" GST_10cm="14.5" GST_15cm="15.9" GST_20cm="16.6" GST_40Cm="13.8" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="0" Q_GST="0" Q_GST_5cm="0" Q_GST_10cm="0" Q_GST_15cm="0" Q_GST_20cm="0" Q_GST_40Cm="0"/>
<R Station_Name="卜尔汉图镇" Country="中国" Province="内蒙古自治区" City="包头市" Cnty="" Town="" Station_Id_C="C4002" Station_Id_d="674002" Lat="40.6644" Lon="109.6661" Alti="1052" PRS_Sensor_Alti="1053" Station_Type="0" Station_levl="16" Admin_Code_CHN="150200" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="890.2" TEM="15" RHU="95" WIN_D_Avg_1mi="2" WIN_S_Avg_1mi="1.3" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="金阁" Country="中国" Province="安徽省" City="芜湖市" Cnty="南陵县" Town="" Station_Id_C="I5904" Station_Id_d="735904" Lat="31.0231" Lon="118.4314" Alti="9" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="340223" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="26.4" RHU="999999" WIN_D_Avg_1mi="158" WIN_S_Avg_1mi="1.7" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="交口" Country="中国" Province="陕西省" City="西安市" Cnty="临潼区" Town="" Station_Id_C="V8552" Station_Id_d="868552" Lat="34.55" Lon="109.2975" Alti="357" PRS_Sensor_Alti="358" Station_Type="0" Station_levl="16" Admin_Code_CHN="610115" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="965.8" TEM="24.9" RHU="74" WIN_D_Avg_1mi="356" WIN_S_Avg_1mi="0.9" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="高要区活道镇首岭村委会明村" Country="中国" Province="广东省" City="肇庆市" Cnty="" Town="" Station_Id_C="G8262" Station_Id_d="718262" Lat="22.8133" Lon="112.4264" Alti="49" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="441200" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="25.4" RHU="999999" WIN_D_Avg_1mi="225" WIN_S_Avg_1mi="0" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="高圳村" Country="中国" Province="福建省" City="三明市" Cnty="建宁县" Town="" Station_Id_C="F8128" Station_Id_d="708128" Lat="26.8458" Lon="116.7783" Alti="343" PRS_Sensor_Alti="343" Station_Type="0" Station_levl="14" Admin_Code_CHN="350430" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="970.6" TEM="22.9" RHU="96" WIN_D_Avg_1mi="176" WIN_S_Avg_1mi="1.1" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="耦山" Country="中国" Province="安徽省" City="铜陵市" Cnty="枞阳县" Town="" Station_Id_C="I7152" Station_Id_d="737152" Lat="30.7728" Lon="117.3278" Alti="28.3" PRS_Sensor_Alti="28.3" Station_Type="0" Station_levl="14" Admin_Code_CHN="340722" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="1005.9" TEM="26.3" RHU="97" WIN_D_Avg_1mi="135" WIN_S_Avg_1mi="0.6" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="澧浦" Country="中国" Province="浙江省" City="金华市" Cnty="金东区" Town="" Station_Id_C="K6060" Station_Id_d="756060" Lat="29.1036" Lon="119.8056" Alti="58" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="330703" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="26.5" RHU="999999" WIN_D_Avg_1mi="210" WIN_S_Avg_1mi="1.1" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="黄茅园站" Country="中国" Province="湖南省" City="怀化市" Cnty="溆浦县" Town="" Station_Id_C="P4130" Station_Id_d="804130" Lat="27.4056" Lon="110.4781" Alti="200" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="431224" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="23.1" RHU="999999" WIN_D_Avg_1mi="999999" WIN_S_Avg_1mi="999999" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="7" Q_WIN_S_Avg_1mi="7" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="灰腾梁" Country="中国" Province="内蒙古自治区" City="锡林郭勒盟" Cnty="锡林浩特市" Town="" Station_Id_C="C2002" Station_Id_d="672002" Lat="43.2972" Lon="116.1158" Alti="1284" PRS_Sensor_Alti="1285" Station_Type="0" Station_levl="16" Admin_Code_CHN="152502" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="860" TEM="13.9" RHU="94" WIN_D_Avg_1mi="217" WIN_S_Avg_1mi="7.6" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="隔河头" Country="中国" Province="河北省" City="秦皇岛市" Cnty="青龙满族自治县" Town="" Station_Id_C="B3689" Station_Id_d="663689" Lat="40.2278" Lon="119.22" Alti="300" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="130321" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="19.2" RHU="999999" WIN_D_Avg_1mi="999999" WIN_S_Avg_1mi="999999" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="7" Q_WIN_S_Avg_1mi="7" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="黄湖农场" Country="中国" Province="浙江省" City="宁波市" Cnty="余姚市" Town="" Station_Id_C="K2628" Station_Id_d="752628" Lat="30.1492" Lon="121.1961" Alti="5" PRS_Sensor_Alti="0" Station_Type="0" Station_levl="14" Admin_Code_CHN="330281" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="28.1" RHU="999999" WIN_D_Avg_1mi="237" WIN_S_Avg_1mi="1.6" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="淳化卜家" Country="中国" Province="陕西省" City="咸阳市" Cnty="淳化县" Town="" Station_Id_C="V0410" Station_Id_d="860410" Lat="34.9769" Lon="108.5269" Alti="1193" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="610430" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="19.8" RHU="999999" WIN_D_Avg_1mi="999999" WIN_S_Avg_1mi="999999" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="7" Q_WIN_S_Avg_1mi="7" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="户县原种场" Country="中国" Province="陕西省" City="西安市" Cnty="鄠邑区" Town="" Station_Id_C="V8283" Station_Id_d="868283" Lat="34.2217" Lon="108.5681" Alti="394.5" PRS_Sensor_Alti="394.5" Station_Type="0" Station_levl="14" Admin_Code_CHN="610118" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="959.8" TEM="26.9" RHU="64" WIN_D_Avg_1mi="302" WIN_S_Avg_1mi="1" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="兰亭" Country="中国" Province="浙江省" City="绍兴市" Cnty="柯桥区" Town="" Station_Id_C="K4019" Station_Id_d="754019" Lat="29.9078" Lon="120.4844" Alti="59" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="330603" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="24.6" RHU="999999" WIN_D_Avg_1mi="324" WIN_S_Avg_1mi="0" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="东关" Country="中国" Province="甘肃省" City="庆阳市" Cnty="合水县" Town="" Station_Id_C="W8120" Station_Id_d="878120" Lat="36.0133" Lon="108.1183" Alti="1129" PRS_Sensor_Alti="0" Station_Type="0" Station_levl="14" Admin_Code_CHN="621024" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="876.3" TEM="17.5" RHU="99" WIN_D_Avg_1mi="329" WIN_S_Avg_1mi="1.4" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="2" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="幸福村" Country="中国" Province="浙江省" City="杭州市" Cnty="建德市" Town="" Station_Id_C="K1675" Station_Id_d="751675" Lat="29.6344" Lon="119.5692" Alti="95" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="330182" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="24.7" RHU="999999" WIN_D_Avg_1mi="333" WIN_S_Avg_1mi="0" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="花果村" Country="中国" Province="陕西省" City="汉中市" Cnty="汉台区" Town="" Station_Id_C="V6005" Station_Id_d="866005" Lat="33.2" Lon="106.9833" Alti="818" PRS_Sensor_Alti="819" Station_Type="0" Station_levl="16" Admin_Code_CHN="610702" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="916.1" TEM="25.9" RHU="68" WIN_D_Avg_1mi="78" WIN_S_Avg_1mi="4.1" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="0" Q_TEM="0" Q_RHU="0" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="里仁村" Country="中国" Province="安徽省" City="安庆市" Cnty="岳西县" Town="" Station_Id_C="I6672" Station_Id_d="736672" Lat="30.7747" Lon="116.1697" Alti="526.4" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="340828" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="22.8" RHU="999999" WIN_D_Avg_1mi="141" WIN_S_Avg_1mi="1.6" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="牛扎坪" Country="中国" Province="湖北省" City="宜昌市" Cnty="" Town="" Station_Id_C="Q4008" Station_Id_d="814008" Lat="30.7667" Lon="111.25" Alti="212" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="420500" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="25.4" RHU="999999" WIN_D_Avg_1mi="320" WIN_S_Avg_1mi="1" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="0" Q_WIN_S_Avg_1mi="0" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="坪中" Country="中国" Province="重庆市" City="市辖区" Cnty="璧山区" Town="" Station_Id_C="A8290" Station_Id_d="658290" Lat="29.3111" Lon="106.0942" Alti="404" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="500120" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="30.6" RHU="999999" WIN_D_Avg_1mi="999999" WIN_S_Avg_1mi="999999" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="7" Q_WIN_S_Avg_1mi="7" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>
<R Station_Name="麻雀岩水库" Country="中国" Province="重庆市" City="市辖区" Cnty="荣昌区" Town="" Station_Id_C="A8279" Station_Id_d="658279" Lat="29.4319" Lon="105.4728" Alti="369" PRS_Sensor_Alti="999999" Station_Type="0" Station_levl="14" Admin_Code_CHN="500153" Year="2018" Mon="9" Day="1" Hour="16" Min="0" PRS="999999" TEM="26.6" RHU="999999" WIN_D_Avg_1mi="999999" WIN_S_Avg_1mi="999999" LGST="999999" GST="999999" GST_5cm="999999" GST_10cm="999999" GST_15cm="999999" GST_20cm="999999" GST_40Cm="999999" Q_PRS="7" Q_TEM="0" Q_RHU="7" Q_WIN_D_Avg_1mi="7" Q_WIN_S_Avg_1mi="7" Q_LGST="7" Q_GST="7" Q_GST_5cm="7" Q_GST_10cm="7" Q_GST_15cm="7" Q_GST_20cm="7" Q_GST_40Cm="7"/>


xml extractor
================

A python code is used to extract the desired information from this xml file::

    > python read_cimiss_surface.py > cimiss_data_surface

The information we want to extract from xml is.
::

    print s.attributes['Station_Id_d'].value, s.attributes['Lat'].value, s.attributes['Lon'].value, s.attributes['Alti'].value, \
        s.attributes['Year'].value, s.attributes['Mon'].value, s.attributes['Day'].value, s.attributes['Hour'].value, s.attributes['Min'].value, \
        s.attributes['PRS'].value, s.attributes['TEM'].value, s.attributes['RHU'].value, s.attributes['WIN_D_Avg_1mi'].value, s.attributes['WIN_S_Avg_1mi'].value

the content of **cimiss_data_surface** is::

    > less cimiss_data_surface
      56076 33.85 102.6333 3429 2018 9 1 16 0 674.7 10.8 97 149 3.4
      674002 40.6644 109.6661 1052 2018 9 1 16 0 890.2 15 95 2 1.3
      735904 31.0231 118.4314 9 2018 9 1 16 0 999999 26.4 999999 158 1.7
      868552 34.55 109.2975 357 2018 9 1 16 0 965.8 24.9 74 356 0.9
      718262 22.8133 112.4264 49 2018 9 1 16 0 999999 25.4 999999 225 0
      708128 26.8458 116.7783 343 2018 9 1 16 0 970.6 22.9 96 176 1.1
      737152 30.7728 117.3278 28.3 2018 9 1 16 0 1005.9 26.3 97 135 0.6
      756060 29.1036 119.8056 58 2018 9 1 16 0 999999 26.5 999999 210 1.1
      804130 27.4056 110.4781 200 2018 9 1 16 0 999999 23.1 999999 999999 999999
      672002 43.2972 116.1158 1284 2018 9 1 16 0 860 13.9 94 217 7.6
      663689 40.2278 119.22 300 2018 9 1 16 0 999999 19.2 999999 999999 999999
      752628 30.1492 121.1961 5 2018 9 1 16 0 999999 28.1 999999 237 1.6
      860410 34.9769 108.5269 1193 2018 9 1 16 0 999999 19.8 999999 999999 999999
      868283 34.2217 108.5681 394.5 2018 9 1 16 0 959.8 26.9 64 302 1
      754019 29.9078 120.4844 59 2018 9 1 16 0 999999 24.6 999999 324 0
      878120 36.0133 108.1183 1129 2018 9 1 16 0 876.3 17.5 99 329 1.4
      751675 29.6344 119.5692 95 2018 9 1 16 0 999999 24.7 999999 333 0

Source code
===========

1. Source code directory::

    > cd /nwprod/decoders/decod_dccimisssurf_v3.0.0/sorc

2. Subroutines to decode surface data

    * lsdcod.f

.. note::

    * The *cimiss.tbl* and *decod_WMO.Res40.headers* are not used, although they are required as arguments and read in.
    * The path and file name of *cimiss_data_surface* file are hard coded in the subroutines.

4. Compile the code
::

    > make

Decode and convert to BUFR format
=================================

1.  enter into the exec directory
::

    > cd /nwprod/decoders/decod_dccimisssurf_v3/exec
    > ls -la
    total 4048
    drwxr-xr-x  9 xinzhang  staff      288 Sep 21 18:46 .
    drwxr-xr-x  6 xinzhang  staff      192 Sep 21 18:46 ..
    lrwxr-xr-x  1 xinzhang  staff       34 Sep 21 18:46 bufrtab.000 -> ../../decod_shared/fix/bufrtab.000
    -rw-r--r--  1 xinzhang  staff  1121683 Sep 21 18:46 cimiss.tbl
    lrwxr-xr-x  1 xinzhang  staff       31 Sep 21 18:46 decod_WMO.Res40.headers -> ../parm/decod_WMO.Res40.headers
    -rwxr-xr-x  1 xinzhang  staff   940680 Sep 21 18:46 decod_dccimisssurf
    -rw-r--r--  1 xinzhang  staff      446 Sep 21 18:46 decod_dccimisssurf.log
    -rwxr-xr-x  1 xinzhang  staff      386 Sep 21 18:46 run.ksh
    drwxr-xr-x  3 xinzhang  staff       96 Sep 21 18:46 tmp


2. run the decoder script
::

    > run.ksh

    > cat run.ksh
    !/bin/bash
    export DBNBUFRT=120
    export TRANJB=/nwprod/ush/tranjb
    export tank_dir=/nwprod/dcom/us007003
    export DBNROOT=`pwd`
    rm tmp/*
    rm decod_dccimiss.log
    ./decod_dccimiss -d decod_dccimiss.log -b 240 -c 180901/1600 bufrtab.000 cimiss.tbl decod_WMO.Res40.headers
    ls -la tmp/*
    
    BUFR_FILES=$(echo tmp/BUFR*)
    echo ${BUFR_FILES}
    
    for file in ${BUFR_FILES}
    do
      ${TRANJB} ${tank_dir} ${file}
    done

.. note::

    * -c 180901/1600 : Set the **current time** (201809011600) used to calculate the time departures of the obs. data.
    * -b 240 : Number of hours to decode prior to "current" time (default)
    * The observations with date/time between **current time** - 240 hours and  **current time** + 3 are **kept**.

 3. The generated BUFR format file will be saved at
 ::

    > ls -la tmp/BUFR.0.aircraft.1.1933.1537419287.73 
    -rw-r--r--  1 xinzhang  staff  4199744 Sep 21 18:45 tmp/BUFR.0.cimiss.1.6436.1536097072.8


Transfer bufr data to BUFR Tanks
================================
* put data in BUFR **tanks**::

    > /nwprod/ush/tranjb /nwprod/dcom/us007003 tmp/BUFR.0.cimiss.1.6436.1536097072.8

    > ls -al /nwprod/dcom/us007003/20180901/b000/xx01 
    -rw-r--r-- 1 vagrant vagrant 4235328 Sep 27 04:42 /nwprod/dcom/us007003/20180901/b000/xx001 

.. note::

    * if environmental variable **SCREEN=ON** :
        * Define **Run Time** is the system time when the tranjb is running.
        * Only observations with date/time between **Run Time** - 10 days and **Run Time** + 12 hours are kept.
    * for retrospective run, set **SCREEN=OFF**
    * /nwprod/dcom/us007003/yyyymmdd/bmmm/xxsss (where mmm is WMO BUFR message type and xxx is local BUFR message subtype)
    * 000.001 (in dump group mnemonic adpsfc): Surface synoptic fixed land reports
    * BUFR format
    * Arranged by UTC day and continuously grow throughout the day, if you run decoders many time, the content of the file will grow
    * No QC (other than rudimentary checks inside decoders)
    * No duplicate checking
    * Interested users can use utility *debufr* to check the content of the bufr file::

        > /nwprod/util/execdebufr /nwprod/dcom/us007003/20180901/b000/xx001

      the output is in *debufr.out*.