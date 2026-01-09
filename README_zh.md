# Opensidian

[English](README.md) | [中文](README_zh.md)

**Opensidian** 是一个功能强大的 Obsidian 多供应商 AI 助手插件，支持在您的笔记中直接运行 **Anthropic (Claude)**、**OpenAI (GPT)** 和 **阿里云 (Qwen/通义千问)** 模型。

它是优秀的 [Claudian](https://github.com/YishenTu/claudian) 插件的一个功能丰富的分支/移植版本，扩展了多 AI 供应商支持、自定义模型和增强的个性化设置。

![Preview](https://github.com/Preview.png)

## ✨主要功能

- **多供应商支持**：无缝切换 **Claude**、**GPT** 和 **Qwen** (阿里云)。
- **自定义模型支持**：通过设置添加任意供应商的任意模型 ID（例如 `gpt-4o`、`qwen-long`、`claude-3-opus-20240229`），即时生效。
- **上下文管理**：
  - **自动当前上下文**：插件会自动检测并包含您当前激活的笔记内容。
  - **@ 文件引用**：输入 `@` 或点击按钮进行模糊搜索，将特定文件添加为上下文。
  - **文件夹上下文**：选择外部文件夹（仅限桌面版）加入上下文。
- **丰富的 UI**：
  - **原生外观**：设计风格完美贴合 Obsidian 和 Claudian 的高级美学。
  - **一键复制**：支持带语言检测的代码块复制，或复制整段 AI 回复。
  - **输入动画**：流畅的“思考中”状态动画。
  - **动态主题**：界面颜色根据所选供应商动态变化（Claude 为橙色，OpenAI 为紫色，Qwen 为蓝色）。
- **终极 API 兼容性 (Mega Strategy)**：V3.0 内置多重回退策略（Fetch/Obsidian 请求 × 标准/Alt/Min 载荷），完美兼容各类第三方代理（如 One API, New API），彻底解决 400 错误。
- **对话历史**：保存并恢复对话会话，支持通过模糊命令面板搜索。

## 🚀 安装指南

### 手动安装 (Release Zip)
1. 从 Releases 页面下载最新的 `opensidian-x.x.x.zip`。
2. 解压该 zip 文件。
3. 将解压后的文件夹复制到您的 Obsidian 仓库插件目录：`<VaultFolder>/.obsidian/plugins/`。
4. 重启 Obsidian。
5. 在 `设置 > 第三方插件` 中启用 **Opensidian**。

## ⚙️ 配置指南

前往 `设置 > Opensidian` 配置您的 API Key。

### 1. 通用设置
- **User Name**：AI 如何称呼您。
- **Default Provider**：默认使用的 AI 供应商。

### 2. 供应商与密钥 (Providers & Keys)
填写您打算使用的供应商的 API Key。不使用的可以留空。

- **Anthropic (Claude)**:
  - API Key: `sk-ant-...`
  - Base URL: (可选) 代理地址。
- **OpenAI / Compatible**:
  - API Key: `sk-...`
  - Base URL: `https://api.openai.com/v1` (或兼容的代理地址)。
- **Aliyun (Qwen / 通义千问)**:
  - API Key: `sk-...` (DashScope API Key)
  - Base URL: `https://dashscope.aliyuncs.com/compatible-mode/v1`
  - 🎁 **国内用户推荐**：前往 [阿里云百炼](https://bailian.console.aliyun.com) 注册，**可免费获取 Token**，足够日常使用！本插件基于阿里云通义系列模型开发和测试。这里感谢一下hhh虽然没有get任何。

### 3. 自定义模型 (Custom Models)
如果有新模型发布（例如 `gpt-5`、`qwen-coder-plus`），您无需等待插件更新！
- 在对应供应商的 **Custom Models** 文本框中输入模型 ID。
- 多个 ID 请用逗号或换行分隔。
- 这些模型将立即出现在聊天界面的模型选择下拉列表中。

## 💡 使用说明

1.  **打开聊天**：点击左侧边栏（Ribbon）的 **Opensidian** 图标，或使用命令 `Opensidian: Open Chat`。
2.  **选择模型**：使用聊天视图底部的下拉菜单切换供应商 (Provider) 和模型 (Model)。
3.  **添加上下文**：
    - 当前激活的笔记会自动添加。
    - 点击 **@** 或 **文件夹** 图标添加更多文件。
4.  **聊天**：输入您的提示词并按 `Enter` 发送（`Shift+Enter` 换行）。
5.  **复制**：
    - 悬停在代码块上可以看到语言标签——点击即可复制代码。
    - 悬停在任意 AI 消息上可以看到 "Copy" 按钮——点击即可复制完整回复。

## ❤️ 致谢
基于 Shabegom 的 [Claudian](https://github.com/YishenTu/claudian) 插件开发。
Opensidian 在此基础上扩展了选择权（OpenAI, Qwen），同时保留了其精美的界面设计，但是也去掉了许多内容（属实看不懂了）。

## 📄 许可证
MIT
