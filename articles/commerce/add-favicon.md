---
title: Bæta við táknmynd
description: Þetta efni útskýrir hvernig á að bæta við táknmynd á vefsíðuna.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696992"
---
# <a name="add-a-favicon"></a><span data-ttu-id="5d7c9-103">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="5d7c9-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5d7c9-104">Þetta efni útskýrir hvernig á að bæta við táknmynd á vefsíðuna.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="5d7c9-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5d7c9-105">Overview</span></span>

<span data-ttu-id="5d7c9-106">Táknmynd er lítil myndaskrá sem er sýnd á flipa vafra, á heimilisfangsstikunni, í vafraferlinum og meðal annars í bókamerkjum eða uppáhaldi.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="5d7c9-107">Við mælum með að þú bætir táknmynd við vefinn þinn vegna þess að það táknar og styrkir vörumerkið þitt og hjálpar til við að greina vefsíðuna frá öðrum síðum sem viðskiptavinir þínir heimsækja.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="5d7c9-108">Þó að þú getir bætt við mörgum táknmyndum af ýmsum stærðum og skráartegundum á vefsíðuna, sýnir þetta efni hvernig á að bæta einni táknmynd við.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="5d7c9-109">Hins vegar er sama ferli og staðsetning notuð til að bæta fleiri táknmyndum við.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="5d7c9-110">Hladdu upp táknmynd í eignasafn vefsvæðisins</span><span class="sxs-lookup"><span data-stu-id="5d7c9-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="5d7c9-111">Til að hlaða upp táknmynd í eignasafn vefsvæðisins skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="5d7c9-112">Farðu í **Eignir \> Hlaða upp \> Hlaða upp eignum**.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="5d7c9-113">Finndu og veldu táknmyndina í skráarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="5d7c9-114">Sláðu inn titil og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="5d7c9-115">Afritaðu opinberu vefslóð hugbúnaðarins í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="5d7c9-116">Ef þú velur ekki valkostinn **Birta eignir eftir upphleðslu** verður þú að fara til baka á síðuna **Eignir** og birta táknmyndina handvirkt síðar.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="5d7c9-117">Búðu til HTML fyrir táknmyndina</span><span class="sxs-lookup"><span data-stu-id="5d7c9-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="5d7c9-118">Notaðu eftirfarandi HTML bút til að búa til HTML fyrir táknmyndina.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="5d7c9-119">Fyrir **href**-eigindið skaltu skipta út **"Public\_URL\_for\_your\_favicon"** fyrir opinberu slóðina sem þú afritaðir áður.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="5d7c9-120">Bættu við HTML fyrir táknmyndina við \<höfuð\>-hluta af vefsíðunum</span><span class="sxs-lookup"><span data-stu-id="5d7c9-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="5d7c9-121">Til að bæta táknmyndinni við vefsvæðið notarðu sömu aðferð og er notuð til að bæta hvers konar HTML eða handriti við **\<höfuð\>**-hlutann af vefsíðunum.</span><span class="sxs-lookup"><span data-stu-id="5d7c9-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d7c9-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5d7c9-122">Additional resources</span></span>

[<span data-ttu-id="5d7c9-123">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="5d7c9-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5d7c9-124">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="5d7c9-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5d7c9-125">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="5d7c9-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5d7c9-126">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="5d7c9-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5d7c9-127">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="5d7c9-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5d7c9-128">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="5d7c9-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

