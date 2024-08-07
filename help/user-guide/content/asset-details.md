---
title: 資產詳細資訊
description: GenStudio會使用豐富的中繼資料儲存已核准的內容，以供搜尋和效能追蹤。
feature: Attributes, Assets
source-git-commit: ba7dced9e62f797cd43a0bd8d8263828ec5c3d5e
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---


# 資產詳細資訊

GenStudio會以豐富的中繼資料儲存已核准的內容，以便探索性和效能追蹤。

每個資產（包括體驗和範本）都有關聯的&#x200B;_詳細資料_ （中繼資料），以協助識別、追蹤、使用內容效能和從中學習。

資產中繼資料型別包含[系統中繼資料](#system-metadata)和[使用者定義的中繼資料](#user-defined-metadata)。

## 系統中繼資料

上傳資產時，會自動收集部分資產中繼資料。 您無法編輯預設的系統中繼資料。

為資產儲存和擷取的預設中繼資料包括檔案名稱、維度、來源等。

### 產生的標籤

當資產核准並儲存在[!DNL Content]中時，GenStudio會使用Adobe的AI和機器學習功能，根據資產功能產生標籤，例如顏色和色調，或識別資產功能的關鍵字。 您無法編輯標籤。

### 產生的內容中繼資料

用來產生新資產或體驗的資訊會成為中繼資料，例如所使用的提示。 內容獲得核准後，您就無法編輯提示，但您可以用它作為產生新內容的起點。

## 使用者定義的中繼資料

使用者定義的中繼資料會將行銷內容新增至資產內容，讓行銷人員更能瞭解如何使用及參與資產。

當您[上傳資產](/help/user-guide/content/manage-assets.md#add-assets)時，您可以將GenStudio中存在的一組選用資產詳細資料定義為中繼資料。

### 中繼資料詳細資料

下表詳細說明您可在建立資產時定義的中繼資料（資產詳細資訊）。

| 欄位 | 說明 | 可編輯 | 必填 |
| ------------- | ----------- | -------- | -------- |
| 行銷活動名稱（專案名稱） | 透過資產擷取及儲存的預設中繼資料 | Y | N |
| 品牌名稱 | [[!DNL Brands]](/help/user-guide/guidelines/brands.md)已新增至GenStudio並發佈以供使用 | Y | N |
| 產品 | [[!DNL Products]](/help/user-guide/guidelines/products.md)已新增至GenStudio以供使用 | Y | N |
| 角色 | [[!DNL Personas]](/help/user-guide/guidelines/personas.md)已新增至GenStudio以供使用 | Y | N |
| 頻道 | 資產使用的GenStudio內容型別，例如電子郵件和中繼廣告 | Y | N |
| 時間範圍 | 其使用之資產的時間範圍，例如季度、季別、年度等。 範例： `Winter 2023` | Y | N |
| 地區 | 使用資產的區域。 範例： `North America`， `APAC`， `Italy` | Y | N |
| 語言 | 使用資產的語言。 範例： `Spanish` | Y | N |
| 關鍵字 | 用於識別資產用途的關鍵字 | Y | N |

## 檢視資產詳細資訊

**若要檢視資產詳細資訊**：

1. 在&#x200B;_[!DNL Content]_中，選取資產。

1. 在資產檢視中，檢閱右側的&#x200B;_[!UICONTROL 詳細資料]_&#x200B;區段。

   如果看不到&#x200B;_[!UICONTROL 詳細資料]_&#x200B;區段，請按一下&#x200B;**[!UICONTROL 資訊]** (i)圖示。

>[!TIP]
>
>您也可以從[!DNL Insights]檢視資產詳細資訊。 「深入分析」提供各體驗的使用狀況統計資料和效能內容。 在&#x200B;_[!DNL Insights]_中，選取&#x200B;**[!UICONTROL Assets]**區段。

<!-- ## History

Expand the _[!UICONTROL History]_ section to view a timeline of approvals and activity.

list other activity, show screenshot?
-->
