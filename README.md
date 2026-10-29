# SingleDemo001

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.


temp here
壽險理賠調查系統重構（前後端開發）
專案背景： 參與壽險理賠調查系統重構，承接既有 Java/XHTML 與 AS400 系統業務，涵蓋案件受理、調查作業、流程簽核、進度查詢、帳務及系統管理，整合 BPM 流程引擎支援案件簽核流轉。

負責工作與技術：

前端開發： 使用 Vue 3、TypeScript、Pinia、PrimeVue 建置 SPA，開發查詢與維護功能，串接 Swagger 產生的 API Client，並建立支援遠端搜尋、分頁及返回前頁定位的共用業務元件。
後端開發： 使用 Java 21、Spring Boot 3.5、Spring Data JPA／Hibernate、Oracle、MapStruct，依 Clean Architecture 多模組架構實作後端 API，負責流程按鈕動作（SV-058）、流程進度查詢清單與明細（SV-136／137），並整合 BPM API 取得工作項目及簽核歷程。
品質治理與問題排查： 建立 AI Agent 輔助開發及逐檔靜態稽核規範，處理型別失真、非同步請求競態、分頁排序不一致、唯讀狀態漏判，以及規格與實作落差等問題。
技術優化與成果：

優化人員姓名查詢，將逐筆查詢改為去重後批次 IN 查詢，相關查詢次數由最壞情況約 10 次降至 2 次，降低資料庫往返並改善 N+1 問題；同時消除重複 COUNT 查詢。
統一前端可編輯／唯讀狀態判斷，完善後端查詢條件驗證、空結果處理及交易邊界。
完成全專案 vue-tsc 型別檢查零錯誤、ESLint 零告警，提升程式一致性、資料查詢正確性與系統可維護性。
技術關鍵字： Vue 3、TypeScript、Pinia、PrimeVue、Java 21、Spring Boot 3.5、Spring Data JPA、Hibernate、Oracle、MapStruct、Clean Architecture、BPM Integration、SQL Optimization、AI Agent
