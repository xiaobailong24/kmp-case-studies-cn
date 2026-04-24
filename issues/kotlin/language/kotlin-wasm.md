# Kotlin/Wasm

> Issue [#63](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/63) · 🌐 Kotlin/Wasm

## 概述

Kotlin/Wasm 是 Kotlin Multiplatform 的 Web 目标之一，将 Kotlin 代码编译为 WebAssembly（Wasm），在浏览器中以接近原生的性能运行。

### 与 Kotlin/JS 的区别

| 特性 | Kotlin/JS | Kotlin/Wasm |
|------|-----------|-------------|
| 编译目标 | JavaScript | WebAssembly |
| 性能 | JS 引擎优化 | 接近原生 |
| DOM 交互 | 直接 | 通过 JS 互操作 |
| 二进制大小 | 较大 | 较小 |
| 生态兼容性 | npm 直接可用 | 需适配 |

### 当前状态

- Compose Multiplatform for Web（基于 Kotlin/Wasm）在 CMP 1.9.0 进入 **Beta**
- Kotlin/Wasm 本身在 Kotlin 2.0+ 为 **Alpha**

## 参考资料

- [Kotlin/Wasm — Kotlin Docs](https://kotlinlang.org/docs/wasm-overview.html)
- [Compose Multiplatform for Web](https://www.jetbrains.com/help/kotlin-multiplatform-dev/compose-multiplatform-web.html)
