# SDUI — Server-Driven UI

> Issue [#66](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/66) · ☁️ SDUI · 2025-12-24

## 概述

Server-Driven UI（SDUI）是一种由服务端定义和控制客户端 UI 结构与行为的架构模式。客户端充当通用渲染引擎，根据服务端下发的 JSON/Proto 描述动态构建界面。

### 核心优势

- **无需发版更新 UI**：服务端修改即时生效
- **缩短反馈循环**：产品/运营可快速实验
- **多平台一致性**：同一份 UI 描述渲染到多端

### 在 KMP/Compose 中的实践

| 方案 | 特点 |
|------|------|
| JSON + 自定义渲染器 | 灵活，需维护组件映射 |
| [RemoteCompose](remote-compose.md) | JetBrains 实验性方案，直接传输 Compose 描述 |
| Protocol Buffers + Compose | 强类型，性能好 |

## 参考

- 另见 [RevenueCat SDUI 实践](sdui-revenuecat.md)
