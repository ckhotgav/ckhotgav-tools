---
name: 17-other-editors
description: 其他 AI 編輯器 — Claude Code、Gemini CLI、Codex CLI 設定。
---

# 17-其他AI編輯器 (選用)

如果你除了 Antigravity 和 OpenCode，還想試試其他 AI 編輯器，這個技能可以幫你設定。

---

## Claude Code

由 Anthropic 公司開發，使用 Claude 模型。

### 安裝
```powershell
npm install -g @anthropic-ai/claude-code
```

### 設定檔位置
- 全域規則：`~/.claude/CLAUDE.md`
- 設定檔：`~/.claude/settings.json`

### GitHub MCP 安裝
```powershell
claude mcp add github -- npx @anthropic-ai/claude-code-mcp-github
```

---

## OpenAI Codex CLI

由 OpenAI 開發，使用 GPT 模型。

### 安裝
```powershell
npm install -g @openai/codex
```

### 設定檔位置
- 全域規則：`~/.codex/AGENTS.md`
- 設定檔：`~/.codex/config.toml`

### GitHub MCP 安裝
```powershell
codex mcp add github -- npx @openai/codex-mcp-github
```

---

## Gemini CLI

由 Google 開發，使用 Gemini 模型。

### 安裝
```powershell
npm install -g @google/gemini-cli
```

### 設定
```powershell
gemini init
```

---

## 重要提醒

- 不同編輯器的設定檔**不相通**，每個都要各自設定
- 這個懶人包的技能以大部份適用於 OpenCode
- 如果你主要是用其他編輯器，可以參考三師爸的專屬懶人包

---

## ✅ 完成

其他 AI 編輯器已設定完成！
