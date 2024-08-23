# 所安裝的插件
## 1. **設定檔安裝的插件**
| 插件名稱          | 描述 |
|-|-|
| indent-rainbow | 提供縮排顏色以視覺化程式碼結構 |
| Better Comments | 改善註解的可讀性和視覺化 |
| Todo Tree | 在程式碼中顯示待辦事項清單 |
| vscode-icons | 提供額外的圖示和視覺效果以增強外觀 |
| Comment Translate | 為多語言開發翻譯註解內容 |
| Bookmarks | 在程式碼中添加書籤以便於導航和搜索 |
| Markdown Preview Enhanced | 提供強大的 Markdown 預覽功能和增強特性 |
## 2. **推薦安裝的插件**
| 插件名稱 | 描述 |
|-|-|
| Chinese (Traditional) Language Pack for Visual Studio Code | VS Code 的中文 (繁體) 語言套件 |
| Code Spell Checker | 檢查程式碼中的拼寫錯誤 |
| CSS Peek | 在 CSS 文件中查看和導航到相關的樣式定義 |
| Excel Viewer | 在 VS Code 中查看和編輯 Excel 文件 |
| Git Graph | 以圖形方式顯示 Git 存儲庫的分支和提交記錄 |
| Git History | 查看和比較 Git 存儲庫的提交歷史記錄 |
| GitHub Actions | 在 VS Code 中管理和執行 GitHub Actions 工作流程 |
| GitHub Pull Requests | 在 VS Code 中查看和管理 GitHub 上的 Pull 請求 |
| GitLens — Git supercharged | 在編輯器中輕鬆查看 Git 存儲庫的文件和代碼歷史 |
| Live Server | 在本地主機上實時預覽和調試網頁 |
| Markdown All in One | 提供 Markdown 編輯的全面功能和快捷鍵 |
| Path Intellisense | 自動完成文件路徑和模塊名稱 |
| Remote - SSH | 通過 SSH 遠程連接到遠程主機進行開發 |
| Remote - SSH: Editing Configuration Files | 在遠程主機上編輯配置文件 |
| Remote - Tunnels | 在遠程主機上設置和管理 SSH 隧道 |
| Remote Development | 通過容器、遠程主機或 WSL 進行開發 |
| Remote Explorer | 瀏覽和管理遠程文件和資源 |
| SonarLint | 在編輯器中檢查代碼質量和漏洞 |
| Test Adapter Converter | 將不同測試框架的測試適配器轉換為 VS Code 測試適配器 |
| Test Explorer UI | 在 VS Code 中運行和管理測試 |
| Vscode Google Translate | 使用 Google 翻譯在編輯器中翻譯文本 |
| vscode-icons | 提供額外的圖示和視覺效果以增強外觀 |
| WSL | 在 Windows Subsystem for Linux 中進行開發 |
# 步驟
## 1. **安裝所需插件**
### 1. **設定檔安裝插件**
開啟命令提示字元 (cmd) 並輸入以下命令以安裝所需插件：
```sh
code --install-extension oderwat.indent-rainbow
code --install-extension aaron-bond.better-comments
code --install-extension gruntfuggly.todo-tree
code --install-extension vscode-icons-team.vscode-icons
code --install-extension hancel.comment-translate
code --install-extension alefragnani.bookmarks
```
### 2. **推薦安裝的插件**
```sh
code --install-extension ms-ceintl.vscode-language-pack-zh-hant
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension pranaygp.vscode-css-peek
code --install-extension GrapeCity.gc-excelviewer
code --install-extension mhutchie.git-graph
code --install-extension donjayamanne.githistory
code --install-extension github.vscode-pull-request-github
code --install-extension eamodio.gitlens
code --install-extension ritwickdey.liveserver
code --install-extension yzhang.markdown-all-in-one
code --install-extension christian-kohler.path-intellisense
code --install-extension ms-vscode-remote.remote-ssh
code --install-extension ms-vscode-remote.remote-ssh-edit
code --install-extension ms-vscode-remote.remote-wsl
code --install-extension ms-vscode-remote.vscode-remote-extensionpack
code --install-extension ms-vscode-remote.vscode-remote-explorer
code --install-extension SonarSource.sonarlint-vscode
code --install-extension hbenl.vscode-test-adapter-converter
code --install-extension hbenl.vscode-test-explorer
code --install-extension felipecaputo.git-project-manager
code --install-extension yuichinukiyama.vscode-google-translate
code --install-extension ms-vscode-remote.remote-wsl
```
## 2. **開啟命令選單**
按下鍵盤中的 `Ctrl + Shift + P`
## 3. **開啟全域設定檔**
輸入指令 `Preferences: Open Settings (JSON)` 並按下 `Enter`
## 4. **新增設定**
`settings.json` 中的 `{...}` 內容結尾處貼下以下內容後，按下鍵盤中的 `Ctrl + Enter`
```json
// {
    // ...

    // > -----------------------------------------------------
    // NOTE VSCode 擴充套件設定
    // > -----------------------------------------------------

    // > 編輯器字型設定
    "editor.fontFamily": "Source Code Pro, monospace",

    // > indent-rainbow 設定
    "indentRainbow.colors": [
        "#1E90FF",  // 道奇藍
        "#32CD32",  // 萊姆綠
        "#468254",  // 深綠色
        "#3CB371",  // 中海綠
        "#5F9EA0",  // 軍藍色
        "#66CDAA"   // 中綠寶石
    ],
    "indentRainbow.indicatorStyle": "light",

    // > Better Comments 設定
    "better-comments.highlightPlainText": true,
    "better-comments.tags": [
        {
            "tag": " ! ",
            "color": "#FFA500",  // 黃色，用於警告標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " ? ",
            "color": "#3498DB",  // 藍色，用於問題標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " > ",
            "color": "#FFFFFF",  // 白色，用於目錄索引標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " -- ",
            "color": "#A9A9A9",  // 深灰色，用於刪除線標籤
            "strikethrough": true,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " bug ",
            "color": "#FF0000",  // 純紅色，用於修正錯誤標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " note ",
            "color": "#8A2BE2",  // 藍紫色，用於備註標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " todo ",
            "color": "#FFD700",  // 金色，用於待辦事項標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        },
        {
            "tag": " * ",
            "color": "#0090B0",  // 亮藍色，用於書籤標籤
            "strikethrough": false,
            "underline": false,
            "backgroundColor": "transparent",
            "bold": false,
            "italic": false
        }
    ],
    
    // > Todo Tree 設定
    "todo-tree.regex.regexCaseSensitive": false,
    "todo-tree.regex.regex": "(//|#|<!--|;|/\\*)\\s+($TAGS)\\s+",
    "todo-tree.general.tags": [
        "!",
        "?",
        ">",
        "*",
        "--",
        "BUG",
        "NOTE",
        "TODO"
    ],
    "todo-tree.highlights.customHighlight": {
        "!": {
            "icon": "alert",
            "foreground": "#FFA500",
            "iconColour": "#FFA500"
        },
        "?": {
            "icon": "question",
            "foreground": "#3498DB",
            "iconColour": "#3498DB"
        },
        ">": {
            "icon": "list-unordered",
            "foreground": "#FFFFFF",
            "iconColour": "#FFFFFF"
        },
        "*": {
            "icon": "bookmark",
            "foreground": "#0090B0",
            "iconColour": "#0090B0"
        },
        "--": {
            "icon": "trash",
            "foreground": "#C9A9A9",
            "iconColour": "#A9A9A9",
            "strikethrough": true
        },
        "BUG": {
            "icon": "bug",
            "foreground": "#FF0000",
            "iconColour": "#FF0000"
        },
        "NOTE": {
            "icon": "note",
            "foreground": "#8A2BE2",
            "iconColour": "#8A2BE2"
        },
        "TODO": {
            "icon": "check",
            "foreground": "#FFD700",
            "iconColour": "#FFD700"
        }
    },

    // > vscode-icons 主題設定
    "workbench.iconTheme": "vscode-icons",

    // > Comment Translate 設定
    "commentTranslate.targetLanguage": "zh-TW",
    
    // > Bookmarks 設定
    "bookmarks.navigateThroughAllFiles": false,
    "bookmarks.saveBookmarksInProject": true,

    // > Markdown Preview Enhanced 預覽增強設定
    "markdown-preview-enhanced.previewTheme": "github-dark.css",

    // ...
// }
```
# 說明
## 1.標籤說明
| 標籤 | 說明 | 顏色 |
|-|-|-|
| ! | 警告 | ![#FFA500](https://via.placeholder.com/15/FFA500/000000?text=+) |
| ? | 問題 | ![#3498DB](https://via.placeholder.com/15/3498DB/000000?text=+) |
| > | 目錄索引 | ![#FFFFFF](https://via.placeholder.com/15/FFFFFF/000000?text=+) |
| * | 書籤 | ![#0090B0](https://via.placeholder.com/15/0090B0/000000?text=+) |
| -- | 刪除線 | ![#A9A9A9](https://via.placeholder.com/15/A9A9A9/000000?text=+) |
| BUG | 修正錯誤 | ![#FF0000](https://via.placeholder.com/15/FF0000/000000?text=+) |
| NOTE | 備註 | ![#8A2BE2](https://via.placeholder.com/15/8A2BE2/000000?text=+) |
| TODO | 待辦事項 | ![#FFD700](https://via.placeholder.com/15/FFD700/000000?text=+) |
