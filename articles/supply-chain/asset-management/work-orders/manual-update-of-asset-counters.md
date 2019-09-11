---
title: Handvirk uppfærsla á eignateljurum
description: Þetta efni lýsir handvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875716"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="e5c49-103">Handvirk uppfærsla á eignateljurum</span><span class="sxs-lookup"><span data-stu-id="e5c49-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e5c49-104">Teljarar eru notaðir til að búa til skráningar á eign varðandi t.d. fjölda vinnustunda eða fjölda framleidds magns.</span><span class="sxs-lookup"><span data-stu-id="e5c49-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="e5c49-105">Ef teljaragerðin sem er valin fyrir teljara er stillt á að erfa teljaragildi (**Eignastjórnun** > **Uppsetning** > **Gerðir eigna** > **Teljarar** > **Almennt** flýtiflipa > skiptihnappurinn **Erfð teljaragildi eigna** stilltur á „Já“), þá er hver undireign sem notar sömu gerð teljara sjálfvirkt uppfærð þegar þú býrð til nýja teljaralínu af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="e5c49-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="e5c49-106">Í **Öllum eignum** stofnarðu teljaraskráningarnar klukkustundir eða magn á eign, byggt á lestri þínum af eigninni.</span><span class="sxs-lookup"><span data-stu-id="e5c49-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="e5c49-107">Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Eignir** > **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e5c49-108">Veldu eignina á listanum og smelltu á **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="e5c49-109">Í glugganum **Eignateljarar** sérðu lista yfir allar fyrri gagnaskráningar á valda eign.</span><span class="sxs-lookup"><span data-stu-id="e5c49-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="e5c49-110">Smelltu á **Nýtt** til að stofna nýja skráningu.</span><span class="sxs-lookup"><span data-stu-id="e5c49-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="e5c49-111">Auðkenni eignarinnar er sjálfkrafa sett inn.</span><span class="sxs-lookup"><span data-stu-id="e5c49-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="e5c49-112">Í reitinn **Teljari** skaltu velja viðeigandi teljara.</span><span class="sxs-lookup"><span data-stu-id="e5c49-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="e5c49-113">Aðeins teljarar sem tengjast eignategundinni sem valin er á eigninni eru tiltækir.</span><span class="sxs-lookup"><span data-stu-id="e5c49-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="e5c49-114">Tengda einingin er sjálfvirkt sett inn í reitinn **Eining**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="e5c49-115">Veldu dagsetningu og tíma fyrir teljaraskráningu.</span><span class="sxs-lookup"><span data-stu-id="e5c49-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="e5c49-116">Í reitinn **Gildi** skaltu setja inn töluna frá síðustu teljaraskráningu, eða, í reitinn **Uppsafnað gildi** skaltu setja inn heildarfjölda talningar.</span><span class="sxs-lookup"><span data-stu-id="e5c49-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="e5c49-117">Ef þú setur upp nýjan teljara á eign þarftu að skrá breytinguna á eignina í **Eignateljarar**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="e5c49-118">Næst verður þú að stofna tvær skráningarlínur með sömu tímastimplum og á línunni varðandi nýja teljarann velurðu gátreitinn **Endurstilling teljara**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="e5c49-119">Þegar þú býrð til skráningarlínurnar tvær verður fyrsta línan að vera fyrir teljarann sem þú ert að skipta um.</span><span class="sxs-lookup"><span data-stu-id="e5c49-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="e5c49-120">Í reitnum **Samtals** er heildartala talningar summan af samanlagðri talningu allra skráðra gilda á þeirri teljaragerð.</span><span class="sxs-lookup"><span data-stu-id="e5c49-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="e5c49-121">Ef gátreiturinn **Endurstilling teljara** er valinn á eign með viðhaldsáætlun með bilgerðinni „Einu sinni frá...“ eða „Einu sinni náð...“ er teljarinn enn virkur á nýju teljaralínunni því þú býrð til aðskilda teljaralínu og byrjar upp á nýtt með nýjum teljara.</span><span class="sxs-lookup"><span data-stu-id="e5c49-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Mynd 1](media/11-work-orders.png)


<span data-ttu-id="e5c49-123">Ef þú þarft að gera teljaraskráningar á nokkrum eignum er hægt að gera það í **Eignastjórnun** > **Fyrirspurnir** > **Eignir** > **Eignateljarar**.</span><span class="sxs-lookup"><span data-stu-id="e5c49-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="e5c49-124">Þú getur sett upp svið til að skilgreina frávik í handvirkum teljaraskráningum og gerð skilaboða sem á að birtast ef skráningar eru utan skilgreinds sviðs.</span><span class="sxs-lookup"><span data-stu-id="e5c49-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="e5c49-125">Sjá efnið [Teljarar](../setup-for-objects/counters.md) varðandi uppsetningu á tengdum teljurum.</span><span class="sxs-lookup"><span data-stu-id="e5c49-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
