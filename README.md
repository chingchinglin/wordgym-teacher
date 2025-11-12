# WordGym 單字健身坊 - 學生版

高中英文單字學習平台,自動從 Google Sheet 載入資料。

## 🚀 功能特色

- ✅ 自動從 Google Sheet 載入單字
- ✅ 主題/詞性/Level 多重篩選
- ✅ 關鍵字搜尋
- ✅ 我的最愛收藏
- ✅ 單字朗讀功能
- ✅ 字根/字首/字尾學習
- ✅ 響應式設計(支援手機/平板/桌面)

## 📋 使用方式

### 學生端
1. 開啟網頁: https://你的帳號.github.io/repo名稱
2. 自動載入最新單字
3. 使用篩選和搜尋功能學習

### 教師端
1. 在 Google Sheet 編輯單字
2. 通知學生重新整理頁面
3. 完成!

## ⚙️ 設定說明

### Google Sheet 配置

在 `index.html` 中修改以下設定:

```javascript
const GOOGLE_SHEET_CONFIG = {
  enabled: true,
  showImporter: false,
  sheets: [
    {
      name: '高中氣候單字',
      sheetId: '你的SHEET_ID',  // 👈 改成你的 Sheet ID
      gid: '你的GID',            // 👈 改成你的工作表 GID
      theme: 'highschool_climate'
    }
  ]
};
```

### 如何找到 Sheet ID 和 GID?

**Sheet ID:**
```
https://docs.google.com/spreadsheets/d/1cGcjubwXM6BA7ynUW7sqLveTzD_vgdM_ETKS4sjqfIE/edit
                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
                                       這就是 Sheet ID
```

**GID:**
```
https://docs.google.com/spreadsheets/d/.../edit#gid=409060486
                                                    ^^^^^^^^^
                                                    這就是 GID
```

### Google Sheet 權限設定

1. 開啟 Google Sheet
2. 點「共用」按鈕
3. 設為「知道連結的人都可檢視」
4. 完成!

## 📊 資料格式

Google Sheet 需包含以下欄位:

| 欄位 | 說明 |
|------|------|
| level | 單字等級 (1-6) |
| CEFR | CEFR 等級 |
| 主題 | 主題標籤 (如: 氣候) |
| english_word | 英文單字 |
| KK音標 | 音標 |
| 中譯 | 中文翻譯 |
| 例句 | 例句 |
| 翻譯 | 例句翻譯 |
| 詞性 | 詞性 |
| 字首 | 字首 (選填) |
| 字根 | 字根 (選填) |
| 字尾 | 字尾 (選填) |

## 🔧 技術規格

- **前端框架:** React 18
- **樣式:** TailwindCSS
- **資料來源:** Google Sheets CSV Export
- **儲存:** localStorage
- **部署:** GitHub Pages / Netlify / Vercel

## 📝 版本資訊

**目前版本:** v5.2

**更新記錄:**
- v5.2: 版面優化,3欄佈局
- v5.1: UI 優化,移除不需要的按鈕
- v5.0: 初始學生版,自動載入功能

## 🆘 常見問題

### Q: 載入失敗怎麼辦?
A: 檢查 Google Sheet 是否設為「可檢視」

### Q: 資料沒更新?
A: 按 Ctrl+F5 強制重新整理

### Q: 如何新增其他主題?
A: 在 `GOOGLE_SHEET_CONFIG` 的 `sheets` 陣列中加入新項目

## 📞 技術支援

如有問題,請查看專案中的詳細文件:
- `快速開始.md` - 5分鐘上線指南
- `使用說明.md` - 完整使用說明
- `設定範例.md` - 進階設定範例

## 📜 授權

本專案供教育用途使用。

---

**開發:** 均一教育平台
**版本:** v5.2
**最後更新:** 2024-11-12
