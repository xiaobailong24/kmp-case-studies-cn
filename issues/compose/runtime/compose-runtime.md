# Compose Runtime — 三阶段渲染管线

> Issue [#61](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/61) · 🎨 Compose Runtime

## 概述

Compose 每一帧都依次经过三个阶段：**Composition（组合）→ Layout（布局）→ Drawing（绘制）**。

- **Composition**：Recomposer 重新执行失效的可组合函数，生成/更新节点树
- **Layout**：`MeasureAndLayoutDelegate` 按深度顺序测量和放置脏节点
- **Drawing**：`NodeCoordinator` 遍历修饰符链，按 z 顺序递归绘制

### 关键源码入口

| 阶段 | 入口 | 职责 |
|------|------|------|
| Composition | `Recomposer.runRecomposeAndApplyChanges()` | 与 Choreographer 帧对齐，执行重组 |
| Layout | `AndroidComposeView.measureAndLayout()` | 深度排序处理 `relayoutNodes` |
| Drawing | `LayoutNode.draw()` → `NodeCoordinator.draw()` | 图形层或画布平移 + 递归绘制 |

### 阶段作用域失效（Phase Scoped Invalidation）

`OwnerSnapshotObserver` 将状态读取限定在读取发生的阶段：

- **测量阶段**读取 → `requestRemeasure()`（最昂贵，可向上传播）
- **布局阶段**读取 → `requestRelayout()`（跳过测量）
- **绘制阶段**读取 → 仅失效图形层（最廉价，跳过组合和布局）

> 因此在 `Modifier.drawWithContent {}` 中读取 `Animatable` 不会触发重组。

## 参考资料

- [Dove Letter — Compose Phases](https://doveletter.dev/preview/interviews/compose-phases)（Jaewoong Eum / skydoves）
- [Jetpack Compose Phases — 官方文档](https://developer.android.com/develop/ui/compose/phases)
