---
name: 08-ollama
description: Ollama 本地AI — 在自己的電腦上跑 AI 模型，不用網路、不用花錢。
---

# 08-Ollama 本地AI

Ollama 讓你在自己的電腦上執行 AI 模型，完全免費、不需網路、資料不外洩！

## 1. 安裝 Ollama

### Windows
去 [Ollama 官網](https://ollama.com/download) 下載 Windows 版安裝檔，直接安裝。

### Mac
去 [Ollama 官網](https://ollama.com/download) 下載 macOS 版，或使用：
```bash
brew install ollama
```

## 2. 下載一個 AI 模型

安裝完成後，在終端機輸入：
```powershell
ollama pull llama3.2
```
這會下載一個輕量級的 AI 模型到你的電腦。（檔案約 2GB，需要等一下）

## 3. 測試看看

```powershell
ollama run llama3.2
```
輸入「你好」，如果 AI 回應你，就代表成功了！輸入 `/bye` 可以退出。

## 4. 讓網頁工具用上本地 AI

對你的 AI 編輯器說：
```
我已經安裝了 Ollama，請幫我寫一個簡單的 HTML 網頁，
讓我可以透過網頁跟 Ollama 聊天。
```

## 也可以裝其他模型

- `ollama pull gemma3` — Google 的輕量模型
- `ollama pull mistral` — 另一個好用的模型
- `ollama list` — 看你已經下載了哪些

## ✅ 完成

Ollama 本地 AI 已安裝完成！你在沒有網路的時候也能用 AI 了。
