---
title: Dæmi um minnkunardaga
description: Dæmi um minnkunardaga.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010523"
---
# <a name="reduction-days-example"></a><span data-ttu-id="fddca-103">Dæmi um minnkunardaga</span><span class="sxs-lookup"><span data-stu-id="fddca-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fddca-104">Þú hefur búið til áskriftrarfærslu fyrir viðhaldsáskrift viðskiptavinar, eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="fddca-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="fddca-105">Dagsetning frá</span><span class="sxs-lookup"><span data-stu-id="fddca-105">From date</span></span></p></th>
<th><p><span data-ttu-id="fddca-106">Dagsetning til</span><span class="sxs-lookup"><span data-stu-id="fddca-106">To date</span></span></p></th>
<th><p><span data-ttu-id="fddca-107">Áskrift</span><span class="sxs-lookup"><span data-stu-id="fddca-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="fddca-108">Gerð áskriftar</span><span class="sxs-lookup"><span data-stu-id="fddca-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="fddca-109">Verkefni</span><span class="sxs-lookup"><span data-stu-id="fddca-109">Project</span></span></p></th>
<th><p><span data-ttu-id="fddca-110">Tegund</span><span class="sxs-lookup"><span data-stu-id="fddca-110">Category</span></span></p></th>
<th><p><span data-ttu-id="fddca-111">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="fddca-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="fddca-112">Söluverð</span><span class="sxs-lookup"><span data-stu-id="fddca-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddca-113">01. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="fddca-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="fddca-114">31. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="fddca-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="fddca-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="fddca-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="fddca-116"><strong>Venjuleg</strong></span><span class="sxs-lookup"><span data-stu-id="fddca-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="fddca-117">9013</span><span class="sxs-lookup"><span data-stu-id="fddca-117">9013</span></span></p></td>
<td><p><span data-ttu-id="fddca-118">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="fddca-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="fddca-119">EUR</span><span class="sxs-lookup"><span data-stu-id="fddca-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="fddca-120">200,00</span><span class="sxs-lookup"><span data-stu-id="fddca-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddca-121">Viðskiptavinurinn tilkynnir að hann þurfi ekki þjónustuþekju í tvo daga (10. mars og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="fddca-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="fddca-122">Þú samþykkir að stytta áskriftina sem nemur þessum tveimur dögum.</span><span class="sxs-lookup"><span data-stu-id="fddca-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="fddca-123">Þú býrð til nýja færslu af gerðinni **Minnkunardagar** eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="fddca-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="fddca-124">Dagsetning frá</span><span class="sxs-lookup"><span data-stu-id="fddca-124">From date</span></span></p></th>
<th><p><span data-ttu-id="fddca-125">Dagsetning til</span><span class="sxs-lookup"><span data-stu-id="fddca-125">To date</span></span></p></th>
<th><p><span data-ttu-id="fddca-126">Áskrift</span><span class="sxs-lookup"><span data-stu-id="fddca-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="fddca-127">Gerð áskriftar</span><span class="sxs-lookup"><span data-stu-id="fddca-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="fddca-128">Verkefni</span><span class="sxs-lookup"><span data-stu-id="fddca-128">Project</span></span></p></th>
<th><p><span data-ttu-id="fddca-129">Tegund</span><span class="sxs-lookup"><span data-stu-id="fddca-129">Category</span></span></p></th>
<th><p><span data-ttu-id="fddca-130">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="fddca-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="fddca-131">Söluverð</span><span class="sxs-lookup"><span data-stu-id="fddca-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddca-132">10. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="fddca-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="fddca-133">11. mars, 2011</span><span class="sxs-lookup"><span data-stu-id="fddca-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="fddca-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="fddca-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="fddca-135"><strong>Lækkunardagar</strong></span><span class="sxs-lookup"><span data-stu-id="fddca-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="fddca-136">9013</span><span class="sxs-lookup"><span data-stu-id="fddca-136">9013</span></span></p></td>
<td><p><span data-ttu-id="fddca-137">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="fddca-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="fddca-138">EUR</span><span class="sxs-lookup"><span data-stu-id="fddca-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="fddca-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="fddca-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddca-140">Þegar færslur fyrir mars 2011 eru reikningsfærðar er söluverðið EUR 200 lækkað um EUR 12.90.</span><span class="sxs-lookup"><span data-stu-id="fddca-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="fddca-141">Reikningshæf upphæð fyrir áskriftarfærsluna er þar af leiðandi EUR 187.10, og tvær færslur eru reikningsfærðar fyrir samtals EUR 187.10.</span><span class="sxs-lookup"><span data-stu-id="fddca-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="fddca-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fddca-142">See also</span></span>

[<span data-ttu-id="fddca-143">Fækka dögum á áskrifarþóknunum</span><span class="sxs-lookup"><span data-stu-id="fddca-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


