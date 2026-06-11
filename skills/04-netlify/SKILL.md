---
name: 04-netlify
description: Netlify 一鍵部署 — 靜態網頁一鍵部署上線。
---

# 04-Netlify 一鍵部署

Netlify 可以讓你做的網頁**一鍵發布到網路上**，任何人都能用手機或電腦打開來看！

## 1. 安裝 Netlify 工具

在終端機輸入：
```powershell
npm install -g netlify-cli
```

### Mac
```bash
npm install -g netlify-cli
```

## 2. 登入 Netlify

```powershell
netlify login
```
瀏覽器會打開，用你的 GitHub 帳號登入即可（或用 Email 註冊）。

## 3. 實戰：發布你的第一個網頁

對你的 AI 編輯器說：
```
請幫我寫一個精美的個人介紹網頁（包含 index.html, style.css），
主題是深色科技風。寫完之後，請直接使用 netlify deploy --prod 指令，
幫我把這個網頁發布到網路上，並把網址給我！
```

AI 會自動寫好網頁，然後透過 Netlify 上線，給你一個網址！
你可以把網址分享給任何人觀看。

## ✅ 完成

Netlify 已設定完成！以後你想做網頁，AI 可以幫你一鍵上線。
