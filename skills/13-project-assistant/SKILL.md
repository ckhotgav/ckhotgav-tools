---
name: 13-project-assistant
description: 專案助理 — 安裝三個全域技能：開工、收工、啟動/初始化專案。
---

# 13-專案助理

這個技能會在你的 AI 編輯器中安裝三個**全域技能**，讓你的編輯器聽得懂「開工」「收工」「啟動專案」「初始化專案」。

## 安裝位置

- **Windows**: `%USERPROFILE%\.config\opencode\skills\`
- **Mac**: `~/.config/opencode/skills/`

## 開始安裝

對你的 AI 編輯器說以下任一指令：

### 安裝開工技能
```
請讀取 skills/13-project-assistant/startup/SKILL.md，
然後幫我安裝 startup 全域技能。
```

### 安裝收工技能
```
請讀取 skills/13-project-assistant/shutdown/SKILL.md，
然後幫我安裝 shutdown 全域技能。
```

### 安裝啟動/初始化專案技能
```
請讀取 skills/13-project-assistant/project-init/SKILL.md，
然後幫我安裝 project-init 全域技能。
```

或者一次全部安裝，對 AI 說：
```
請讀取 skills/13-project-assistant/ 資料夾中的所有 SKILL.md，
幫我把 startup、shutdown、project-init 三個全域技能都安裝好。
```

## 三個技能總覽

| 你說 | 觸發技能 | 它會做 |
|------|---------|--------|
| 「開工」 | startup | 讀取專案 → 同步 Obsidian → 回報任務目標 |
| 「收工」 | shutdown | git push → 記錄筆記 → 完整性檢查 |
| 「啟動專案」 | project-init | 分析建立專案結構 → 建立目錄 → 產生設定檔 |
| 「初始化專案」 | project-init | (同上) |

## ✅ 完成

你的 AI 編輯器現在有了專案助理！試著對它說「開工」看看。
