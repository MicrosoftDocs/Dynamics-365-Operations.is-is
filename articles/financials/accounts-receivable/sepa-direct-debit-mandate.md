---
title: "Setja upp sjálfgefna debet tilskipun SEPA"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="fe3d0-102">Setja upp sjálfgefna debet tilskipun SEPA</span><span class="sxs-lookup"><span data-stu-id="fe3d0-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="fe3d0-103">SEPA-beingreiðsla (Single Euro Payment Area )  gerir kleift að safna fjármagn frá bankareikningi viðskiptavinar hjá lánardrottni svo lengi sem undirrituð umboðið hefur verið veitt af viðskiptavini í lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="fe3d0-104">Viðskiptavinurinn skrifar umboð sem heimilar lánardrottins til að innheimta greiðslu og veitir banka viðskiptavinar fyrirmæli um að greiða innheimtuna.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="fe3d0-105">Þessu efnissviði er raðað þannig að það sýnir ferli fyrir uppsetningu SEPA-umboð fyrir beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe3d0-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="fe3d0-106">Prerequisites</span></span>
<span data-ttu-id="fe3d0-107">Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="fe3d0-108">Tegund</span><span class="sxs-lookup"><span data-stu-id="fe3d0-108">Category</span></span>       | <span data-ttu-id="fe3d0-109">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="fe3d0-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3d0-110">Land/svæði</span><span class="sxs-lookup"><span data-stu-id="fe3d0-110">Country/region</span></span> | <span data-ttu-id="fe3d0-111">Aðalaðsetur fyrir lögaðilann verður að vera í eftirfarandi löndum/svæðum:</span><span class="sxs-lookup"><span data-stu-id="fe3d0-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="fe3d0-112">Setja upp númeraröð fyrir umboð fyrir beint debet Hvert umboð fyrir beint debet verður að hafa einkvæmt númer.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="fe3d0-113">Nota skal síðuna **númeraraðir** til að stofna númeraröð fyrir umboð fyrir beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="fe3d0-114">Þú munt nota þetta kenni til að úthluta númeraröð á umboð fyrir beingreiðslu í á    **færibreytur viðskiptakrafna** síða.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="fe3d0-115">Setja upp færibreytur viðskiptavina fyrir umboð fyrir beint debet Nota skal síðuna **Færibreytur viðskiptakrafna** til að setja upp færibreytur fyrir umboð fyrir beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="fe3d0-116">Til að setja upp færibreytur á **beingreiðsla** flipa skal breyta sjálfgefnum færibreytum eins og krafist er.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="fe3d0-117">Síðan skal á **Númeraraðir** flipanum uppfæra **Kenni umboðs fyrir beint debet** svæði með númeraröð sem var sett upp áður.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="fe3d0-118">Til að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu verður þú að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="fe3d0-119">Nota þennan greiðsluhátt til að spyrjast fyrir um reikninga til að mynda beingreiðslur fyrir.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="fe3d0-120">Nota skal **Greiðslumáti** síða til að setja upp greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="fe3d0-121">Til að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu, verður að fylgja þessum viðbótarskref fyrir greiðslumáta:</span><span class="sxs-lookup"><span data-stu-id="fe3d0-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="fe3d0-122">Í **reitnum greiðslugerð** skal velja **rafræn greiðsla**</span><span class="sxs-lookup"><span data-stu-id="fe3d0-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="fe3d0-123">Valfrjálst: Ef þú átt von á að hver viðskiptavinur þinn hafi mörg umboð, í reitnum **Tímabil** skaltu velja **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="fe3d0-124">Aðskild greiðsla verður stofnuð fyrir hvern reikning og hver greiðsla notar umboð sem er tilgreind fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="fe3d0-125">Velja skal **krefjast umboðs** valkost til að búa til greiðslur með umboð fyrir beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="fe3d0-126">**Krefjast umboðs** valkosturinn er tiltækur aðeins ef þú velur **Rafræna greiðslu** í á **greiðslugerð** svæði.</span><span class="sxs-lookup"><span data-stu-id="fe3d0-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="fe3d0-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fe3d0-127">See Also</span></span>

[<span data-ttu-id="fe3d0-128">Yfirlit yfir beingreiðslu</span><span class="sxs-lookup"><span data-stu-id="fe3d0-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="fe3d0-129">Stofna beingreiðsluumboð fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="fe3d0-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


