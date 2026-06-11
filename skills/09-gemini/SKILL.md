---
name: 09-gemini
description: Gemini 免費API — Google 免費 AI API，讓你的網頁工具也有 AI 能力。
---

# 09-Gemini 免費API

Gemini 是 Google 提供的免費 AI API。設定好之後，你的網頁工具就能呼叫 Google 的 AI 能力！

## 1. 取得 API 金鑰

1. 用瀏覽器打開 [Google AI Studio](https://aistudio.google.com/apikey)
2. 用你的 Google 帳號登入
3. 點「建立 API 金鑰」(Create API Key)
4. 複製金鑰（一串英數字混合的文字）

## 2. 安裝 Gemini SDK

### Windows / Mac 都一樣
```powershell
npm install @google/generative-ai
```

## 3. 讓 AI 幫你寫一支測試程式

對你的 AI 編輯器說：
```
我取得了一組 Gemini API 金鑰：[貼上你的金鑰]
請幫我寫一個簡單的 Node.js 程式，用 Gemini API 回答「台灣有哪些好玩的地方？」
執行給我看。
```

## 安全性提醒

- API 金鑰就像你的密碼，**不要上傳到 GitHub**
- 免費方案每天有使用次數限制
- 可以把金鑰寫在 `.env` 檔案中，AI 會自動忽略它

## ✅ 完成

Gemini API 已設定完成！你的網頁工具現在有 Google AI 加持了。
