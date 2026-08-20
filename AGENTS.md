# SocialRadar Content Monitor Spec 規則

- 本 repo 是 Module Spec git
- 產品為 SocialRadar
- module id 為 `no1_content_monitor`
- 本 repo 承載行為規格

## 多層配對

- Product git 承載上游決策
- Design git 不建立，profile 為 app_basic
- 本 repo 是 Spec 仲裁端
- Impl git 承載瀏覽器自動化與推播腳本
- 配對以 `decision_framework_router` 的註冊表為準

---

## 產品機制

- 產品是跨社群平台巡邏分類推播機器人
- 首個平台為 Threads
- 核心為依關鍵字巡邏、套篩選條件與內容相關性判斷、推播至 Discord

---

## Spec 分層

- `no1_data_models/`
  - 承載監控關鍵字清單
  - 套用 `spec_writer` Model 政策
- `no3_logics/`
  - 承載巡邏、篩選、判斷、推播的行為規則
  - 套用 `spec_writer` Logic 政策
- 無 `no2_screens/`
  - 本產品無 UI

---

## 原生工作規則

- 任何改動先使用 `decision_framework_router`
- 所有 Spec 改動使用 `spec_writer`
- Markdown 改動使用 `universal_writing_linter`
- Spec 變動要檢查 Impl
- 上游需求與 Product Map 目前未建
- 跨層 branch 名稱必須一致
- 配對 commit 內容必須一致

---

## 相容與漂移控制

- `AGENTS.md` 是本目錄的規則真相
- `CLAUDE.md` 只保留 Claude Code 入口
- 產品規則不得複製回相容入口
- 漂移檢查確認相容入口只含導向規則
