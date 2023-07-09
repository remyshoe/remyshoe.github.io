---
layout: default
---

#### Notes

| Keyword      | Contents          |
|:-------------|:------------------|
| AC voltage and frequency | (1) [List of Worldwide AC Voltages and Frequencies](https://www.school-for-champions.com/science/ac_world_volt_freq_list.htm#.Y8tQrnZBw2w)  ([PDF version](https://www.oaktreeproducts.com/img/product/description/List%20of%20Worldwide%20AC%20Voltages.pdf)) <br> (2) [List of Voltages & Frequencies (Hz) Around the World](https://www.generatorsource.com/Voltages_and_Hz_by_Country.aspx) |
| Barcode foramt | - Code 39 (Regular/Normal) DOESNOT support lowercase letters and * <br> - [Code 39 Full ASCII](https://barcodeguide.seagullscientific.com/Content/Symbologies/Code_39_Full_ASCII.htm#:~:text=The%20Code%2039%20-%20Full%20ASCII%20symbology%20is,be%20configured%20to%20perform%20Full%20ASCII%20character%20translations.) supports full 128 ASCII characters |
| github hosts | Check https://github.com.ipaddress.com/#ipinfo and replace C:\Windows\System32\drivers\etc\hosts with the latest IPs. |
| pacemaker | 起搏器的功能类型（PM普通起搏器。ICD植入型心律转复除颤器，高级起搏器的一种） <br> - 心房按需（AAI）型：电极置于心房。VVIR型频率自适应 <br> - 心室按需（VVI）型：电极置于心室。AAIR型频率自适应 <br> - 双腔（DDD）起搏器：心房和心室都放置电极。DDDR型频率自适应 <br> - 三腔（CRT）起搏器。  |
| Search NMPA/FDA | - [NMPA search](https://www.nmpa.gov.cn/datasearch/home-index.html#category=ylqx), 输入注册证编号/公司名 <br> - [FDA search](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfRL/rl.cfm) e.g. Proprietary Name:"SE-1200", Product Code:"DPS", Establishment Type:"Manufacturer" <br> - CE拿证只能看手册里有没有EC REP标识 |
| Search Clinical Trial | - 中国临床试验: [药物临床试验登记与信息公示平台](http://www.chinadrugtrials.org.cn/index.html) > 高级查询 > 输入登记号(例如"CTR20221099") <br> - 全球临床试验: [U.S. National Library of Medicine](https://clinicaltrials.gov/)  (ref. [知乎](https://zhuanlan.zhihu.com/p/86874330)) |
| Sensitivity, PPV | - Sensitivity=TP/(TP+FN) <u>敏感性</u>：真病人中能检出有病的人的比例 <br> - Precision or PPV=TP/(TP+FP) 精确度：检出阳性病人中有多少真病人 <br> - Specificity=TN/(TN+FP) <u>特异性</u>：没病人中能检出没病的人即阴性病人的比例 [(公式)](https://geekymedics.com/sensitivity-specificity-ppv-and-npv/) <br> - Accuracy=(TP+TN)/(TP+TN+FP+FN) 准确率：整体无论正负预测都包含的准确率 |
| Time AM/PM | 12-hour clock should be 1-12 for both AM and PM. PM starts at noon. <br> eg. <u>12:33:45AM is 00:33:45 (midnight)</u>; 12:33:45PM is 12:33:45 (noon) |
| WLAN Country Code | [WiFi Country Code](https://gitlab.com/recalbox/github/recalbox-os/-/wikis/Wifi%20country%20code%20(EN)); [WLAN Fequency Bands & Channels](https://www.cablefree.net/wirelesstechnology/wireless-lan/wlan-frequency-bands-channels/) |
| - 心电专题 - | • ECG 12导联计算公式: I=LA-RA, II=LL-RA, III=II-I;  aVL=LA-(RA+LL)/2, aVF=LL-(RA+LA)/2, aVR=RA-(LA+LL)/2; <br>  Vw=(LA+LL+RA)/3, V1..V6=V1..V6-Vw <br> • 胸痛中心用18导，卒中中心用动态。 <br> |
| - Classification分类判定 - | • SW Unit Class A/B/C判定：关联的CMT Cause的Severity是Critical及以上->Class C，Severity是Serious或者Minor的->Class B，没有Risk link的->Class A。 <br> • SUT中Critical task判定：UFMEA中关联的CMT Cause的Severity是Serious及以上的是Critical task. <br> • EC Part判定：关联的CMT Cause的Pre Risk Level是RMR及以上的Cause mitigation追溯到的HW Part. <br> |
| - DOORS - | • PFRS中'_Program'列加下拉项"Xxx_D": <br>  (1) 打开PFRS module, Edit Mode开启'Exclusive Edit', <br>  (2) 菜单Edit > Types.. > 弹出框中选'_Program Type', 点Edit, 切到Enumerations tab: Value填Xxx_D, Related number填3100 > Add. <br> • PFRS中导出In-links SSRS: <br>  (1) 打开PFRS module, 切到或者另存一个Trace View, <br>  (2) 菜单Analysis > Wizard.. > <br> &emsp;Step 1: Link direction单选In-links, Link types多选DOORS links和External links, <br> &emsp;Step 2: Select formal module选'Specific', Browse选SSRS模块, <br> &emsp;Step 3: <1>Module name and object attribute可以选'Object Identifier', 也可多选'Object Text'显示SSRS item内容; <2>DOORS link attribute都不选; <3>External link attribute可选Description?; <4>Specify depth of analysis填'1'因为只要显示PFRS->SSRS一层; Finish. <br> |
| - Excel公式模板 - | • 公式-Date数据(K2格)提取年和月组合显示 =IF(AB2="No", TEXT(K2, "YYYY")&"-"&TEXT(K2, "M"), "Invalid") <br> • 公式-Date数据(K2格)判断是否在一定范围内 =IF(AND(K2>=DATE(2023,2,1), K2<=DATE(2023,2,28), AB2="No"), "Yes", "No") <br> • 公式-INDIRECT函数获取C列最后一行的值 =SUM(C4:C6)/INDIRECT("C"&COUNTA(A:A)+1) (注:Pivot表的最后一行统计行算不进COUNTA的表格有效行数所以要+1; 收藏照片235X) <br> • 公式-判断数据(Z2格)是否包含某个字符并截取其左边的字符串 =IF(COUNTIF(Z2, "\*-\*")>0, LEFT(Z2, SEARCH("-",Z2)-1), " "&Z2 ) (收藏照片2362) <br> --- <br> • Pivot Table数据透视表: >Insert >Pivot Table, 选New Sheet创建; 点中Pivot表中任一单元格右击对该列排序.(收藏照片235V) <br> • VLOOKUP查找Pivot表A2值的结果为#N/A，可以试试查"\*"&A2&"\*"。 <br> • Pareto帕累托图选项在直方图中. <br> |
| - ISO/IEC - | ISO 10993, Biocompatibility? <br> <u>ISO 13485</u>, MD Quality Mgmt Systems医疗器械质量管理体系==国标GB/T42061从医药行标YY/T0287升级而来 <br> <u>ISO 14971</u>, Risk Management <br> ISO 15223, Symbols to be used <br> ISO 20417, Information to be supplied <br> IEC 62304, SW life-cycle process <br> IEC 62366, Usability engineering <br> |
| - Movie Maker - | 1-1. 导入排好序的照片和视频，导入Audio。 (如果音长不够，拖动末尾段并且按住Ctrl复制一份到最后，拖动第二段音乐到第一段末尾，点中第二段音乐 > Options tab > 'Start point'调节第二段音乐从本身中途的哪个时间点开始放) <br> 1-2. 选中第一张照片 > Home tab > Add区域加'Caption'片头和片尾字幕。 <br> 1-3. AutoMovie themes区域选择'Cinematic'。 (删掉多余的场景如当中和末尾的) <br> 1-4. 选中最后一张照片 > Edit tab > Adjust区域'Duration'下拉选10.00秒，Options tab > Audio区域'Fade out'选择Slow。 <br> 2. 试播放，在Animations tab下，左边Transitions区域选择上一张到当前这张的过渡效果，右边Pan and zoom区域选择当前这张的停留效果如放大/旋转等。 <br> 3. 导出，文件tab > Save movie > Android Phone (medium)。 <br> |

* * *

#### 工具官网
[Everything](https://www.voidtools.com) • 本地文件搜索工具  
_[EV录屏](https://www.ieway.cn/index.html) • 桌面录屏工具_  
[Format Factory(格式工厂)](http://www.pcfreetime.com/) • 音视频转换工具  
_[Inkscape](https://inkscape.org/) • 开源矢量作图工具_  
[Q-Dir](http://q-dir.com/) • Windows多窗口工具  
[ScreenToGif](https://www.screentogif.com/) • Gif录制/剪辑工具  
[vdhcoapp](https://github.com/mi-g/vdhcoapp) • Audio/Video DownloadHelper browser add-on  
[XMind](https://www.xmind.cn/) • 思维导图工具  
[蜜蜂剪辑](https://beecut.cn/video-to-gif-online) • 在线视频转换成GIF动画  

##### 特别鸣谢
