# 图解 Redis

一个面向后端工程师的 Redis 内部机制图解项目。内容从基础数据结构开始，逐步覆盖对象编码、持久化、I/O、多路复用、内存管理、复制、高可用、Cluster、事务、Lua、Stream、ACL、性能调优与监控。

## 在线阅读

**GitHub Pages 渲染站点：**

https://hqqw2h-lgtm.github.io/redis-visualizer/

> 注意：`https://github.com/.../blob/main/index.html` 是 GitHub 的源码查看页面，只会展示 HTML 源码。请使用上面的 GitHub Pages 地址阅读渲染后的网页。

## 项目定位

这个项目不是 Redis 命令速查表，也不是简单的源码摘录，而是试图把 Redis 的关键实现机制拆成可以阅读、可以复盘、可以用于工程讨论的图解材料。

重点包括：

- Redis 为什么这样设计，而不只是“源码长什么样”
- 数据结构、对象编码和命令行为之间的关系
- 内存占用、扩容、复制、持久化、删除延迟等工程影响
- 从单机机制逐步过渡到高可用、Cluster 和现代特性

## 内容结构

| Part | 章节 | 主题 |
|---|---:|---|
| Part I | 01-08 | 基础数据结构：SDS、adlist、dict、skiplist、intset、listpack、quicklist、rax |
| Part II | 09-16 | 对象系统与算法：redisObject、编码切换、HyperLogLog、GeoHash、LRU/LFU、SipHash、CRC/LZF、Bloom Filter |
| Part III | 17-22 | 持久化与 I/O：RDB、AOF、事件循环、I/O 多路复用、RESP、jemalloc |
| Part IV | 23-24 | 内存管理：淘汰策略、LazyFree |
| Part V | 25-29 | 集群与高可用：复制、Sentinel、Cluster、事务、Lua |
| Part VI | 30-39 | 现代特性与工程实践：Pub/Sub、Stream、客户端缓存、模块、ACL/TLS、Linux 调优、性能、监控、演进史 |

## 本地预览

这个仓库是纯静态站点，不需要构建步骤。

```bash
python -m http.server 8080
```

然后访问：

```text
http://localhost:8080/
```

## 部署说明

当前站点通过 GitHub Pages 部署：

- Source branch: `main`
- Source folder: `/`
- Pages URL: https://hqqw2h-lgtm.github.io/redis-visualizer/
