---
name: 11-obsidian
description: Obsidian 知識管理系統 — 連接你的 Obsidian 筆記本到 AI 編輯器。
---

# 11-Obsidian 知識管理系統

Obsidian 是一個超好用的本地筆記軟體。裝好之後，AI 可以直接讀寫你的筆記！

> 💡 這個技能教你「怎麼裝」。裝好之後，技能 12 會教你「怎麼用」。

## 1. 下載安裝 Obsidian

去 [Obsidian 官網](https://obsidian.md/) 下載安裝檔並安裝。

## 2. 建立或找到你的筆記庫 (Vault)

打開 Obsidian，你會看到：
- **建立新筆記庫**：取個名稱（例如 `我的知識庫`），選一個資料夾位置
- **開啟既有筆記庫**：如果你已經在用 Obsidian，直接選你原來的資料夾

### 不知道 Vault 在哪？讓電腦自動找

Windows 在終端機輸入這行：
```powershell
Get-ChildItem -Path "$env:USERPROFILE" -Directory -Filter ".obsidian" -Recurse -ErrorAction SilentlyContinue | Select-Object FullName
```

Mac 在終端機輸入這行：
```bash
find ~ -name ".obsidian" -type d 2>/dev/null
```

找到的資料夾路徑，它的**上一層**就是你的筆記庫位置。

### 筆記庫路徑範例

| 系統 | 路徑範例 |
|------|---------|
| Windows | `C:\Users\你的名字\我的知識庫` |
| Mac | `/Users/你的名字/我的知識庫` |
| Google Drive (Windows) | `G:\我的雲端硬碟\知識庫` |
| OneDrive (Windows) | `C:\Users\你的名字\OneDrive\文件\知識庫` |

### 如果你用 Google Drive 或 OneDrive 同步

- 兩台電腦登入同一個雲端帳號，Obsidian 筆記就會自動同步
- **同步前請確認**：檔案總管中的雲端圖示顯示「已完成同步」（綠色勾勾）
- **很重要**：不要同時從兩台電腦編輯同一篇筆記，會產生衝突檔
- 如果同步怪怪的，先等雲端圖示變綠再打開 Obsidian

## 3. 安裝 MCPVault 外掛

MCPVault 是讓 AI 能夠讀寫你 Obsidian 筆記的橋樑。

### 方法一：讓 AI 自動設定（最簡單）

對你的 AI 編輯器說：
```
我已經安裝了 Obsidian，筆記庫在 [貼上你的筆記庫路徑]。
請幫我安裝 MCPVault，讓我可以透過 AI 讀寫 Obsidian 筆記。
```

### 方法二：手動安裝（如果方法一失敗）

在終端機輸入：
```powershell
npm install -g @bitbonsai/mcpvault
```

然後手動編輯 MCP 設定檔：

**如果你用 OpenCode**
打開 `C:\Users\你的名字\.config\opencode\opencode.json`，把以下內容加進去：
```json
{
  "mcp": {
    "obsidian": {
      "type": "local",
      "command": ["npx", "-y", "@bitbonsai/mcpvault"],
      "args": ["C:\\Users\\你的名字\\我的知識庫"],
      "enabled": true
    }
  }
}
```

**如果你用 Antigravity**
打開 `C:\Users\你的名字\.gemini\antigravity\mcp_config.json`，用同樣的格式加入。

**如果你用其他編輯器（Claude Code / Codex CLI）**
告訴 AI 你的編輯器名稱，它會告訴你設定檔在哪裡。

> ⚠️ Windows 注意：路徑中的反斜線要寫成雙反斜線 `\\`

## 4. 重新啟動

設定完成後，**關掉 AI 編輯器重新打開**，讓設定生效。

## 5. 跑一次驗證檢查

請 AI 幫你跑檢查，或手動對 AI 說以下每一項：

| # | 檢查項目 | 對 AI 說 |
|---|---------|---------|
| 1 | Obsidian 有裝好 | 「檢查 Obsidian 是否已安裝」 |
| 2 | MCPVault 有裝好 | 「檢查 MCPVault 是否已安裝」 |
| 3 | MCP 設定正確 | 「幫我檢查 Obsidian 的 MCP 設定是否正確」 |
| 4 | AI 可以讀 Obsidian | 「幫我列出 Obsidian 筆記庫中有哪些檔案」 |
| 5 | AI 可以寫 Obsidian | 「幫我在 Obsidian 建立一個測試筆記，標題是「測試」，內容是「test」」 |
| 6 | 三層資料夾存在 | 如果你已經裝過技能 12，檢查收件匣/專案/知識庫 三個資料夾是否存在 |

所有項目都通過後，就可以往下走了！

## 常見問題

| 問題 | 解法 |
|------|------|
| `npm install -g` 出現權限錯誤 | Windows 請以系統管理員身分執行 PowerShell |
| 找不到 vault 路徑 | 用上面「讓電腦自動找」的指令搜尋 |
| 設定檔 JSON 格式錯誤 | 最後一項結尾不能有逗號，路徑前後要有雙引號 |
| Google Drive 還沒同步完 | 等檔案總管圖示顯示綠色勾勾再開始 |
| AI 說「沒有權限讀取 Obsidian」 | 檢查 MCP 設定檔中的路徑是否正確 |
| Obsidian 出現「衝突檔」 | 表示你同時從兩台電腦編輯，請手動合併內容 |

## ✅ 完成

Obsidian 已連接到你的 AI 編輯器！接下來可以安裝技能 12，學會怎麼整理你的知識。
