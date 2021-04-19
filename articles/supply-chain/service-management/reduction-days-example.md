---
title: Dæmi um minnkunardaga
description: Dæmi um minnkunardaga.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836063"
---
# <a name="reduction-days-example"></a><span data-ttu-id="8a11c-103">Dæmi um minnkunardaga</span><span class="sxs-lookup"><span data-stu-id="8a11c-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8a11c-104">Þú hefur búið til áskriftrarfærslu fyrir viðhaldsáskrift viðskiptavinar, eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="8a11c-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a11c-105">Dagsetning frá</span><span class="sxs-lookup"><span data-stu-id="8a11c-105">From date</span></span></p></th>
<th><p><span data-ttu-id="8a11c-106">Dagsetning til</span><span class="sxs-lookup"><span data-stu-id="8a11c-106">To date</span></span></p></th>
<th><p><span data-ttu-id="8a11c-107">Áskrift</span><span class="sxs-lookup"><span data-stu-id="8a11c-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8a11c-108">Gerð áskriftar</span><span class="sxs-lookup"><span data-stu-id="8a11c-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8a11c-109">Verkefni</span><span class="sxs-lookup"><span data-stu-id="8a11c-109">Project</span></span></p></th>
<th><p><span data-ttu-id="8a11c-110">Tegund</span><span class="sxs-lookup"><span data-stu-id="8a11c-110">Category</span></span></p></th>
<th><p><span data-ttu-id="8a11c-111">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="8a11c-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8a11c-112">Söluverð</span><span class="sxs-lookup"><span data-stu-id="8a11c-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a11c-113">01. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="8a11c-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="8a11c-114">31. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="8a11c-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="8a11c-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="8a11c-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8a11c-116"><strong>Venjuleg</strong></span><span class="sxs-lookup"><span data-stu-id="8a11c-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="8a11c-117">9013</span><span class="sxs-lookup"><span data-stu-id="8a11c-117">9013</span></span></p></td>
<td><p><span data-ttu-id="8a11c-118">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="8a11c-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8a11c-119">EUR</span><span class="sxs-lookup"><span data-stu-id="8a11c-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="8a11c-120">200,00</span><span class="sxs-lookup"><span data-stu-id="8a11c-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a11c-121">Viðskiptavinurinn tilkynnir að hann þurfi ekki þjónustuþekju í tvo daga (10. mars og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="8a11c-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="8a11c-122">Þú samþykkir að stytta áskriftina sem nemur þessum tveimur dögum.</span><span class="sxs-lookup"><span data-stu-id="8a11c-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="8a11c-123">Þú býrð til nýja færslu af gerðinni **Minnkunardagar** eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="8a11c-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a11c-124">Dagsetning frá</span><span class="sxs-lookup"><span data-stu-id="8a11c-124">From date</span></span></p></th>
<th><p><span data-ttu-id="8a11c-125">Dagsetning til</span><span class="sxs-lookup"><span data-stu-id="8a11c-125">To date</span></span></p></th>
<th><p><span data-ttu-id="8a11c-126">Áskrift</span><span class="sxs-lookup"><span data-stu-id="8a11c-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8a11c-127">Gerð áskriftar</span><span class="sxs-lookup"><span data-stu-id="8a11c-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8a11c-128">Verkefni</span><span class="sxs-lookup"><span data-stu-id="8a11c-128">Project</span></span></p></th>
<th><p><span data-ttu-id="8a11c-129">Tegund</span><span class="sxs-lookup"><span data-stu-id="8a11c-129">Category</span></span></p></th>
<th><p><span data-ttu-id="8a11c-130">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="8a11c-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8a11c-131">Söluverð</span><span class="sxs-lookup"><span data-stu-id="8a11c-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a11c-132">10. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="8a11c-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="8a11c-133">11. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="8a11c-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="8a11c-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="8a11c-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8a11c-135"><strong>Lækkunardagar</strong></span><span class="sxs-lookup"><span data-stu-id="8a11c-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="8a11c-136">9013</span><span class="sxs-lookup"><span data-stu-id="8a11c-136">9013</span></span></p></td>
<td><p><span data-ttu-id="8a11c-137">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="8a11c-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8a11c-138">EUR</span><span class="sxs-lookup"><span data-stu-id="8a11c-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="8a11c-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="8a11c-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a11c-140">Þegar færslur fyrir mars 2011 eru reikningsfærðar er söluverðið EUR 200 lækkað um EUR 12.90.</span><span class="sxs-lookup"><span data-stu-id="8a11c-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="8a11c-141">Reikningshæf upphæð fyrir áskriftarfærsluna er þar af leiðandi EUR 187.10, og tvær færslur eru reikningsfærðar fyrir samtals EUR 187.10.</span><span class="sxs-lookup"><span data-stu-id="8a11c-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a11c-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8a11c-142">See also</span></span>

[<span data-ttu-id="8a11c-143">Fækka dögum á áskrifarþóknunum</span><span class="sxs-lookup"><span data-stu-id="8a11c-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]