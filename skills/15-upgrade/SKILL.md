---
name: 15-upgrade
description: 一鍵升級工具 — 所有 CLI 工具一次升級到最新版。
---

# 15-一鍵升級工具

這個技能會幫你把所有已安裝的工具一次升級到最新版。

## 升級指令

依序執行以下升級：

### npm 全域工具升級
```powershell
npm update -g
```

### Python 套件升級
```powershell
pip install --upgrade notebooklm-mcp-cli
```

### Netlify CLI
```powershell
npm install -g netlify-cli
```

### Firebase CLI
```powershell
npm install -g firebase-tools
```

### Supabase CLI
### Windows
```powershell
winget upgrade --id Supabase.Supabase
```
### Mac
```bash
brew upgrade supabase
```

### Ollama
重新下載最新版安裝檔，或：
```powershell
ollama pull llama3.2
```

### GitHub CLI
### Windows
```powershell
winget upgrade --id GitHub.cli
```
### Mac
```bash
brew upgrade gh
```

## 升級後確認

升級完成後，可以執行技能 14（系統健康檢查）來確認所有版本都已更新。
