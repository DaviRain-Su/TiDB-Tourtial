# TiDB Course for Application Developers based on version 4.0

课程描述

在学完101课程的基础上，通过201课程的学习

- 普通业务开发者可以基于TiDB实现业务逻辑
- 高阶开发者可以掌握TiDB日常运维，调优等



## 2.1 When to use TiDB platform （TiDB的适用场景）

本节课程介绍了TiDB 的一些典型使用场景，介绍了TiDB在OLTP类型的场景中使用，在实时HTAP场景中的使用，借助TiSpark使Spark能够读取TiDB的数据，进一步加强数据整合以及TiDB不适用的场景。

学习目标：熟悉TiDB的一些典型使用场景，并且能大致的判断哪些场景适合TiDB,哪些不适合

关键知识点：OLTP场景；实时分析数据库；Spark





### OLTP-like workload

when you need random, Real-time Read/Write access to you big data(billions of row), with

- ACID compliance
- Secondary index support 二级索引的支持
- MySQL syntax 兼容MySQL协议

兼容MySQL协议，支持弹性的水平扩展，对于应用层无感知，对于海量数据是一个不错的选择，对于数据的访问时均匀（随机）的。对小范围的热点数据需要注意。TiDB 是一个100%的OLTP数据库，交易型数据库，建立二级索引。保证毫秒级的延迟。带索引的单行查询，业务侵入性。没有容量的上限

### Real-time HTAP (混合事务分析负载的数据库，HTAP)

- Real-time HTAP(Hybrid transactional/analytical processing)
- When you have a OLPT-like workload using TiDB, and you want to perform OLAP query in place with the help of TiFlash
  - With fresh data
  - with zero interferene on OLTP performance 
- Data integration
  - When you have multiple data sources like (OLTP databases, streaming ingestion and etc), you want to perform OLAP query on the integrated data set

数据的原地进行分析，不像传统的数据仓库批量的更新，批量的离线操作，TiFlash(列式存储引擎）原地进行分析。

数据的汇总分析作为上游数据库的存库。

### Connect with Spark Eco-system via TiSpark

With TiSpark you can use Spark to process data within TiDB platform inplace without moving your data out.

It's useful when you want workload like:

- Iterative processing
  - Like traditional ETL job
- Joining datasets
  - joining large datasets from multiple data sources
  - a lot of shuffling and sorting is needed

使用TiSpark联同Spark处理数据，分布式数据处理平台

将Spark中的分布式计算任务下推到TiKV分布式节点中进行计算

### TiDB may not be your best choice when:

- your data can fit on a single server
- You need to perform heavy analytics tasks
  - Scanning and aggregation on large data sets, that intermediate results can not fit in single server's memory 
- You need sub-millisecond latency
  - Take a look at Redis?

哪些场景TiDB不是一个好的选择，业务可以放在一台机器上完美的解决，业务中需要非常重度的分析场景也不太适用

关联查询产生的中间数据超过了物理机的存储空间，需要亚毫秒级的延迟，不能容忍一毫秒级的延迟，

TiDB持久化，分布式事务是一个很好的选择

### Review 

- TiDB for OLTP-like workload
- TiDB for Real-time HTAP workload
- Connect with Spark Eco-system via TiSpark
- When TiDB is not a good choice



## 2.2 How to connect TiDB platform （如何连接到TiDB)

本课程主要介绍了如何适用TiDB,通过实例介绍了如何使用相关工具连接到TiDB

学习目标：能够使用相关工具连接TiDB

关键知识点：MySQL协议；客户端工具；应用程序工具；ORM

## 2.3.1 How to Deploy TiDB Platform with TiUP(如何通过TiUP部署TiDB)

本课程简要介绍了TiUP的设计目标，组件管理方式，以及如何使用TiUP管理TiDB集群。在各种系统软件和应用软件的安装管理中，包管理器均有着广泛的应用，包管理工具的出现大大简化了软件的安装和升级维护工作。在早起的TiDB生态中，没哟专门的包管理工具，使用者只能通过相应的配置文件和文件夹命令来手动管理，从TiDB 4.0版本开始，TiUP作为新的工具，承担包管理器的角色，管理者TiDB生态下众多的组件，用户想要运行TiDB生态中的任何组件时，只需要执行TiUP一行命令即可，相比以前，极大地降低了管理难度

学习目标：了解TiUP组件管理方式和集群管理方式

关键知识点：TiDB;集群；部署；升级；扩缩容

## 2.3.2 Deploy TiDB in Kubernetes (在Kubernetes上部署TiDB集群)

## 2.3.3 Import Data to TiDB （将数据导入TiDB)

## 2.3.4 How to Benchmark 如何对TiDB进行基准测试

## 2.3.5 How to Use Transactions in TiDB (如何在TiDB中使用事务)

## 2.3.6 How to use TiDB Dashboard (如何使用TiDB Dashboard)

## 2.4 Beahavior Differences Between MySQL and TiDB （TIDB与MySQL的差异）

## 2.5.1 The  Lifecycle of a SQL Statement （在TiDB中一条SQL的生命周期）



## 2.5.2 TiDB 4.0 System Tables （TiDB 的系统表）



## 2.5.3 Usage of PD control （PD Control 的典型使用场景）



## 2.5.4 Advanced Features in Dashboard (TIDB Dashboard的高级功能)



## 2.5.5 SQL Tuning Guide (TiDB的SQL性能优化指南)

## 2.5.6 TIKV Tuning Guide (TiDB 的TiKV 性能优化指南)

