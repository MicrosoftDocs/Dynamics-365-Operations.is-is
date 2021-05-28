---
title: Breyta eða endurúthluta fjárhagsdagatali
description: Þetta efnisatriði útskýrir hvernig á að breyta dagatalinu sem nú er úthlutað í fjárhag og hvernig á að úthluta nýju dagatali í fjárhag.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039951"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="f69f6-103">Breyta eða endurúthluta fjárhagsdagatali</span><span class="sxs-lookup"><span data-stu-id="f69f6-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f69f6-104">Þetta efnisatriði útskýrir hvernig á að breyta dagatalinu sem nú er úthlutað í fjárhag og hvernig á að úthluta nýju dagatali í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="f69f6-105">Gefa út</span><span class="sxs-lookup"><span data-stu-id="f69f6-105">Issue</span></span>

<span data-ttu-id="f69f6-106">Stundum verða fyrirtæki annaðhvort að breyta núverandi dagatali sem er úthlutað í fjárhag eða úthluta nýju dagatali.</span><span class="sxs-lookup"><span data-stu-id="f69f6-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="f69f6-107">Lausn</span><span class="sxs-lookup"><span data-stu-id="f69f6-107">Resolution</span></span>

<span data-ttu-id="f69f6-108">Tvær aðstæður eru til staðar þar sem nauðsynlegt gæti verið að breyta eða endurúthluta fjárhagsdagatali.</span><span class="sxs-lookup"><span data-stu-id="f69f6-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="f69f6-109">Fyrri felur í sér að breyta fyrirliggjandi dagatali sem þegar hefur verið úthlutað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="f69f6-110">Annað felur í sér að búa til nýtt dagatal og úthluta því í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="f69f6-111">Hægt er að gera báðar breytingarnar hvenær sem er, jafnvel eftir að færslur hafa verið bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="f69f6-112">Breyta fyrirliggjandi fjárhagsdagatali</span><span class="sxs-lookup"><span data-stu-id="f69f6-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="f69f6-113">Til að breyta fyrirliggjandi dagatali sem er úthlutað í fjárhag skaltu fara í **Fjárhagur \> Uppsetning fjárhags \> Fjárhagur** og velja tengilinn fyrir fjárhagsdagatalið til að opna síðuna **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="f69f6-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="f69f6-114">Takmarkanir eru á því hverju er hægt að breyta í dagatali.</span><span class="sxs-lookup"><span data-stu-id="f69f6-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="f69f6-115">Það er til dæmis hægt að breyta upphafs- og lokadegi *tímabilanna* á ári en ekki upphafs- og lokadegi *árs* í dagatalinu.</span><span class="sxs-lookup"><span data-stu-id="f69f6-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="f69f6-116">Til að breyta tímabilum árs skal velja viðeigandi dagatal og ár.</span><span class="sxs-lookup"><span data-stu-id="f69f6-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="f69f6-117">Fyrst skaltu nota hnappinn **Eyða tímabili** til að eyða sumum eða öllum núverandi rekstrartímabilum.</span><span class="sxs-lookup"><span data-stu-id="f69f6-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="f69f6-118">Hægt er að eyða öllum rekstrartímabilum nema því fyrsta.</span><span class="sxs-lookup"><span data-stu-id="f69f6-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="f69f6-119">Notaðu síðan hnappinn **Skipta tímabili** til að skipta eftirstöðvum tímabila í ný tímabil með því að slá inn viðeigandi upphafsdag fyrir næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="f69f6-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="f69f6-120">Þegar þú breytir tímabilunum í dagatali verður þú að keyra ferlið **Endurreikna fjárhagstímabil** í öllum lögaðilum (fyrirtækjum) þar sem dagatalinu er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="f69f6-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="f69f6-121">Þrátt fyrir að engin viðvörunarskilaboð minni þig á að ljúka þessu skrefi er endurútreikningsferlið nauðsynlegt til að uppfæra tímabilið sem er úthlutað fyrir hverja færslu sem er bókuð í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="f69f6-122">Til að keyra endurútreikningsferlið velur þú **Endurreikna fjárhagstímabil** á síðunni **Fjárhagsuppsetning** í hverju fyrirtæki fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="f69f6-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="f69f6-123">Ef endurútreikningsferlið er ekki keyrt gætu færslustöður í prófjöfnuði eða fjárhagsskýrslum verið ranglega hafðar með í tímabilum.</span><span class="sxs-lookup"><span data-stu-id="f69f6-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="f69f6-124">Í þessu tilfelli er hægt að leiðrétta stöðurnar hvenær sem er með því að keyra endurútreikningsferlið.</span><span class="sxs-lookup"><span data-stu-id="f69f6-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="f69f6-125">Úthluta nýju fjárhagsdagatali</span><span class="sxs-lookup"><span data-stu-id="f69f6-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="f69f6-126">Til að úthluta nýju fjárhagsdagatali skal opna **Fjárhagur \> Fjárhagsuppsetning \> Fjárhagur** og velja **Breyta** til að færa síðu **Fjárhags** yfir í breytingastillingu.</span><span class="sxs-lookup"><span data-stu-id="f69f6-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="f69f6-127">Því næst skal velja nýtt fjárhagsdagatal í reitnum **Fjárhagsdagatal**.</span><span class="sxs-lookup"><span data-stu-id="f69f6-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="f69f6-128">Þegar þú breytir fjárhagsdagatalinu fyrir fjárhag þarftu að keyra **Endurreikna fjárhagstímabil**.</span><span class="sxs-lookup"><span data-stu-id="f69f6-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="f69f6-129">Þegar þú úthlutar nýju fjárhagsdagatali í bókhald birtast skilaboð sem minna þig á að ljúka þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="f69f6-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="f69f6-130">Þó að skilaboðin virðist benda til þess að endurútreikningsferlið sé valfrjálst er það ekki svo.</span><span class="sxs-lookup"><span data-stu-id="f69f6-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="f69f6-131">Það þarf að uppfæra tímabilið sem er úthlutað fyrir hverja færslu sem er bókuð í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f69f6-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="f69f6-132">Til að keyra endurútreikningsferlið velur þú **Endurreikna fjárhagstímabil** á síðunni **Fjárhagsuppsetning**.</span><span class="sxs-lookup"><span data-stu-id="f69f6-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="f69f6-133">Ef endurútreikningsferlið er ekki keyrt gætu færslustöður í prófjöfnuði eða fjárhagsskýrslum verið ranglega hafðar með í tímabilum.</span><span class="sxs-lookup"><span data-stu-id="f69f6-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="f69f6-134">Í þessu tilfelli er hægt að leiðrétta stöðurnar hvenær sem er með því að keyra endurútreikningsferlið.</span><span class="sxs-lookup"><span data-stu-id="f69f6-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
