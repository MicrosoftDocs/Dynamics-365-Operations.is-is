---
title: Handvirk uppfærsla á eignateljurum
description: Þetta efni lýsir handvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6dfea7ca166948f507a1cdea20f3e4cce16080ce
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219486"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="5465e-103">Handvirk uppfærsla á eignateljurum</span><span class="sxs-lookup"><span data-stu-id="5465e-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5465e-104">Teljarar eru notaðir til að búa til skráningar á eign, svo sem skráningar um fjölda klukkustunda sem eignin hefur verið starfrækt eða magnið sem hefur verið framleitt.</span><span class="sxs-lookup"><span data-stu-id="5465e-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="5465e-105">Teljarategundin sem er valin fyrir teljara gæti verið stillt á að erfa teljaragildi.</span><span class="sxs-lookup"><span data-stu-id="5465e-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="5465e-106">Með öðrum orðum er valkosturinn **Erfð teljaragildi eigna** stilltur á **Já** á flýtiflipanum **Almennt** á síðunni **Teljarar** (**Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**).</span><span class="sxs-lookup"><span data-stu-id="5465e-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="5465e-107">Í þessu tilfelli, þegar þú býrð til nýja teljaralínu af þeirri gerð, er hver undireign sem notar sömu teljarategund uppfærð sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="5465e-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="5465e-108">Á síðunni **Allar eignir** stofnarðu teljaraskráningarnar klukkustundir eða magn á eign, byggt á lestri þínum af eigninni.</span><span class="sxs-lookup"><span data-stu-id="5465e-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="5465e-109">Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="5465e-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="5465e-110">Veldu eignina og síðan, í aðgerðaglugganum, á flipanum **Eign**, í hópnum **Fyrirbyggjandi**, velurðu **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="5465e-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="5465e-111">Síðan **Eignateljarar** sýnir lista yfir allar fyrri gagnaskráningar sem hafa verið gerðar á valinni eign.</span><span class="sxs-lookup"><span data-stu-id="5465e-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="5465e-112">Veldu **Nýr** til að stofna skráningu.</span><span class="sxs-lookup"><span data-stu-id="5465e-112">Select **New** to create a registration.</span></span> <span data-ttu-id="5465e-113">Eignakennið er fært sjálfkrafa inn í reitinn **Eign**.</span><span class="sxs-lookup"><span data-stu-id="5465e-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="5465e-114">Í reitinn **Teljari** skaltu velja viðeigandi teljara.</span><span class="sxs-lookup"><span data-stu-id="5465e-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="5465e-115">Aðeins teljarar sem tengjast eignategundinni sem valin er á eigninni eru tiltækir til vals.</span><span class="sxs-lookup"><span data-stu-id="5465e-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="5465e-116">Tengda einingin er sjálfvirkt sett inn í reitinn **Eining**.</span><span class="sxs-lookup"><span data-stu-id="5465e-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="5465e-117">Í reitnum **Skráð** velurðu dagsetningu og tíma fyrir gagnaskráningu.</span><span class="sxs-lookup"><span data-stu-id="5465e-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="5465e-118">Í reitinn **Gildi** slærðu inn númerið frá síðustu gagnaskráningu.</span><span class="sxs-lookup"><span data-stu-id="5465e-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="5465e-119">Að öðrum kosti, í reitinn **Uppsafnað gildi** slærðu inn heildarfjölda tölu.</span><span class="sxs-lookup"><span data-stu-id="5465e-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="5465e-120">Athugið eftirfarandi stig:</span><span class="sxs-lookup"><span data-stu-id="5465e-120">Note the following points:</span></span>

- <span data-ttu-id="5465e-121">Ef þú setur upp nýjan teljara á eign verður að skrá breytingu á eigninni á síðunni **Eignateljarar**.</span><span class="sxs-lookup"><span data-stu-id="5465e-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="5465e-122">Næst verðurðu að búa til tvær skráningarlínur sem eru með eins tímastimpla.</span><span class="sxs-lookup"><span data-stu-id="5465e-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="5465e-123">Fyrsta línan verður að vera fyrir teljarann sem þú ert að skipta um.</span><span class="sxs-lookup"><span data-stu-id="5465e-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="5465e-124">Á línunni sem tengist nýja teljaranum velurðu gátreitinn **Endurstilling teljara**.</span><span class="sxs-lookup"><span data-stu-id="5465e-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="5465e-125">Í reitnum **Samtals** er heildartala talningar summan af samanlagðri talningu allra skráðra gilda á þeirri teljaragerð.</span><span class="sxs-lookup"><span data-stu-id="5465e-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="5465e-126">Ef gátreiturinn **Endurstilling teljara** er valinn á eign með viðhaldsáætlun sem hefur bilgerðina „Einu sinni frá...“ eða „Einu sinni náð...“ er teljarinn enn virkur á nýju teljaralínunni því þú býrð til aðskilda teljaralínu og byrjar upp á nýtt með nýjum teljara.</span><span class="sxs-lookup"><span data-stu-id="5465e-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="5465e-127">Myndin hér að neðan sýnir dæmi um síðuna **Eignateljarar**.</span><span class="sxs-lookup"><span data-stu-id="5465e-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Mynd 1](media/11-work-orders.png)

<span data-ttu-id="5465e-129">Á síðunni **Eignateljarar** (**Eignastýring** > **Fyrirspurnir** > **Eignir** > **Eignateljarar**) er hægt að gera gagnaskráningar á nokkrum eignum í einu, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5465e-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="5465e-130">Þú getur sett upp svið til að skilgreina frávik í handvirkum gagnaskráningum.</span><span class="sxs-lookup"><span data-stu-id="5465e-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="5465e-131">Þú getur einnig tilgreint hvaða skilaboð birtast ef skráningar eru utan skilgreinds sviðs.</span><span class="sxs-lookup"><span data-stu-id="5465e-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="5465e-132">Nánari upplýsingar um hvernig setja skal upp teljara er að finna í [Teljarar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5465e-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]