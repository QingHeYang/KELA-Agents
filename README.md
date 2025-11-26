<p align="center">
  <img src="images/logo.png" alt="KELA Agents Logo" width="128">
</p>

<h1 align="center">KELA Agents</h1>

<p align="center">
  智能 Excel 数据分析助手 - 让非技术用户通过自然语言查询和分析 Excel 数据
</p>

KELA (KoalaQ Excel Language Agent) 是一款面向办公白领的桌面应用，无需懂 SQL 或编程，只需用自然语言提问，即可完成复杂的数据查询、分析和可视化。

## ✨ 功能特性

- **自然语言查询** - 用日常语言提问，AI 自动转换为数据库查询
- **Excel 智能导入** - 自动识别表头、数据类型，一键导入
- **多表关联分析** - 支持跨表查询和数据关联
- **图表可视化** - 自动生成柱状图、折线图、饼图等
- **数据导出** - 查询结果可导出为 Excel 文件
- **本地运行** - 数据存储在本地，保护隐私安全

## 📸 截图

<!-- TODO: 添加应用截图 -->

## 🚀 快速开始

### 下载安装

从 [Releases](https://github.com/QingHeYang/KELA-Agents/releases) 页面下载最新版本：

- Windows: `KELA-Agents-x.x.x-Setup.exe`
- macOS (Intel): `KELA-Agents-x.x.x-x64.dmg`
- macOS (Apple Silicon): `KELA-Agents-x.x.x-arm64.dmg`

### 配置 LLM

首次使用需要配置大语言模型：

1. 打开应用，进入「设置」→「LLM 配置」
2. 选择模型提供商（支持 OpenAI、DeepSeek、通义千问等）
3. 填入 API Key
4. 测试连接成功后保存

### 开始使用

1. 创建工作区
2. 上传 Excel 文件
3. 等待 AI 自动分析表结构
4. 在对话框中用自然语言提问

## 💡 使用示例

```
用户: 统计每个部门的人数
AI: 已查询完成，共 5 个部门...

用户: 哪个部门平均工资最高？
AI: 研发部平均工资最高，为 ¥25,000...

用户: 用柱状图展示各部门人数
AI: [生成柱状图]
```

## 🛠 技术架构

```
┌─────────────────────────────────────┐
│         Electron 桌面应用            │
│  ┌───────────────────────────────┐  │
│  │      Vue 3 前端界面            │  │
│  └───────────────────────────────┘  │
│                 ↕                    │
│  ┌───────────────────────────────┐  │
│  │     Python 后端 (FastAPI)      │  │
│  │  • AI Agent 框架               │  │
│  │  • Excel 处理引擎              │  │
│  │  • SQLite 数据库               │  │
│  └───────────────────────────────┘  │
└─────────────────────────────────────┘
```

## 🌍 国际化

支持多语言界面：

- 简体中文 (zh-CN)
- English (en-US)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

- [提交 Bug](https://github.com/QingHeYang/KELA-Agents/issues/new?template=bug_report.md)
- [功能建议](https://github.com/QingHeYang/KELA-Agents/issues/new?template=feature_request.md)

## 📄 许可证

[MIT License](LICENSE)

## 📮 联系

- 作者: [QingHeYang](https://github.com/QingHeYang)
- 项目主页: [https://github.com/QingHeYang/KELA-Agents](https://github.com/QingHeYang/KELA-Agents)
