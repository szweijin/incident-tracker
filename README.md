# 製造異常回報與追蹤系統 Manufacturing Incident Tracker

[🔗 https://szweijin.github.io/incident-tracker/](https://szweijin.github.io/incident-tracker/)

本專案是一套用於回報、追蹤與視覺化分析工廠生產異常事件的系統，整合表單輸入、事件列表與統計報表等功能，協助工廠優化異常處理流程並提升管理效率。

## 專案預覽
![Screenshot 2025-06-26 at 2 34 08 PM](https://github.com/user-attachments/assets/f6f9d125-19d6-4579-9b6e-5857f738d059)


## 專案架構

| 層級 | 技術 | 描述 |
|------|------|------|
| 前端 | Vue 3, Composition API, Chart.js | 實現異常表單、事件列表與圖表報表 |
| 後端 | Spring Boot, Java | 提供 RESTful API，負責資料處理與存取 |
| 資料庫 | SQL Server | 儲存異常事件、分類、使用者資訊等資料 |
| 其他 | Docker, Postman | 測試與部署環境、API 驗證工具 |

## 功能介紹

### 異常回報表單（Report Form）

- 動態表單驗證
- 可選擇分類、部門、日期與描述內容
- 錯誤提示與 UX 優化處理

### 事件列表（Incident List）

- 支援分頁、查詢與刪除操作
- 顯示所有異常回報紀錄
- 可根據分類或部門過濾

### 異常報表分析（Chart Report）

- 使用 Chart.js 呈現統計圖表
- 類別分布長條圖、部門事件趨勢圖
- 支援按月、季度或年度篩選

## 開發與執行方式

### 1. Clone 專案
```bash
git clone https://github.com/szweijin/incident-tracker.git
cd incident-tracker
````

### 2. 安裝前端依賴
```bash
cd frontend
npm install
npm run dev
```

### 3. 啟動後端（Spring Boot）

```bash
cd backend
./mvnw spring-boot:run
```

> 可使用 Docker Compose 啟動整合環境（未來版本）

## API 文件

使用 Postman 撰寫並測試 RESTful API：

* GET `/api/incidents`：取得事件列表
* POST `/api/incidents`：新增異常事件
* DELETE `/api/incidents/{id}`：刪除事件
* 更多 API 詳見 docs/api-spec.md


## 未來優化方向

* 登入驗證與權限管理（JWT + Spring Security）
* 匯出 PDF/Excel 報表
* 部門主管審核機制
* 系統多語系支援（i18n）


## 技術學習資源

* Vue 3 Composition API 文件
* Chart.js 圖表製作指南
* Spring Boot RESTful 開發實戰
* Docker + Postgres 開發環境佈署


## 聯絡與貢獻

歡迎任何建議或貢獻，請至 [issues](https://github.com/szweijin/incident-tracker/issues) 區提出回饋。

作者：[@szweijin](https://github.com/szweijin)
