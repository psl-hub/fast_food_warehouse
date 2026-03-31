# fast_food_warehouse
项目描述：基于快餐连锁企业真实业务场景，构建全流程离线数据仓库体系，整合订单、用户、门店、商品、支付等多源业务数据，完成数据采集、指标计算与FindBI可视化输出，支撑运营分析、经营决策等业务需求。实现全链路离线数仓开发，熟悉数仓分层与建模思想；处理万级数据，具备数据倾斜优化、SQL调优等实战经验；备良好的数据规范意识，熟悉字段命名、分层规范等工程化实践，产出可直接用于业务决策的统计指标。
项目过程:通过 DataX 完成历史全量同步，利用 Maxwell 解析 MySQL binlog 实现增量数据实时采集至 Kafka，再经 Flume 写入 HDFS，保障 ODS 层数据完整性与时效性；基于维度建模完成 ODS、DWD、DWS、ADS 四层设计，处理缓慢变化维；使用 Hive on Spark计算引擎 在 DataGrip 上进行数据清洗、多表关联与聚合计算，构建明细层与轻量聚合层；在 DWS 层按日、周、月粒度构建公共聚合指标，开发 ADS 层应用指标，涵盖门店销售额、订单量、热销商品、复购率等核心报表；编写 Shell 脚本封装各层 ETL 任务，通过 DolphinScheduler 配置任务依赖与定时调度，确保数据 T+1 准时产出。
技术栈：Hadoop,zookeeper,MySQL,Hive,Maxwell,Flume,Kafka,Spark,DataX,DolphinScheduler,FindBI
