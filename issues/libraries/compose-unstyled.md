# Compose Unstyled — 缺失的 Design System 层

> Issue [#22](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/22) / [#31](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/31) · 标签：`libraries`

## 概述

Compose Unstyled 提供了一套**无样式的**、可访问的 Compose UI 原语，介于 Material 组件和底层 Foundation 之间，让开发者可以构建完全自定义的 Design System。

### 定位

```
Material 3  ← 完整设计系统，固定风格
Compose Unstyled  ← 行为 + 可访问性，无视觉样式
Foundation  ← 底层构建块
```

### 适用场景

- 需要完全自定义品牌风格的应用
- 不想受 Material Design 约束
- 需要可访问性支持但想自定义外观
