
# CyberSec Wiki — AI Development Guidelines

## 1. Project Overview

CyberSec Wiki 是一個以繁體中文為主的資訊安全知識庫網站。
網站目標是提供容易理解、結構清楚的資安教學內容，讓使用者能夠學習 Linux Security、Web Security 與 Cloud Security 的基本概念。
本專案使用 HTML、CSS、JavaScript 開發，並透過 GitHub Pages 部署。
AI 在新增或修改網站內容時，必須遵守本文件的規範，確保所有頁面具有一致的結構、外觀與內容品質。

## 2. Technology Rules

本專案使用：

- HTML5：網頁結構
- CSS3：網頁樣式
- JavaScript：互動功能
- GitHub Pages：靜態網站部署

開發規則：

1. 不使用需要後端伺服器的功能。
2. 不使用資料庫。
3. 優先使用原生 HTML、CSS、JavaScript。
4. 不任意加入新的框架或外部套件。
5. 所有網頁必須能在 GitHub Pages 正常運作。
6. 使用相對路徑連結網站內部資源，確保專案部署於子路徑時仍可正常使用。

## 3. Project Structure

所有檔案必須按照以下結構建立：
```text
cybersec-wiki/
├── AGENTS.md
├── README.md
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── pages/
│   ├── linux/
│   │   └── ssh-security.html
│   ├── web/
│   │   └── sql-injection.html
│   └── cloud/
│       └── iam-security.html
└── assets/
    └── images/
```


規則：

1. `index.html` 為網站首頁。
2. 所有共用 CSS 放在 `css/style.css`。
3. 所有共用 JavaScript 放在 `js/main.js`。
4. Linux 文章放在 `pages/linux/`。
5. Web Security 文章放在 `pages/web/`。
6. Cloud Security 文章放在 `pages/cloud/`。
7. 圖片存放於 `assets/images/`。
8. 不得隨意更改既有資料夾名稱。

以上為目標檔案結構，尚未建立的檔案可以在新增對應內容時建立。

## 4. Website Design Rules

### 4.1 Color Theme

使用深色科技風格。

主要顏色：

- Background：#0B1120
- Card Background：#1E293B
- Primary Color：#38BDF8
- Text Color：#F8FAFC
- Secondary Text：#94A3B8

### 4.2 Layout

所有頁面必須包含：

1. 網站名稱 CyberSec Wiki
2. 頂部導覽列
3. 主要內容區域
4. 返回首頁的連結
5. 頁尾資訊

### 4.3 Visual Consistency

1. 所有文章使用相同的 CSS。
2. 標題與內文字體大小必須一致。
3. 文章內容使用卡片式區塊呈現。
4. 網頁必須支援手機與電腦瀏覽。
5. 不任意使用新的配色。
6. 程式碼範例使用深色區塊顯示。
7. 互動按鈕必須具有明確用途。

## 5. Content Categories

網站分成三個主要分類：

### Linux Security

內容包含：
- SSH Security
- Linux Logs
- File Permissions
- User Management

### Web Security

內容包含：
- SQL Injection
- Cross-Site Scripting (XSS)
- Authentication Security
- Common Web Vulnerabilities

### Cloud Security

內容包含：
- AWS IAM Security
- Cloud Access Control
- Cloud Configuration Risks
- Cloud Security Best Practices

新增文章時，必須放入對應分類。

## 6. Article Writing Rules

所有文章以繁體中文撰寫。

英文專有名詞第一次出現時，必須附上中文說明。

每篇文章必須按照以下順序：

1. 文章標題
2. 主題介紹
3. 基本原理
4. 安全風險或常見問題
5. 防護與改善方法
6. 重點整理

可以視主題加入程式碼範例、表格及示意圖。

內容規則：

- 文字應清楚易懂。
- 避免沒有解釋的專業術語。
- 不捏造資安事件、漏洞編號或技術資訊。
- 不將示範情境描述為真實攻擊紀錄。
- 教學範例以合法授權的測試環境為前提。
- 不加入真實 API Key、密碼或敏感資料。

## 7. File Naming Rules

所有檔案名稱使用：

- 英文小寫
- 單字之間使用連字號 `-`
- 不使用空白
- 不使用中文檔名

正確範例：

- ssh-security.html
- sql-injection.html
- iam-security.html

錯誤範例：

- SSH Security.html
- SQL注入.html
- IAM_Security.html

## 8. Adding a New Article

AI 新增文章時，必須按照以下流程：

### Step 1：確認分類

判斷文章屬於 Linux、Web 或 Cloud Security。

### Step 2：建立檔案

在對應資料夾建立新的 HTML 檔案，並遵守命名規則。

### Step 3：使用統一模板

新文章必須沿用既有文章的：

- 頂部導覽列
- CSS 樣式
- 文章區塊結構
- 頁尾
- 返回首頁連結

### Step 4：撰寫內容

依照 Article Writing Rules 的六個段落產生文章。

### Step 5：更新首頁

在 `index.html` 的對應分類新增文章卡片及連結。

不得刪除其他既有文章。

### Step 6：確認連結

檢查新增文章、首頁及其他相關頁面的連結是否正確。

### Step 7：測試

確認文章可以正常開啟，且手機與桌面版面不會出現明顯錯誤。

## 9. AI Modification Rules

AI 修改既有專案時：

1. 必須先閱讀本 AGENTS.md。
2. 必須先了解目前專案的檔案結構。
3. 優先沿用已有的 CSS 與 HTML 結構。
4. 不得任意刪除原有文章。
5. 不得隨意更改網站主題與配色。
6. 修改共用 CSS 時，必須考慮其他頁面。
7. 不得新增無用途的 JavaScript。
8. 不得自行加入外部追蹤程式。
9. 若修改超出使用者要求的範圍，應先說明原因。
10. 完成修改後，應摘要新增或修改的檔案。

## 10. Quality Checklist

AI 每次新增文章或修改網站後，必須檢查：

- [ ] 檔案位置符合規範
- [ ] 檔案名稱符合命名規則
- [ ] 網頁使用統一深色主題
- [ ] 文章包含六個必要段落
- [ ] 網站導覽正常
- [ ] 首頁有對應文章連結
- [ ] CSS 與 JavaScript 路徑正確
- [ ] 手機與桌面版面正常
- [ ] 沒有破壞既有頁面
- [ ] 沒有洩漏敏感資訊

若未通過檢查，必須先修正再完成。

## 11. Reusability Goal

本專案的核心目標是建立可重複使用的網站開發規則。

未來只要使用者提出：

「請新增一篇 Linux 日誌分析教學」

或

「請新增一篇 SQL Injection 介紹」

AI 就應該能根據 AGENTS.md：

1. 判斷文章分類。
2. 建立符合規範的檔案。
3. 套用相同的網頁設計。
4. 產生統一格式的文章。
5. 更新首頁文章連結。
6. 檢查網站是否正常運作。

讓網站可以持續擴充，而不需要每次重新說明所有開發規則。
