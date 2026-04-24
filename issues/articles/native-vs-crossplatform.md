# Native or Cross-Platform?

> Issue [#56](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/56) · 标签：`articles`

## 概述

原生开发与跨平台开发的技术选型讨论，帮助团队根据实际场景做出合理选择。

### 选型考量

| 维度 | 原生 | 跨平台（KMP/CMP） |
|------|------|-------------------|
| 性能 | 最优 | 接近原生 |
| 开发效率 | 需双端团队 | 共享 70-80% 代码 |
| 平台特性 | 第一时间支持 | 有滞后 |
| 团队要求 | iOS + Android | Kotlin（可选 iOS） |
| 维护成本 | 两套代码 | 一套核心逻辑 |
| UI 一致性 | 各平台原生风格 | 可共享或独立 |

### 适合跨平台的场景

- 业务逻辑占比高的应用
- 需要快速迭代的项目
- 团队以 Android/Kotlin 为主
- 对 iOS 原生 UI 不需要极致定制
