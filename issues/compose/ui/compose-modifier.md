# Compose Modifier — 顺序与约束传递

> Issue [#54](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/54) · 标签：`articles` · 2025-10-08

## 核心要点

Modifier 的链式调用顺序决定了最终效果，理解其工作机制是 Compose 进阶的关键：

1. **Modifier 按声明顺序从外到内依次应用**，每个 Modifier 接收上一个传递的约束并可能修改它
2. **第一个尺寸 Modifier 优先**：当多个尺寸 Modifier 冲突时，先声明的生效
3. **约束向下流动**：父级约束 → 第一个 Modifier → 第二个 Modifier → ... → 实际内容

### 常见陷阱

```kotlin
// ❌ padding 在 background 之后，背景不包含内边距
Box(Modifier.padding(16.dp).background(Color.Red))

// ✅ background 在 padding 之后，背景包含内边距
Box(Modifier.background(Color.Red).padding(16.dp))
```

## 参考资料

- [Understanding Modifier Ordering in Jetpack Compose](https://www.droidcon.com/2025/10/01/understanding-modifier-ordering-in-jetpack-compose/)（droidcon）
