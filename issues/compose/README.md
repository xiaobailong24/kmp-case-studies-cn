# Compose 技术深度

Compose（Jetpack Compose / Compose Multiplatform）相关的技术深度内容，涵盖 Runtime 原理、UI 组件与样式、以及工具链。

## 子分类

### [Runtime / 状态管理](runtime/)

Compose 运行时核心机制：渲染管线、重组、状态与稳定性。

| Issue | 标题 | 简介 |
|-------|------|------|
| [#61](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/61) | [Compose Runtime](runtime/compose-runtime.md) | 三阶段渲染管线（Composition → Layout → Drawing） |
| [#58](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/58) | [Compose State Stable](runtime/compose-state-stable.md) | @Stable/@Immutable 注解与重组跳过机制 |

### [UI 组件 / 样式 / 布局](ui/)

Compose UI 层面的组件、修饰符、布局与互操作。

| Issue | 标题 | 简介 |
|-------|------|------|
| [#54](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/54) | [Compose Modifier](ui/compose-modifier.md) | Modifier 顺序与约束传递 |
| [#70](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/70) | Compose Canvas | 自定义绘制 |
| [#71](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/71) | Compose GPU | GPU 加速渲染 |
| [#74](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/74) | Compose Cheat Sheet | 速查表 |
| [#75](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/75) | Compose Styles | 样式系统 |
| [#81](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/81) | Compose FlexBox | FlexBox 布局 |
| [#76](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/76) | [Compose in RecyclerView](ui/compose-in-recyclerview.md) | Compose 与 RecyclerView 混用 |
| [#60](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/60) | [Compose 嵌套原生 View](ui/compose-native-interop.md) | 嵌套原生 View/UIKit |
| [#77](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/77) | [CMP interop View/UIKit](ui/compose-native-interop.md) | CMP 与原生 View 互操作 |
| [#79](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/79) | Compose 进阶系列 | by 发呆自习室 |

### [Compose 工具链](tooling/)

Hot-Reload、Preview、Visual Editor 等开发体验工具。

| Issue | 标题 | 简介 |
|-------|------|------|
| [#47](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/47) | [Compose Hot-Reload](tooling/compose-hot-reload.md) | 热重载 |
| [#69](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/69) | Compose Visual Editor | 可视化编辑器 |
| [#15](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/15) | [CMP Previews](tooling/cmp-previews.md) | 配置 CMP 预览 |
