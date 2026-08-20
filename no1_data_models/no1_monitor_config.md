# 監控設定資料結構

## App 標準定義資料

### 監控關鍵字 MonitorKeyword

- **說明:**
  - 巡邏時逐一送入平台搜尋的關鍵字清單，依主題分組
- **檔案:**
  - `no1_data_models/keywords.json`
- **欄位:**
  - `platform`: `String` - 適用平台代碼
  - `category`: `String` - 分組名稱，值域為品牌提及、競品比較文、產業觀察文、痛點話題文
  - `keyword`: `String` - 實際送入搜尋的關鍵字文字
