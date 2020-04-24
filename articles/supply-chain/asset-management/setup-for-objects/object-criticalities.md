---
title: Mikilvægisgerðir eigna
description: Umræðuefnið útskýrir gerðir eignamikilvægis í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c6d3742425a3b92282a62c142b9c325e2d7042f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216598"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="c02c0-103">Mikilvægisgerðir eigna</span><span class="sxs-lookup"><span data-stu-id="c02c0-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c02c0-104">Umræðuefnið útskýrir gerðir eignamikilvægis í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="c02c0-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="c02c0-105">Mikilvægi eigna er tengd eignum og færð yfir í verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="c02c0-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="c02c0-106">Það er ekki hægt að breyta því í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="c02c0-106">It can't be changed on a work order.</span></span> <span data-ttu-id="c02c0-107">Skilvirkni eigna er notuð til að reikna út gagnrýni á verkþörf meðan á tímasetningu verkbeiðni stendur.</span><span class="sxs-lookup"><span data-stu-id="c02c0-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="c02c0-108">Með öðrum orðum, það er notað til að reikna út að hve miklu leyti viðhaldsstörf á eign hafa áhrif á framleiðsluáætlun og framleiðni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c02c0-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="c02c0-109">Nánari upplýsingar um uppsetninguna sem er tengd útreikningi á matseinkunnum fyrir tímasetningar verkbeiðni, sjá [Færibreytur eignastýringar](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c02c0-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="c02c0-110">Til að setja upp gagnrýni skaparðu fyrst þær tegundir gagnrýni sem ætti að nota í uppsetningu eigna.</span><span class="sxs-lookup"><span data-stu-id="c02c0-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="c02c0-111">Þú setur síðan upp eignamikilvægi.</span><span class="sxs-lookup"><span data-stu-id="c02c0-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="c02c0-112">Setja upp gerðir mikilvægis</span><span class="sxs-lookup"><span data-stu-id="c02c0-112">Set up criticality types</span></span>

1. <span data-ttu-id="c02c0-113">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Gerðir mikilvægis**.</span><span class="sxs-lookup"><span data-stu-id="c02c0-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="c02c0-114">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="c02c0-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c02c0-115">Í retinum **Gagnrýni** slærðu inn tölu sem gefur til kynna mikilvægi.</span><span class="sxs-lookup"><span data-stu-id="c02c0-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="c02c0-116">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir gerð mikilvægis.</span><span class="sxs-lookup"><span data-stu-id="c02c0-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="c02c0-117">Í reitnum **Stuðull** skal slá inn stuðul.</span><span class="sxs-lookup"><span data-stu-id="c02c0-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="c02c0-118">Þessi þáttur er notaður við útreikning á tímasetningu verkbeiðnaáætlana til að ákvarða mikilvægisskrá sem ætti að nota.</span><span class="sxs-lookup"><span data-stu-id="c02c0-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="c02c0-119">(Færslan sem hefur hæsta þáttinn er alltaf notuð.) Þessi stilling skiptir máli ef, eins og sýnt er á eftirfarandi mynd, eru gagnrýni línur búnar til sem hafa sama gagnrýni gildi.</span><span class="sxs-lookup"><span data-stu-id="c02c0-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Síðan Gerðir mikilvægis](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="c02c0-121">Setja upp mikilvægi eigna</span><span class="sxs-lookup"><span data-stu-id="c02c0-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="c02c0-122">Veldu **Eignastýring** \> **Uppsetning** \> **Eignamikilvægi**.</span><span class="sxs-lookup"><span data-stu-id="c02c0-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="c02c0-123">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="c02c0-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c02c0-124">Taktu viðeigandi val í upplýsingagjöfina eftir því hvaða smáatriða er krafist varðandi gagnrýni í reitunum **Virk staðsetning**, **Gerð eigna**, **Framleiðandi**, **Fyrirmynd**, **Eignir**, **Starfsflokkur**, **Atvinnugerð**, **Atvinnugerðafbrigði**, og **Starfsskylda**.</span><span class="sxs-lookup"><span data-stu-id="c02c0-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c02c0-125">Þegar eignagagnrýni er valið fer Eignastjórn í gegnum allar skrár yfir mikilvægi eigna til að athuga hvort mögulegt sé samsvörun.</span><span class="sxs-lookup"><span data-stu-id="c02c0-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="c02c0-126">Það athugar alltaf sértækustu samsetninguna fyrst.</span><span class="sxs-lookup"><span data-stu-id="c02c0-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="c02c0-127">Með öðrum orðum, Eignastjórnun kannar fyrst **Starfsskylda**.</span><span class="sxs-lookup"><span data-stu-id="c02c0-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="c02c0-128">Ef engin samsvörun finnst, þá athugar hún **Atvinnugerðafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="c02c0-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="c02c0-129">Ef engin samsvörun finnst, þá athugar hún **Atvinnugerðafbrigði** og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="c02c0-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="c02c0-130">Eins og þú sérð á skipulagi síðunnar þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik.</span><span class="sxs-lookup"><span data-stu-id="c02c0-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="c02c0-131">Ef engin samsvörun er notuð er „sjálfgefna“ skráin sem hefur engin val verið notuð.</span><span class="sxs-lookup"><span data-stu-id="c02c0-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="c02c0-132">Í **Gagnrýni** veldu eitt af mikilvægisgildunum sem þú bjóst til í fyrri aðferð.</span><span class="sxs-lookup"><span data-stu-id="c02c0-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="c02c0-133">Athugasemdir um skipulag gagnrýni</span><span class="sxs-lookup"><span data-stu-id="c02c0-133">Notes about criticality setup</span></span>

- <span data-ttu-id="c02c0-134">Ef þú breytir mikilvægi eigna í þessari uppsetningu eftir að þú hefur þegar notað það í vinnupöntun, er gagnrýninn á vinnuskipulagið ekki uppfærður til samræmis.</span><span class="sxs-lookup"><span data-stu-id="c02c0-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="c02c0-135">Gagnrýnin á verkbeiðni er endurútreiknuð í hvert skipti sem vinnupöntunarlínu er bætt við eða henni eytt úr verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="c02c0-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="c02c0-136">Ef verkbeiðni inniheldur nokkur vinnupöntunarstörf er mesta gagnrýni samkvæmt **Þáttur** reit á síðunni **Gerðir gagnrýni**, er alltaf notuð í nni.</span><span class="sxs-lookup"><span data-stu-id="c02c0-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="c02c0-137">Almennt getur gagnrýni eigna breyst á tímabili.</span><span class="sxs-lookup"><span data-stu-id="c02c0-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="c02c0-138">Gagnrýni getur orðið fyrir áhrifum af kaup á nýjum búnaði, endurbótum og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="c02c0-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="c02c0-139">Íhugaðu að endurmeta eignatengsl þitt með reglulegu millibili (til dæmis einu sinni á ári eða annað hvert ár) til að ganga úr skugga um að skilgreiningar á mikilvægi þínu samsvari núverandi framleiðsluuppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="c02c0-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
