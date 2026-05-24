# 🚀 npm管理器 v1.0.0 正式发布

> 一键管理 npm 包的可视化工具，支持命令行 / 桌面 / 网页三种界面，无需记忆任何 npm 命令。

---

## ✨ 功能特性

### 📦 包管理
- 查看本地和全局已安装的 npm 包
- 过期版本高亮显示，一目了然
- 漏洞包红色标记，安全风险早知道
- 支持同时操作多个包

### ⬇️ 安装 / ⬆️ 更新 / 🗑️ 卸载
- 支持多包空格分隔安装：`express axios lodash`
- 支持指定版本：`npm install vue@3.2.0`
- 一键更新全部过期包
- 卸载有二次确认，防止误操作

### 🌍 镜像源管理
- 内置四大镜像源：官方 / 淘宝 / 腾讯云 / 华为云
- 一键切换，自动验证连通性
- 失败自动回滚，绝不断线
- **测速功能**：四源 Ping 对比，毫秒级显示最快源

### 🧹 项目清理
- 清理 node_modules 释放磁盘空间
- 彻底重置项目（+ package-lock.json）
- 显示清理前后的空间大小

### 💾 npm 缓存管理
- 查看缓存路径和占用大小
- `npm cache verify` 校验缓存完整性
- 一键清理缓存

### 🛡️ npm 错误中文翻译
- 常见 npm 错误信息自动翻译为中文提示
- 无需 Google 搜索，直接看懂报错

---

## 🖥️ 三种界面

| 界面 | 启动命令 | 适用场景 |
|------|---------|---------|
| **命令行 TUI** | `node tui/index.js` | 服务器、无图形环境 |
| **桌面 GUI** | `cd gui && npm start` | Windows/macOS 桌面 |
| **网页仪表盘** | `cd web && npm start` | 手机、平板、多设备管理 |

---

## 🔧 快速开始

```bash
# TUI 命令行
npm install
node tui/index.js

# GUI 桌面
cd gui
npm install
npm start

# Web 仪表盘
cd web
npm install
npm start
# 访问 http://localhost:8080
```

---

## 🛠️ 技术栈

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Electron-47848F?style=for-the-badge&logo=electron&logoColor=white" alt="Electron">
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/Inquirer.js-E34F26?style=for-the-badge&logo=npm&logoColor=white" alt="Inquirer">
</p>

---

## 📁 项目结构

```
npm-manager/
├── core/               # 核心模块（所有阶段共用）
│   ├── npm.js          # 封装 npm CLI 调用
│   ├── mirror.js       # 镜像源切换与测速
│   └── utils.js        # 通用工具函数
├── tui/                # 命令行 TUI 界面
├── gui/                # 桌面 Electron GUI
├── web/                # 网页仪表盘
├── SPEC.md             # 功能规格说明书
└── README.md
```

---

## 📌 支持的平台

- ✅ Windows 10/11
- ✅ macOS
- ✅ Linux

---

## 📄 License

MIT — 放心使用，欢迎 Star ⭐

---

**如果你觉得这个项目有帮助，欢迎在 GitHub 上点个 ⭐**
