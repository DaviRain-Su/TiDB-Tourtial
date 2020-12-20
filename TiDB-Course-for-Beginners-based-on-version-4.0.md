# TiDB Course for Beginners based on version 4.0 

## 课程描述

通过101课程的学习，初学者可以了解以下知识点：

- 什么是HTAP？
- TIDB是如何实现HTAP的？
- TiDB的适用场景及典型成功案例

## 1.1 Brief History of Distributed Database（分布式数据库发展简史）

本课程简要介绍了从20世纪到21世纪分布式数据库的发展历史

学习目标：帮助学员了解分布式数据库的发展历史

关键知识点：分布式数据库历史，NoSQL和NewSQL, OLTP和HTAP,新技术



## 1.2 Why HTAP Matters （HTAP 数据库简介）

本课程简要介绍了HTAP意义，技术难点，TiDB如何实现HTAP以及相关的应用场景

学习目标：帮助学员熟悉HTAP领域

关键知识点：HTAP意义，设计原则以及应用场景



## 1.3 A Brief History About the TiDB database platform(TIDB发展史)

本课程简要介绍了TiDB的发展历史，自从v1.0.0GA 开始，TiDB 做到了；可以从计算和存储两个层面的无限扩展，兼容了MySQL的语法和协议，强一致的真分布式事务。到今天，TiDB可以称为一个真正的HTAP系统，不需要ETL工具进行数据转换，在系统运行OLTP业务时，也可以方便进行报表查询。

学习目标：了解TiDB的发展历史

关键知识点：TiDB; HTAP; 数据中台；TiSpark; TiFlash



## 1.4 The TiDB platform architecture and landscape (TiDB平台架构和全景图)

本课程简要介绍了TiDB核心系统的各个组件以及部分TiDB的生态工具

学习目标：对TiDB的核心组件和生态工具的功能有一定的理解

关键知识点：TiDB架构，计算存储分离，Raft共识协议，多副本，调度和负载均衡

## 1.5 Important features of TiDB database platform (TiDB技术特性)

本课程简要介绍了原生分布式数据库TiDB的技术特性，相比于传统的单机关系数据，以及基于分库分表中间件架构的分布式数据库的不同点

学习目标：了解TiDB的基础架构以及特性，能够帮助业务解决什么样的问题

关键知识点：TiDB的基本架构，扩展HTAP架构，TiDB 4.0提供的新功能及改进点



## 1.6 Read and Write data in the TiDB database platform (TiDB中的读写流程)

本课程主要包括TiDB架构的简单介绍，各个组件的作用，以及读写请求在TiDB中的过程

学习目标：对TiDB整体架构以及读写路程有大概的了解

关键知识点：TiDB架构；读写流程

## 1.7 Use cases and success stories with the TiDB (TiDB典型应用场景及用户案例)

本课程简要介绍了TiDB的适用场景以及用户案例。从TiDB具有的可扩展性，搞可用，分布式事务，实时分析等特点出发，总结出TiDB的各种适用场景。在海量数据，高并发等大规模集群中，TiDB能够体现出超强的处理能力。同时基于HTAP的架构设计，TIDB也非常适合作为实时分析类系统的数据库

学习目标：了解TiDB的特性及适用的场景

关键知识点：TiDB； HTAP；用户案例

