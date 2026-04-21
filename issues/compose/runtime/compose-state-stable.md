# Compose State Stable — 稳定性与重组跳过

> Issue [#58](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/58) · 🎨 Compose State Stable

## 核心概念

Compose 编译器会评估可组合函数参数的**稳定性（Stability）**，以决定是否可以跳过重组。

### 稳定性判定规则

| 类型 | 稳定性 | 说明 |
|------|--------|------|
| 基本类型 `Int`, `String`, `Float` 等 | ✅ Stable | 不可变 |
| `data class`（所有属性为 `val` 且类型稳定） | ✅ Stable | 编译器自动推断 |
| 含 `var` 属性的类 | ❌ Unstable | 可变导致不稳定 |
| `List`, `Set`, `Map` | ❌ Unstable | 始终标记为不稳定（即使是只读接口） |
| `MutableState<T>` | ✅ Stable | Compose 感知变化 |

### 解决不稳定性的方式

1. **使用 `kotlinx.collections.immutable`**：`ImmutableList`, `PersistentList` 等
2. **添加 `@Immutable` 或 `@Stable` 注解**：手动告知编译器
3. **Compose 编译器报告**：通过编译器参数生成稳定性报告，排查问题

### 关键原则

- 不是每个可组合函数都需要是 Skippable 的
- 优先关注高频重组路径上的稳定性
- 使用编译器报告（`-P plugin:...reportsDestination=...`）验证推断结果

## 参考资料

- [全网最详细的 Compose Stable 讲解](https://mp.weixin.qq.com/s/)（微信公众号）
- [Jetpack Compose Stability — 官方文档](https://developer.android.com/develop/ui/compose/performance/stability)
