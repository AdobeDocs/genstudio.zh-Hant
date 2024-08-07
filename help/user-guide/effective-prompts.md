---
title: 撰寫有效的提示
description: 瞭解如何為GenStudio撰寫有效的提示。
feature: Prompt, Generative AI, Brands Service, Personas Service, Products Service, Guidelines
source-git-commit: d7de679ce310dcdcec4a1b5ea814b2ca8b1fc413
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---


# 撰寫有效的提示

與創作AI溝通對於GenStudio中的有效運作至關重要。

每當有機會建立或修改資產時，GenStudio都會提供產生式AI提示。 有效提示的元件應包括描述性語言、範例，以及未透過您設定的准則提供的資訊。

最佳實務是使用[指南](/help/user-guide/guidelines/overview.md)為GenStudio提供您的品牌資訊，然後您就可以完全運用創作AI來製作符合品牌標準的內容。

## 描述性語言

您可以使用自然語言來表達您的想法以建立體驗。 您的提示會引導AI產生個人化的頻道內容以及補充您視覺效果的影像。 您提供的詳細資訊越多，產生符合您需求的影像或體驗的機會就越大。 使用清楚的描述性語言，儘可能提供詳細資訊：

- 對於&#x200B;**影像**，請使用描述氣氛、情緒、色彩、作文和樣式的文字。
- 針對&#x200B;**副本**，請使用描述對象、用途、新功能說明、範例和動作的文字。

以下是範例提示，詳述有關您的意圖、目標對象和樣式的資訊。

```bash
Write an email to motivate infrequent users of Photoshop to follow an in-app tutorial that teaches them to combine elements of two photos into a beautiful work of art. Highlight the generative AI capabilities of Photoshop and use references to natural imagery.
```

+++檢視範例結果

![三個產生的電子郵件](/help/assets/sample-email.png)

+++

## 提示條件

在GenStudio [[!DNL Create]](/help/user-guide/create/overview.md)中，您可以在提示區域使用&#x200B;**[!UICONTROL 提示條件]** （[_引數_](/help/user-guide/create/overview.md#parameters)&#x200B;和提示），透過選取來新增詳細資料，以改善AI解譯。

對於[電子郵件](/help/tutorials/create-email-experience.md)，提示條件可能包括在&#x200B;_引數_&#x200B;中新增[指南](/help/user-guide/guidelines/overview.md)、上傳要在電子郵件變體中使用的資產，以及描述性提示。 對於[中繼廣告](/help/tutorials/create-meta-ad.md)，提示條件可能包括&#x200B;_引數_&#x200B;中的品牌指引、選取或上傳現有資產、影像或資產（例如外觀比例）的相關設定以及提示。 真正的力量始於[設定GenStudio指導方針](/help/user-guide/guidelines/add-guidelines.md)。

>[!NOTE]
>
>如果在提示區域的&#x200B;_引數_&#x200B;中新增准則，您就不需要在提示中包含對這些准則的參照。 GenStudio將在內容產生中善用這些[!DNL Brands]、[!DNL Products]和[!DNL Personas]。

### 准則

GenStudio指南可協助創作AI個人化您的GenStudio資產構成。 出現提示條件時，您可以從已設定的准則中選擇[[!DNL Brand]](/help/user-guide/guidelines/brands.md)、[[!DNL Persona]](/help/user-guide/guidelines/personas.md)和[[!DNL Product]](/help/user-guide/guidelines/products.md)。

>[!TIP]
>
>您可以控制GenStudio使用您[!DNL Brand]指引的方式和時間。 請參閱[准則](/help/user-guide/guidelines/overview.md)以瞭解如何設定和管理您的品牌准則。

## 再試一次

提示是一個反複的過程。 如果結果不符合您的預期，請檢視您的提示並進行一些變更或新增更多詳細資訊。 您可以提供URL作為範例或進一步資訊的來源，以精簡提示。

```bash
Write an email to motivate infrequent users of Photoshop to follow an in-app tutorial that teaches them to combine elements of two photos into a beautiful work of art. Highlight the generative AI capabilities of Photoshop and use references to natural imagery.

Use information from https://www.adobe.com/products/photoshop.html to inspire users with the latest features.
```

或者，您也可以貼上行銷活動簡報的區段。 您甚至可以要求GenStudio避免使用某些字詞、元素或主題。

## 最佳做法

在GenStudio中製作有效提示的一些簡單最佳實務：

- 做到具體，並提供該做什麼和不該做什麼的詳細資訊。
- 使用外部參照提供內容。
- 運用GenStudio指引。
- 定期檢閱和調整指引。
- 反複和調整。
- 透過實驗瞭解。
