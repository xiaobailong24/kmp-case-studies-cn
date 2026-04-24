# Compose Hot-Reload

> Issue [#47](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/47) · 标签：`tools` · ⚒️ Compose Hot-Reload

## 概述

Compose Hot-Reload 允许在不重启应用的情况下实时预览 Compose UI 变更，极大提升开发效率。

### 现状（2026）

- CMP 1.9+ 已 **Stable**，默认开启
- 支持 Android、Desktop、iOS（实验性）
- 修改 `@Composable` 函数后自动热重载

### 工作原理

1. 编译器检测到 Composable 函数代码变更
2. 增量编译受影响的函数
3. 通过 JVM HotSwap / 自定义 Agent 替换函数实现
4. Recomposer 自动触发受影响的 Composition 重组

## 参考资料

- [Compose Hot Reload — JetBrains Blog](https://blog.jetbrains.com/kotlin/2025/02/compose-hot-reload/)
