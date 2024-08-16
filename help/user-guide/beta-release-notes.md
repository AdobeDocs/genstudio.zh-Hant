---
title: 高效能行銷人員Adobe GenStudioBeta發行說明
description: 瞭解Adobe GenStudio的最新功能和增強功能。
source-git-commit: 5505e3fdc78e217dd1eb73ed5bffa5e43d4f3084
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 2%

---


# 高效能行銷人員Adobe GenStudioBeta發行說明

這些附註著重於截至8月16日的一週內的重大Adobe GenStudio修正和增強功能。

## 反白顯示

GenStudio功能開發既快速又持續。 重要新功能包括：

### 品牌

品牌驗證面板已增強，以改善使用者體驗，包括下列變更：

* _以百分比為基礎的驗證分數_：品牌驗證現在會以百分比顯示品牌驗證分數，而非通過/失敗值。

* _已更新品牌擷取介面_：品牌擷取現在會以百分比顯示擷取流程的完成。

* _在擷取期間遞增品牌載入_：品牌指引現在以遞增方式載入使用者介面。

* _簡化Copy Guideline結構描述_： `unique attributes`和`frequent keywords`欄位已從Copy Guideline結構描述中移除，以簡化指引設定程式。

### 建立

* **多節電子郵件建立**：使用者現在可以建立包含個別標題、影像、內文和CTA元素的電子郵件。

* **中繼廣告調整大小**：建立者可以調整中繼廣告外觀比例。

### Insights

* **受限的Insights登入帳戶**： Insights登入現在僅支援每個客戶一個帳戶。

## 增強功能和已修正的問題

此版本包含下列其他修正。

### Insights

* _體驗詳細資料_&#x200B;頁面摘要位置名稱現在會指定Facebook或Instagram摘要。

* 現在，當使用者從&#x200B;_資產總覽_&#x200B;檢視導覽至&#x200B;_資產詳細資訊_&#x200B;檢視時，裁切較大的影像和視訊會保持一致。

* 在使用者登入之前，屬性畫面搜尋結果計數不再顯示`0 of`。<!-- GS- 3665 -->

* 按一下&#x200B;**[!UICONTROL 分析]** > **[!UICONTROL 資產]**&#x200B;計數欄位不再清除搜尋和篩選設定。<!-- GS-3476 -->

## 已知問題

下列已知問題將由適用於效能行銷人員的GenStudio GA版本解決。

### 分析

* 目前未追蹤&#x200B;**[!UICONTROL 新增範本]**&#x200B;和&#x200B;**[!UICONTROL 上傳]**&#x200B;按鈕所觸發的動作。<!-- GS-3505 -->

### Insights

* 無法從&#x200B;_Assets_&#x200B;播放視訊。<!-- GS-3846 -->

* 使用者也必須登入Facebook才能登入兩次。 **因應措施**：登入Insights之前請先登出Facebook。

* 行銷活動層級的&#x200B;**支出**&#x200B;值不準確。 目前Facebook Ads Manager與資料湖之間的資料不一致。<!-- GS-3202 -->

### 稽核與核准

* 建立者可在資產核准後於發佈前變更資產。 這些變更不會通知核准者。

