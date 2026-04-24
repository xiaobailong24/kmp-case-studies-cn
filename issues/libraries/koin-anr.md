# Koin 防止 ANR 指南

> Issue [#28](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/28) · 标签：`articles` `libraries` `tools`

## 概述

在 Kotlin 和 KMP 应用中使用 Koin 依赖注入框架时，不当的配置可能导致 ANR（Application Not Responding）。本指南介绍如何预防和修复相关问题。

### 常见 ANR 原因

1. **主线程初始化耗时模块**：大量依赖在 `startKoin` 时同步创建
2. **循环依赖**：模块间循环引用导致死锁
3. **重型单例**：数据库、网络客户端等在首次访问时阻塞主线程

### 解决方案

- 使用 `lazyModules` 延迟加载非关键模块
- 将耗时初始化移至后台线程
- 使用 `createdAtStart` 标记仅用于真正需要预加载的依赖

## 参考资料

- [How to Prevent and Fix ANRs in Kotlin and KMP Apps — Koin Blog](https://blog.insert-koin.io/)
