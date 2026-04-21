# Android Jetpack Compose in RecyclerView

> Issue [#76](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/76) · 🎨 Android Jetpack Compose in RecyclerView

## 概述

在现有 Android 项目中，RecyclerView 仍然是列表场景的主力。将 Compose 逐步引入 RecyclerView 是渐进式迁移的常见方式。

### 关键方案

1. **`ComposeViewHolder`**：在 RecyclerView.ViewHolder 中使用 `ComposeView` 渲染 Compose 内容
2. **生命周期管理**：需正确处理 `ViewCompositionStrategy`，避免内存泄漏
3. **性能考量**：每个 `ComposeView` 都有独立的 Composition，大量 item 时需注意性能

### 推荐策略

- 新页面优先使用 `LazyColumn` / `LazyRow`
- 存量页面可通过 `ComposeViewHolder` 渐进迁移
- 注意设置 `ViewCompositionStrategy.DisposeOnViewTreeLifecycleDestroyed`
