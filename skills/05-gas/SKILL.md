---
name: 05-gas
description: Google Apps Script — 雲端腳本部署與自動化。
---

# 05-Google Apps Script (GAS)

Google Apps Script 是 Google 的自動化腳本工具。你可以讓 AI 幫你寫好腳本，自動寄信、處理試算表、串聯 Google 服務！

## 1. 打開 GAS 權限

用瀏覽器打開這個網址：
[https://script.google.com/home/usersettings](https://script.google.com/home/usersettings)

把「Google Apps Script API」切換成**開啟 (ON)**。

## 2. 安裝上傳工具

在終端機輸入：
```powershell
npm install -g @google/clasp
```

### Mac
```bash
npm install -g @google/clasp
```

## 3. 登入 Google

```powershell
clasp login
```
瀏覽器會打開，登入你的 Google 帳號。

## 4. 實戰：請 AI 寫一個自動寄信腳本

對你的 AI 編輯器說：
```
請幫我寫一個 Google Apps Script 腳本，
功能是「每天早上九點自動寄一封早安信給我自己」。
寫完之後，請使用 clasp push 指令幫我上傳到我的 Google 雲端。
```

AI 會自動寫好腳本並上傳。之後你打開 Google 試算表或 Apps Script 後台就能看到它。

## ✅ 完成

GAS 已設定完成！你可以讓 AI 幫你寫各種 Google 自動化腳本。
