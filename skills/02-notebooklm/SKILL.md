---
name: 02-notebooklm
description: NotebookLM 知識庫 — AI 知識庫串接與 MCP 外掛設定。
---

# 02-NotebookLM 知識庫

NotebookLM 是 Google 的 AI 知識庫工具。裝好之後，你的 AI 編輯器就能直接把資料丟進 NotebookLM 整理分析。

## 1. 安裝連線工具

在終端機輸入：
```powershell
pip install notebooklm-mcp-cli
```

### Mac 使用者
```bash
pip3 install notebooklm-mcp-cli
```

## 2. 登入 Google 帳號

```powershell
nlm login
```
瀏覽器會自動跳出來，登入你的 Google 帳號並允許授權。

## 3. 綁定你的 AI 編輯器

### 如果你用 Antigravity
```powershell
nlm setup add antigravity
```

### 如果你用 OpenCode
```powershell
nlm setup add opencode
```

## 4. 測試看看

輸入以下指令，看你有哪些筆記本：
```powershell
nlm list notebooks
```
如果有看到筆記本清單，就代表成功了！

## 小提醒

- **OpenCode 使用者**：綁定後重新啟動編輯器，AI 就能自動幫你操作 NotebookLM
- **Antigravity (Windows) 使用者**：因為系統保護較嚴格，AI 無法全自動上傳。你只要查出筆記本 ID，AI 會給你一行指令，複製貼上就能上傳

## ✅ 完成

NotebookLM 已連接完成！
