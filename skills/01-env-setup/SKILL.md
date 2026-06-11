---
name: 01-env-setup
description: 基礎環境建置 — Node.js、Python、PowerShell 權限設定。
---

# 01-基礎環境建置

在開始之前，你的電腦需要先安裝幾個「底層工具」。這就像在手機上裝 APP 一樣簡單。

## 1. 打開你的終端機

在 AI 編輯器（Antigravity 或 OpenCode）最下方，會有一個黑色的輸入框，叫做**終端機**或 **Terminal**。這就是你對電腦下指令的地方。

## 2. 設定執行權限

### Windows 使用者
Windows 會阻擋一些自動化腳本。請照著做：
1. 在「開始」選單搜尋 `PowerShell`
2. 按右鍵選**「以系統管理員身分執行」**
3. 複製貼上這行，按 Enter：
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
4. 如果問你是否確定，輸入 `Y` 按 Enter

### Mac 使用者
Mac 不需要做這個步驟，可以直接跳過。

## 3. 安裝 Node.js

Node.js 是讓你的電腦能執行 JavaScript 程式的工具。

### Windows
```powershell
winget install --id OpenJS.NodeJS.LTS -e --source winget
```

### Mac
```bash
brew install node
```

安裝完後，關掉終端機重新打開，輸入以下指令確認有裝好：
```powershell
node --version
npm --version
```
如果有出現版本號碼（例如 v18.xxx），就代表成功了！

## 4. 安裝 Python

Python 是目前最主流的程式語言，很多 AI 工具都靠它。

### Windows
1. 去 [Python 官網](https://www.python.org/downloads/) 下載最新版
2. **安裝時第一件事：一定要勾選「Add Python to PATH」**（非常重要！）
3. 其他一直按下一步就好

### Mac
```bash
brew install python
```

安裝完後確認：
```powershell
python --version
```

## ✅ 完成

基礎環境已經準備好了！接下來可以安裝其他技能了。
