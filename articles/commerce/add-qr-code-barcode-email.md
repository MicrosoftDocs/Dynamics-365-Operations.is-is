---
title: Bæta QR-kóða eða strikamerki við tölvupósta sem tengjast færslum eða kvittunum
description: Þetta efnisatriði útskýrir hvernig á að setja QR-kóða og strikamerki sem standa fyrir auðkenni pantana inn í tölvupósta sem tengjast færslum og kvittunum í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797504"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="3afc4-103">Bæta QR-kóða eða strikamerki við tölvupósta sem tengjast færslum eða kvittunum</span><span class="sxs-lookup"><span data-stu-id="3afc4-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3afc4-104">Þetta efnisatriði útskýrir hvernig á að setja QR-kóða og strikamerki sem standa fyrir auðkenni pantana inn í tölvupósta sem tengjast færslum og kvittunum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3afc4-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3afc4-105">Auðvelt er að hafa með QR-kóða og strikamerki í tölvupóstum sem tengjast færslum til að flýta fyrir uppflettingu pöntunar í smásöluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="3afc4-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="3afc4-106">Til að setja QR-kóða og strikamerki inn í tölvupósta skal nota HTML-merki **\<img\>** sem biður um mynd af QR-kóða og strikamerki frá myndþýðingarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="3afc4-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="3afc4-107">Microsoft býður ekki upp á þessa þjónustu.</span><span class="sxs-lookup"><span data-stu-id="3afc4-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="3afc4-108">Hins vegar eru til margar ókeypis eða ódýrar þjónustur sem geta afgreitt QR-kóða eða strikamerki sem eru mynduð sjálfkrafa samkvæmt gildi sem gefið er upp í fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="3afc4-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="3afc4-109">Bæta QR-kóða eða strikamerki við tölvupóst sem tengist færslu</span><span class="sxs-lookup"><span data-stu-id="3afc4-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="3afc4-110">Til að bæta QR-kóða eða strikamerki við færslutengdan tölvupóst sem er sendur sem hluti af rafrænum viðskiptum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3afc4-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="3afc4-111">Opnið upprunalegt HTML fyrir sniðmát færslutölvupósts og bætið við HTML-merki **\<img\>** sem vísar á QR-kóða- eða strikamerkjaþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="3afc4-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3afc4-112">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="3afc4-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="3afc4-113">Hér er skýring á fyrrgreindu dæmi:</span><span class="sxs-lookup"><span data-stu-id="3afc4-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3afc4-114">**ÞÍN\_QR\_KÓÐA\_STRIKA\_MERKJA\_ÞJÓNUSTA** stendur fyrir lén QR-kóða- eða strikamerkjaþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="3afc4-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3afc4-115">**gögn** standa fyrir færibreytuna sem QR-kóða- eða strikamerkjaþjónustan notar til að taka við efninu sem á að breyta í QR-kóða eða strikamerki.</span><span class="sxs-lookup"><span data-stu-id="3afc4-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3afc4-116">Gildinu **%salesid%** verður að vera úthlutað á þessa færibreytu.</span><span class="sxs-lookup"><span data-stu-id="3afc4-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3afc4-117">Takið eftir að í þessu dæmi er gildið einnig notað sem baktexti fyrir myndina.</span><span class="sxs-lookup"><span data-stu-id="3afc4-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3afc4-118">**param1** og **param2** standa fyrir aukalegar, valfrjálsar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="3afc4-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3afc4-119">Farið í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis** og hlaðið upp uppfærðu HTML í viðeigandi sniðmát færslutölvupósts.</span><span class="sxs-lookup"><span data-stu-id="3afc4-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="3afc4-120">Færibreytur gæti verið mismunandi á milli þjónustanna sem bjóða upp á QR-kóða og strikamerki.</span><span class="sxs-lookup"><span data-stu-id="3afc4-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3afc4-121">Því skal hafa samband við þjónustuveituna til að staðfesta færibreyturnar sem þarf að úthluta gildum til.</span><span class="sxs-lookup"><span data-stu-id="3afc4-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="3afc4-122">Bæta QR-kóða eða strikamerki við tölvupóst sem tengist kvittun</span><span class="sxs-lookup"><span data-stu-id="3afc4-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="3afc4-123">Til að setja QR-kóða eða strikamerki inn í tölvupóst kvittunar sem hægt er að senda að loknum kaupum á sölustað (POS) skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3afc4-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="3afc4-124">Opnið upprunalegt HTML fyrir sniðmát kvittunartölvupósts og bætið við HTML-merki **\<img\>** sem vísar á QR-kóða- eða strikamerkjaþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="3afc4-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3afc4-125">Hér fyrir neðan er dæmi.</span><span class="sxs-lookup"><span data-stu-id="3afc4-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="3afc4-126">Hér er skýring á fyrrgreindu dæmi:</span><span class="sxs-lookup"><span data-stu-id="3afc4-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3afc4-127">**ÞÍN\_QR\_KÓÐA\_STRIKA\_MERKJA\_ÞJÓNUSTA** stendur fyrir lén QR-kóða- eða strikamerkjaþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="3afc4-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3afc4-128">**gögn** standa fyrir færibreytuna sem QR-kóða- eða strikamerkjaþjónustan notar til að taka við efninu sem á að breyta í QR-kóða eða strikamerki.</span><span class="sxs-lookup"><span data-stu-id="3afc4-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3afc4-129">Gildinu **%receiptid%** verður að vera úthlutað á þessa færibreytu.</span><span class="sxs-lookup"><span data-stu-id="3afc4-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3afc4-130">Takið eftir að í þessu dæmi er gildið einnig notað sem baktexti fyrir myndina.</span><span class="sxs-lookup"><span data-stu-id="3afc4-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3afc4-131">**param1** og **param2** standa fyrir aukalegar, valfrjálsar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="3afc4-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3afc4-132">Farið í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis** og hlaðið upp uppfærðu HTML í tölvupóstssniðmátið sem er með tölvupóstskennið **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="3afc4-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="3afc4-133">Færibreytur gæti verið mismunandi á milli þjónustanna sem bjóða upp á QR-kóða og strikamerki.</span><span class="sxs-lookup"><span data-stu-id="3afc4-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3afc4-134">Því skal hafa samband við þjónustuveituna til að staðfesta færibreyturnar sem þarf að úthluta gildum til.</span><span class="sxs-lookup"><span data-stu-id="3afc4-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3afc4-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3afc4-135">Additional resources</span></span>

[<span data-ttu-id="3afc4-136">Senda kvittanir í tölvupósti frá Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3afc4-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="3afc4-137">Stofna sniðmát fyrir tölvupóst fyrir færslutilvik</span><span class="sxs-lookup"><span data-stu-id="3afc4-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
