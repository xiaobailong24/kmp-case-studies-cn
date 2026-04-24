# Meta 在 Buck2 上启用 Kotlin 增量编译

> Issue [#35](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/35) · 标签：`articles` `ecosystems` `tools`

## 概述

Meta 工程团队在其自研构建系统 Buck2 上启用了 Kotlin 增量编译，显著提升了大规模 Kotlin 项目的构建速度。

### 关键意义

- 证明 Kotlin 在超大规模项目中的可行性
- Buck2 是 Meta 内部数千名工程师使用的构建系统
- 增量编译对开发体验至关重要
