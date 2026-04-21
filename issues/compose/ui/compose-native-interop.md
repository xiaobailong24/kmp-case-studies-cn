# Compose 与原生 View/UIKit 互操作

> Issue [#60](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/60) · 🔳 Compose 嵌套原生 View/UIKit
> Issue [#77](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/77) · 🎨 CMP interop View/UIKit

## 概述

在 Compose Multiplatform 项目中，经常需要与平台原生 View 进行互操作：

- **Android**：在 Compose 中嵌入 Android View（`AndroidView`），或在 View 体系中嵌入 Compose（`ComposeView`）
- **iOS**：在 Compose 中嵌入 UIKit 组件（`UIKitView`），或在 SwiftUI 中嵌入 Compose

### Android 互操作

| 方向 | API | 场景 |
|------|-----|------|
| View → Compose | `ComposeView` | 在 Fragment/Activity 中嵌入 Compose |
| Compose → View | `AndroidView` | 使用 MapView、WebView、广告 SDK 等 |

### iOS 互操作（CMP）

| 方向 | API | 场景 |
|------|-----|------|
| UIKit → Compose | `ComposeUIViewController` | 在 SwiftUI/UIKit 中嵌入 Compose 界面 |
| Compose → UIKit | `UIKitView` | 使用 MKMapView、WKWebView 等原生组件 |

## 参考资料

- [Compose Multiplatform — iOS Integration](https://www.jetbrains.com/help/kotlin-multiplatform-dev/compose-ios-ui-integration.html)
