# Kotlin Coroutines Flow 操作符速览

> Issue [#65](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/65) · Kotlin Coroutines Flow

## 操作符分类总览

### 1. 值变换

| 操作符 | 用途 |
|--------|------|
| `map` | 逐个转换元素 |
| `filter` | 按条件过滤 |
| `distinctUntilChanged` | 去除连续重复值 |

### 2. 值累积

| 操作符 | 用途 |
|--------|------|
| `scan` | 带初始值的累积，发射每步结果 |
| `runningReduce` | 无初始值的累积 |
| `fold` | 终端累积，返回最终值 |
| `reduce` | 终端累积，无初始值 |

### 3. 多次发射

| 操作符 | 用途 |
|--------|------|
| `transform` | 每个元素可发射 0~N 个值 |

### 4. 嵌套/动态 Flow

| 操作符 | 用途 |
|--------|------|
| `flatMapConcat` | 串行展开内部 Flow |
| `flatMapMerge` | 并发展开内部 Flow |
| `flatMapLatest` | 切换到最新的内部 Flow |

### 5. 性能控制

| 操作符 | 用途 |
|--------|------|
| `buffer` | 缓冲发射，上下游并发执行 |
| `conflate` | 跳过中间值，只处理最新 |
| `collectLatest` | 新值到来取消前一次处理 |
| `flowOn` | 切换上游执行的调度器 |

### 6. 流合并

| 操作符 | 用途 |
|--------|------|
| `zip` | 一对一配对两个 Flow |
| `combine` | 任一流发射新值时组合最新值 |
| `merge` | 将多个 Flow 合并为一个 |

### 7. 错误处理

| 操作符 | 用途 |
|--------|------|
| `catch` | 捕获上游异常 |
| `onCompletion` | 流完成时执行 |
| `retryWhen` | 条件重试 |

### 8. 高频发射

| 操作符 | 用途 |
|--------|------|
| `debounce` | 去抖动，仅发射间隔后的最新值 |

### 9. 终端操作符

`collect`, `collectLatest`, `first`, `single`, `toList`, `reduce`, `fold`

## 参考资料

- [十分钟速览 Kotlin Flow 操作符](https://mp.weixin.qq.com/s/UcdNNFH1vSQpS6BIkQrq5Q)（微信公众号）
- [Kotlin Flow — Kotlin Docs](https://kotlinlang.org/docs/flow.html)
