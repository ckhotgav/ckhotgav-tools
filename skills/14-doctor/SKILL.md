---
name: 14-doctor
description: 系統健康檢查 — 列出所有已裝工具的版本與狀態。
---

# 14-系統健康檢查

這個技能會幫你檢查電腦上所有工具是否都正常運作。

## 檢查清單

請依序執行以下檢查：

### Node.js
```powershell
node --version
```

### npm
```powershell
npm --version
```

### Python
```powershell
python --version
```

### Git
```powershell
git --version
```

### GitHub CLI
```powershell
gh --version
```

### Netlify CLI (如果有裝)
```powershell
netlify --version
```

### Firebase CLI (如果有裝)
```powershell
firebase --version
```

### Supabase CLI (如果有裝)
```powershell
supabase --version
```

### Ollama (如果有裝)
```powershell
ollama --version
```

### NotebookLM (如果有裝)
```powershell
nlm --version
```

## 結果回報

AI 會幫你整理一份檢查報告：

```
📋 系統健康檢查報告
─────────────────────
✅ Node.js     v18.17.0
✅ npm         9.6.7
✅ Python      3.11.5
✅ Git         2.41.0
✅ GitHub CLI  2.32.0
✅ Netlify     17.0.0
⚠️ Firebase    未安裝
⚠️ Supabase   未安裝
✅ Ollama      0.1.32
✅ NotebookLM  2.1.0
─────────────────────
10 項檢查：7 項正常，3 項未安裝
```

## 遇到問題？

如果有工具顯示錯誤或找不到，安裝技能 16（疑難排解）來解決。
