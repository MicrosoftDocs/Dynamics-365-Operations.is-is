---
title: Vinna með áætlaðar pantanir
description: Þetta efnisatriði gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum. Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f62381ca212e711fd61e12c9ec8f066ec124a933
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430573"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="6a947-104">Vinna með áætlaðar pantanir</span><span class="sxs-lookup"><span data-stu-id="6a947-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a947-105">Þetta efnisatriði gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum.</span><span class="sxs-lookup"><span data-stu-id="6a947-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="6a947-106">Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun.</span><span class="sxs-lookup"><span data-stu-id="6a947-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="6a947-107">Hægt er að stjórna áætluðum pöntunum úr vinnusvæðinu **Aðaláætlanagerð**, úr listanum **Áætluð pöntun** eða listunum **Áætlaðar framleiðslupantanir**, **Áætlaðar innkaupapantanir**, og **Flutningsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="6a947-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="6a947-108">Staða tillögu</span><span class="sxs-lookup"><span data-stu-id="6a947-108">Planned order status</span></span>
<span data-ttu-id="6a947-109">Hægt er að nota svæðið **Staða** til að aðstoða við að rekja framgang.</span><span class="sxs-lookup"><span data-stu-id="6a947-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="6a947-110">Eftirtalin gildi eru notuð:</span><span class="sxs-lookup"><span data-stu-id="6a947-110">The following values are used:</span></span>

-   <span data-ttu-id="6a947-111">Þegar aðaláætlunagerð°myndar áætlaðar pantanir, hafa áætlaðar pantanir stöðuna **Óunnið**.</span><span class="sxs-lookup"><span data-stu-id="6a947-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="6a947-112">Þegar valið er að staðfesta ekki áætlaða pöntun getur hún fengið stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6a947-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="6a947-113">Ef þú vilt festa skipulagða pöntun geturðu breytt stöðunni í **Samþykkt**.</span><span class="sxs-lookup"><span data-stu-id="6a947-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="6a947-114">Skipulagðar pantanir með stöðuna **Samþykkt** eru virtar af aðaláætlanagerð, svo þeim er ekki breytt eða þeim eytt í síðari keyrslu á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="6a947-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="6a947-115">Til að ná þessu afritar áætlunargrunnurinn **Samþykktar** áætlaðar pantanir úr gömlu áætlunarútgáfunni yfir í nýju áætlunarútgáfuna við aðalskipulagningu.</span><span class="sxs-lookup"><span data-stu-id="6a947-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="6a947-116">Staðfesting á tillögum</span><span class="sxs-lookup"><span data-stu-id="6a947-116">Firming planned orders</span></span> 
<span data-ttu-id="6a947-117">Með því að staðfesta tillögur eru raunverulegar pantanir búnar til.</span><span class="sxs-lookup"><span data-stu-id="6a947-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="6a947-118">Þær eru líka þekkar sem *losaðar* eða *opnar pantanir*.</span><span class="sxs-lookup"><span data-stu-id="6a947-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="6a947-119">Þegar áætluð pöntun er staðfest er hún færð í pöntunarhluta í viðeigandi einingu.</span><span class="sxs-lookup"><span data-stu-id="6a947-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="6a947-120">Þú getur valið tvo staðfestingarvalkosti af síðunni **Tillögur**:</span><span class="sxs-lookup"><span data-stu-id="6a947-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="6a947-121">**Staðfesta** - Þetta mun staðfesta eina eða margar valdar tillögur.</span><span class="sxs-lookup"><span data-stu-id="6a947-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="6a947-122">**Staðfesta allt** - Þetta staðfestir allar tillögur í síunni.</span><span class="sxs-lookup"><span data-stu-id="6a947-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="6a947-123">Með því að nota **Staðfesta allt** þarftu ekki að velja tillöguna, allar tillögur innan síunnar verða staðfestar.</span><span class="sxs-lookup"><span data-stu-id="6a947-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="6a947-124">Þessi valkostur getur verið gagnlegur ef þú ert að styrkja mikinn fjölda tillagna.</span><span class="sxs-lookup"><span data-stu-id="6a947-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="6a947-125">Þú getur fylgst með fyrirhugaðri pöntun sem var stytt frá **Staðfestingarsaga** undir **Skjámyndinni Tillögur > Skoða > Staðfestingasaga**.</span><span class="sxs-lookup"><span data-stu-id="6a947-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="6a947-126">Samhliða staðfesting</span><span class="sxs-lookup"><span data-stu-id="6a947-126">Parallelize firming</span></span>
<span data-ttu-id="6a947-127">Ef þú ætlar að vinna margar pantanir í einu getur samhliða keyrsla bætt keyrslutímann eða frammistöðu.</span><span class="sxs-lookup"><span data-stu-id="6a947-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="6a947-128">Þessi valkostur er tiltækur við staðfestingu á mörgum tillögum með annaðhvort **Staðfesta** eða **Staðfesta allt**.</span><span class="sxs-lookup"><span data-stu-id="6a947-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="6a947-129">Eftirfarandi færibreytur eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="6a947-129">The following parameters are available:</span></span>

-   <span data-ttu-id="6a947-130">**Samhliða staðfesting** - Ef **Já** verður staðfestingarferlið gert samhliða með fjölda þráða sem skilgreindir eru í **Fjöldi þráða**.</span><span class="sxs-lookup"><span data-stu-id="6a947-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="6a947-131">**Fjöldi þráða** - Stýrir fjölda þráða sem notaðir eru til að gera staðfestingarferlið samhliða.</span><span class="sxs-lookup"><span data-stu-id="6a947-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="6a947-132">Færiubreytan er aðeins sýnd þegar **Samhliða staðfesting** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6a947-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="6a947-133">Valkosturinn fyrir **Samhliða staðfesting** er aðeins sýndur þegar fleiri en ein áætluð röð er valin til staðfestngar.</span><span class="sxs-lookup"><span data-stu-id="6a947-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6a947-134">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6a947-134">Additional resources</span></span>
--------

[<span data-ttu-id="6a947-135">Yfirlit aðaláætlana</span><span class="sxs-lookup"><span data-stu-id="6a947-135">Master plans overview</span></span>](master-plans.md)



