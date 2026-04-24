# CLAUDE.md

## 本仓库是什么

本仓库 fork 自 [JetBrains/kotlin-multiplatform-dev-docs](https://github.com/JetBrains/kotlin-multiplatform-dev-docs)（JetBrains 官方 KMP/CMP 开发者文档），在保留上游全部英文文档的基础上，**新增了大量中国视角的原创中文内容**。

**这不是软件项目** — 没有构建系统（Gradle/Maven）、没有测试、没有应用代码。纯文档站，通过 Writerside 发布。

## 与上游仓库的核心差异

### 上游仓库（JetBrains 官方）

JetBrains 官方 KMP 文档，英文，内容包括入门教程、API 参考、Compose Multiplatform 文档、工具链指南。**没有中文内容，没有中国公司案例**。

### 本 Fork 新增的内容

#### 1. 中国公司 KMP/CMP 实践案例 `topics/case-studies-cn/`

核心差异化内容。收录了 8 家中国科技公司、10+ 款应用的 KMP/CMP 实践：

| 公司 | 应用 | 平台 |
|------|------|------|
| 美团 | 餐饮 SaaS | Android, iOS, Windows |
| 携程 | 携程旅行 | Android, iOS |
| 哔哩哔哩 | Bilibili | Android, iOS, HarmonyOS, CMP |
| 腾讯 | QQ, 腾讯视频 | Android, iOS, HarmonyOS, CMP |
| 快手 | 快手 | Android, iOS, HarmonyOS |
| 阿里 | 淘宝, 支付宝 | Android, iOS, HarmonyOS, CMP |
| 字节跳动 | 抖音 | Android, Desktop, HarmonyOS, CMP |
| 月之暗面 | Kimi | Android, Desktop, HarmonyOS, CMP |

每个案例包含公司背景、架构图、公开演讲链接（Bilibili 视频、微信公众号文章、会议 PPT）。

#### 2. Issue 知识库 `issues/`

将仓库 GitHub Issue 整理为结构化知识库，按 9 个主题分类（releases / compose / kotlin / architecture / tools / libraries / conferences / ecosystem / articles），每级目录有 `README.md` 汇总，重要 Issue 有独立子文档。详见 [`issues/README.md`](issues/README.md)。
