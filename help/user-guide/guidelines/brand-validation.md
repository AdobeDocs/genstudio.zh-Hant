---
title: GenStudio中的品牌驗證
description: 瞭解內建品牌驗證系統如何在GenStudio中運作。
feature: Brands Service, Guidelines
source-git-commit: d7de679ce310dcdcec4a1b5ea814b2ca8b1fc413
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---


# 品牌驗證

在GenStudio中，品牌驗證是與產生AI功能和指導方針 — [[!DNL Brands]](/help/user-guide/guidelines/brands.md)、[[!DNL Products]](/help/user-guide/guidelines/products.md)和[[!DNL Personas]](/help/user-guide/guidelines/personas.md) — 共同運作的基本元件。 這可確保所有內容符合您的品牌識別。

GenStudio會針對不同方面進行品牌驗證，包括：

* 各客戶專屬的品牌指引
* 複製不同管道平台的准則
* AI產生的內容中與性別、種族、種族、殘疾狀況和年齡相關的倫理考量

## 品牌准則檢查

可透過「畫布」中每個變體旁的&#x200B;_品牌指引檢查_&#x200B;圖示，存取每個已產生內容變體的品牌驗證資訊摘要。

_品牌准則檢查_&#x200B;會顯示您的[品牌](brands.md)的相容性百分比。 百分比的計算方式為通過驗證的[准則](overview.md)數目與測試的准則數目。

按一下圖示，檢視哪些指引符合您的品牌，哪些需要檢閱。

請參閱[改善品牌一致性](#improve-brand-alignment)。

## 品牌驗證面板

_品牌驗證面板_&#x200B;提供詳細的品牌驗證資訊，並指出每個變體片段的改進機會。

_品牌驗證面板_&#x200B;顯示下列專案的資訊：

* **電子郵件**：
   * 主旨列片段
   * 預覽文字片段
   * 頁首片段
   * 內文片段
   * CTA （呼叫動作）片段
   * 品牌語調指南
* **中繼廣告**：
   * 標題片段
   * 內文復製片段
   * CTA （呼叫動作）片段
   * 影像上文字片段

請參閱[改善品牌一致性](#improve-brand-alignment)。

### 篩選

在&#x200B;_品牌驗證面板_&#x200B;中，您可以篩選顯示的准則。 按一下面板頂端的篩選圖示以檢視：

* **失敗的准則**—_顯示失敗的准則_&#x200B;只顯示未通過品牌驗證的准則。
* **所有准則**—_顯示失敗且通過准則_&#x200B;顯示測量變體所依據的所有准則。
* **通過准則**—_顯示通過准則_&#x200B;僅顯示通過品牌驗證的准則。

<!-- The _Brand Validation panel_ has different areas of focus for each content channel:

* Email - brand voice and channel compliance
* Images - application photography restrictions and other considerations -->

## 改善品牌一致性

若要最大化產生內容的有效性並維持一致的品牌識別，請使用&#x200B;_品牌准則檢查_&#x200B;和&#x200B;_品牌驗證面板_。 您可以手動修改特定片段或[產生改良的變體](/help/user-guide/create/generate-variants.md)，以符合您的[品牌指導方針](brands.md)。

**若要改善產生的內容變體的品牌一致性**：

1. 按一下&#x200B;**[!UICONTROL [!DNL Brand]指南核取]**&#x200B;圖示以取得個別變體。

   根據您的品牌檢查時，檢視特定變體表現的摘要（通過品牌驗證的准則和需要稽核的准則）。

1. 若要取得需要改進的片段與指引的詳細資訊，請按一下&#x200B;**[!UICONTROL 檢閱]** _或_，按一下頂端功能表列中的品牌驗證圖示，以開啟&#x200B;_品牌驗證面板_。

   檢視需要您注意的所有片段和品牌指引。 面板中反白顯示的片段對應至畫布中產生變數中反白顯示的片段。

   >[!NOTE]
   >
   > _品牌驗證面板_&#x200B;中註記的&#x200B;_品牌聲音_&#x200B;指引適用於整個變體，而非個別片段。 系統會強調顯示整個內容變體，以利提出改善建議。

1. 手動修訂變體片段，以最符合您的品牌。

1. 進行必要的修訂後，請按一下[重新檢查] ****&#x200B;以驗證您的變更，確保變更更符合您的品牌識別。

   品牌驗證程式將再次執行。 如果片段/指引通過驗證，_品牌驗證面板_&#x200B;中會針對該片段顯示綠色核取記號。 修訂變體的&#x200B;_品牌指引檢查_&#x200B;圖示中的百分比也會顯示您的進度。

1. 繼續修訂片段，以確保整個變體通過品牌驗證。

   使用&#x200B;**[!UICONTROL 下一個]**&#x200B;和&#x200B;**[!UICONTROL 上一個]**&#x200B;按鈕，在&#x200B;_品牌驗證面板_&#x200B;中的准則之間導覽。

1. 在&#x200B;_品牌驗證面板_&#x200B;頂端，使用箭頭瀏覽每個變體（例如，使用箭頭從`Email 1`移至`Email 2`），並繼續修訂片段以更符合您的品牌。

   請參閱[品牌語音准則](/help/user-guide/guidelines/brands.md#brand-voice-guidelines)，以取得考慮准則的詳細資訊。
