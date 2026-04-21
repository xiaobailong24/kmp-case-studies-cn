# Compose RemoteCompose

> Issue [#64](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/64) · 🎨 Compose RemoteCompose

## 概述

RemoteCompose 是 JetBrains 的一个实验性项目，旨在实现远程 Compose UI 渲染——服务端发送 Compose UI 描述，客户端直接渲染为原生 Compose 界面。

### 与传统 SDUI 的区别

| 特性 | 传统 SDUI | RemoteCompose |
|------|-----------|---------------|
| UI 描述格式 | JSON/Proto（自定义） | Compose 专用协议 |
| 组件支持 | 需逐个映射 | 直接支持 Compose 组件 |
| 布局能力 | 受限于预定义组件 | 完整 Compose 布局 |
| 成熟度 | 已有大量生产实践 | 实验性 |

## 参考资料

- [RemoteCompose — GitHub](https://github.com/niclasforsblad/remotecompose)
