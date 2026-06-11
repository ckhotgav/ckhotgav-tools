---
name: 06-supabase
description: Supabase 資料庫 — 免費雲端資料庫串接。
---

# 06-Supabase 資料庫

Supabase 是一個免費的雲端資料庫。你的網站或 APP 可以把資料（會員名單、文章、商品等）存在裡面。

## 1. 註冊 Supabase 帳號

用瀏覽器打開 [https://supabase.com](https://supabase.com)，點「Start your project」，用 GitHub 帳號登入。

## 2. 建立一個專案

1. 登入後點「New project」
2. 取一個專案名稱（例如 `my-first-db`）
3. 設定資料庫密碼（請記下來！）
4. 選擇離你最近的區域（台灣選 Singapore 或 Tokyo）
5. 點「Create new project」

## 3. 安裝 Supabase CLI

### Windows
```powershell
winget install --id Supabase.Supabase -e
```
或用 npm 安裝：
```powershell
npm install -g supabase
```

### Mac
```bash
brew install supabase/tap/supabase
```

## 4. 取得連線資訊

在 Supabase 網站上：
1. 進入你的專案
2. 左邊選單點「Project Settings」→「Database」
3. 找到「Connection string」，複製下來

## 5. 讓 AI 幫你用

對你的 AI 編輯器說：
```
我有一個 Supabase 專案，連線資訊是 [貼上你的連線字串]，
請幫我建立一個「會員資料表」，裡面有 name、email、created_at 三個欄位。
```

## ✅ 完成

Supabase 資料庫已就緒！你的專案從此可以儲存資料了。
