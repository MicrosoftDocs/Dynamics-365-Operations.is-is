---
title: Taka afslátt sem er meiri en reiknaður afsláttur fyrir greiðslu lánardrottins
description: Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66296bc22cb3b940ed914b77b8c3a7c054d4aa71
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "326838"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="52c3a-104">Taka afslátt sem er meiri en reiknaður afsláttur fyrir greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52c3a-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52c3a-105">Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="52c3a-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="52c3a-106">Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn.</span><span class="sxs-lookup"><span data-stu-id="52c3a-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="52c3a-107">Lánardrottni 3051 gefur Fabrikam 4 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan sjö daga.</span><span class="sxs-lookup"><span data-stu-id="52c3a-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="52c3a-108">Þann 29. júní færir Apríl inn reikning uppá 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="52c3a-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="52c3a-109">Lánardrottinninn heimilar Apríl að taka afslátt upp á 60,00 í staðinn fyrir sjálfgefinn afslátt upp á 40,00 sem er tiltækur fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="52c3a-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="52c3a-110">Apríl skráir eingreiðslu með því að nota greiðslubók viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="52c3a-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="52c3a-111">Hún færir inn lánardrottinn fyrir greiðsluna og opnar svo síðuna **Jafna færslur**.</span><span class="sxs-lookup"><span data-stu-id="52c3a-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="52c3a-112">Hún merkir reikninginn og breytir gildinu í reitnum **Upphæð staðgreiðsluafsláttar** í **60,00**.</span><span class="sxs-lookup"><span data-stu-id="52c3a-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="52c3a-113">Merkja</span><span class="sxs-lookup"><span data-stu-id="52c3a-113">Mark</span></span>     | <span data-ttu-id="52c3a-114">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="52c3a-114">Use cash discount</span></span> | <span data-ttu-id="52c3a-115">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="52c3a-115">Voucher</span></span>   | <span data-ttu-id="52c3a-116">Reikningur</span><span class="sxs-lookup"><span data-stu-id="52c3a-116">Account</span></span> | <span data-ttu-id="52c3a-117">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="52c3a-117">Date</span></span>      | <span data-ttu-id="52c3a-118">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="52c3a-118">Due date</span></span>  | <span data-ttu-id="52c3a-119">Reikningur</span><span class="sxs-lookup"><span data-stu-id="52c3a-119">Invoice</span></span> | <span data-ttu-id="52c3a-120">Upphæð í gjaldmiðli færslu</span><span class="sxs-lookup"><span data-stu-id="52c3a-120">Amount in transaction currency</span></span> | <span data-ttu-id="52c3a-121">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="52c3a-121">Currency</span></span> | <span data-ttu-id="52c3a-122">Upphæð til jöfnunar</span><span class="sxs-lookup"><span data-stu-id="52c3a-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="52c3a-123">Valið</span><span class="sxs-lookup"><span data-stu-id="52c3a-123">Selected</span></span> | <span data-ttu-id="52c3a-124">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="52c3a-124">Normal</span></span>            | <span data-ttu-id="52c3a-125">Reikn-10040</span><span class="sxs-lookup"><span data-stu-id="52c3a-125">Inv-10040</span></span> | <span data-ttu-id="52c3a-126">3051</span><span class="sxs-lookup"><span data-stu-id="52c3a-126">3051</span></span>    | <span data-ttu-id="52c3a-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="52c3a-127">6/29/2015</span></span> | <span data-ttu-id="52c3a-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="52c3a-128">7/29/2015</span></span> | <span data-ttu-id="52c3a-129">10040</span><span class="sxs-lookup"><span data-stu-id="52c3a-129">10040</span></span>   | <span data-ttu-id="52c3a-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="52c3a-130">1,000.00</span></span>                       | <span data-ttu-id="52c3a-131">USD</span><span class="sxs-lookup"><span data-stu-id="52c3a-131">USD</span></span>      | <span data-ttu-id="52c3a-132">940,00</span><span class="sxs-lookup"><span data-stu-id="52c3a-132">940.00</span></span>           |

<span data-ttu-id="52c3a-133">Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="52c3a-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="52c3a-134">Dagsetning staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="52c3a-134">Cash discount date</span></span>           | <span data-ttu-id="52c3a-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="52c3a-135">7/12/2015</span></span> |
| <span data-ttu-id="52c3a-136">Upphæð staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="52c3a-136">Cash discount amount</span></span>         | <span data-ttu-id="52c3a-137">60,00</span><span class="sxs-lookup"><span data-stu-id="52c3a-137">60.00</span></span>     |
| <span data-ttu-id="52c3a-138">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="52c3a-138">Use cash discount</span></span>            | <span data-ttu-id="52c3a-139">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="52c3a-139">Normal</span></span>    |
| <span data-ttu-id="52c3a-140">Notaður staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="52c3a-140">Cash discount taken</span></span>          | <span data-ttu-id="52c3a-141">0,00</span><span class="sxs-lookup"><span data-stu-id="52c3a-141">0.00</span></span>      |
| <span data-ttu-id="52c3a-142">Upphæð staðgreiðsluafsláttar sem á að veita</span><span class="sxs-lookup"><span data-stu-id="52c3a-142">Cash discount amount to take</span></span> | <span data-ttu-id="52c3a-143">60,00</span><span class="sxs-lookup"><span data-stu-id="52c3a-143">60.00</span></span>     |

<span data-ttu-id="52c3a-144">Apríl bókar greiðslubókina.</span><span class="sxs-lookup"><span data-stu-id="52c3a-144">April posts the payment journal.</span></span> <span data-ttu-id="52c3a-145">Reikningurinn er fulljafnaður með greiðslu upp á 940,00 og afslátt upp á 60,00.</span><span class="sxs-lookup"><span data-stu-id="52c3a-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



