---
name: 18-other-deploy
description: 其他部署平台 — Vercel、Cloudflare Pages、Railway 設定。
---

# 18-其他部署平台 (選用)

除了 Netlify，還有其他平台可以部署你的網站。

---

## Vercel

Vercel 和 Netlify 很像，也是熱門的一鍵部署平台。

### 安裝工具
```powershell
npm install -g vercel
```

### 登入
```powershell
vercel login
```

### 讓 AI 幫你部署
對 AI 說：
```
請幫我寫一個簡單的網頁，然後用 vercel deploy --prod 發布。
```

---

## Cloudflare Pages (臨時與正常部署)

Cloudflare 提供了兩種極佳的部署方案，適用於不同的開發場景：

### 方案 A：臨時部署 (Wrangler Ephemeral Deploy) — 60 分鐘免登入
適合快速預覽、AI 自動部署或不想註冊帳號的臨時測試場景。
* **前提條件**：確保未處於登入狀態（若已登入，可執行 `npx wrangler logout`）。
* **部署步驟**：
  1. 安裝 CLI 工具：`npm install -g wrangler` (建議 4.102.0 以上版本)。
  2. 在專案根目錄下執行以下指令部署靜態目錄（例如 `./dist` 或 `./assets`）：
     ```powershell
     npx wrangler deploy ./dist --temporary
     ```
  3. 執行後，Cloudflare 會自動生成一個 **臨時預覽網址** (有效時間 60 分鐘)，並提供一個 **Claim URL (認領網址)**。
  4. 如果滿意，可在 60 分鐘內點擊 Claim URL 登入並認領，將此部署永久轉移至你的個人帳戶中；若不認領，60 分鐘後該部署將被自動刪除。

### 方案 B：正常部署 (Wrangler Pages Normal Deploy) — 永久部署
適合有個人 Cloudflare 帳戶，需要長期維護專案的場景。
* **方式一：瀏覽器互動登入**
  1. 終端機執行：`npx wrangler login`，瀏覽器會自動彈出，登入你的 Cloudflare 帳戶授權。
  2. 執行 Pages 部署：
     ```powershell
     npx wrangler pages deploy ./dist --project-name=your-project-name
     ```
* **方式二：API Token 免互動登入（適合自動化/隱私環境）**
  1. 在 Cloudflare Dashboard 的「My Profile -> API Tokens」建立具有 `Cloudflare Pages -> Edit` 權限的 Token。
  2. 執行命令時帶入 Token：
     * **Windows PowerShell**:
       ```powershell
       $env:CLOUDFLARE_API_TOKEN="您的_API_TOKEN"; npx wrangler pages deploy ./dist --project-name=your-project-name
       ```
     * **macOS / Linux**:
       ```bash
       CLOUDFLARE_API_TOKEN="您的_API_TOKEN" npx wrangler pages deploy ./dist --project-name=your-project-name
       ```

---

## Railway

Railway 可以部署有後端的應用程式（不只是靜態網頁）。

### 安裝工具
```powershell
npm install -g @railway/cli
```

### 登入
```powershell
railway login
```

### 讓 AI 幫你部署
對 AI 說：
```
請幫我建立一個 Node.js 網站，然後用 railway up 部署。
```

---

## 該選哪個？

| 平台 | 適合 | 免費方案 |
|------|------|---------|
| **Netlify** | 靜態網頁、個人網站 | ✅ 夠用 |
| **Vercel** | 靜態網頁、前端框架 | ✅ 夠用 |
| **Cloudflare** | 靜態網頁、速度優先 | ✅ 夠用 |
| **Railway** | 有後端的應用程式 | 有限制 |

新手建議先從 **Netlify**（技能 04）開始就好！
