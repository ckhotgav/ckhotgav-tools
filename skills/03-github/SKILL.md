---
name: 03-github
description: GitHub 版本控制 — 版本控制、帳號登入、避坑指南。
---

# 03-GitHub 版本控制

GitHub 是程式碼的「雲端時光機」。寫程式最怕不小心弄壞原本寫好的東西，GitHub 可以隨時還原！

## 1. 安裝 Git

### Windows
```powershell
winget install --id Git.Git -e --source winget
```
如果安裝失敗，去 [Git 官網](https://gitforwindows.org/) 手動下載安裝。

### Mac
```bash
brew install git
```

**安裝完請重啟你的 AI 編輯器！**

## 2. 安裝 GitHub CLI

### Windows
```powershell
winget install --id GitHub.cli -e --source winget
```
如果失敗，去 [GitHub CLI 官網](https://cli.github.com/) 下載。

### Mac
```bash
brew install gh
```

## 3. 登入 GitHub

在終端機輸入：
```powershell
gh auth login --web --git-protocol https
```
一直按 Enter，瀏覽器會打開，登入你的 GitHub 帳號。

## 4. 告訴電腦你是誰

```powershell
git config --global user.name "你的英文名字或暱稱"
git config --global user.email "你的信箱@gmail.com"
```

## 5. 測試一下

```powershell
gh auth status
```
看到「Logged in to github.com」就代表成功了！

## ✅ 完成

GitHub 已設定完成！你的程式碼從此有雲端時光機保護了。
