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

#### 2. 会议演讲 PDF `docs/case-studies/`

2025 Kotlin 中文开发者大会的原始 PPT：
- `alibaba/` — 支付宝 KMP 架构（何斌）
- `bytedance/` — 字节跳动 KMP 工程实践（吴霖鹏）
- `kuaishou/` — 快手 KMP 多平台实践（张人杰、闫昌森）

#### 3. 架构图 `images/case-studies/`

21 张原创图片：各公司 KMP/CMP 架构图、对比截图、技术方案图。

#### 4. HarmonyOS 图标 `images/icons/harmonyos.svg`

上游仅有 Android/iOS/Desktop/Web/Server 图标。本 Fork 新增了 HarmonyOS 图标，反映中国市场对鸿蒙的重视。

#### 5. Issue 知识库 `issues/`

将仓库 GitHub Issue 整理为结构化知识库，按 9 个主题分类（releases / compose / kotlin / architecture / tools / libraries / conferences / ecosystem / articles），每级目录有 `README.md` 汇总，重要 Issue 有独立子文档。详见 [`issues/README.md`](issues/README.md)。

#### 6. README.md 完全重写

上游 README 是标准项目说明。本 Fork 的 README.md 是中文案例汇总表，含公司链接、App Store 链接、平台图标、可折叠架构摘要。

### 未改动的部分

以下内容与上游保持同步，未做修改：
- `topics/compose/` `topics/compose-onboard/` `topics/development/` 等标准教程
- `topics/multiplatform-onboard/` `topics/journal/` `topics/overview/` `topics/tools/`
- `writerside.cfg` `mpd.tree` `v.list` `labels.list` `cfg/` 配置
- `snippets/` 代码示例

## 仓库结构

```
kmp-case-studies-cn/
├── .github/workflows/     # CI
├── .devcontainer/         # Dev container (Java 21)
├── cfg/                   # Writerside 构建配置
├── docs/case-studies/     # 【Fork 新增】会议 PDF（alibaba/bytedance/kuaishou）
├── images/
│   ├── case-studies/      # 【Fork 新增】案例架构图（21 张）
│   ├── compose/           # Compose 图片（上游）
│   └── icons/             # 平台图标（上游 + Fork 新增 harmonyos.svg）
├── issues/                # 【Fork 新增】Issue 知识库（详见 issues/README.md）
├── snippets/              # 代码示例（上游）
├── topics/
│   ├── case-studies-cn/   # 【Fork 新增】中国公司案例
│   ├── compose/           # Compose 文档（上游）
│   ├── compose-onboard/   # Compose 入门（上游）
│   ├── development/       # 开发教程（上游）
│   ├── journal/           # 文章（上游）
│   ├── multiplatform-onboard/ # KMP 入门（上游）
│   ├── overview/          # 概览（上游）
│   ├── tools/             # 工具文档（上游）
│   └── whats-new/         # 更新日志（上游）
├── writerside.cfg         # Writerside 主配置
├── mpd.tree               # 导航树（95 个节点）
├── v.list                 # 版本变量
├── README.md              # 【Fork 重写】中文案例汇总表
└── README_EN.md           # 英文 README
```

## 关键配置文件

| 文件 | 用途 |
|------|------|
| `writerside.cfg` | 主配置 — Writerside 2.1.1991-p6895, 模块、路径 |
| `mpd.tree` | 导航树，定义站点结构和页面顺序 |
| `v.list` | 模板变量（Compose/Kotlin/Ktor 等版本号） |
| `labels.list` | 标签系统（deprecated/experimental/platform） |
| `cfg/buildprofiles.xml` | 构建配置、分析、自定义 CSS |

## 内容规范

### 文档文件 (topics/)
- **格式**: Markdown (`.md`) 和 Writerside topic (`.topic`)
- **命名**: kebab-case（如 `multiplatform-create-first-app.md`）
- **语言**: 案例和 Issue 知识库为中文；上游教程为英文
- **变量**: 使用 `%varName%` 引用 `v.list` 中的版本号

### 案例 (topics/case-studies-cn/)
- 每家公司一个 `.md` 文件
- 包含公司背景、使用 KMP/CMP 的应用、架构细节
- 图片引用 `images/case-studies/`
- 链接外部演讲、GitHub 仓库和文章

### Issue 知识库 (issues/)
- 每级目录有 `README.md` 汇总表
- 重要 Issue 有独立 `.md` 子文档
- 官方更新类按时间倒序排列（见 `issues/releases/timeline.md`）
- 英文博客提供中文归纳或翻译

## 开发工作流

### 新增案例
1. 在 `topics/case-studies-cn/` 创建 `.md` 文件
2. 在 `images/case-studies/` 添加架构图
3. 在 `docs/case-studies/<company>/` 添加 PDF 资源
4. 更新 `mpd.tree` 导航树
5. 更新 `README.md` 汇总表

### 新增 Issue 知识库文档
1. 在 `issues/` 对应分类目录下创建 `.md` 文件
2. 更新该分类的 `README.md`
3. 更新 `issues/README.md` 顶层速查表
4. 官方更新类同步更新 `issues/releases/timeline.md`

### 提交规范
- 中文或英文均可
- 描述性（如 "Add 字节跳动-抖音实践案例", "Update README.md"）
- 无严格 conventional commit 格式要求

## AI 助手注意事项

1. **无构建/测试命令** — 纯文档仓库，没有 `./gradlew`、测试套件或 CI 构建
2. **大二进制文件** — `images/` 约 230MB，避免无谓读取图片文件
3. **Writerside 语法** — 文档使用 Writerside 扩展（折叠区、Tab、提示框），参考 [Writerside 文档](https://www.jetbrains.com/help/writerside/)
4. **中文内容** — 案例和 Issue 知识库为中文，上游教程保持英文
5. **导航树** — 新增的 topic 文件必须添加到 `mpd.tree`
6. **Fork 差异意识** — 修改文件前判断是上游内容还是 Fork 新增内容；上游内容一般不主动修改
7. **License** — Apache License 2.0
