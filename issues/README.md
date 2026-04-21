# KMP/CMP Issue 知识库

本目录整理归纳了 [kmp-case-studies-cn](https://github.com/xiaobailong24/kmp-case-studies-cn) 仓库的所有 Issue，按主题分类，方便检索和学习。

> 数据来源：GitHub Issues，截至 2026-04-21

## 目录结构

```
issues/
├── releases/          # 版本发布与路线图
├── compose/           # Compose 技术深度
│   ├── runtime/       #   Runtime / 状态管理
│   ├── ui/            #   UI 组件 / 样式 / 布局
│   └── tooling/       #   Compose 工具链（Hot-Reload / Visual Editor）
├── kotlin/            # Kotlin 语言与运行时
│   ├── language/      #   语言特性（expect/actual / Wasm）
│   ├── native/        #   Kotlin/Native 互操作
│   └── coroutines/    #   协程 / Flow / 并发
├── architecture/      # 架构设计（分层 / SDUI / RemoteCompose）
├── tools/             # 开发工具（IDE / Gradle / 调试）
├── libraries/         # 生态库（Navigation / Koin / Firebase 等）
├── conferences/       # 技术会议（KotlinConf / DroidKaigi 等）
├── ecosystem/         # 生态与行业动态
└── articles/          # 文章、经验与观点
```

## 分类速查表

### 版本发布与路线图 [`releases/`](releases/)

| Issue | 标题 | 关键词 |
|-------|------|--------|
| [#32](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/32) | Kotlin Roadmap Update 2025 August | 路线图, KLP, CMP iOS Stable |
| [#16](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/16) | Kotlin 2.2.20 发布 | Kotlin 版本 |
| [#53](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/53) | Kotlin 2.3.0 发布 | Kotlin 版本 |
| [#23](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/23) | CMP runtime klibs 缩小 600 倍 | CMP 1.9.0-beta01 |
| [#24](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/24) | Jetpack Compose 1.9 发布 | Jetpack Compose |
| [#46](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/46) | Compose Multiplatform 1.9.0 发布 | CMP, Web Beta |
| [#55](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/55) | Compose Multiplatform 1.10.0 发布 | CMP |
| [#67](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/67) | CMP 1.10 | CMP |
| [#68](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/68) | CMP 1.11 | CMP |
| [#20](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/20) | Gradle 9.0.0 GA 发布 | Gradle |
| [#45](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/45) | Java 25 LTS and IntelliJ IDEA | Java, IDE |
| [#73](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/73) | KMP 2025 was huge, 2026 will be bigger! | 年度总结 |

### Compose 技术深度 [`compose/`](compose/)

| Issue | 标题 | 子分类 |
|-------|------|--------|
| [#61](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/61) | Compose Runtime | runtime/ |
| [#58](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/58) | Compose State Stable | runtime/ |
| [#54](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/54) | Compose Modifier | ui/ |
| [#70](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/70) | Compose Canvas | ui/ |
| [#71](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/71) | Compose GPU | ui/ |
| [#74](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/74) | Compose Cheat Sheet | ui/ |
| [#75](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/75) | Compose Styles | ui/ |
| [#81](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/81) | Compose FlexBox | ui/ |
| [#76](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/76) | Android Jetpack Compose in RecyclerView | ui/ |
| [#60](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/60) | Compose 嵌套原生 View/UIKit | ui/ |
| [#77](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/77) | CMP interop View/UIKit | ui/ |
| [#79](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/79) | Compose 进阶系列 by 发呆自习室 | ui/ |
| [#47](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/47) | Compose Hot-Reload | tooling/ |
| [#69](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/69) | Compose Visual Editor | tooling/ |
| [#15](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/15) | Setting up CMP Previews | tooling/ |

### Kotlin 语言与运行时 [`kotlin/`](kotlin/)

| Issue | 标题 | 子分类 |
|-------|------|--------|
| [#62](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/62) | Kotlin expect/actual | language/ |
| [#63](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/63) | Kotlin/Wasm | language/ |
| [#19](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/19) | Kotlin/Native interop: ObjC/Swift import | native/ |
| [#39](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/39) | Kotlin/Native runtime | native/ |
| [#65](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/65) | Kotlin Coroutines Flow | coroutines/ |
| [#52](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/52) | Kotlin Mutex | coroutines/ |

### 架构设计 [`architecture/`](architecture/)

| Issue | 标题 |
|-------|------|
| [#80](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/80) | KMP/CMP 架构分层 |
| [#66](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/66) | SDUI（Server-Driven UI） |
| [#64](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/64) | Compose RemoteCompose |
| [#10](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/10) | Server-driven UI SDK on Android (RevenueCat) |

### 开发工具 [`tools/`](tools/)

| Issue | 标题 |
|-------|------|
| [#48](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/48) | Kotlin Multiplatform plugin for IDEA & Android Studio |
| [#72](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/72) | Android Gradle Plugin 9.0 |
| [#11](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/11) | Develocity Plugin for IntelliJ |
| [#13](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/13) | IntelliJ IDEA 统一发行版 |
| [#14](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/14) | Git Client from JetBrains |
| [#26](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/26) | Android Studio 月度发布节奏加速 |
| [#27](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/27) | Android Device Streaming |

### 生态库 [`libraries/`](libraries/)

| Issue | 标题 |
|-------|------|
| [#21](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/21) | Jetpack Navigation 3 |
| [#29](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/29) | Navigation 3 跨平台支持 |
| [#9](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/9) | Firebase in KMP |
| [#28](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/28) | Koin 防止 ANR 指南 |
| [#12](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/12) | Compose Apple Liquid Glass |
| [#22](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/22) | Compose Unstyled |
| [#31](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/31) | Compose Unstyled（重复） |
| [#37](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/37) | Compose 组件库 |
| [#51](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/51) | Map for CMP |
| [#57](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/57) | KMP Logger |

### 技术会议 [`conferences/`](conferences/)

| Issue | 标题 |
|-------|------|
| [#7](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/7) | droidcon & Fluttercon 2024 |
| [#8](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/8) | KotlinConf 2025 |
| [#17](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/17) | KMP for iOS: Myths vs Reality (Swift Heroes 2025) |
| [#41](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/41) | KotlinConf'26 |
| [#42](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/42) | DroidKaigi 2025 |
| [#50](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/50) | droidcon Berlin 2025 |
| [#78](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/78) | KotlinConf'26（重复） |

### 生态与行业动态 [`ecosystem/`](ecosystem/)

| Issue | 标题 |
|-------|------|
| [#25](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/25) | 近 1/5 开发者使用 KMP 进行跨平台开发 |
| [#18](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/18) | Kotlin 在 StackOverflow 2025 排名第 15 |
| [#35](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/35) | Meta 在 Buck2 上启用 Kotlin 增量编译 |
| [#38](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/38) | Why not Compose Multiplatform |
| [#40](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/40) | 腾讯视频 ovCompose |
| [#30](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/30) | 腾讯 Kuikly 开源，一码五端 |
| [#49](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/49) | Android for PC coming next year |
| [#59](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/59) | KMP/CMP at Google |
| [#82](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/82) | AI for KMP |

### 文章与经验 [`articles/`](articles/)

| Issue | 标题 |
|-------|------|
| [#36](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/36) | How I made side income from Jetpack Compose |
| [#56](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/56) | Native or Cross-Platform? |
