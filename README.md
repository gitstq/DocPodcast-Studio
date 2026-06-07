<p align="center">
  <h1 align="center">DocPodcast Studio</h1>
  <p align="center"><strong>轻量级文档转AI播客引擎</strong></p>
  <p align="center">
    <a href="https://github.com/gitstq/DocPodcast-Studio"><img src="https://img.shields.io/badge/版本-v1.0.0-blue.svg" alt="Version"></a>
    <a href="https://github.com/gitstq/DocPodcast-Studio/blob/main/LICENSE"><img src="https://img.shields.io/badge/协议-MIT-green.svg" alt="License"></a>
    <a href="https://github.com/gitstq/DocPodcast-Studio"><img src="https://img.shields.io/badge/零依赖-纯前端-orange.svg" alt="Zero Dependencies"></a>
  </p>
</p>

<p align="center">
  <a href="#简体中文">简体中文</a> | <a href="#繁體中文">繁體中文</a> | <a href="#english">English</a>
</p>

---

## 简体中文

![Screenshot](docs/screenshot.png)

### 🎉 项目介绍

**DocPodcast Studio** 是一款轻量级的文档转AI播客引擎，旨在让每一份文档都能以播客的形式被"听见"。

**解决的核心痛点：**

- 📄 文档阅读门槛高——长篇技术文档、论文、报告让人望而却步
- 🎙️ 播客制作门槛高——需要专业录音设备、剪辑软件和配音能力
- 🔌 现有工具依赖重——动辄需要配置复杂环境、安装大量依赖

**差异化亮点：**

- **零依赖纯前端**：纯 HTML + CSS + JavaScript，无需安装任何包管理器或运行时环境
- **开箱即用**：浏览器打开 `index.html` 即可运行，无需构建、无需编译
- **双引擎AI脚本**：内置模板引擎（零API调用）+ 多LLM API支持（GLM-5.1 / OpenAI / Claude），灵活切换
- **全流程闭环**：从文档上传、脚本生成、章节编排、语音合成到字幕导出，一站搞定

---

### ✨ 核心特性

- 📂 **文档上传与解析** — 支持 TXT、Markdown、JSON 三种主流格式，智能提取内容结构
- 🤖 **AI播客脚本生成** — 内置模板引擎（零API调用即可生成播客脚本），同时支持接入 GLM-5.1、OpenAI、Claude 等大语言模型API，**满足不同场景需求**
- 📋 **播客章节管理** — 可视化章节列表，支持**拖拽排序**与实时编辑，轻松编排播客结构
- 🔊 **TTS语音合成** — 基于浏览器原生 Web Speech API，**支持多语言语音合成**，无需额外服务
- ▶️ **音频播放器** — 内置播放器支持播放/暂停、进度拖拽、**语速调节**，播放体验完整
- ✏️ **脚本编辑器** — 编辑与预览**双模式切换**，所见即所得地打磨播客脚本
- 📝 **导出SRT字幕与Markdown** — 一键导出SRT字幕文件和Markdown格式脚本，方便分发与存档
- 🕸️ **知识图谱Canvas可视化** — 以交互式图谱展示文档核心概念与关联关系，**直观呈现知识脉络**
- 🌓 **暗色/亮色主题切换** — 自由切换暗色与亮色主题，**适应不同使用场景与个人偏好**
- 🌐 **中英文界面切换** — 完整支持中文与英文界面，**服务全球用户**
- 📱 **响应式设计** — 桌面端与移动端均可流畅使用，**随时随地制作播客**

---

### 🚀 快速开始

**环境要求：**

- 现代浏览器（Chrome 90+、Firefox 88+、Safari 14+、Edge 90+）
- 无需安装任何其他软件或依赖

**使用步骤：**

```bash
# 1. 克隆仓库
git clone https://github.com/gitstq/DocPodcast-Studio.git

# 2. 进入项目目录
cd DocPodcast-Studio

# 3. 直接在浏览器中打开 index.html 即可使用
#    推荐使用本地服务器以获得最佳体验：
python -m http.server 8080
# 然后访问 http://localhost:8080
```

> 💡 **提示**：也可以直接双击 `index.html` 文件在浏览器中打开，功能完全可用。使用本地服务器可避免部分浏览器对本地文件API的限制。

---

### 📖 详细使用指南

#### 📂 文档上传与解析

点击界面上方的"上传文档"按钮，选择 TXT、Markdown 或 JSON 格式的文件。系统会自动解析文件内容并提取文本结构，为后续脚本生成做好准备。

#### 🤖 AI脚本生成

系统提供两种脚本生成方式：

- **模板引擎模式**：无需配置任何API，基于内置模板自动生成播客脚本，适合快速体验和离线使用
- **LLM API模式**：在设置中配置 API Key 后，可选择接入 GLM-5.1、OpenAI 或 Claude 模型，获得更高质量的播客脚本

#### 📋 章节管理

脚本生成后，播客内容会被拆分为多个章节。你可以通过拖拽调整章节顺序，点击章节卡片进行编辑，或添加/删除章节来优化播客结构。

#### 🔊 语音合成与播放

点击"合成语音"按钮，系统将调用浏览器 TTS 引擎逐章合成音频。合成完成后，使用内置播放器即可播放播客，支持暂停、跳转进度和调节语速。

#### ✏️ 脚本编辑

在脚本编辑器中，可随时切换"编辑"与"预览"模式。编辑模式下可自由修改脚本文本，预览模式下可实时查看渲染效果。

#### 📝 导出功能

- **SRT字幕**：导出标准SRT格式字幕文件，可用于视频剪辑软件或字幕平台
- **Markdown脚本**：导出Markdown格式的播客脚本，方便存档和二次编辑

#### 🕸️ 知识图谱可视化

在知识图谱页面，系统会以交互式Canvas图谱展示文档中的核心概念及其关联关系。支持缩放、拖拽和节点点击交互，帮助你直观理解文档的知识脉络。

#### 🎨 主题与语言

- 在设置面板中可切换暗色/亮色主题
- 支持中文/英文界面切换，语言偏好会自动保存

---

### 💡 设计思路与迭代规划

**设计理念：**

- **极简优先**：零依赖、零构建，降低使用门槛，让技术不成为障碍
- **渐进增强**：内置模板引擎满足基础需求，API接入满足进阶需求
- **隐私安全**：模板模式下所有数据在本地处理，不上传任何信息到第三方服务器

**迭代规划：**

- 📌 **v1.1**：支持 PDF 和 DOCX 格式解析，增加更多播客脚本模板
- 📌 **v1.2**：引入音频波形可视化，优化播放器交互体验
- 📌 **v1.3**：支持自定义TTS引擎接入，增加语音角色选择
- 📌 **v2.0**：支持多人对话式播客，增加背景音乐与音效混合

---

### 📦 部署指南

本项目为纯静态项目，部署非常简单：

**方式一：GitHub Pages**

```bash
# 将仓库推送到 GitHub 后，进入仓库 Settings -> Pages
# 选择分支并保存，即可通过 GitHub Pages 访问
```

**方式二：任意静态文件服务器**

将项目所有文件上传到任意静态文件服务器（Nginx、Apache、Vercel、Netlify 等）即可。

**方式三：本地直接使用**

直接在浏览器中打开 `index.html` 文件即可运行。

---

### 🤝 贡献指南

欢迎任何形式的贡献！无论是提交Bug报告、功能建议还是代码贡献，都非常感谢。

**贡献流程：**

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/your-feature-name`
3. 提交更改：`git commit -m "feat: 描述你的更改"`
4. 推送分支：`git push origin feature/your-feature-name`
5. 提交 Pull Request

**注意事项：**

- 请保持零外部依赖的原则
- 代码风格请与现有代码保持一致
- 提交前请在本地测试确保功能正常

---

### 📄 开源协议

本项目基于 [MIT License](https://github.com/gitstq/DocPodcast-Studio/blob/main/LICENSE) 开源。

---

## 繁體中文

![Screenshot](docs/screenshot.png)

### 🎉 專案介紹

**DocPodcast Studio** 是一款輕量級的文件轉AI播客引擎，旨在讓每一份文件都能以播客的形式被「聽見」。

**解決的核心痛點：**

- 📄 文件閱讀門檻高——長篇技術文件、論文、報告讓人望而卻步
- 🎙️ 播客製作門檻高——需要專業錄音設備、剪輯軟體和配音能力
- 🔌 現有工具依賴重——動輒需要配置複雜環境、安裝大量依賴

**差異化亮點：**

- **零依賴純前端**：純 HTML + CSS + JavaScript，無需安裝任何套件管理器或執行環境
- **開箱即用**：瀏覽器開啟 `index.html` 即可運行，無需建置、無需編譯
- **雙引擎AI腳本**：內建模板引擎（零API呼叫）+ 多LLM API支援（GLM-5.1 / OpenAI / Claude），靈活切換
- **全流程閉環**：從文件上傳、腳本生成、章節編排、語音合成到字幕匯出，一站搞定

---

### ✨ 核心特性

- 📂 **文件上傳與解析** — 支援 TXT、Markdown、JSON 三種主流格式，智慧提取內容結構
- 🤖 **AI播客腳本生成** — 內建模板引擎（零API呼叫即可生成播客腳本），同時支援接入 GLM-5.1、OpenAI、Claude 等大型語言模型API，**滿足不同場景需求**
- 📋 **播客章節管理** — 可視化章節列表，支援**拖曳排序**與即時編輯，輕鬆編排播客結構
- 🔊 **TTS語音合成** — 基於瀏覽器原生 Web Speech API，**支援多語言語音合成**，無需額外服務
- ▶️ **音訊播放器** — 內建播放器支援播放/暫停、進度拖曳、**語速調節**，播放體驗完整
- ✏️ **腳本編輯器** — 編輯與預覽**雙模式切換**，所見即所得地打磨播客腳本
- 📝 **匯出SRT字幕與Markdown** — 一鍵匯出SRT字幕檔案和Markdown格式腳本，方便分發與存檔
- 🕸️ **知識圖譜Canvas視覺化** — 以互動式圖譜展示文件核心概念與關聯關係，**直觀呈現知識脈絡**
- 🌓 **暗色/亮色主題切換** — 自由切換暗色與亮色主題，**適應不同使用場景與個人偏好**
- 🌐 **中英文介面切換** — 完整支援中文與英文介面，**服務全球使用者**
- 📱 **響應式設計** — 桌面端與行動端均可流暢使用，**隨時隨地製作播客**

---

### 🚀 快速開始

**環境要求：**

- 現代瀏覽器（Chrome 90+、Firefox 88+、Safari 14+、Edge 90+）
- 無需安裝任何其他軟體或依賴

**使用步驟：**

```bash
# 1. 複製倉庫
git clone https://github.com/gitstq/DocPodcast-Studio.git

# 2. 進入專案目錄
cd DocPodcast-Studio

# 3. 直接在瀏覽器中開啟 index.html 即可使用
#    建議使用本地伺服器以獲得最佳體驗：
python -m http.server 8080
# 然後造訪 http://localhost:8080
```

> 💡 **提示**：也可以直接雙擊 `index.html` 檔案在瀏覽器中開啟，功能完全可用。使用本地伺服器可避免部分瀏覽器對本地檔案API的限制。

---

### 📖 詳細使用指南

#### 📂 文件上傳與解析

點擊介面上方的「上傳文件」按鈕，選擇 TXT、Markdown 或 JSON 格式的檔案。系統會自動解析檔案內容並提取文字結構，為後續腳本生成做好準備。

#### 🤖 AI腳本生成

系統提供兩種腳本生成方式：

- **模板引擎模式**：無需配置任何API，基於內建模板自動生成播客腳本，適合快速體驗和離線使用
- **LLM API模式**：在設定中配置 API Key 後，可選擇接入 GLM-5.1、OpenAI 或 Claude 模型，獲得更高品質的播客腳本

#### 📋 章節管理

腳本生成後，播客內容會被拆分為多個章節。你可以透過拖曳調整章節順序，點擊章節卡片進行編輯，或新增/刪除章節來優化播客結構。

#### 🔊 語音合成與播放

點擊「合成語音」按鈕，系統將呼叫瀏覽器 TTS 引擎逐章合成音訊。合成完成後，使用內建播放器即可播放播客，支援暫停、跳轉進度和調節語速。

#### ✏️ 腳本編輯

在腳本編輯器中，可隨時切換「編輯」與「預覽」模式。編輯模式下可自由修改腳本文字，預覽模式下可即時查看渲染效果。

#### 📝 匯出功能

- **SRT字幕**：匯出標準SRT格式字幕檔案，可用於影片剪輯軟體或字幕平台
- **Markdown腳本**：匯出Markdown格式的播客腳本，方便存檔和二次編輯

#### 🕸️ 知識圖譜視覺化

在知識圖譜頁面，系統會以互動式Canvas圖譜展示文件中的核心概念及其關聯關係。支援縮放、拖曳和節點點擊互動，幫助你直觀理解文件的知識脈絡。

#### 🎨 主題與語言

- 在設定面板中可切換暗色/亮色主題
- 支援中文/英文介面切換，語言偏好會自動儲存

---

### 💡 設計思路與迭代規劃

**設計理念：**

- **極簡優先**：零依賴、零建置，降低使用門檻，讓技術不成為障礙
- **漸進增強**：內建模板引擎滿足基礎需求，API接入滿足進階需求
- **隱私安全**：模板模式下所有資料在本地處理，不上傳任何資訊到第三方伺服器

**迭代規劃：**

- 📌 **v1.1**：支援 PDF 和 DOCX 格式解析，增加更多播客腳本模板
- 📌 **v1.2**：引入音訊波形視覺化，優化播放器互動體驗
- 📌 **v1.3**：支援自訂TTS引擎接入，增加語音角色選擇
- 📌 **v2.0**：支援多人對話式播客，增加背景音樂與音效混合

---

### 📦 部署指南

本專案為純靜態專案，部署非常簡單：

**方式一：GitHub Pages**

```bash
# 將倉庫推送到 GitHub 後，進入倉庫 Settings -> Pages
# 選擇分支並儲存，即可透過 GitHub Pages 造訪
```

**方式二：任意靜態檔案伺服器**

將專案所有檔案上傳到任意靜態檔案伺服器（Nginx、Apache、Vercel、Netlify 等）即可。

**方式三：本地直接使用**

直接在瀏覽器中開啟 `index.html` 檔案即可運行。

---

### 🤝 貢獻指南

歡迎任何形式的貢獻！無論是提交Bug報告、功能建議還是程式碼貢獻，都非常感謝。

**貢獻流程：**

1. Fork 本倉庫
2. 建立特性分支：`git checkout -b feature/your-feature-name`
3. 提交變更：`git commit -m "feat: 描述你的變更"`
4. 推送分支：`git push origin feature/your-feature-name`
5. 提交 Pull Request

**注意事項：**

- 請保持零外部依賴的原則
- 程式碼風格請與現有程式碼保持一致
- 提交前請在本地測試確保功能正常

---

### 📄 開源協議

本專案基於 [MIT License](https://github.com/gitstq/DocPodcast-Studio/blob/main/LICENSE) 開源。

---

## English

![Screenshot](docs/screenshot.png)

### 🎉 Introduction

**DocPodcast Studio** is a lightweight document-to-AI-podcast engine designed to turn any document into an audible podcast experience.

**Core Problems Solved:**

- 📄 **High reading barrier** — Long technical docs, papers, and reports are intimidating to read through
- 🎙️ **High production barrier** — Creating podcasts requires professional recording equipment, editing software, and voiceover skills
- 🔌 **Heavy dependencies** — Existing tools often require complex environment setup and numerous dependencies

**What Makes Us Different:**

- **Zero-dependency pure frontend** — Built with plain HTML + CSS + JavaScript. No package managers or runtimes needed
- **Ready out of the box** — Open `index.html` in any browser and you're good to go. No build step, no compilation
- **Dual-engine AI scripting** — Built-in template engine (zero API calls) + multi-LLM API support (GLM-5.1 / OpenAI / Claude), switch as you need
- **End-to-end workflow** — From document upload, script generation, chapter arrangement, and speech synthesis to subtitle export — all in one place

---

### ✨ Core Features

- 📂 **Document Upload & Parsing** — Supports TXT, Markdown, and JSON formats with intelligent content structure extraction
- 🤖 **AI Podcast Script Generation** — Built-in template engine generates scripts with zero API calls; also supports GLM-5.1, OpenAI, and Claude APIs for **higher-quality output**
- 📋 **Podcast Chapter Management** — Visual chapter list with **drag-and-drop reordering** and inline editing for easy podcast structuring
- 🔊 **TTS Speech Synthesis** — Powered by the browser-native Web Speech API with **multi-language support**, no external services required
- ▶️ **Audio Player** — Built-in player with play/pause, seekable progress bar, and **playback speed control** for a complete listening experience
- ✏️ **Script Editor** — **Dual-mode switching** between edit and preview, WYSIWYG podcast script refinement
- 📝 **Export SRT Subtitles & Markdown** — One-click export to standard SRT subtitle files and Markdown-formatted scripts for easy distribution and archiving
- 🕸️ **Knowledge Graph Canvas Visualization** — Interactive canvas graph displaying core concepts and their relationships from your document, **making knowledge connections visually intuitive**
- 🌓 **Dark/Light Theme Toggle** — Freely switch between dark and light themes to **suit different environments and personal preferences**
- 🌐 **Chinese/English Interface** — Full bilingual support for **serving a global user base**
- 📱 **Responsive Design** — Smooth experience on both desktop and mobile, **create podcasts anytime, anywhere**

---

### 🚀 Quick Start

**Requirements:**

- A modern browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)
- No other software or dependencies needed

**Steps:**

```bash
# 1. Clone the repository
git clone https://github.com/gitstq/DocPodcast-Studio.git

# 2. Navigate to the project directory
cd DocPodcast-Studio

# 3. Open index.html directly in your browser to get started
#    For the best experience, use a local server:
python -m http.server 8080
# Then visit http://localhost:8080
```

> 💡 **Tip**: You can also simply double-click the `index.html` file to open it in your browser — all features will work. Using a local server avoids certain browser restrictions on local file APIs.

---

### 📖 Detailed User Guide

#### 📂 Document Upload & Parsing

Click the "Upload Document" button at the top of the interface and select a TXT, Markdown, or JSON file. The system will automatically parse the file content and extract the text structure, preparing it for script generation.

#### 🤖 AI Script Generation

Two script generation modes are available:

- **Template Engine Mode**: No API configuration needed. Generates podcast scripts using built-in templates — perfect for quick trials and offline use
- **LLM API Mode**: After configuring an API Key in settings, connect to GLM-5.1, OpenAI, or Claude models for higher-quality podcast scripts

#### 📋 Chapter Management

After script generation, the podcast content is split into multiple chapters. Drag and drop to reorder chapters, click chapter cards to edit, or add/remove chapters to optimize the podcast structure.

#### 🔊 Speech Synthesis & Playback

Click the "Synthesize Speech" button and the system will invoke the browser's TTS engine to synthesize audio chapter by chapter. Once complete, use the built-in player to listen to your podcast with pause, seek, and speed controls.

#### ✏️ Script Editing

In the script editor, switch between "Edit" and "Preview" modes at any time. Edit mode allows free-form text modification, while Preview mode renders the formatted output in real time.

#### 📝 Export

- **SRT Subtitles**: Export standard SRT subtitle files compatible with video editors and subtitle platforms
- **Markdown Script**: Export Markdown-formatted podcast scripts for archiving and further editing

#### 🕸️ Knowledge Graph Visualization

The Knowledge Graph page renders an interactive Canvas graph showing core concepts and their relationships extracted from your document. Supports zoom, pan, and node-click interactions for intuitive understanding of the document's knowledge structure.

#### 🎨 Theme & Language

- Toggle between dark and light themes in the settings panel
- Switch between Chinese and English interfaces; language preferences are saved automatically

---

### 💡 Design Philosophy & Roadmap

**Design Principles:**

- **Simplicity first** — Zero dependencies, zero build steps. Lower the barrier to entry so technology never gets in the way
- **Progressive enhancement** — Built-in templates cover basic needs; API integration serves advanced use cases
- **Privacy & security** — In template mode, all data is processed locally. Nothing is sent to third-party servers

**Roadmap:**

- 📌 **v1.1**: PDF and DOCX format parsing; additional podcast script templates
- 📌 **v1.2**: Audio waveform visualization; improved player interaction
- 📌 **v1.3**: Custom TTS engine integration; voice character selection
- 📌 **v2.0**: Multi-speaker conversational podcasts; background music and sound effect mixing

---

### 📦 Deployment Guide

This is a purely static project, making deployment straightforward:

**Option 1: GitHub Pages**

```bash
# After pushing the repo to GitHub, go to Settings -> Pages
# Select a branch and save — your site will be live via GitHub Pages
```

**Option 2: Any Static File Server**

Upload all project files to any static file hosting service (Nginx, Apache, Vercel, Netlify, etc.).

**Option 3: Local Usage**

Simply open `index.html` directly in your browser.

---

### 🤝 Contributing

Contributions of all kinds are welcome — bug reports, feature suggestions, and code contributions are all greatly appreciated.

**How to Contribute:**

1. Fork this repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "feat: describe your changes"`
4. Push the branch: `git push origin feature/your-feature-name`
5. Submit a Pull Request

**Guidelines:**

- Please maintain the zero-external-dependency principle
- Follow the existing code style
- Test locally before submitting to ensure everything works correctly

---

### 📄 License

This project is open-sourced under the [MIT License](https://github.com/gitstq/DocPodcast-Studio/blob/main/LICENSE).

---

<p align="center">
  Built with ❤️ by <a href="https://github.com/gitstq/DocPodcast-Studio">DocPodcast Studio Team</a>
</p>
