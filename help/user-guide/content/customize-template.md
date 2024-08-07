---
title: 自訂範本
description: 瞭解如何建立GenStudio的自訂範本。
level: Intermediate
feature: Templates, Content
source-git-commit: 423956d6fdbf5b31041d44eb434f90d55a87d7c0
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---


# 自訂範本

您可以使用&#x200B;_Handlebars_&#x200B;範本語言，調整GenStudio的HTML範本。 Handlebars語法使用帶有雙大括弧的規則文字作為內容預留位置。 請參閱&#x200B;_Handlebars語言指南_&#x200B;中的[`What is Handlebars?`](https://handlebarsjs.com/guide/#what-is-handlebars)，瞭解如何準備您的範本。

## 範本結構

<!-- This is for email. In the future, maybe use tabs to provide guidance for other template types.
-->

如果您沒有可以在GenStudio中使用的HTML範本，您可以先使用HTML標籤來定義電子郵件的結構： `DOCTYPE`、`html`、`head`和`body`。 您可以包含CSS樣式來自訂電子郵件的外觀。

```html
<!DOCTYPE html>
<html>
<head>
    <title>Title</title>
    <style>
    </style>
</head>
<body>
</body>
</html>
```

>[!TIP]
>
>在接下來的幾個小節中，為電子郵件欄位新增內容預留位置、在預覽中隱藏不必要的元素，並管理靜態內容的連結。 您的範本準備就緒後，您可以[將其上傳到GenStudio](use-templates.md#upload-a-template)，並開始根據您的自訂範本產生個人化電子郵件。

## 內容預留位置

在範本的head或body中，您可以使用Handlebars語法來插入內容預留位置，以要求GenStudio將實際內容填入電子郵件中。 GenStudio會根據欄位名稱自動辨識及解譯內容預留位置。

例如，您可以使用`{{ headline }}`來指示電子郵件標題的放置位置：

```handlebars
<div>{{ headline }}</div>
```

自訂範本中允許的欄位數量上限為20個。

**可辨識的欄位名稱**：

| 欄位 | 角色 | 頻道範本 |
| -------------- | ---------------------- | -------------------- |
| `pre_header` | 前置標題 | 電子郵件 |
| `headline` | 標題 | 電子郵件<br>社交廣告 |
| `body` | 內文 | 電子郵件<br>社交廣告 |
| `cta` | 行動號召 | 電子郵件<br>社交廣告 |
| `on_image_text` | 在影像文字上 | 社交廣告 |
| `image` | 影像 | 電子郵件<br>社交廣告 |
| `brand_logo` | 所選品牌的標誌 | 社交廣告 |

>[!IMPORTANT]
>
>GenStudio會在[!DNL Create]程式期間自動提供包含`subject`欄位的電子郵件範本，因此不需要在您的電子郵件範本中加入主旨欄位。

+++範例：基本範本

以下是電子郵件HTML範本的基本範例。 標題包含用於樣式的簡單、內嵌CSS。 本文包含`pre-header`、`headline`和`image`預留位置，供GenStudio在電子郵件產生程式期間用來插入內容。

```handlebars {line-numbers="true" highlight="13"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
    </div>
</body>
</html>
```

+++

### 背景影像

為Meta設計廣告時，必須使用背景影像搭配文字和品牌標誌覆蓋圖。 為確保影像的正確縮放，中繼廣告範本需要指定`aspect ratio`。 在這種情況下，您只能提供一個影像欄位。

## 區段或群組

_區段_&#x200B;提供一種通知GenStudio屬於某個區段的欄位需要高度一致性的方法。 建立此關係可協助AI產生符合區段中創意元素的內容。 範本最多可包含三個區段。

在欄位名稱中使用您選擇的前置詞，表示此欄位屬於區段或群組。 例如，您可能想要將焦點放在出現在反白區域中的內容。 您可以選擇以共同前置詞來識別此區域的內容：

- `spotlight_headline`
- `spotlight_body`

每個區段只能有一個欄位型別。 例如，上述首碼為`spotlight`的範例群組只能有一個`spotlight_headline`欄位。

當您有多個區段（最多三個）時：

- `headline`
- `body`
- `spotlight_headline`
- `spotlight_body`
- `news_headline`
- `news_body`

GenStudio瞭解`spotlight_headline`與`spotlight_body`的關聯性比`news_body`更密切。

+++範例：具有多個區段的範本

以下是上述範例中的相同HTML範本，但包含另外兩個區段。 標題包含用於設定Pod樣式的內嵌CSS。 本文使用兩個Pod，內容預留位置使用首碼。

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
        .pod {
            background-color: #f8f8f8;
            margin: 10px;
            padding: 20px;
            border-radius: 5px;
        }
        .pod h2 {
            color: #333;
        }
        .pod p {
            color: #666;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
        <div class="pod">
            <h2>{{ pod1_headline }}</h2>
            <p>This is Pod 1 content.</p>
        </div>
        <div class="pod">
            <h2>{{ pod2_headline }}</h2>
            <p>This is Pod 2 content.</p>
        </div>
    </div>
</body>
</html>
```

+++

## 範本預覽

電子郵件範本有時包含不需要在GenStudio中預覽的特殊內容。 您可以使用內建協助程式來控制此內容的可見度，這些是Handlebars範本語言中的特殊運算式，可協助您執行某些動作。

呈現範本時會設定`_genStudio.browser`值，匯出範本時會設定`genStudio.export`值。 例如，當範本用於匯出時，您可使用條件包裝函式，決定在電子郵件頂端包含特定內容：

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

另一個範例可能是為了防止在GenStudio中預覽電子郵件範本時使用追蹤程式碼。 此範例說明如何將追蹤引數新增至匯出範本中的連結，同時保持預覽連結整齊：

```handlebars
<a class="button" {{#if _genStudio.browser }}
   href="{{ link }}"{{/if}}{{#if _genStudio.export }}
   href="{{ link }}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{ cta }}</a>
```

## 靜態內容

電子郵件和中繼範本通常會連結至GenStudio外部託管的影像和CSS檔案。 當GenStudio為這些範本或衍生自這些範本的體驗產生縮圖時，如果這些外部資源沒有正確的跨原始資源共用(CORS)標題，則可能會忽略這些外部資源。

為了確保這些資源在縮圖產生程式期間可供使用，請考慮兩個選項：

1. **使用CORS標頭**：主機伺服器必須傳送回應，且生產環境的`Access-Control-Allow-Origin`標頭設為`https://experience.adobe.com`值。 此方法可讓GenStudio存取並包含資源。
1. **使用資料URL**：使用資料URL將外部資源直接內嵌到範本中。 此方法會繞過CORS限制，並確保資源在產生縮圖期間可供使用。
