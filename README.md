# 技术图解系列

一个面向后端工程师的技术图解站点，收录 Redis、Kafka、Lucene、Spring Boot、JPA、jOOQ、Blaze-Persistence 七套可在线阅读的静态 HTML 图解材料。

## 在线阅读

**GitHub Pages 渲染站点：**

https://hqqw2h-lgtm.github.io/redis-visualizer/

> 注意：`https://github.com/.../blob/main/index.html` 是 GitHub 的源码查看页面，只会展示 HTML 源码。请使用上面的 GitHub Pages 地址阅读渲染后的网页。

## 项目定位

这个仓库不是命令速查表，也不是简单的源码摘录，而是把后端核心技术拆成可以阅读、可以复盘、可以用于工程讨论的图解材料。

重点包括：

- 为什么这样设计，而不只是“源码长什么样”
- 数据结构、运行时行为和工程影响之间的关系
- 存储、索引、复制、事务、缓存、I/O、框架启动等关键机制
- 从单个组件机制逐步过渡到生产实践和架构取舍

## 收录系列

| 系列 | 入口 | 章节数 | 主题 |
|---|---|---:|---|
| 图解 Redis | [`redis/`](redis/) | 39 | 数据结构、对象编码、持久化、I/O、复制、高可用、Cluster、Stream、ACL、性能与监控 |
| 图解 Kafka | [`kafka/`](kafka/) | 26 | 日志存储、索引、Producer/Consumer、ISR、KRaft、Exactly Once、网络模型与 Tiered Storage |
| 图解 Lucene | [`lucene/`](lucene/) | 35 | 倒排索引、Analyzer、BM25、Segment、FST、DocValues、BKD Tree、HNSW、Codec 文件格式 |
| 图解 Spring Boot | [`spring-boot/`](spring-boot/) | 37 | 启动流程、自动配置、IoC、AOP、WebMVC、事务、Data、Security、Observability、GraalVM、Cloud |
| 图解 JPA | [`jpa/`](jpa/) | 30 | 实体生命周期、Persistence Context、映射、JPQL、Criteria、Fetch、N+1、缓存、事务、Hibernate 架构 |
| 图解 jOOQ | [`jooq/`](jooq/) | 30 | Codegen、DSLContext、类型系统、SELECT/DML、MULTISET、QOM、Parser、Dialect、R2DBC、生产实践 |
| 图解 Blaze-Persistence | [`blaze-persistence/`](blaze-persistence/) | 26 | CriteriaBuilder、Entity View、可更新视图、高级 SQL、Keyset 分页、Spring Data 集成、SQL 优化与 CRUD 实战 |

## 适合读者

- 想系统理解后端基础设施内部机制的工程师
- 正在准备中高级后端面试、架构面试的开发者
- 需要排查 Redis、Kafka、Lucene、JPA、Spring Boot 等问题的工程师
- 希望从源码设计角度理解框架和中间件的学习者

## 本地预览

这个仓库是纯静态站点，不需要构建步骤。

方式一：直接打开 `index.html`。

方式二：用本地静态服务器预览：

```bash
python -m http.server 8080
```

然后访问：

```text
http://localhost:8080/
```

## 仓库结构

```text
.
├── index.html              # 总入口页
├── styles.css              # 总入口页与 Redis 旧入口共用样式
├── redis/                  # Redis 图解系列
├── kafka/                  # Kafka 图解系列
├── lucene/                 # Lucene 图解系列
├── spring-boot/            # Spring Boot 图解系列
├── jpa/                    # JPA 图解系列
├── jooq/                   # jOOQ 图解系列
├── blaze-persistence/      # Blaze-Persistence 图解系列
├── 01-sds.html             # 兼容旧 Redis 根目录链接
├── ...
├── 39-evolution.html       # 兼容旧 Redis 根目录链接
├── .nojekyll               # 禁用 GitHub Pages 的 Jekyll 处理
└── README.md
```

每个子目录都保留自己的 `index.html` 和 `styles.css`，避免不同系列的样式互相覆盖。

## 部署说明

当前站点通过 GitHub Pages 部署：

- Source branch: `main`
- Source folder: `/`
- Pages URL: https://hqqw2h-lgtm.github.io/redis-visualizer/

只要更新 `main` 分支中的静态文件，GitHub Pages 会自动重新发布。

## 说明

本项目主要用于学习、复盘和技术交流。内容会优先保证结构清晰、图文一致和可读性，而不是追求最短篇幅。
