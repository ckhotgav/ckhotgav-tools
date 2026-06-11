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

## Cloudflare Pages

Cloudflare 提供免費的網頁託管，速度很快。

### 安裝工具
```powershell
npm install -g wrangler
```

### 登入
```powershell
wrangler login
```

### 讓 AI 幫你部署
對 AI 說：
```
請幫我寫一個網頁，然後用 wrangler pages deploy 發布到 Cloudflare Pages。
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
