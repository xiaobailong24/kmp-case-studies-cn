# Kotlin Mutex

> Issue [#52](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/52) · 标签：`articles` · 🔒 Kotlin Mutex

## 概述

`Mutex` 是 Kotlin 协程中用于保护共享可变状态的同步原语，是 `synchronized` 的协程友好替代。

### 基本用法

```kotlin
val mutex = Mutex()
var counter = 0

coroutineScope {
    repeat(1000) {
        launch {
            mutex.withLock {
                counter++
            }
        }
    }
}
```

### Mutex vs synchronized

| 特性 | `Mutex` | `synchronized` |
|------|---------|----------------|
| 挂起支持 | ✅ 挂起等待 | ❌ 阻塞线程 |
| KMP 支持 | ✅ 全平台 | ❌ 仅 JVM |
| 可重入 | ❌ 不可重入 | ✅ 可重入 |
| 性能 | 适合 IO 密集 | 适合 CPU 密集短操作 |

### 注意事项

- `Mutex` 不可重入，同一协程重复加锁会死锁
- 优先使用 `withLock {}` 确保释放
- 考虑使用 `Channel` 或 `StateFlow` 替代手动互斥

## 参考资料

- [Shared mutable state and concurrency — Kotlin Docs](https://kotlinlang.org/docs/shared-mutable-state-and-concurrency.html)
