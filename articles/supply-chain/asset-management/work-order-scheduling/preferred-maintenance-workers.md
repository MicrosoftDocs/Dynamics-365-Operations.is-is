---
title: Setja upp æskilega viðhaldsstarfskrafta
description: Þetta efni útskýrir hvernig á að setja upp forgangsviðhaldsstarfskrafta í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ab36d9fde0cc6e864f21f9ebd09834f5098c1913
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021405"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="80c07-103">Setja upp æskilega viðhaldsstarfskrafta</span><span class="sxs-lookup"><span data-stu-id="80c07-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="80c07-104">Við tímasetningu verkbeiðni er hægt að stofna forgang varðandi hvaða viðhaldsstarfsmanni eða starfsmannahóp er úthlutað til að ljúka verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="80c07-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="80c07-105">Notkun þessarar virkni er valkvæð, en hún getur hjálpað þér að velja fyrir hæfasta viðhaldsstarfsmanninn til að ljúka verki, byggt á færni og hæfni starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="80c07-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="80c07-106">Aðeins viðhaldsstarfsmenn sem eru tiltækir, þegar áætlun er gerð, verða áætlaðir.</span><span class="sxs-lookup"><span data-stu-id="80c07-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="80c07-107">Ef valin uppsetning viðhaldsstarfsmanna passar við verkbeiðni við tímasetningu, en viðhaldsstarfsmanni er úthlutað til annarra starfa, verður verkbeiðnin áætluð fyrir annan tiltækan viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="80c07-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="80c07-108">Áður en þú getur sett upp valda viðhaldsstarfsmenn verður þú fyrst að setja upp viðhaldsstarfsmenn og starfsmannahópa.</span><span class="sxs-lookup"><span data-stu-id="80c07-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="80c07-109">Fyrir lýsingu á hvernig setja skuli upp viðhaldsstarfsmenn og starfsmannahópa skals sjá [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="80c07-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="80c07-110">Setja upp forgangsstarfskrafta</span><span class="sxs-lookup"><span data-stu-id="80c07-110">Set up preferred workers</span></span>

<span data-ttu-id="80c07-111">Forgangsviðhaldsstarfsmaður eða starfsmannahópur getur verið skyldur einum eða fleiri af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="80c07-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="80c07-112">Viðskipti</span><span class="sxs-lookup"><span data-stu-id="80c07-112">trade</span></span>  
- <span data-ttu-id="80c07-113">afbrigði viðhaldsverkgerðar</span><span class="sxs-lookup"><span data-stu-id="80c07-113">maintenance job type variant</span></span>  
- <span data-ttu-id="80c07-114">gerð viðhaldsverks</span><span class="sxs-lookup"><span data-stu-id="80c07-114">maintenance job type</span></span>  
- <span data-ttu-id="80c07-115">tegund viðhaldsverkgerðar</span><span class="sxs-lookup"><span data-stu-id="80c07-115">maintenance job type category</span></span>  
- <span data-ttu-id="80c07-116">fastafjármunur</span><span class="sxs-lookup"><span data-stu-id="80c07-116">asset</span></span>  
- <span data-ttu-id="80c07-117">gerð eignar</span><span class="sxs-lookup"><span data-stu-id="80c07-117">asset type</span></span>  

<span data-ttu-id="80c07-118">Því meira val sem þú gerir fyrir sömu skrá, því nákvæmari verður uppsetningin.</span><span class="sxs-lookup"><span data-stu-id="80c07-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="80c07-119">Smelltu á **Eignastjórnun** > **Uppsetning** > **Starfskraftar** > **Forgangstarfsmenn viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="80c07-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="80c07-120">Smelltu á **Nýtt** til að stofna nýja færslu.</span><span class="sxs-lookup"><span data-stu-id="80c07-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="80c07-121">Byrjaðu á því að búa til „sjálfgefinn“ viðhaldsstarfsmann eða starfsmannahóp.</span><span class="sxs-lookup"><span data-stu-id="80c07-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="80c07-122">Þetta þýðir að þú gerir aðeins val í reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="80c07-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="80c07-123">Á skjámyndinni hér að neðan sérðu dæmi í fyrstu skránni þar sem „Beiðnir“ eru valdar sem **Valinn hópur starfsmanna viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="80c07-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="80c07-124">Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="80c07-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="80c07-125">Endurtaktu skref 2 til að stofna nýja færslu.</span><span class="sxs-lookup"><span data-stu-id="80c07-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="80c07-126">Taktu nauðsynlegar ákvarðanir, eftir því smáatriðastigi fyrir valinn starfsmann eða starfsmannahóp.</span><span class="sxs-lookup"><span data-stu-id="80c07-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="80c07-127">*Dæmi:* Á skjámyndinni hér að neðan, í sjöttu skránni, er viðhaldsstarfsmaðurinn Shawn Richardson valinn valinn starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="80c07-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="80c07-128">Hann verður sjálfkrafa valinn við tímasetningu verkbeiðni sem felur í sér eignina „CH-BP1-03-02 og gerð viðhaldsverks „Aðstöðumat“, ef hann er tiltækur á tilsettum tíma.</span><span class="sxs-lookup"><span data-stu-id="80c07-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="80c07-129">Almennt þegar valinn viðhaldsstarfsmaður er valinn meðan á tímasetningu vinnu stendur fer eignastýring í gegnum allar **Forgangsstarfsmenn viðhalds** skrár til að leita að mögulegri samsvörun, athugaðu alltaf sérstaka samsetningu fyrst.</span><span class="sxs-lookup"><span data-stu-id="80c07-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="80c07-130">Ef engin samsvörun er að finna, er „sjálfgefna“ skráin með valinu í annaðhvort reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds** notuð.</span><span class="sxs-lookup"><span data-stu-id="80c07-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Mynd 1](media/02-work-order-scheduling.png)

<span data-ttu-id="80c07-132">Þú getur líka sett upp *ábyrga* viðhaldsstarfsmenn sem hægt er að velja þegar viðhaldsbeiðni eða verkbeiðni er búin til.</span><span class="sxs-lookup"><span data-stu-id="80c07-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="80c07-133">Hægt er að breyta valinu í **Öllum verkbeiðnum** og **Öllum viðhaldsbeiðnum**, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="80c07-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="80c07-134">Nánari upplýsingar er að finna í [Ábyrgir viðhaldsstarfsmenn](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="80c07-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="80c07-135">Við tímatökuáætlun verkbeiðni eru mismunandi stig reiknuð út til að ákvarða hvaða starfsmenn ættu að ljúka störfum sem tengjast verkbeiðni (þessi stig eru sett upp í tenglinum **Færibreytur eignastýringar** > **Tímasetningar verkbeiðni**).</span><span class="sxs-lookup"><span data-stu-id="80c07-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="80c07-136">Ef tveir eða fleiri forgangsviðhaldsstarfsmenn eða ábyrgir starfsmenn við viðhald fá sömu einkunn við tímasetningu verkbeiðni er einn starfsmaður valinn af handahófi.</span><span class="sxs-lookup"><span data-stu-id="80c07-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="80c07-137">Annars er það alltaf starfsmaðurinn með hæstu einkunn sem er úthlutað til að ljúka verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="80c07-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

