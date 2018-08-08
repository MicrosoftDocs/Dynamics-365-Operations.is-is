---
title: "Sameina þjónustupantanir"
description: "Þú getur sameinað þjónustupantanir."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="c97c4-103">Sameina þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="c97c4-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c97c4-104">Þegar þú stofnar þjónustupantanalínur sjálfkrafa í **þjónustusamningunum** skjámynd getur þú valið einn af eftirfarandi valkostum til að tilgreina hvernig þú vilt flokka þær:</span><span class="sxs-lookup"><span data-stu-id="c97c4-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="c97c4-105">**Eftir þjónustusamningum**</span><span class="sxs-lookup"><span data-stu-id="c97c4-105">**By service agreement**</span></span>

  - <span data-ttu-id="c97c4-106">**Eftir þjónustuverk**</span><span class="sxs-lookup"><span data-stu-id="c97c4-106">**By service task**</span></span>

  - <span data-ttu-id="c97c4-107">**Eftir starfsmönnum**</span><span class="sxs-lookup"><span data-stu-id="c97c4-107">**By employee**</span></span>

  - <span data-ttu-id="c97c4-108">**Eftir þjónustuhlutum**</span><span class="sxs-lookup"><span data-stu-id="c97c4-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="c97c4-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c97c4-109">Example</span></span>

<span data-ttu-id="c97c4-110">Þú stofnar þjónustusamning sem hefur upphafsdag þann 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="c97c4-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="c97c4-111">Í **Sameina þjónustupantanir** reitinn tilgreinir þú **Eftir þjónustuhlut**.</span><span class="sxs-lookup"><span data-stu-id="c97c4-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="c97c4-112">Svo eru eftirfarandi þjónustusamningslínur stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="c97c4-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c97c4-113">Samningslínunúmer</span><span class="sxs-lookup"><span data-stu-id="c97c4-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="c97c4-114">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="c97c4-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="c97c4-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="c97c4-115">Description</span></span></p></th>
<th><p><span data-ttu-id="c97c4-116">Bil</span><span class="sxs-lookup"><span data-stu-id="c97c4-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="c97c4-117">Þjónustuhlutur</span><span class="sxs-lookup"><span data-stu-id="c97c4-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="c97c4-118">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c97c4-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c97c4-119">1</span><span class="sxs-lookup"><span data-stu-id="c97c4-119">1</span></span></p></td>
<td><p><span data-ttu-id="c97c4-120"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="c97c4-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="c97c4-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="c97c4-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="c97c4-122">Vikulega</span><span class="sxs-lookup"><span data-stu-id="c97c4-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="c97c4-123">X-1</span><span class="sxs-lookup"><span data-stu-id="c97c4-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="c97c4-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="c97c4-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c97c4-125">2</span><span class="sxs-lookup"><span data-stu-id="c97c4-125">2</span></span></p></td>
<td><p><span data-ttu-id="c97c4-126"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="c97c4-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="c97c4-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="c97c4-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="c97c4-128">Aðra hverja viku</span><span class="sxs-lookup"><span data-stu-id="c97c4-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="c97c4-129">X-2</span><span class="sxs-lookup"><span data-stu-id="c97c4-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="c97c4-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="c97c4-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c97c4-131">3</span><span class="sxs-lookup"><span data-stu-id="c97c4-131">3</span></span></p></td>
<td><p><span data-ttu-id="c97c4-132"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="c97c4-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="c97c4-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="c97c4-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="c97c4-134">Vikulega</span><span class="sxs-lookup"><span data-stu-id="c97c4-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="c97c4-135">X-2</span><span class="sxs-lookup"><span data-stu-id="c97c4-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="c97c4-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="c97c4-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c97c4-137">Ekki eru skilgreindir tímagluggar fyrir neina af þjónustupöntunarlínunum.</span><span class="sxs-lookup"><span data-stu-id="c97c4-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="c97c4-138">Þess vegna munu þjónustupöntunarlínurnar ekki færast frá þeim reiknaða degi sem þær raðast niður á.</span><span class="sxs-lookup"><span data-stu-id="c97c4-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="c97c4-139">Næst býrðu til þjónustupantanalínur frá **Búa til þjónustupantanir** skjámynd frá 04-01-2007 til 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="c97c4-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="c97c4-140">Í allt eru 10 þjónustupantanir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="c97c4-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="c97c4-141">Vegna þess að sameinaða stillingin sem þú valdir var **Eftir þjónustuhlut** eru allar þjónustupantanir sem eru búnar til aðeins með þjónustupantanalínur með eina tiltekna þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="c97c4-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="c97c4-142">Þjónustupantanalínur sem búnar eru til úr þjónustusamningi og hafa sömu þjónustudagsetningu og hlut er sameinuð á sömu þjónustustigi.</span><span class="sxs-lookup"><span data-stu-id="c97c4-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c97c4-143">Í þessu dæmi er dagatalið sem er tilgreint í <STRONG>Færibreytur þjónustukerfis</STRONG> skjámynd ekki með neina lokaðir dagar.</span><span class="sxs-lookup"><span data-stu-id="c97c4-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="c97c4-144">Viðbótar flokkun þjónustupantanalína í þjónustupantanir fer fram í samræmi við hvaða tímaglugga sem þú tilgreinir á þjónustusamningslínum.</span><span class="sxs-lookup"><span data-stu-id="c97c4-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="c97c4-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c97c4-145">See also</span></span>

[<span data-ttu-id="c97c4-146">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="c97c4-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



