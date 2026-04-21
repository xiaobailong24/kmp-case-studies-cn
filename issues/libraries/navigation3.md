# Jetpack Navigation 3 — 专为 Compose 打造的全新导航库

> Issue [#21](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/21) · 标签：`articles` `libraries`

## 概述

Navigation 3 是 Google 为 Jetpack Compose 从头设计的导航库，取代了基于 Fragment 思维的 Navigation 2.x。

### 与 Navigation 2.x 的区别

| 特性 | Navigation 2.x | Navigation 3 |
|------|---------------|--------------|
| 设计理念 | Fragment 迁移 | Compose-first |
| 路由类型 | String 路由 | 类型安全（类/对象） |
| 后退栈 | 框架管理 | 开发者可控的 `List<T>` |
| 多平台 | 仅 Android | 计划支持 KMP（[#29](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/29)） |

## 参考资料

- [Navigation 3 — Android Developers](https://developer.android.com/guide/navigation/navigation3)
