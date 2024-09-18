---
title: 連線至AEM Assets Content Hub存放庫
description: 瞭解如何將適用於效能行銷人員的GenStudio連結至Adobe Experience Manager (AEM) Content Hub存放庫，並運用現有的已核准內容。
level: Experienced
feature: Assets, Content
source-git-commit: dc438085cfe7c93b20dc7fb0d5919d2dc8b3dcde
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# 連線到[!DNL AEM Assets Content Hub]存放庫

如果您在Adobe Experience Manager (AEM)中有資產，您可以依照這些步驟操作，以便在GenStudio中為效能行銷人員存取這些資產。

>[!BEGINSHADEBOX]

**必要條件**：

下列步驟需要對Admin Console和AEM Assetsas a Cloud Service的管理存取權。

>[!ENDSHADEBOX]

## 步驟1：啟用[!DNL AEM Assets Content Hub]

請依照&#x200B;**部署Content Hub**&#x200B;自助服務程式，為您在Cloud Manager中的現有AEM Assets啟用[!DNL Content Hub]。 請參閱&#x200B;_AEM as a Cloud Service_&#x200B;檔案中的[部署 [!DNL Content Hub]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub)。

啟用[!DNL AEM Assets Content Hub]後，您在Admin Console的[!DNL AEM Assets as a Cloud Service]內有一個尾碼為`contenthub`的新執行個體。

## 步驟2：入門GenStudio使用者

在[!DNL Admin Console]中，將GenStudio使用者或使用者群組新增至[!DNL AEM Assets Content Hub]產品設定檔。 [!DNL AEM Assets Content Hub]個使用者可以檢視資產，但無法新增資產或修改現有資產。

- [內建 [!DNL Content Hub] 系統管理員](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub#onboard-content-hub-administrator)
- [內建 [!DNL Content Hub] 使用者](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub#onboard-content-hub-users)

## 步驟3：核准資產

核准要在[!DNL AEM Assets Content Hub]中使用的資產，以便在GenStudio中供效能行銷人員使用。 請參閱&#x200B;_AEM as a Cloud Service_&#x200B;檔案中的[核准Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/approve-assets)中的資產。

## 步驟4：設定資產可見度

在&#x200B;_[!DNL AEM Assets Content Hub]_組態選項中，檢閱篩選器、資產詳細資訊、搜尋和品牌推廣的每組組態選項。 請參閱_ Content Hub _檔案中的[設定AEM as a Cloud Service使用者介面](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/configure-content-hub-ui-options)。

## 步驟5：驗證連線

在適用於效能行銷人員內容的GenStudio中，_[!UICONTROL 位置]_&#x200B;清單可在右側的相簿上方取得。 如果您沒有存取權，或您的組織尚未部署和連線[!DNL AEM Assets Content Hub]存放庫，清單將不可用。
