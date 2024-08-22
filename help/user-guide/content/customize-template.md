---
title: 自訂範本
description: 瞭解如何為效能行銷人員建立自訂範本Adobe GenStudio。
level: Intermediate
feature: Templates, Content
source-git-commit: 44390d551e638fcff47cff5844fcfda4ed9f98f3
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---


# 自訂範本

使用&#x200B;_Handlebars_&#x200B;範本化語言，調整您的HTML範本以符合效能行銷人員的Adobe GenStudio。 Handlebars語法使用帶有雙大括弧的規則文字作為內容預留位置。 請參閱&#x200B;_Handlebars語言指南_&#x200B;中的[`What is Handlebars?`](https://handlebarsjs.com/guide/#what-is-handlebars)，瞭解如何準備您的範本。

如果您沒有現成的HTML範本可在GenStudio中使用以進行效能行銷人員，您可以先使用HTML標籤定義範本的結構： `DOCTYPE`、`html`、`head`和`body`。 以下是基本電子郵件範本，包含CSS樣式以自訂外觀：

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
>在接下來的幾個小節中，為電子郵件欄位新增內容預留位置、參閱範本、在預覽中隱藏不必要的元素，以及管理靜態內容的連結。 您的範本準備就緒後，您可以[將其上傳到GenStudio以進行效能行銷人員](use-templates.md#upload-a-template)，並開始根據您的自訂範本產生個人化電子郵件。

## 內容預留位置

在範本的head或body中，您可以使用Handlebars語法來插入內容預留位置，以要求GenStudio的效能行銷人員將實際內容填入範本。 適用於效能的GenStudio行銷人員會根據欄位名稱自動辨識和解譯內容預留位置。

例如，您可以使用`{{ headline }}`來指示電子郵件標題的放置位置：

```handlebars
<div>{{ headline }}</div>
```

### 可辨識的欄位名稱

自訂範本中允許的欄位數量上限為20個。

下表列出GenStudio針對效能行銷人員識別的欄位名稱，以便將其填入範本。

| 欄位 | 角色 | 頻道範本 |
| -------------- | ---------------------- | -------------------- |
| `pre_header` | 前置標題 | 電子郵件（建議） |
| `headline` | 標題 | 電子郵件（建議）<br>中繼廣告 |
| `body` | 內文 | 電子郵件（建議）<br>中繼廣告 |
| `cta` | 行動號召 | 電子郵件（建議）<br>中繼廣告 |
| `on_image_text` | 在影像文字上 | 中繼廣告（建議） |
| `image` | 影像 | 電子郵件（建議）<br>中繼廣告（建議） |
| `brand_logo` | 選取品牌<br>的標誌[欄位名稱](#brand-logo-field-name)建議使用方式。 | 電子郵件<br>中繼廣告 |

適用於效能的GenStudio行銷人員會自動填入範本中的特定欄位，因此不需要將其納入您的範本設計：

- `subject`欄位（電子郵件範本）
- `headline`、`body`和`CTA`欄位（中繼廣告範本）

>[!WARNING]
>
>針對Instagram廣告，產生的標題不會出現在最終體驗中。

#### 品牌標誌欄位名稱

下列範例示範兩種有條件地呈現品牌標誌的方法，驗證來源、提供預設或替代標誌（若品牌標誌無法使用）以及套用樣式：

_範例_：在HTML`img src`定義中

```html
<img src="{{#if brand_logo}}{{brand_logo}}{{else}}<default-image>{{/if}}" alt="img alt text" style="max-width: 88px; margin: 10px auto; display: block;"> 
```

_範例_：在Handlebars條件中

```handlebars
{{#if brand_logo}}
    <img src="{{brand_logo}}" alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
    {{else}}
    <img src="data:image/png;base64,iVBORw0KGgo..." alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
{{/if}}
```

#### 手動欄位名稱

所有其他欄位名稱會視為手動填入的欄位。 若要建立可編輯的區段，請在區段名稱兩側加上雙括弧：

```handlebars
{{customVariable}}
```

## 區段或群組

_區段_&#x200B;會通知GenStudio for Performance行銷人員此區段中的欄位需要高度一致性。 建立此關係可協助AI產生符合區段中創意元素的內容。

在欄位名稱中使用您選擇的前置詞來指示欄位是區段或群組的一部分。

例如，您可能想要將焦點放在反白區域中出現的內容：

- `spotlight_headline`
- `spotlight_body`

每個區段只能有一個欄位型別。 在上述範例中，`spotlight`首碼只能有一個`spotlight_headline`欄位。

範本最多可包含三個區段：

- `headline`
- `body`
- `spotlight_headline`
- `spotlight_body`
- `news_headline`
- `news_body`

適用於效能行銷人員的GenStudio瞭解，`spotlight_headline`與`spotlight_body`的關聯性比`news_body`更密切。

## 範本範例

+++範例：電子郵件範本包含一個區段

以下是包含一節之電子郵件的HTML範本基本範例。 標題包含用於樣式的簡單、內嵌CSS。 內文包含`pre-header`、`headline`和`image` [預留位置](#content-placeholders)，供GenStudio的效能行銷人員在電子郵件產生程式期間插入內容。

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

+++範例：具有多個區段的電子郵件範本

以下是上述範例中的相同HTML範本，但包含另外兩個區段。 標題包含用於設定群組樣式的內嵌CSS。 本文使用兩個群組，其中的[內容預留位置](#content-placeholders)使用前置詞。

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

+++範例：中繼廣告範本

以下是中繼廣告範本的基本範例。 標題包含用於樣式的內嵌CSS。 本文使用前置詞的[內容預留位置](#content-placeholders)。

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adobe</title>
    <style>
        .ad-container {
            width: 300px;
            border: 1px solid #ddd;
            padding: 16px;
            font-family: Arial, sans-serif;
        }
        .ad-image {
            width: 100%;
            height: auto;
        }
        .ad-headline {
            font-size: 18px;
            font-weight: bold;
            margin: 12px 0;
        }
        .ad-body {
            font-size: 14px;
            margin: 12px 0;
        }
        .ad-cta {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
<div class="ad-container">
    <img src="{{ image }}" alt="Ad Image" class="ad-image">
    <div class="ad-headline">"{{ headline }}"</div>
    <div class="ad-body">"{{ body }}"</div>
    <a href="(https://example.com)" class="ad-cta">"{{ CTA }}"</a>
</div>
</body>
</html>
```

+++

## 範本預覽

使用內建協助程式（Handlebars範本語言中可執行特定動作的特殊運算式）控制特殊內容的可見度。 例如，您可以將追蹤引數新增至匯出範本中的連結，同時保持預覽連結整齊。

呈現範本時會設定`_genStudio.browser`值，匯出範本時會設定`genStudio.export`值。 例如，當範本用於匯出時，您可使用條件包裝函式，決定在電子郵件頂端包含特定內容：

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

另一個範例可能是為了防止在GenStudio中預覽範本時使用追蹤程式碼。 此範例說明如何將追蹤引數新增至匯出範本中的連結，同時保持預覽連結整齊：

```handlebars
<a class="button" {{#if _genStudio.browser }}
   href="{{ link }}"{{/if}}{{#if _genStudio.export }}
   href="{{ link }}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{ cta }}</a>
```

## 靜態內容

電子郵件和中繼範本通常會連結至GenStudio外部託管的影像和CSS檔案，以供效能行銷人員使用。 當適用於效能的GenStudio行銷人員為這些範本或從中衍生的體驗產生縮圖時，如果他們沒有正確的跨原始資源共用(CORS)標頭，則可能會忽略這些外部資源。

為了確保這些資源在縮圖產生程式期間可供使用，請考慮兩個選項：

1. **使用CORS標頭**：主機伺服器必須傳送回應，且生產環境的`Access-Control-Allow-Origin`標頭設為`https://experience.adobe.com`值。 此方法可讓GenStudio的效能行銷人員存取並包含資源。
1. **使用資料URL**：使用資料URL將外部資源直接內嵌到範本中。 此方法會繞過CORS限制，並確保資源在產生縮圖期間可供使用。
