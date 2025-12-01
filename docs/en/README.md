<h1 align="center">
  <img src="../../images/logo.png" alt="KELA Agents Logo" width="36" style="vertical-align: middle;">
  KELA Agents
</h1>
<p align="center"><strong>Koalaq Excel Agents - Intelligent Excel Data Analysis Agent</strong></p>

<p align="center">
  <a href="https://github.com/QingHeYang/KELA-Agents/releases/latest">
    <img src="https://img.shields.io/github/v/release/QingHeYang/KELA-Agents?style=flat-square&logo=github&label=Release" alt="Release">
  </a>
  <a href="https://github.com/QingHeYang/KELA-Agents/releases">
    <img src="https://img.shields.io/github/downloads/QingHeYang/KELA-Agents/total?style=flat-square&logo=github&label=Downloads" alt="Downloads">
  </a>
  <a href="https://github.com/QingHeYang/KELA-Agents/stargazers">
    <img src="https://img.shields.io/github/stars/QingHeYang/KELA-Agents?style=flat-square&logo=github&label=Stars" alt="Stars">
  </a>
  <a href="https://github.com/QingHeYang/KELA-Agents/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/QingHeYang/KELA-Agents?style=flat-square&label=License" alt="License">
  </a>
</p>

<p align="center">
  <strong>Let AI analyze your Excel data using natural language queries</strong><br>
  No formulas or SQL required. Handle 50+ columns and 100,000+ rows with ease.
</p>

<p align="center">
  <a href="../../README.md">简体中文</a> | <strong>English</strong>
</p>

---

## Philosophy

| Principle | Description |
|:---:|------|
| **Data-Focused, Simplified Operations** | All operations revolve around data, helping users find core information intuitively |
| **Goal-Oriented, Traceable Actions** | Every tool is designed for user objectives, with each operation fully traceable |
| **Security-First, Freedom of Choice** | Data stays local, use your own LLM configuration, pay-as-you-go with no lock-in |

## Screenshots

<table>
  <tr>
    <td><img src="../../images/Home.png" width="400" alt="Home"></td>
    <td><img src="../../images/工作区详情.png" width="400" alt="Workspace Details"></td>
  </tr>
  <tr>
    <td><img src="../../images/数据表.png" width="400" alt="Data Table"></td>
    <td><img src="../../images/智能理解分析.png" width="400" alt="Smart Import"></td>
  </tr>
</table>

> [View all screenshots](screenshots.md)

---

## How It Works

```
Import Excel  ──→  AI Understanding  ──→  Data Storage  ──→  Natural Language Q&A  ──→  Output
                        │                                         │
                        ▼                                         ▼
                 Identify headers                         AI converts questions to SQL
                 Understand fields                        Execute queries/aggregations
```

---

## Workflow

<details>
<summary><b>Phase 1: Smart Import</b></summary>

<br>

| Step | Description |
|:---:|------|
| **Smart Analysis** | LLM analyzes data structure, generates feasibility report, evaluates import compatibility |
| **Header Recognition & Description** | Confirms data start row, identifies header levels, auto-fills field descriptions |
| **Deep Analysis** (Optional) | Analyzes data distribution, understands data format and shape, improves first query accuracy |

</details>

<details>
<summary><b>Phase 2: Data Storage</b></summary>

<br>

| Step | Description |
|:---:|------|
| **Create Data Table** | Automatically creates structured tables based on AI analysis |
| **Import Data** | Writes Excel data to local database |
| **Field Management** | Users can modify field descriptions, types, and configurations |

> Supports up to 3 Excel files, 100 columns total per workspace

</details>

<details>
<summary><b>Phase 3: Natural Language Q&A</b></summary>

<br>

**Flow**: User Question → LLM Intent Understanding → Tool Invocation → Information Gathering → Conclusion

**Available Tools**:

| Tool | Function |
|:---:|------|
| Data Filtering | Filter data by conditions, supports complex combinations |
| Data Aggregation | Statistics, grouping, sorting operations |
| Chart Generation | 8 chart types for data visualization |
| Blackboard Summary | Organizes key information for users |
| Excel Export | Exports query results to Excel files |

**Example Questions**:
- "What are the top 10 products by sales?"
- "Show order counts by region as a pie chart"
- "Export all Shanghai customer data to Excel"

</details>

<details>
<summary><b>Phase 4: Process Management</b></summary>

<br>

| Feature | Description |
|:---:|------|
| **Data Traceability** | Every query saves process data, click results to trace original SQL for verification |
| **Chart Management** | Historical charts viewable anytime, supports re-editing and export, traceable to conversation |
| **File Management** | Unified export file management, quick access to file locations |

</details>

## Core Features

### Intelligent Q&A

| Feature | Description |
|:---:|------|
| **Natural Language Queries** | Ask in everyday language, AI converts to precise database queries |
| **Multi-turn Conversations** | Supports contextual continuous dialogue for deeper analysis |
| **Message Management** | Historical conversations viewable and traceable, each round reproducible |
| **Reference Function** | Reference previous query results to reduce repetitive input |

### Data Management

| Feature | Description |
|:---:|------|
| **Multi-table Support** | Up to 3 Excel files per workspace, 100 columns total |
| **Cross-table Queries** | Query across multiple Excel tables with associations |
| **Field Management** | View and edit field descriptions and types to optimize AI understanding |
| **Quick Hide Columns** | Batch hide irrelevant columns to focus on core data |

### Data Visualization

**8 chart types** supported, powered by ECharts:

| Bar | Line | Pie | Scatter |
|:------:|:------:|:----:|:------:|
| Area | Funnel | Radar | Word Cloud |

- Charts can be saved as images
- Historical charts unified management
- Click to trace back to corresponding conversation

### Excel Export

**4 export methods**:

| Method | Description |
|:---:|------|
| **Full Table** | Export complete data table |
| **Filtered** | Export by current filter conditions |
| **Query Results** | Export AI query results |
| **AI Generated** | Describe requirements in natural language, AI aggregates and generates report |

### Blackboard

- AI organizes key conclusions on the blackboard for clear presentation
- All blackboard records viewable in one place

---

## Supported LLM Platforms

| International | Chinese | Local Deployment |
|:---:|:---:|:---:|
| ChatGPT | Tongyi Qianwen | Ollama |
| Claude | DeepSeek | Xinference |
| Gemini | Zhipu ChatGLM | |
| Grok | Doubao | |
| | Kimi | |
| | Wenxin Yiyan | |

> Supports all OpenAI-compatible APIs. Use your own API Key, pay-as-you-go.

---

## Advantages & Limitations

<table>
<tr>
<th>✅ Advantages</th>
<th>⚠️ Limitations</th>
</tr>
<tr>
<td>

**Performance**
- Fast queries on 50+ columns, 100,000+ rows
- Database-based design, better with larger datasets

**Security**
- Data stored completely locally, never uploaded
- Only necessary query info sent to LLM

**Transparency**
- All AI operations traceable
- Query results verifiable and reproducible

**Cost**
- Software is free to use
- Pay-as-you-go with your own API Key

</td>
<td>

**Format Limitations**
- Single sheet only (split multi-sheet Excel before import)
- Cannot adjust Excel styling

**Functional Boundaries**
- Cannot directly manipulate Office files
- Cannot append data to existing tables (except AI additions)
- Less flexible than native Excel

**Use Cases**
- Small datasets (dozens of rows) better handled in Excel directly
- Initial import requires AI header understanding, takes time

</td>
</tr>
</table>

### Capacity Limits

| Item | Limit |
|:---:|:---:|
| Excel Files | Max 3 per workspace |
| Columns | Max 100 (combined) |
| Rows | Unlimited (depends on memory) |

## Language Support

| Language | Status |
|:---:|:---:|
| 简体中文 (Chinese Simplified) | ✅ |
| English | ✅ |
| 日本語 (Japanese) | ✅ |
| 한국어 (Korean) | ✅ |
| Français (French) | ✅ |
| Deutsch (German) | ✅ |
| Русский (Russian) | ✅ |

## Open Source Plan

This project plans to be open source. Currently in active development, source code will be released when features stabilize.

Current status: **In Development, Not Yet Open Source**

> Welcome to Star this repository to follow project progress!

## Download

Download from [Releases](https://github.com/QingHeYang/KELA-Agents/releases):

| Platform | File |
|:---:|------|
| Windows | `KELA-Agents-x.x.x-Setup.exe` |
| macOS (Apple Silicon) | `KELA-Agents-x.x.x-arm64.dmg` |

| Item | Size |
|:---:|:---:|
| Installer | ~170 MB |
| Installed | ~660 MB |

## Contributing & Feedback

- [Report Bug](https://github.com/QingHeYang/KELA-Agents/issues/new?template=bug_report.md)
- [Feature Request](https://github.com/QingHeYang/KELA-Agents/issues/new?template=feature_request.md)
- [Ask Question](https://github.com/QingHeYang/KELA-Agents/issues/new?template=question.md)

## License

[MIT License](../../LICENSE)
