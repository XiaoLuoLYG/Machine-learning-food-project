# Food Project

[TOC]



## 项目简介

依靠ML、aws/ali Cloud、python爬虫等进行：

- 大数据选址
- 食品菜单推荐
- 营业额预测

餐厅类别：快餐/工作餐/简餐

## Location Finder 

> This is to find the best location for the delivery system of the new food brand which targets on the bussiness professionals

### Aim

针对南京几个较大型商圈/办公区域的白领用餐，开设名为“每日研选”的餐厅。主营业务为套餐外卖，需具有快速、健康、定制化推荐等特点。项目需在南京市依据数据分析结果选择合适开业地点试营业。

### Time and Deadline

Expecting First Draft: 10/25

Preproject report: 11/3

Code Structure: 11/5

Code final draft: 11/20

Final Report: 12/1



### Factors

- 人口密度：所在区域属于商业区/住宅区/办公区
- 白领占比：针对人群所占比例
- 地理位置：规划前景
- 竞争：同类型餐馆/其他种类餐馆数量/员工食堂



- 成本投入：租金
- 供货运输
- 消费能力：高新产业园区

  

### **数据来源**

- 人口/位置
- 餐厅
- ML

#### 地理位置/人口

http://www.stats.gov.cn/

腾讯位置大数据 https://heat.qq.com/

http://www.resset.cn/pop

CPOP.bnk

#### 竞争

开放API接口

爬虫爬取大众点评数据（MongoDB）

​	(https://segmentfault.com/a/1190000017891608)

​	(https://www.jianshu.com/p/930076792542)



爬虫逻辑：

1. 获取范围内前50页shopid
2. 进入店铺详情页
3. 获取评分、点评数等有用数据

#### ML

DBSCAN

Cluster/kmeans



### Methodology

1. 获取地理位置数据（地图API）

   1. 建立坐标系、南京各区域地图、经纬度（建立dataframe）

   2. geocoder

      

2. 地理数据处理/可视化(panda/json/matplotlib)

   1. Dataframe  Update（区域内所含街道/面积/区域类别/邮编）
   2. 分区地图（包含中心点坐标）
   3. 办公区单独提取出来

   

3. 人口数据处理

   1. 白领的数据（ideal）
   2. Dataframe Update(人口/人口密度/职业种类/收入水平)
   3. 计算消费能力

   

   **Output: A dataframe contains the info needed for the training **

   可视化图表：办公区subframe/各地区白领人口密度/消费能力



4. 大众点评数据处理

   1. 分区爬取/根据每个中心点范围指定半径内街区
   2. 商家的数量/密度
   3. 同类型餐厅的数量/密度/评价高低

   

   **Output: A dataframe sorts according to the map**

   图表



5. Combine 2 framework and do ML

   1. cluster number = 6
   2. 人口密度/白领密度/消费能力/餐厅数量/同类餐厅数量/面积

   

6. Cluster analysis

   1. Cluster characteristics analysis
   2. 结果图表/处理

### Daily Progress

#### 10.22

- [x] Github SSH key set up

- [x] Git Tutorial Reading 

  ​	[Git tutorial](https://www.runoob.com/git/git-tutorial.html)

  ​	[Git Cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

- [x] Version Control Reading 

  ​	[VCS](https://www.atlassian.com/git/tutorials/what-is-version-control)

- [x] Project Flow Chart

- [x] Github Project Review

#### 10.23/24

- [x] Python 爬虫
- [x] 获取大众点评区域内所需shopid



#### 10.25/26

- [x] github 大数据选址project
- [x] https://github.com/murak038/Optimal-Location-for-Opening-a-Restaurant
- [x] https://github.com/surgarman/python-site-selection（大众点评爬虫选址）
- [x] beautifulsoup reading



#### 10.27/28

- [x] 接洽腾讯位置大数据服务
- [x] 地图API (https://lbsyun.baidu.com/)
- [x] 数据可视化reading

#### 10.29/30

- [x] methodology update
- [x] kmeans training reading 
- [x] https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html

#### 11.1/2

- [x] methodology modify
- [x] 找数据来源
- [x] 梳理整体逻辑，输出report

### Plan

- coding!!!!!

- Data manipulation

- ML learning 

  

## Problem Facing

数据来源 ：没有经验/国内外差异/没有数据来源/

- 人口数据：项目描述不够充足/南京只有部分商业区开放接口

- 地理数据： 工业体量

  

- 精力有限

  

## 分工



## Reference 



https://github.com/RickWeng/optimal-restaurant-location

https://github.com/zt0910/dp_scripy （大众点评爬虫）

https://github.com/zt0910/dp_scripy（评论数量/星级爬虫）

https://github.com/murak038/Optimal-Location-for-Opening-a-Restaurant#methodology

https://www.pythonf.cn/read/86953

