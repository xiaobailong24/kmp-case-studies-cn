# CLAUDE.md

## Project Overview

This is a **JetBrains Writerside documentation repository** that collects Kotlin Multiplatform (KMP) and Compose Multiplatform (CMP) adoption case studies from Chinese technology companies. It supplements the official [JetBrains KMP Case Studies](https://www.jetbrains.com/help/kotlin-multiplatform-dev/case-studies.html).

**This is NOT a software project** — there is no build system (Gradle/Maven), no tests, and no application code. It is a pure documentation site published via Writerside.

## Repository Structure

```
kmp-case-studies-cn/
├── .github/workflows/     # CI (Junie workflow for documentation processing)
├── .devcontainer/         # Dev container config (Java 21, Maven, Gradle)
├── cfg/                   # Writerside build profiles, analytics, styling
│   ├── buildprofiles.xml
│   ├── build-script.xml
│   └── thirdparty/        # Third-party analytics and favicon configs
├── docs/case-studies/     # PDF resources for case studies
│   ├── alibaba/
│   ├── bytedance/
│   └── kuaishou/
├── images/                # Image assets (~230MB) for documentation
│   ├── case-studies/      # Case study screenshots and architecture diagrams
│   ├── compose/           # Compose Multiplatform images
│   └── icons/             # Platform icons (android, ios, desktop, etc.)
├── snippets/              # Code examples referenced by documentation
│   ├── android-ios-tutorial/  # Swift code examples
│   └── multiplatform-tutorial/ # Kotlin code examples
├── topics/                # Markdown documentation content (64 files)
│   ├── case-studies-cn/   # Chinese company case studies
│   ├── compose/           # Compose Multiplatform docs
│   ├── compose-onboard/   # Compose onboarding guides
│   ├── development/       # Development tutorials
│   ├── journal/           # Articles and journals
│   ├── multiplatform-onboard/ # KMP onboarding
│   ├── overview/          # Overview and FAQ
│   ├── tools/             # Tooling documentation
│   └── whats-new/         # Release notes
├── writerside.cfg         # Main Writerside config (module, topics, snippets)
├── mpd.tree               # Documentation navigation tree (95 toc-elements)
├── v.list                 # Version variables (Compose, Kotlin, Ktor, etc.)
├── labels.list            # Label definitions (deprecated, experimental, etc.)
├── README.md              # Chinese README with case study summary table
└── README_EN.md           # English README
```

## Key Configuration Files

| File | Purpose |
|------|---------|
| `writerside.cfg` | Main config — Writerside 2.1.1991-p6895, module name, paths |
| `mpd.tree` | Navigation tree defining the site structure and page ordering |
| `v.list` | Template variables for library versions used across docs |
| `labels.list` | Label system for experimental/deprecated/platform markers |
| `cfg/buildprofiles.xml` | Build profiles, analytics, custom CSS |
| `cfg/build-script.xml` | Artifact type (web2) configuration |

## Content Conventions

### Documentation Files (topics/)
- **Format**: Markdown (`.md`) and Writerside topic (`.topic`) files
- **Naming**: kebab-case filenames (e.g., `multiplatform-create-first-app.md`)
- **Language**: Content is primarily in Chinese; some technical docs in English
- **Variables**: Use `%varName%` syntax referencing values from `v.list`

### Case Studies (topics/case-studies-cn/)
- Each company gets its own `.md` file
- Include company background, apps using KMP/CMP, architecture details
- Reference images from `images/case-studies/`
- Link to external presentations, GitHub repos, and articles

### README.md (root)
- Contains a summary table of all case studies with:
  - Company name and link
  - App names with App Store links
  - Platform support icons (Android/iOS/Desktop)
  - Links to public presentations and articles
  - Collapsible summaries with architecture diagrams

### Images
- Stored in `images/` with subdirectories by topic
- Platform icons in `images/icons/` (android.svg, ios.svg, desktop.svg, etc.)
- Case study diagrams in `images/case-studies/`
- Referenced via relative paths in markdown

### Code Snippets
- Located in `snippets/` directory
- Referenced from documentation using Writerside snippet syntax
- Kotlin and Swift examples for tutorials

## Version Variables (v.list)

Key versions tracked:
- Compose Multiplatform: 1.7.3 (EAP: 1.7.0-rc01)
- Kotlin: 2.0.0
- Coroutines: 1.7.3
- Ktor: 2.3.7
- SQLDelight: 2.0.1
- Koin: 3.5.3

## Development Workflow

### Adding a New Case Study
1. Create a new `.md` file in `topics/case-studies-cn/`
2. Add architecture diagrams/screenshots to `images/case-studies/`
3. Add any PDF resources to `docs/case-studies/<company>/`
4. Update `mpd.tree` to include the new page in the navigation
5. Update the summary table in `README.md`

### Editing Documentation
1. Modify `.md` files in `topics/`
2. If adding new pages, register them in `mpd.tree`
3. Use Writerside variables (`%varName%`) for version numbers
4. Preview locally using JetBrains Writerside IDE plugin

### Commit Message Conventions
- Commit messages are in Chinese or English
- Descriptive of the change (e.g., "Add 字节跳动-抖音实践案例", "Update README.md")
- No strict conventional commit format enforced

## Important Notes for AI Assistants

1. **No build/test commands** — This is a documentation-only repo. There are no `./gradlew` commands, test suites, or CI builds to run.
2. **Large binary assets** — The `images/` directory is ~230MB. Avoid reading image files unnecessarily.
3. **Writerside-specific syntax** — Documentation uses Writerside extensions (collapsible sections, tabs, tooltips, admonitions). Refer to [Writerside docs](https://www.jetbrains.com/help/writerside/) for syntax.
4. **Chinese content** — Most documentation and commit messages are in Chinese. Respect the existing language conventions when editing.
5. **Navigation tree** — Any new topic file MUST be added to `mpd.tree` to appear in the published site.
6. **License** — Apache License 2.0. Follow JetBrains Open Source Code of Conduct.
