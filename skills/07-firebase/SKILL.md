---
name: 07-firebase
description: Firebase 資料庫 — Google 雲端資料庫串接。
---

# 07-Firebase 資料庫

Firebase 是 Google 的雲端資料庫，可以用來儲存網站的會員資料、文章內容等。

## 1. 註冊 Firebase

用瀏覽器打開 [https://firebase.google.com](https://firebase.google.com)，用你的 Google 帳號登入。

## 2. 建立專案

1. 點「建立專案」(Create a project)
2. 輸入專案名稱（例如 `my-app`）
3. Google Analytics 可以選「不啟用」
4. 等它建立完成

## 3. 安裝 Firebase CLI

### Windows
```powershell
npm install -g firebase-tools
```

### Mac
```bash
npm install -g firebase-tools
```

## 4. 登入 Firebase

```powershell
firebase login
```
瀏覽器會打開，登入你的 Google 帳號。

## 5. 讓 AI 幫你用

對你的 AI 編輯器說：
```
我有一個 Firebase 專案，請幫我初始化 Firestore 資料庫，
建立一個「products」集合，裡面可以存放商品名稱和價格。
使用 firebase init 和 firebase deploy 來完成設定。
```

## ✅ 完成

Firebase 資料庫已就緒！
