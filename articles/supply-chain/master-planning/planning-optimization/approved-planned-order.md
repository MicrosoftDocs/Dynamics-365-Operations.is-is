---
title: Skoða, stjórna og samþykkja áætlaðar pantanir
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig eigi að skoða, stjórna og samþykkja áætlaðar pantanir í Fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304368"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="ac7ba-103">Skoða, stjórna og samþykkja áætlaðar pantanir</span><span class="sxs-lookup"><span data-stu-id="ac7ba-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac7ba-104">Í þessu efnisatriði eru veittar upplýsingar um hvernig eigi að skoða, stjórna og samþykkja áætlaðar pantanir í Fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="ac7ba-105">Skoða og hafa umsjón með áætluðum pöntunum</span><span class="sxs-lookup"><span data-stu-id="ac7ba-105">View and manage planned orders</span></span>

<span data-ttu-id="ac7ba-106">Hægt er að skoða og stjórna áætlaðum pöntunum á listasíðu fyrir allar áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="ac7ba-107">Fara á einn af eftirfarandi stöðum eftir því hvaða tegund áætlaðra pantana á að vinna með:</span><span class="sxs-lookup"><span data-stu-id="ac7ba-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="ac7ba-108">Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="ac7ba-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="ac7ba-109">Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="ac7ba-110">Framleiðslustýring \> Framleiðslupantanir \> Áætlaðar framleiðslutillögur</span><span class="sxs-lookup"><span data-stu-id="ac7ba-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="ac7ba-111">Innkaup og aðföng \> Innkaupapantanir \> Áætlaðar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="ac7ba-112">Birgðastjórnun \> Pantanir á innleið \> Áætlaðir flutningar</span><span class="sxs-lookup"><span data-stu-id="ac7ba-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="ac7ba-113">Birgðastjórnun \> Pantanir á útleið \> Áætlaðir flutningar</span><span class="sxs-lookup"><span data-stu-id="ac7ba-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="ac7ba-114">Skoða og breyta stöðu áætlaðra pantana</span><span class="sxs-lookup"><span data-stu-id="ac7ba-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="ac7ba-115">Hægt er að nota reitinn **Staða** fyrir hverja áætlaða pöntun til að auðvelda að fylgjast með framgangi mála eða breyta því hvernig unnið verður úr áætlaðri pöntun.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="ac7ba-116">Eftirfarandi gildi fyrir **Stöðu** eru í boði:</span><span class="sxs-lookup"><span data-stu-id="ac7ba-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="ac7ba-117">**Óunnið** – Þegar aðaláætlanagerð býr til áætlaðar pantanir fá þær þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="ac7ba-118">Áætluðum pöntunum sem eru með þessa stöðu verður eytt við næstu áætlunarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="ac7ba-119">**Lokið** – Þessi staða gefur til kynna að áætluðu pöntuninni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="ac7ba-120">Þegar valið er að staðfesta ekki áætlaða pöntun er hægt að breyta stöðu hennar í *Lokið*.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="ac7ba-121">Athugið að kerfið meðhöndlar stöðurnar *Óunnið* og *Lokið* á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="ac7ba-122">**Samþykkt** – Þessi staða gefur til kynna að áætluð pöntun sé samþykkt til staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="ac7ba-123">Ef staðfesta á áætlaða pöntun er hægt að breyta stöðunni í *Samþykkt*.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="ac7ba-124">Ef á að geyma breytingarnar sem voru gerðar á áætlaðri pöntun, eða ef áform eru um að staðfesta áætlaða pöntun, skal breyta stöðu hennar í *Samþykkt*.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="ac7ba-125">Fyrirhugaðar pantanir sem hafa stöðuna *Samþykktar* teljast fastar og væntanlegar birgðir samkvæmt aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="ac7ba-126">Þeim er þar af leiðandi ekki breytt eða eytt í síðari áætlunarkeyrslum.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="ac7ba-127">Til að ná fram þessari hegðun afritar áætlanagerðin áætlaðar pantanir sem eru með stöðuna *Samþykkt* úr gömlu áætlunarútgáfunni yfir í nýja áætlunarútgáfu í aðaláætlanagerðinni.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="ac7ba-128">Athugið að áætlaðar pantanir með stöðuna *Samþykkt* teljast eingöngu framboð innan tiltekinnar aðaláætlunar.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="ac7ba-129">Til að breyta stöðu einnar áætlaðrar pöntunar skal [opna einhverja listasíðu áætlaðra pantana](#view-planned-orders), opna pöntunina og síðan fylgja einu af þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="ac7ba-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="ac7ba-130">Á flipanum **Almennt** er gildi reitsins **Staða** breytt.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="ac7ba-131">Á aðgerðasvæðinu, í flipanum **Áætluð pöntun**, í flokknum **Ferli**, skal velja **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="ac7ba-132">Veljið **Samþykkja** á aðgerðarúðunni til að merkja pöntunina sem samþykkta.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="ac7ba-133">Til að breyta stöðu nokkurra áætlaðra pantana samtímis skal [opna einhverja listasíðu áætlaðra pantana](#view-planned-orders), velja gátreitinn fyrir hverja pöntun sem ætlunin er að breyta og því næst fylgja einu af þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="ac7ba-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="ac7ba-134">Á aðgerðasvæðinu, í flipanum **Áætluð pöntun**, í flokknum **Ferli**, skal velja **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="ac7ba-135">Veljið **Samþykkja** á aðgerðarúðunni til að merkja pöntunirnar sem samþykktar.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="ac7ba-136">Samþykkja tillögur</span><span class="sxs-lookup"><span data-stu-id="ac7ba-136">Approve planned orders</span></span>

<span data-ttu-id="ac7ba-137">Samþykki áætlaðra pantana er valfrjálst skref í ferlinu við að búa til staðfesta pöntun úr áætlaðri pöntun.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="ac7ba-138">Eftirfarandi mynd sýnir hvernig hægt er að nota gildið fyrir **Stöðu** sem úthlutað er á hverja áætlaða pöntun til að innleiða samþykktarverkflæði.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="ac7ba-139">Til að innleiða samþykktarferli skal stilla gildið fyrir **Stöðu** á handvirkan hátt fyrir hverja áætlaða pöntun eins og lýst var í hlutanum hér á undan.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Áætlað pöntunarflæði](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="ac7ba-141">Mælt er með því að breyttar áætlaðar pantanir séu samþykktar.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="ac7ba-142">Annars verða breytingarnar hunsaðar og skrifað yfir þær af næstu áætlunarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac7ba-143">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ac7ba-143">Additional resources</span></span>

- [<span data-ttu-id="ac7ba-144">Staðfesta áætlaðar pantanir</span><span class="sxs-lookup"><span data-stu-id="ac7ba-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
