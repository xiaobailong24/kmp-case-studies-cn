# Kotlin/Native Runtime

> Issue [#39](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/39) · 标签：`libraries` · 🔨 Kotlin/Native runtime

## 概述

Kotlin/Native runtime 是在非 JVM 平台（iOS、macOS、Linux、Windows）上运行 Kotlin 代码的基础。

### 核心组件

- **内存管理**：Kotlin/Native 从 1.7.20 起默认使用新内存管理器（基于 tracing GC），取代了旧的冻结对象模型
- **线程模型**：新 MM 下对象可在线程间自由共享，无需 `freeze()`
- **编译器后端**：基于 LLVM，支持 ARM64、x86_64 等架构

### 性能特点

- 启动速度快于 JVM（无 JIT 预热）
- 稳态性能通常低于 JVM（无 JIT 优化）
- 二进制大小相对较大（包含 runtime）

## 参考资料

- [Kotlin/Native — Kotlin Docs](https://kotlinlang.org/docs/native-overview.html)
- [Kotlin/Native memory management](https://kotlinlang.org/docs/native-memory-manager.html)
