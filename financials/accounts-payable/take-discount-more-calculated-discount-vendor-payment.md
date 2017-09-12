---
title: "Taka afslátt sem er meiri en reiknaður afsláttur fyrir greiðslu lánardrottins"
description: "Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 39830014593b7b1bc2868afffcca0f77a0c8a029
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="699cf-104">Taka afslátt sem er meiri en reiknaður afsláttur fyrir greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="699cf-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="699cf-105">Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="699cf-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="699cf-106">Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn.</span><span class="sxs-lookup"><span data-stu-id="699cf-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="699cf-107">Lánardrottni 3051 gefur Fabrikam 4 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan sjö daga.</span><span class="sxs-lookup"><span data-stu-id="699cf-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="699cf-108">Þann 29. júní færir Apríl inn reikning uppá 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="699cf-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="699cf-109">Lánardrottinninn heimilar Apríl að taka afslátt upp á 60,00 í staðinn fyrir sjálfgefinn afslátt upp á 40,00 sem er tiltækur fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="699cf-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="699cf-110">Apríl skráir eingreiðslu með því að nota greiðslubók viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="699cf-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="699cf-111">Hún færir inn lánardrottinn fyrir greiðsluna og opnar svo síðuna **Jafna færslur**.</span><span class="sxs-lookup"><span data-stu-id="699cf-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="699cf-112">Hún merkir reikninginn og breytir gildinu í reitnum **Upphæð staðgreiðsluafsláttar** í **60,00**.</span><span class="sxs-lookup"><span data-stu-id="699cf-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>
| <span data-ttu-id="699cf-113">Merkja</span><span class="sxs-lookup"><span data-stu-id="699cf-113">Mark</span></span>     | <span data-ttu-id="699cf-114">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="699cf-114">Use cash discount</span></span> | <span data-ttu-id="699cf-115">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="699cf-115">Voucher</span></span>   | <span data-ttu-id="699cf-116">Reikningur</span><span class="sxs-lookup"><span data-stu-id="699cf-116">Account</span></span> | <span data-ttu-id="699cf-117">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="699cf-117">Date</span></span>      | <span data-ttu-id="699cf-118">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="699cf-118">Due date</span></span>  | <span data-ttu-id="699cf-119">Reikningur</span><span class="sxs-lookup"><span data-stu-id="699cf-119">Invoice</span></span> | <span data-ttu-id="699cf-120">Upphæð í gjaldmiðli færslu</span><span class="sxs-lookup"><span data-stu-id="699cf-120">Amount in transaction currency</span></span> | <span data-ttu-id="699cf-121">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="699cf-121">Currency</span></span> | <span data-ttu-id="699cf-122">Upphæð til jöfnunar</span><span class="sxs-lookup"><span data-stu-id="699cf-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="699cf-123">Valið</span><span class="sxs-lookup"><span data-stu-id="699cf-123">Selected</span></span> | <span data-ttu-id="699cf-124">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="699cf-124">Normal</span></span>            | <span data-ttu-id="699cf-125">Reikn-10040</span><span class="sxs-lookup"><span data-stu-id="699cf-125">Inv-10040</span></span> | <span data-ttu-id="699cf-126">3051</span><span class="sxs-lookup"><span data-stu-id="699cf-126">3051</span></span>    | <span data-ttu-id="699cf-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="699cf-127">6/29/2015</span></span> | <span data-ttu-id="699cf-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="699cf-128">7/29/2015</span></span> | <span data-ttu-id="699cf-129">10040</span><span class="sxs-lookup"><span data-stu-id="699cf-129">10040</span></span>   | <span data-ttu-id="699cf-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="699cf-130">1,000.00</span></span>                       | <span data-ttu-id="699cf-131">USD</span><span class="sxs-lookup"><span data-stu-id="699cf-131">USD</span></span>      | <span data-ttu-id="699cf-132">940,00</span><span class="sxs-lookup"><span data-stu-id="699cf-132">940.00</span></span>           |

<span data-ttu-id="699cf-133">Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="699cf-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>
|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="699cf-134">Dagsetning staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="699cf-134">Cash discount date</span></span>           | <span data-ttu-id="699cf-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="699cf-135">7/12/2015</span></span> |
| <span data-ttu-id="699cf-136">Upphæð staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="699cf-136">Cash discount amount</span></span>         | <span data-ttu-id="699cf-137">60,00</span><span class="sxs-lookup"><span data-stu-id="699cf-137">60.00</span></span>     |
| <span data-ttu-id="699cf-138">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="699cf-138">Use cash discount</span></span>            | <span data-ttu-id="699cf-139">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="699cf-139">Normal</span></span>    |
| <span data-ttu-id="699cf-140">Notaður staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="699cf-140">Cash discount taken</span></span>          | <span data-ttu-id="699cf-141">0,00</span><span class="sxs-lookup"><span data-stu-id="699cf-141">0.00</span></span>      |
| <span data-ttu-id="699cf-142">Upphæð staðgreiðsluafsláttar sem á að veita</span><span class="sxs-lookup"><span data-stu-id="699cf-142">Cash discount amount to take</span></span> | <span data-ttu-id="699cf-143">60,00</span><span class="sxs-lookup"><span data-stu-id="699cf-143">60.00</span></span>     |

<span data-ttu-id="699cf-144">Apríl bókar greiðslubókina.</span><span class="sxs-lookup"><span data-stu-id="699cf-144">April posts the payment journal.</span></span> <span data-ttu-id="699cf-145">Reikningurinn er fulljafnaður með greiðslu upp á 940,00 og afslátt upp á 60,00.</span><span class="sxs-lookup"><span data-stu-id="699cf-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




