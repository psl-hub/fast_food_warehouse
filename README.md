# fast_food_warehouse
项目描述：基于快餐连锁企业真实业务场景，构建全流程离线数据仓库体系，整合订单、用户、门店、商品、支付等多源业务数据，完成数据采集、指标计算与FindBI可视化输出，支撑运营分析、经营决策等业务需求。实现全链路离线数仓开发，熟悉数仓分层与建模思想；处理万级数据，具备数据倾斜优化、SQL调优等实战经验；备良好的数据规范意识，熟悉字段命名、分层规范等工程化实践，产出可直接用于业务决策的统计指标。
项目过程:通过 DataX 完成历史全量同步，利用 Maxwell 解析 MySQL binlog 实现增量数据实时采集至 Kafka，再经 Flume 写入 HDFS，保障 ODS 层数据完整性与时效性；基于维度建模完成 ODS、DWD、DWS、ADS 四层设计，处理缓慢变化维；使用 Hive on Spark计算引擎 在 DataGrip 上进行数据清洗、多表关联与聚合计算，构建明细层与轻量聚合层；在 DWS 层按日、周、月粒度构建公共聚合指标，开发 ADS 层应用指标，涵盖门店销售额、订单量、热销商品、复购率等核心报表；编写 Shell 脚本封装各层 ETL 任务，通过 DolphinScheduler 配置任务依赖与定时调度，确保数据 T+1 准时产出。
技术栈：Hadoop,zookeeper,MySQL,Hive,Maxwell,Flume,Kafka,Spark,DataX,DolphinScheduler,FindBI

业务层数据表：<img width="1566" height="524" alt="屏幕截图 2026-03-31 153320" src="https://github.com/user-attachments/assets/5179757c-98b6-4171-bbfa-004a8eaac554" />
数据采集组件：<img width="771" height="659" alt="屏幕截图 2026-03-31 160832" src="https://github.com/user-attachments/assets/c47f8ee1-6baf-440e-997f-0c7c1d600db7" />
hive on spark 计算引擎依赖包：<img width="1807" height="927" alt="屏幕截图 2026-03-31 161027" src="https://github.com/user-attachments/assets/9bc32950-48a3-41db-851a-0b5eefa3b216" />
ods层数据表：<img width="1829" height="1078" alt="屏幕截图 2026-03-31 161231" src="https://github.com/user-attachments/assets/56bf3ec7-0b50-4720-ad8b-0ddc9f51005a" />
dim层数据表：<img width="1750" height="613" alt="屏幕截图 2026-03-31 161255" src="https://github.com/user-attachments/assets/753813cd-d23e-4639-83ef-05e1996ff0cb" />
dwd层数据表：<img width="1774" height="600" alt="屏幕截图 2026-03-31 161326" src="https://github.com/user-attachments/assets/a749606a-f2d7-4c33-9ea0-f5db06395f70" />
dws层数据表：<img width="1811" height="1229" alt="屏幕截图 2026-03-31 161309" src="https://github.com/user-attachments/assets/1e4993d6-6468-4ea6-a882-ca57f5003828" />
ads层数据表：<img width="1785" height="1289" alt="屏幕截图 2026-03-31 161344" src="https://github.com/user-attachments/assets/b1d4570b-a01d-4500-bd0a-d2e5a28bb632" />
数据调度shell执行脚本：<img width="956" height="268" alt="屏幕截图 2026-03-31 161524" src="https://github.com/user-attachments/assets/91a71ce4-60be-4ba2-b024-0996cc360ae5" />
ads层数据全量同步至mysql供数据可视化的datax执行json文件：<img width="915" height="673" alt="屏幕截图 2026-03-31 162922" src="https://github.com/user-attachments/assets/1bb34bbc-f3c6-49f2-80aa-678381af6a48" />
ods层数据展示：<img width="1981" height="549" alt="屏幕截图 2026-03-31 170402" src="https://github.com/user-attachments/assets/fcc129e6-0720-4b97-9c7f-03d3c06e129b" />
dwd层数据展示：<img width="2373" height="186" alt="屏幕截图 2026-03-31 170509" src="https://github.com/user-attachments/assets/7f921cdb-827f-4936-9751-6d709fe366f3" />
dim层数据展示：<img width="2287" height="211" alt="屏幕截图 2026-03-31 170608" src="https://github.com/user-attachments/assets/9ba675b0-8d7f-41e7-a369-01345bb64418" />
dws层数据展示：<img width="2438" height="568" alt="屏幕截图 2026-03-31 170752" src="https://github.com/user-attachments/assets/1c747fb1-a0e1-4114-927f-7f6f40136e79" />
ads层数据展示：<img width="2367" height="776" alt="屏幕截图 2026-03-31 171013" src="https://github.com/user-attachments/assets/9f9be62b-128d-461f-a3ed-67df151f89c4" />
dolphinscheduler数据流调度：![4d71a3398c0c41711d4eded3d604332d](https://github.com/user-attachments/assets/a00df6aa-99c8-4211-96da-8939f3bb920f)






