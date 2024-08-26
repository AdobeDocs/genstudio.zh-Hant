---
title: 建立無障礙範本
description: 建立可觸及所有對象的範本，以便用於效能行銷人員的Adobe GenStudio。
feature: Templates, Content
source-git-commit: 26d1b9c7b392e93e87ffcd9444f391c2980d1c3c
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# 建立無障礙範本

Adobe致力於為所有受眾提供最佳體驗。 如需進一步閱讀，請參閱Adobe](https://www.adobe.com/trust/accessibility/initiatives.html)的[協助工具方案。

在適用於效能行銷人員的GenStudio中，您可以上傳資產和範本，以針對各種體驗建立內容。 遵循協助工具標準有助於您的內容觸及到最大的目標受眾。

使用下列建議，以使用最佳協助工具標準準備您的範本。

## 替代文字

為非文字內容（例如影像）提供替代文字。

```html
<img alt="Collage of ideas, books, man holding giant pencil, computer" src="card-create-assets.png">
```

![創意拼貼、書籍、拿著巨鉛筆的男人、電腦](../../assets/card-create-assets.png){width="400"}

## 連結目的（僅限連結）

建立說明連結目的和位置的清楚連結文字。

例如，使用「按一下這裡」或「閱讀更多」之類的連結文字無法清楚說明連結的用途：

```html
<a href="product-site.html">Click here</a>
```

作為最佳作法，您應該使用清楚說明連結前往位置的文字。 較佳的範例可能會使用連結來源的標題及用途：

```html
<a href="product-site.html">Explore Product Site</a>
```

## 語言

許多產品和服務都會以創意或獨特的方式使用語言。 避免使用行話、長句子和複雜片語。 使用與目標受眾相容的清晰、簡潔、易讀語言。

- 儘可能使用清楚的說明、內嵌定義或相關的範例。 翻譯獨特的白話可能很困難。

- 拼出或連結至首度縮寫或縮寫例項的定義。 縮寫可能很難翻譯。

- 儘可能使用視覺元素來補充文字或複雜的想法。
