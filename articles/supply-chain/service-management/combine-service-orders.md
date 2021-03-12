---
title: Sameina þjónustupantanir
description: Þú getur sameinað þjónustupantanir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55de251f7f9cdbae99eaec13d4ddd7d3bf26b2bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996678"
---
# <a name="combine-service-orders"></a><span data-ttu-id="ee664-103">Sameina þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="ee664-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ee664-104">Þegar þú stofnar þjónustupantanalínur sjálfkrafa í **þjónustusamningunum** skjámynd getur þú valið einn af eftirfarandi valkostum til að tilgreina hvernig þú vilt flokka þær:</span><span class="sxs-lookup"><span data-stu-id="ee664-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="ee664-105">**Eftir þjónustusamningum**</span><span class="sxs-lookup"><span data-stu-id="ee664-105">**By service agreement**</span></span>

  - <span data-ttu-id="ee664-106">**Eftir þjónustuverk**</span><span class="sxs-lookup"><span data-stu-id="ee664-106">**By service task**</span></span>

  - <span data-ttu-id="ee664-107">**Eftir starfsmönnum**</span><span class="sxs-lookup"><span data-stu-id="ee664-107">**By employee**</span></span>

  - <span data-ttu-id="ee664-108">**Eftir þjónustuhlutum**</span><span class="sxs-lookup"><span data-stu-id="ee664-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="ee664-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ee664-109">Example</span></span>

<span data-ttu-id="ee664-110">Þú stofnar þjónustusamning sem hefur upphafsdag þann 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="ee664-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="ee664-111">Í **Sameina þjónustupantanir** reitinn tilgreinir þú **Eftir þjónustuhlut**.</span><span class="sxs-lookup"><span data-stu-id="ee664-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="ee664-112">Svo eru eftirfarandi þjónustusamningslínur stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="ee664-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="ee664-113">Samningslínunúmer</span><span class="sxs-lookup"><span data-stu-id="ee664-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="ee664-114">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="ee664-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="ee664-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="ee664-115">Description</span></span></p></th>
<th><p><span data-ttu-id="ee664-116">Bil</span><span class="sxs-lookup"><span data-stu-id="ee664-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="ee664-117">Þjónustuhlutur</span><span class="sxs-lookup"><span data-stu-id="ee664-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="ee664-118">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="ee664-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee664-119">1</span><span class="sxs-lookup"><span data-stu-id="ee664-119">1</span></span></p></td>
<td><p><span data-ttu-id="ee664-120"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="ee664-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="ee664-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="ee664-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="ee664-122">Vikulega</span><span class="sxs-lookup"><span data-stu-id="ee664-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="ee664-123">X-1</span><span class="sxs-lookup"><span data-stu-id="ee664-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="ee664-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="ee664-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee664-125">2</span><span class="sxs-lookup"><span data-stu-id="ee664-125">2</span></span></p></td>
<td><p><span data-ttu-id="ee664-126"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="ee664-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="ee664-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="ee664-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="ee664-128">Aðra hverja viku</span><span class="sxs-lookup"><span data-stu-id="ee664-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="ee664-129">X-2</span><span class="sxs-lookup"><span data-stu-id="ee664-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="ee664-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="ee664-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee664-131">3</span><span class="sxs-lookup"><span data-stu-id="ee664-131">3</span></span></p></td>
<td><p><span data-ttu-id="ee664-132"><strong>Vinnustund</strong></span><span class="sxs-lookup"><span data-stu-id="ee664-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="ee664-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="ee664-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="ee664-134">Vikulega</span><span class="sxs-lookup"><span data-stu-id="ee664-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="ee664-135">X-2</span><span class="sxs-lookup"><span data-stu-id="ee664-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="ee664-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="ee664-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee664-137">Ekki eru skilgreindir tímagluggar fyrir neina af þjónustupöntunarlínunum.</span><span class="sxs-lookup"><span data-stu-id="ee664-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="ee664-138">Þess vegna munu þjónustupöntunarlínurnar ekki færast frá þeim reiknaða degi sem þær raðast niður á.</span><span class="sxs-lookup"><span data-stu-id="ee664-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="ee664-139">Næst býrðu til þjónustupantanalínur frá **Búa til þjónustupantanir** skjámynd frá 04-01-2007 til 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="ee664-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="ee664-140">Í allt eru 10 þjónustupantanir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="ee664-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="ee664-141">Vegna þess að sameinaða stillingin sem þú valdir var **Eftir þjónustuhlut** eru allar þjónustupantanir sem eru búnar til aðeins með þjónustupantanalínur með eina tiltekna þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="ee664-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="ee664-142">Þjónustupantanalínur sem búnar eru til úr þjónustusamningi og hafa sömu þjónustudagsetningu og hlut er sameinuð á sömu þjónustustigi.</span><span class="sxs-lookup"><span data-stu-id="ee664-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ee664-143">Í þessu dæmi er dagatalið sem er tilgreint í <STRONG>Færibreytur þjónustukerfis</STRONG> skjámynd ekki með neina lokaðir dagar.</span><span class="sxs-lookup"><span data-stu-id="ee664-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="ee664-144">Viðbótar flokkun þjónustupantanalína í þjónustupantanir fer fram í samræmi við hvaða tímaglugga sem þú tilgreinir á þjónustusamningslínum.</span><span class="sxs-lookup"><span data-stu-id="ee664-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee664-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ee664-145">See also</span></span>

[<span data-ttu-id="ee664-146">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="ee664-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


