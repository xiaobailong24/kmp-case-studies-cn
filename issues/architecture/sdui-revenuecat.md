# RevenueCat SDUI 实践 — Server-Driven Android Paywalls

> Issue [#10](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/10) · 标签：`articles`

## 概述

RevenueCat 的工程博客介绍了他们如何利用 Server-Driven UI 在 Android 上实现远程 Paywall（付费墙），无需应用更新即可动态调整付费界面。

### 核心方案

1. **服务端定义 UI 结构**：Paywall 的布局、样式、文案均由后端配置
2. **SDK 动态渲染**：Android SDK 接收描述后即时渲染对应组件
3. **消除发版依赖**：修改 Paywall 不再需要重新构建/提交应用商店

### 关键收益

- 更短的实验反馈循环
- A/B 测试无需客户端发版
- 多平台 Paywall 保持一致

## 参考资料

- [Server-driven UI SDK on Android — RevenueCat Engineering Blog](https://www.revenuecat.com/blog/engineering/server-driven-android/)
