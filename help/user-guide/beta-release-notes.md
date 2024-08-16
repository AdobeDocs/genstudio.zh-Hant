---
title: 高效能行銷人員Adobe GenStudioBeta發行說明
description: 瞭解效能行銷人員適用的Adobe GenStudio的最新功能和增強功能。
source-git-commit: cbae3aeb1b8282fb64f2a6405a7ad9e07a48dbbd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# 高效能行銷人員Adobe GenStudioBeta發行說明

這些附註著重於截至8月16日的一週內的重大Adobe GenStudio修正和增強功能。

## 反白顯示

功能開發是快速且持續的。 重要新功能包括：

### [!DNL Brands]

已增強[!DNL Brand]驗證面板以改善使用者體驗，包括這些變更：

* **以百分比為基礎的驗證分數**：品牌驗證現在會以百分比顯示品牌驗證分數，而非通過/失敗值。

* **已更新品牌擷取介面**：品牌擷取現在會以百分比顯示擷取流程的完成。

* **在擷取期間遞增品牌載入**：品牌指引現在以遞增方式載入使用者介面。

* **簡化複製指引結構描述**： `unique attributes`和`frequent keywords`欄位已從複製指引結構描述中移除，簡化了指引設定程式。

### [!DNL Create]

* **多節電子郵件建立**：使用者現在可以建立包含個別標題、影像、內文和CTA元素的電子郵件。

* **中繼廣告調整大小**：建立者可以調整中繼廣告外觀比例。

### [!DNL Insights]

* **受限的Insights登入帳戶**： Insights登入現在僅支援每個客戶一個帳戶。

## 增強功能和已修正的問題

此版本包含下列其他修正。

### [!DNL Insights]

* _體驗詳細資料_&#x200B;頁面摘要位置名稱現在會指定Facebook或Instagram摘要。

* 現在，當使用者從&#x200B;_資產總覽_&#x200B;檢視導覽至&#x200B;_資產詳細資訊_&#x200B;檢視時，裁切較大的影像和視訊會保持一致。

* 在使用者登入之前，屬性畫面搜尋結果計數不再顯示`0 of`。<!-- GS- 3665 -->

* 按一下&#x200B;**[!UICONTROL [!DNL Insights]]** > **[!UICONTROL 資產]**&#x200B;計數欄位不再清除搜尋和篩選設定。<!-- GS-3476 -->

## 已知問題

下列已知問題將由適用於效能行銷人員的GenStudio GA版本解決。

### 分析

* 目前未追蹤&#x200B;**[!UICONTROL 新增範本]**&#x200B;和&#x200B;**[!UICONTROL 上傳]**&#x200B;按鈕所觸發的動作。<!-- GS-3505 -->

### [!DNL Insights]

* 無法從&#x200B;_Assets_&#x200B;播放視訊。<!-- GS-3846 -->

* 使用者也必須登入Facebook才能登入兩次。 **因應措施**：登入[!DNL Insights]之前請先登出Facebook。

* 行銷活動層級的&#x200B;**支出**&#x200B;值不準確。 目前Facebook Ads Manager與資料湖之間的資料不一致。<!-- GS-3202 -->

### [!DNL Reviews and Approvals]

* 建立者可在資產核准後於發佈前變更資產。 這些變更不會通知核准者。

