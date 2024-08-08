---
title: 開始使用GenStudio
description: 瞭解如何設定GenStudio以產生新的品牌一致行銷內容。
level: Beginner
feature: Prompt, Brands Service, Personas Service, Products Service, Generative AI, Guidelines
source-git-commit: c8fa0cf1633a5ca0ab94d9a0f33d9b7e7d6d61ed
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 1%

---


# 開始使用GenStudio

GenStudio是建立、評估及管理行銷體驗的綜合平台，可反映並遵循您的品牌識別。

利害關係人對其許多功能的存取權由指派的使用者角色控制。 您指派的使用者角色會決定您可以在GenStudio中執行的工作。 GenStudio管理員會設定您的許可權，這些許可權會在您的歡迎電子郵件中定義。

如果您是創作AI型工具的新手，或只是想瞭解GenStudio的核心原則，請參閱[GenStudio概念](concepts.md)和[撰寫有效提示](effective-prompts.md)。

## GenStudio使用者角色

建立和部署現代行銷活動需要具有不同責任和技能的利害關係人之間的合作。

三種GenStudio使用者角色型別可支援這種組織角色的多樣性。 許可權會針對每個使用者型別量身打造，並支援行銷組織中每個使用者的職責。

**三種使用者角色型別為**：

* **建立者**&#x200B;使用GenStudio的創作AI功能來建立行銷活動資產、要求內容檢閱和核准，以及發佈此內容的已核准草稿。 當資產的建立者將資產儲存至「內容」後，所有GensStudio使用者都可以存取及使用資產。

* **共同作業人員**&#x200B;是GenStudio使用者最廣泛的範圍。 共同作業人員可以檢視及核准GenStudio內容，並且是工作流程中不可或缺的部分，可確保您產生的內容符合組織的需求和標準。

* **系統管理員**&#x200B;在GenStudio中擁有最廣泛的許可權集。 系統管理員可以從Genstudio新增和刪除使用者和內容。 管理員會執行重要的上線任務，為行銷活動資產建立和部署建立根本的護欄。 管理員可透過上傳品牌和組織特定資訊（例如[品牌指引](/help/user-guide/guidelines/overview.md)）來實作這些護欄。

>[!NOTE]
>在將任何使用者布建到這些Adobe之前，管理員必須在Admin Console中指定為超級使用者，以執行一次性設定工作。 此超級使用者角色僅在Adobe Admin Console的上下文中運作。 它在GenStudio平台介面中沒有任何角色。 GenStudio角色指派中沒有超級使用者的概念。

### 建立者

**建立者**&#x200B;擁有建立GenStudio [!DNL Brands]、[!DNL Campaigns]和[!DNL Content]資產所需的核心許可權。 他們也可以編輯和刪除已建立的資產。 GenStudio支援快速建立數百個內容。 這些使用者可以產生內容片段或完整體驗，以協調核准內容的分散片段，以滿足特定行銷活動的需求。

建立者可透過&#x200B;_提示_&#x200B;與GenStudio的創作AI技術互動。 GenStudio在畫布中的提示區域提供工具，可在特定行銷活動指引的內容中放置提示。 因此，產生內容的品質和成功部分取決於貴組織上傳的品牌指引品質和提示的特定性。

請參閱[撰寫有效的提示](effective-prompts.md)。

下表顯示預設的GenStudio建立者許可權：

| 功能 | 建立 | 更新 | 刪除 | 檢視 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 否 | 否 | 否 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 僅可設定廣告聯結器 |    |     | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 是 | 是 | 是 | 是 |

### 共同作業人員

**共同作業人員**&#x200B;可以在GenStudio中檢視資產，但無法建立、編輯或刪除這些資產。 共同作業人員包括對GenStudio內容成功進行稽核和核准程式至關重要的利害關係人，但他們不需要建立或直接編輯內容。 潛在共同作業人員的範例包括法律專家與創作者的經理。 GenStudio共同作業人員可能有權在其他Creative Cloud產品中建立和檢視資產。

下表顯示預設的GenStudio Collaborator許可權：

| 功能 | 建立 | 更新 | 刪除 | 檢視 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 是 | 是 | 是 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 否 | 否 | 否 | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 否 | 否 | 否 | 是 |

### 管理員

**管理員**&#x200B;會建立使用者，並將使用者指派給任何GenStudio支援的角色。 他們可以視需要指派新許可權給個別建立者或共同作業人員。 他們最關鍵的工作是完成初始入門任務，讓您的組織準備部署GenStudio。

下表顯示預設的GenStudio系統管理員許可權：

| 功能 | 建立 | 更新 | 刪除 | 檢視 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 是 | 是 | 是 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 是 | 是 | 是 | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 是 | 是 | 是 | 是 |


## 準備GenStudio以產生內容

系統管理員準備組織的GenStudio環境，讓建立者和共同作業人員建立行銷活動資產。 這些初步設定工作包括：

1. [為[!DNL Brands]、[!DNL Products]和[!DNL Personas]新增准則](./guidelines/overview.md)。 設定組織品牌識別的重要建置組塊，是GenStudio建立者和共同作業人員工作的必要先決條件。 您可以上傳品牌指引檔案或手動輸入品牌資訊。
   * **準備您的指引檔案**。 品牌指引的描述性和全面性越強，GenStudio的輸出效果就越好。 加入您認為對品牌而言不可或缺的簡短功能範例，並新增要從GenStudio內容建立中排除的行為說明。 GenStudio會從這些上傳的檔案中擷取資訊，並開始建立您的品牌。 品牌聲音、管道和影像指引等資訊會填入，因為GenStudio會從您上傳的檔案中組合每個指引。
   * **視需要編輯或完成品牌指引欄位**。 完整的品牌指引是GenStudio瞭解貴組織品牌的基礎。 GenStudio從品牌指引檔案中擷取所需的資訊後，系統會提示您手動編輯或完成擷取資訊的欄位。 新增[!DNL Product]，指定內容建立的個別產品焦點區域。 [!DNL Personas]指引可協助針對已定義的客戶區段量身打造內容建立。

   雖然設定組織的品牌指引可能是一次性動作，但您可能需要根據組織的波動、成長和不斷變化的市場環境修訂和增強這些指引。

1. **[上傳範本](./content/use-templates.md)**。 範本提供捷徑並加速內容建立。 範本包含核准的功能（例如頁首和頁尾），並建立內容建立的護欄。 管理員通常會上傳和管理組織的範本。 建立者使用範本，在組織品牌的既定界限內快速啟動內容建立流程。

1. **[上傳已核准的資產](./content/manage-assets.md)**。 GenStudio [!DNL Content]中已核准的資產可供所有GenStudio建立者使用。 您可以用建立者可用來建立新體驗或資產的資產來植入[!DNL Content]。

1. **[連線至中繼(Facebook)帳戶](./insights/connect-channel.md)**。 您必須設定GenStudio與貴組織社交帳戶之間的連線，以接收來自有效行銷活動、資產和體驗的資料。 GenStudio [Insights](./insights/overview.md)提供可分析管道衍生資料的工具。
