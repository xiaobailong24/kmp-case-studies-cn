# Setting up Compose Multiplatform Previews

> Issue [#15](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/15) · 标签：`tools`

## 概述

在 Compose Multiplatform 项目中配置预览功能，可以在 IDE 中直接查看 UI 效果，无需运行完整应用。

### 配置要点

1. 在 `commonMain` 中使用 `@Preview` 注解标记可组合函数
2. 确保 IDE 插件版本支持 CMP Preview
3. Desktop 目标可直接预览，其他目标需特定配置

## 参考资料

- [Setting up Compose Multiplatform Previews — JetBrains](https://www.jetbrains.com/help/kotlin-multiplatform-dev/compose-multiplatform-previews.html)
