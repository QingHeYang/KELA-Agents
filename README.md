<h1 align="center">
  <img src="images/logo.png" alt="KELA Agents Logo" width="36" style="vertical-align: middle;">
  KELA Agents
</h1>
<p align="center"><strong>Koalaq Excel Agents - Excel 数据分析智能体</strong></p>

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
  <strong>让 AI 帮你分析 Excel，用自然语言查询数据</strong><br>
  无需编写公式或 SQL，轻松处理 50+ 列、10 万+ 行的大型表格
</p>

<p align="center">
  <strong>简体中文</strong> | <a href="docs/en/README.md">English</a>
</p>

---

## 项目理念

| 理念 | 说明 |
|:---:|------|
| **关注数据，简化操作** | 一切操作围绕数据展开，让用户最直观地找到核心信息 |
| **关注需求，操作溯源** | 所有工具为用户目标而设计，每一步操作都可追溯验证 |
| **关注安全，选择自由** | 数据留存本地，使用自己的 LLM 配置，按量付费无绑定 |

## 功能截图

<table>
  <tr>
    <td><img src="images/Home.png" width="400" alt="主页"></td>
    <td><img src="images/工作区详情.png" width="400" alt="工作区详情"></td>
  </tr>
  <tr>
    <td><img src="images/数据表.png" width="400" alt="数据表"></td>
    <td><img src="images/智能理解分析.png" width="400" alt="智能导入"></td>
  </tr>
</table>

> [查看完整截图](docs/zh/screenshots.md)

---

## 工作原理

```
导入 Excel  ──→  AI 智能理解  ──→  数据入库  ──→  自然语言问答  ──→  结果输出
                     │                              │
                     ▼                              ▼
              识别表头结构                    AI 将问题转为 SQL
              理解字段含义                    执行查询/聚合/修改
```

---

## 工作流程

<details>
<summary><b>第一阶段：智能导入</b></summary>

<br>

| 步骤 | 说明 |
|:---:|------|
| **智能理解分析** | LLM 分析数据结构，出具可行性报告，评估是否可导入 |
| **表头识别与描述填充** | 确认数据起始行，识别表头层级，自动填充字段描述 |
| **深度分析**（可选） | 统计数据分布，理解数据格式与形状，提升首次问答准确率 |

</details>

<details>
<summary><b>第二阶段：数据入库</b></summary>

<br>

| 步骤 | 说明 |
|:---:|------|
| **创建数据表** | 根据 AI 分析结果自动创建结构化数据表 |
| **导入数据** | 将 Excel 数据写入本地数据库 |
| **字段管理** | 用户可修改字段描述、类型等配置，支持多表管理 |

> 支持最多 3 个 Excel，合计 100 列

</details>

<details>
<summary><b>第三阶段：自然语言问答</b></summary>

<br>

**流程**：用户提问 → LLM 理解意图 → 调用工具 → 收集信息 → 给出结论

**工具集**：

| 工具 | 功能 |
|:---:|------|
| 数据筛选 | 按条件筛选数据，支持复杂条件组合 |
| 数据聚合 | 统计、分组、排序等聚合操作 |
| 图表生成 | 8 种图表类型可视化数据 |
| 黑板总结 | 将关键信息整理展示给用户 |
| 导出 Excel | 将查询结果导出为 Excel 文件 |

**示例问题**：
- "销售额最高的 10 个产品是什么？"
- "按地区统计订单数量，画个饼图"
- "把上海的客户数据导出成 Excel"

</details>

<details>
<summary><b>第四阶段：过程管理</b></summary>

<br>

| 功能 | 说明 |
|:---:|------|
| **数据溯源** | 每次查询保存过程数据，点击结果可追溯原始 SQL，方便核查验证 |
| **图表管理** | 历史图表可反复查看，支持重新编辑导出，溯源到对应对话轮次 |
| **文件管理** | 导出文件统一管理，随时打开文件位置，清晰掌握所有产出 |

</details>

## 核心功能

### 智能问答

| 功能 | 说明 |
|:---:|------|
| **自然语言查询** | 用日常语言提问，AI 自动转换为精确的数据库查询 |
| **多轮对话** | 支持上下文连续对话，逐步深入分析 |
| **消息管理** | 历史对话可查看、可追溯，每轮问答结果可复现 |
| **引用功能** | 引用之前的查询结果，减少重复输入 |

### 数据管理

| 功能 | 说明 |
|:---:|------|
| **多表支持** | 单工作区最多导入 3 个 Excel，合计 100 列 |
| **多表联查** | 多个 Excel 数据表可关联查询分析 |
| **字段管理** | 查看、编辑字段描述和类型，优化 AI 理解 |
| **快速隐藏列** | 批量隐藏无关列，聚焦核心数据 |

### 数据可视化

支持 **8 种图表类型**，基于 ECharts：

| 柱状图 | 折线图 | 饼图 | 散点图 |
|:------:|:------:|:----:|:------:|
| 面积图 | 漏斗图 | 雷达图 | 词云 |

- 图表可保存为图片
- 历史图表统一管理，可反复查看
- 点击可溯源到对应对话轮次

### Excel 导出

**4 种导出方式**：

| 方式 | 说明 |
|:---:|------|
| **全表导出** | 导出完整数据表 |
| **筛选导出** | 按当前筛选条件导出 |
| **查询导出** | 导出 AI 查询结果 |
| **AI 生成** | 用自然语言描述需求，AI 聚合生成报表 |

### 黑板功能

- AI 将关键结论整理到黑板，清晰呈现分析结果
- 全部黑板记录可统一查看

---

## 支持的 LLM 平台

| 国际平台 | 国内平台 | 本地部署 |
|:---:|:---:|:---:|
| ChatGPT | 通义千问 | Ollama |
| Claude | DeepSeek | Xinference |
| Gemini | 智谱 ChatGLM | |
| Grok | 豆包 | |
| | Kimi | |
| | 文心一言 | |

> 支持所有 OpenAI 兼容接口，使用自己的 API Key，按量付费

---

## 优势与局限

<table>
<tr>
<th>✅ 优势</th>
<th>⚠️ 局限</th>
</tr>
<tr>
<td>

**性能**
- 50+ 列、10 万+ 行数据可快速查询
- 基于数据库设计，数据量越大优势越明显

**安全**
- 数据完全本地存储，不上传任何平台
- 仅向 LLM 发送必要查询信息

**透明**
- 所有 AI 操作可追溯
- 查询结果可验证复现

**成本**
- 软件免费使用
- 按量付费，用自己的 API Key

</td>
<td>

**格式限制**
- 仅支持单 Sheet（多 Sheet 需拆分导入）
- 无法调整 Excel 样式

**功能边界**
- 不能直接操作 Office 文件
- 无法对已有表追加数据（AI 新增除外）
- 操作灵活性不如原生 Excel

**适用场景**
- 小数据量（几十行）建议直接用 Excel
- 首次导入需 AI 理解表头，耗时较长

</td>
</tr>
</table>

### 容量限制

| 项目 | 限制 |
|:---:|:---:|
| Excel 文件数 | 最多 3 个/工作区 |
| 数据列数 | 最多 100 列（合计） |
| 数据行数 | 无限制（取决于内存） |

> 📊 [查看详细性能测试数据](docs/zh/performance.md)

## 多语言支持

| 语言 | Language | 状态 |
|:---:|:---:|:---:|
| 简体中文 | Chinese (Simplified) | ✅ |
| English | English | ✅ |
| 日本語 | Japanese | ✅ |
| 한국어 | Korean | ✅ |
| Français | French | ✅ |
| Deutsch | German | ✅ |
| Русский | Russian | ✅ |

## 开源计划

本项目计划开源，目前仍在积极开发中，待功能稳定后将公开源代码。

当前状态：**开发中，暂未开源**

> 欢迎 Star 本仓库，关注项目进展！

## 下载安装

从 [Releases](https://github.com/QingHeYang/KELA-Agents/releases) 页面下载：

| 平台 | 文件 |
|:---:|------|
| Windows | `KELA-Agents-x.x.x-Setup.exe` |
| macOS (Apple Silicon) | `KELA-Agents-x.x.x-arm64.dmg` |

| 项目 | 大小 |
|:---:|:---:|
| 安装包 | ~170 MB |
| 安装后占用 | ~660 MB |

## 贡献与反馈

- [提交 Bug](https://github.com/QingHeYang/KELA-Agents/issues/new?template=bug_report.md)
- [功能建议](https://github.com/QingHeYang/KELA-Agents/issues/new?template=feature_request.md)
- [使用问题](https://github.com/QingHeYang/KELA-Agents/issues/new?template=question.md)

## 许可证

[MIT License](LICENSE)
