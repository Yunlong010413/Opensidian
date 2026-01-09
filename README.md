# Opensidian

[English](README.md) | [中文](README_zh.md)

**Opensidian** is a powerful, multi-provider AI assistant plugin for Obsidian, capable of running **Anthropic (Claude)**, **OpenAI (GPT)**, and **Aliyun (Qwen)** models directly within your notes.

It is a feature-rich fork/port of the excellent [Claudian](https://github.com/YishenTu/claudian) plugin, extended to support multiple AI providers, custom models, and enhanced customization.

![Preview](https://github.com/Yunlong010413/Opensidian/blob/main/Preview.png)

## ✨ Key Features

- **Multi-Provider Support**: Switch seamlessly between **Claude**, **GPT**, and **Qwen** (Aliyun).
- **Custom Model Support**: Add *any* model ID for any provider (e.g., `gpt-4o`, `qwen-long`, `claude-3-opus-20240229`) via settings.
- **Context Management**: 
  - **Auto-Active Context**: The plugin automatically detects and includes your currently active note.
  - **@ File Reference**: Type `@` or click the button to fuzzy search and attach specific files as context.
  - **Folder Context**: Select an external folder (Desktop only) to include in the context.
- **Rich UI**:
  - **Native Look & Feel**: Designed to match Obsidian and Claudian's premium aesthetic.
  - **One-Click Copy**: Copy code blocks with language detection or copy entire AI responses.
  - **Typing Indicators**: Smooth animations for "Thinking" states.
  - **Dynamic Theming**: Interface colors adapt to the selected provider (Orange for Claude, Purple for OpenAI, Blue for Qwen).
- **Mega Strategy API Compatibility**: V3.0 features a robust fallback system (Fetch Stream / Obsidian Request × Standard/Alt/Min payload) for seamless compatibility with custom proxies (e.g., One API) and "Invalid Request" errors.
- **Chat History**: Save and restore chat sessions, searchable via a fuzzy command palette.

## 🚀 Installation

### Manual Installation (Release Zip)
1.  Download the latest `opensidian-x.x.x.zip` from the Releases page.
2.  Extract the zip file.
3.  Copy the extracted folder to your Obsidian vault's plugins directory: `<VaultFolder>/.obsidian/plugins/`.
4.  Restart Obsidian.
5.  Enable **Opensidian** in `Settings > Community Plugins`.

## ⚙️ Configuration

Go to `Settings > Opensidian` to configure your API keys.

### 1. General
- **User Name**: How the AI should address you.
- **Default Provider**: Select your preferred AI provider to start with.

### 2. Providers & Keys
Fill in the API Key for the provider(s) you intend to use. You can leave others blank.

- **Anthropic (Claude)**:
  - API Key: `sk-ant-...`
  - Base URL: (Optional) Proxy URL.
- **OpenAI / Compatible**:
  - API Key: `sk-...`
  - Base URL: `https://api.openai.com/v1` (or compatible proxy).
- **Aliyun (Qwen)**:
  - API Key: `sk-...` (DashScope API Key)
  - Base URL: `https://dashscope.aliyuncs.com/compatible-mode/v1`
  - 🎁 **Recommended for Chinese users**: Sign up at [Aliyun Bailian](https://bailian.console.aliyun.com) to get **free tokens** to get started! This plugin was built and tested with Aliyun's Qwen models.

### 3. Custom Models
If a new model is released (e.g., `gpt-5`, `qwen-coder-plus`), you don't need to wait for a plugin update!
- Enter the Model ID in the **Custom Models** text area for the respective provider.
- Separate multiple IDs with commas or newlines.
- These will immediately appear in the model selection dropdown in the chat view.

## 💡 Usage

1.  **Open Chat**: Click the **Opensidian** icon in the ribbon (left sidebar) or use the command `Opensidian: Open Chat`.
2.  **Select Model**: Use the dropdowns at the bottom of the chat view to switch Providers and Models.
3.  **Add Context**:
    - Your active note is automatically added.
    - Click **@** or the **Folder** icon to add more files.
4.  **Chat**: Type your prompt and hit `Enter` (or `Shift+Enter` for new line).
5.  **Copying**:
    - Hover over code blocks to see the language label—click it to copy code.
    - Hover over any AI message to see the "Copy" button—click it to copy the full response.

## ❤️ Credits
Based on the [Claudian](https://github.com/YishenTu/claudian) plugin by Shabegom.
Opensidian extends this foundation to bring the power of choice (OpenAI, Qwen) to the same beautiful interface,but lost something.

## 📄 License
MIT
