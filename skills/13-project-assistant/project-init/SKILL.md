---
name: project-init
description: 自動專案助理 — 啟動/初始化專案。建立包含 PROJECT.md 與 AGENTS.md 在內的標準專案結構與 Git 初始化。支援關鍵字：「啟動專案」、「專案啟動」、「開啟專案」、「專案初始化」、「初始化專案」、「建立專案」。
---

# project-init — 啟動專案 / 初始化專案

當使用者說「**啟動專案**」、「**專案啟動**」、「**開啟專案**」、「**專案初始化**」、「**初始化專案**」或「**建立專案**」時，請引導執行以下流程。

---

## 步驟一：詢問專案資訊

以親切的白話中文詢問使用者以下資訊：
1. **專案名稱**：例如 `my-website` 或 `python-tools`。
2. **專案類型**：提供以下選項讓使用者選擇：
   * **1️⃣ 靜態網頁** — HTML / CSS / JavaScript 網頁專案。
   * **2️⃣ Node.js 應用** — 使用 npm 管理的 JavaScript 後端或工具專案。
   * **3️⃣ Python 工具** — 用於數據處理、自動化的 Python 專案。
   * **4️⃣ 文件／筆記專案** — 純寫文件與 Markdown 筆記的專案。
   * **5️⃣ 其他** — 使用者自設結構與語言（如 Go, Rust, Java，或自訂目錄）。若選擇此項，請詢問使用者需要的語言或目錄檔案規劃。

---

## 步驟二：建立標準目錄結構與檔案

在目前的工作區目錄下，建立專案資料夾並依類型寫入預設檔案：

### 1. 靜態網頁
* 建立資料夾：`assets/images`、`assets/css`、`assets/js`
* 建立檔案：
  * `index.html` (預設簡潔網頁骨架，使用 UTF-8)
  * `assets/css/style.css` (基本 CSS Reset 與簡潔樣式)
  * `assets/js/script.js` (空的 JS 檔案)

### 2. Node.js 應用
* 建立資料夾：`src`、`tests`
* 建立檔案：
  * `src/index.js` (進入點檔案)
  * `package.json` (使用 `npm init -y` 產生，並改寫為簡潔版)
  * `.gitignore` (忽略 `node_modules` 與 `.env`)

### 3. Python 工具
* 建立資料夾：`src`
* 建立檔案：
  * `main.py` (包含基本的 `if __name__ == '__main__':` 進入點)
  * `requirements.txt` (空白套件清單)
  * `.gitignore` (忽略 `__pycache__/`、`.venv`、`.env`)

### 4. 文件／筆記專案
* 建立資料夾：`docs`
* 建立檔案：
  * `docs/summary.md` (說明大綱)

### 5. 其他（使用者自設）
* 根據使用者輸入的語言或自定義需求（例如想要 C#、Go、Rust，或指定的檔案夾結構），由 AI 助理動態分析並建立對應的目錄結構與基本的進入點檔案（例如 `main.go` 或 `main.rs`）。
* 同樣必須產生適用的 `.gitignore`。

### 🛡️ 全方位防禦性 .gitignore 規範
不論何種專案類型（包含自設專案），建立 `.gitignore` 時，**必須自動寫入**以下防禦性屏蔽，確保隱私安全不外洩：
```gitignore
# 環境變數與機密金鑰 (絕對禁止上傳)
.env
.env.local
.env.development.local
.env.test.local
.env.production.local
*.pem
*.key
*.p12
*.pfx
secrets.json
credentials.json

# 系統與編輯器臨時檔案
.DS_Store
Thumbs.db
.vscode/
.idea/
*.suo
*.ntvs*
*.njsproj
*.sln
*.swp

# 常見依賴與編譯輸出目錄
node_modules/
/dist/
/build/
/out/
__pycache__/
*.pyc
.venv/
venv/
ENV/

# Cloudflare Wrangler
.wrangler/
wrangler.toml
wrangler.jsonc
```

---

## 步驟三：自動建立專案管理核心檔案 (相容性關鍵)

不論何種專案類型，**皆必須自動建立以下檔案**：

### 📄 1. README.md
寫入專案標題與簡單描述，並包含以下內容：
```markdown
# 專案名稱

這是一個使用 AI 助理建立的專案。

## 如何開始開發？
對 AI 助理說「開工」即可啟動開發流程！🚀
```

### 📄 2. PROJECT.md
寫入符合「自動專案助理」開工讀取規格的進度表：
```markdown
# 專案名稱 - 開發進度表

本檔案記錄此專案的開發與里程碑狀態。

## 🎯 目前開發進度
- [ ] 待處理：撰寫第一版核心功能
- [ ] 待處理：完成基礎功能測試

## 📝 開發里程碑與技術細節
* **專案初始化**：使用自動專案助理啟動專案，建立目錄結構與 Git 初始化。
```

### 📄 3. AGENTS.md — 專案協作規則
```markdown
# 專案名稱 — AI 協作規範

## 程式碼習慣
- 使用繁體中文註解與說明。
- 變數名稱與命名遵循英文規範。
- 每個代碼檔案開頭皆須簡單說明用途。

## 開發流程
1. 開工時讀取 PROJECT.md，了解前一次開發進度與里程碑。
2. 完成功能開發與測試後，更新 PROJECT.md 進度狀態。
3. 收工時自動進行 Git commit，備妥總結。
```

---

## 步驟四：初始化 Git 倉庫

1. 在專案目錄下執行 `git init`。
2. 執行 `git branch -M main` 將預設分支命名為 `main`。
3. 執行 `git add .` 將所有初始化檔案加入暫存區。
4. 執行 `git commit -m "chore: initialize project using automatic project assistant"` 進行首次提交。

---

## 步驟五：回報初始化結果

建立完成後，向使用者呈報以下訊息：
1. 本次建立的專案目錄樹狀結構。
2. 提示使用者：
   > **「🎉 專案已初始化成功！且已為您完成了首次 Git 提交。您隨時可以輸入『開工』開始開發囉！🚀」**
   > (系統已自動為您配置防禦性 `.gitignore`，安全有保障！)
