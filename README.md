# 所安裝的插件
| 插件名稱          | 描述                                 |
|-------------------|--------------------------------------|
| indent-rainbow    | 提供縮排顏色以視覺化程式碼結構 |
| Better Comments   | 改善註解的可讀性和視覺化 |
| Todo Tree         | 在程式碼中顯示待辦事項清單 |
| vscode-icons      | 提供額外的圖示和視覺效果以增強外觀 |
| Comment Translate | 為多語言開發翻譯註解內容 |
| Bookmarks         | 在程式碼中添加書籤以便於導航和搜索 |
| Markdown Preview Enhanced | 提供強大的 Markdown 預覽功能和增強特性 |
# 步驟
## 1. **安裝所需插件**
    開啟命令提示字元 (cmd) 並輸入以下命令以安裝所需插件：

    ```sh
    code --install-extension oderwat.indent-rainbow
    code --install-extension aaron-bond.better-comments
    code --install-extension gruntfuggly.todo-tree
    code --install-extension vscode-icons-team.vscode-icons
    code --install-extension hancel.comment-translate
    code --install-extension alefragnani.bookmarks
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

    // 編輯器字型設定
    "editor.fontFamily": "Source Code Pro, monospace",

    // 縮排彩虹設定
    "indentRainbow.colors": [
        "#1E90FF",  // 道奇藍
        "#32CD32",  // 萊姆綠
        "#468254",  // 深綠色
        "#3CB371",  // 中海綠
        "#5F9EA0",  // 軍藍色
        "#66CDAA"   // 中綠寶石
    ],
    "indentRainbow.indicatorStyle": "light",

    // Better Comments 設定
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

    // Todo-Tree 設定
    "todo-tree.regex.regex": "(//|#|<!--|;|/\\*)\\s+($TAGS)\\s+",
    "todo-tree.general.tags": [
        "!",
        "?",
        ">",
        "--",
        "bug",
        "note",
        "todo",
        "*"
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
        "--": {
            "icon": "trash",
            "foreground": "#C9A9A9",
            "iconColour": "#A9A9A9",
            "strikethrough": true
        },
        "bug": {
            "icon": "bug",
            "foreground": "#FF0000",
            "iconColour": "#FF0000"
        },
        "note": {
            "icon": "note",
            "foreground": "#8A2BE2",
            "iconColour": "#8A2BE2"
        },
        "todo": {
            "icon": "check",
            "foreground": "#FFD700",
            "iconColour": "#FFD700"
        },
        "*": {
            "icon": "bookmark",
            "foreground": "#0090B0",
            "iconColour": "#0090B0"
        }
    },

    // 工作區圖示主題設定
    "workbench.iconTheme": "vscode-icons",

    // 翻譯設定
    "commentTranslate.targetLanguage": "zh-TW",

    // Bookmarks 設定
    "bookmarks.navigateThroughAllFiles": false,
    "bookmarks.saveBookmarksInProject": true

    // Markdown 預覽增強設定
    "markdown-preview-enhanced.previewTheme": "github-dark.css",

    // ...
    // }
```

# 說明
## 1.標籤意思
| 標籤   | 意思           | 顏色     |
|--------|----------------|----------|
| !      | 警告標籤       | ![#FFA500](https://via.placeholder.com/15/FFA500/000000?text=+)  |
| ?      | 問題標籤       | ![#3498DB](https://via.placeholder.com/15/3498DB/000000?text=+)  |
| >      | 目錄索引標籤   | ![#FFFFFF](https://via.placeholder.com/15/FFFFFF/000000?text=+)  |
| --     | 刪除線標籤     | ![#A9A9A9](https://via.placeholder.com/15/A9A9A9/000000?text=+)  |
| bug    | 修正錯誤標籤   | ![#FF0000](https://via.placeholder.com/15/FF0000/000000?text=+)  |
| note   | 備註標籤       | ![#8A2BE2](https://via.placeholder.com/15/8A2BE2/000000?text=+)  |
| todo   | 待辦事項標籤   | ![#FFD700](https://via.placeholder.com/15/FFD700/000000?text=+)  |
| *      | 書籤標籤       | ![#0090B0](https://via.placeholder.com/15/0090B0/000000?text=+)  |
