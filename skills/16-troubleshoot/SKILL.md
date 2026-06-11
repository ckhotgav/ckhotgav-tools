---
name: 16-troubleshoot
description: 疑難排解 — 常見錯誤與修復流程。
---

# 16-疑難排解

遇到問題了嗎？以下整理最常見的錯誤和解決方法。

---

## 1. 「node 不是內部或外部命令」

**原因**：Node.js 沒裝好或路徑設定有問題。

**解決方法**：
1. 重新開機
2. 如果還是不行，重新安裝 Node.js（安裝時記得用預設路徑）

---

## 2. 「Python 不是內部或外部命令」

**原因**：安裝 Python 時忘了勾選「Add Python to PATH」。

**解決方法**：
1. 重新執行 Python 安裝檔
2. **這次一定要記得勾選「Add Python to PATH」**
3. 安裝完重開終端機

---

## 3. 「nlm 不是內部或外部命令」

**原因**：Python 套件沒裝好。

**解決方法**：
```powershell
pip install notebooklm-mcp-cli
```
### Mac
```bash
pip3 install notebooklm-mcp-cli
```

---

## 4. Git 說「Please tell me who you are」

**原因**：忘記設定使用者名稱和 Email。

**解決方法**：
```powershell
git config --global user.name "你的名字"
git config --global user.email "你的信箱@gmail.com"
```

---

## 5. 「權限不足」或「Access Denied」

### Windows
1. 在「開始」搜尋 PowerShell
2. 按右鍵「以系統管理員身分執行」
3. 再執行一次原本的指令

### Mac
在指令前面加上 `sudo`，例如：
```bash
sudo npm install -g netlify-cli
```

---

## 6. 瀏覽器沒有自動跳出登入畫面

**原因**：有時候防火牆或瀏覽器設定會擋住。

**解決方法**：
1. 手動複製終端機中出現的網址
2. 貼到瀏覽器打開
3. 完成登入後回到終端機按 Enter

---

## 還是不行？

把所有錯誤訊息複製貼上，對 AI 說：
> 「我遇到了這個錯誤：[貼上錯誤訊息]，幫我看看怎麼解決」
