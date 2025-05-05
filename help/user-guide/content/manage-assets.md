---
title: 管理資產和體驗
description: 簡化並增強對品牌核准資產的管理，以便在您的數位行銷歷程中使用和重複使用。
feature: Content, Assets, Experiences
exl-id: e2ce8797-6d3b-46d4-b12f-f5f80e26c669
source-git-commit: bd3c5c9ff12c962d4123ac992fb74cd94e184172
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# 管理資產和體驗

Adobe GenStudio for Performance Marketing [!DNL Content]簡化並增強品牌核准資產的管理，以便在您的數位行銷歷程中使用和重複使用。

## Assets相簿

[!UICONTROL Assets]相簿會顯示已核准資產的詳細目錄。 表格左上方的篩選器（漏斗）圖示會開啟&#x200B;**[!UICONTROL 篩選器]**&#x200B;功能表，您可在此從許多類別中選取，以篩選資產庫中顯示的資產。 按一下搜尋（放大鏡）圖示，使用關鍵字尋找資產。

下列顯示對[!UICONTROL Assets]相簿中字詞`dog`的搜尋：

![Assets檢視（含搜尋dog](../../assets/content-assets.png)）

### Assets位置

依預設，您透過[!DNL Create]程式或上傳新增至[!DNL Content]的資產會儲存在`GenStudio assets`存放庫中。 `GenStudio assets`存放庫是GenStudio for Performance Marketing中的讀寫存放庫。 這表示您可以儲存、編輯和刪除`GenStudio assets`存放庫中的資產。

右側相簿上方的&#x200B;**[!UICONTROL 位置]**&#x200B;清單可讓您從已連線的Adobe Experience Manager (AEM) [!DNL Assets Content Hub]存放庫中進行選取。 當您選取AEM存放庫時，相簿會顯示該存放庫中的資產詳細目錄，好讓您利用這些存放庫中已核准的資產作為內容建立的輸入專案。 篩選器選項會變更，以反映[!DNL AEM Assets Content Hub]中設定的類別。

AEM存放庫為唯讀，這表示您無法將草稿、新資產或中繼資料儲存至AEM存放庫。 資產、體驗和範本的所有草稿和最終更新都會使用新的[系統中繼資料](asset-details.md#system-metadata)儲存到`GenStudio assets`存放庫。

如需將[!DNL AEM Assets Content Hub]存放庫新增到GenStudio for Performance Marketing的指引，請參閱[連線AEM存放庫](connect-aem-repo.md)。

## Assets管理

在[!UICONTROL Content]中，效能行銷人員可輕鬆儲存、擷取及管理其數位資產。 藉由運用`GenStudio assets`存放庫和AEM存放庫，使用者可確保他們的資產有良好的組織且可供各種行銷活動存取。 此多存放庫方法可讓您靈活控制各環境中的資產使用情況，確保行銷工作中僅使用已核准和最新的資產。

### 新增資產

將資產新增至[!DNL Content]時，預設會儲存在`GenStudio assets`存放庫中。 _[!UICONTROL 新增資產]_&#x200B;按鈕僅在&#x200B;_[!UICONTROL 位置]_&#x200B;是`GenStudio assets`存放庫時可用。

![位置欄位](../../assets/content-location.png){width="350" align="center"}

**若要新增一或多個資產**：

1. 在&#x200B;_[!DNL Content]_&#x200B;中，按一下&#x200B;**[!UICONTROL 新增資產]**。

1. 在&#x200B;_新增您核准的資產_&#x200B;檢視中，將一或多個檔案拖放至放置區。 您可以選擇使用&#x200B;**[!UICONTROL 瀏覽]**&#x200B;從本機檔案選取，或是從Dropbox或Microsoft OneDrive匯入檔案。

1. 在&#x200B;_新增詳細資料_&#x200B;區段中，選取&#x200B;**[!UICONTROL 促銷活動名稱]**&#x200B;或輸入新名稱。

1. 若要改善可發現性，請在&#x200B;**更多詳細資料**&#x200B;區段中新增選用的詳細資料，例如&#x200B;_品牌名稱_、_角色_、_地區_&#x200B;和&#x200B;_關鍵字_。

   您提供的詳細資料越多，就越能體驗GenStudio for Performance Marketing的強大功能。 從清單中選取一或多個詳細資訊，或輸入適用的新詳細資訊，例如關鍵字。 您新增的每個詳細資訊都會顯示在清單下方。 按一下&#x200B;**`x`**&#x200B;以移除詳細資料。

   您新增的任何詳細資料都會套用至此動作中新增的所有資產。

   檢視[中繼資料詳細資料](/help/user-guide/content/asset-details.md#system-metadata)。

1. 按一下&#x200B;**[!UICONTROL 新增資產]**。

1. 當資產上傳完成時，按一下&#x200B;**完成**。

1. 若要檢視您上傳的新資產，請按一下畫布底部的&#x200B;_可用新資產_&#x200B;通知中的&#x200B;**[!UICONTROL 重新整理]**。

<!-- 
In the future, need guidance on template upload errors. For now, the UI just says error.
-->

### 搜尋內容

篩選和搜尋介面快速且回應迅速，並提供高生產力的搜尋優先體驗。 每個[!DNL Content]檢視都提供篩選選項，以縮小搜尋範圍，找出理想的資產、體驗或範本。 針對資產和體驗，您可以選取行銷活動和特定准則，例如為特定產品製作的內容。

有以[關鍵字](asset-details.md#user-defined-metadata)和[屬性](/help/user-guide/insights/attributes.md)為基礎的篩選器，可縮小搜尋結果的範圍。 例如，您可能會想要尋找特定檔案型別或主題的資產，以協助您為行銷活動建立新的體驗。

搜尋&#x200B;_體驗_&#x200B;時，您可以使用&#x200B;**[!UICONTROL 由]**&#x200B;建立篩選器來限制清單，以僅顯示您或特定人員建立的體驗。

**若要搜尋要重複使用的內容**：

1. 在&#x200B;_[!DNL Content]_&#x200B;中，選取&#x200B;**[!UICONTROL Assets]**&#x200B;區段。

1. 從&#x200B;**[!UICONTROL 位置]**&#x200B;清單中選取資產存放庫，或確認您所檢視的資產存放庫是否正確。 `GenStudio assets`是預設存放庫。

   >[!IMPORTANT]
   >
   >_位置_&#x200B;清單只有在您[連線至AEM存放庫](connect-aem-repo.md)時才能使用。

1. 按一下&#x200B;**[!UICONTROL 搜尋]** （放大鏡）以輸入關鍵字或說明。

1. 從&#x200B;_[!UICONTROL 篩選器]_&#x200B;清單中選取類別，以縮小搜尋範圍。 例如，如果您正在尋找PNG檔案，請按一下&#x200B;**[!UICONTROL 檔案格式]**&#x200B;並選擇&#x200B;**PNG**。

   縮小搜尋範圍愈多，可用的篩選選項愈少。 按一下&#x200B;**[!UICONTROL 全部清除]**&#x200B;以移除所有篩選器。

1. 選取要完整檢視和詳細資訊清單的資產。

   按一下「**[!UICONTROL 下載]**」（向下箭頭）以在本機工作站中使用資產。
