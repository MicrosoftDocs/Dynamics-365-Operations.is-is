---
title: Setja upp æskilega viðhaldsstarfskrafta
description: Þetta efni útskýrir hvernig á að setja upp forgangsviðhaldsstarfskrafta í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887412"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="e18f5-103">Æskilegir viðhaldsstarfskraftar</span><span class="sxs-lookup"><span data-stu-id="e18f5-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e18f5-104">Þú getur stofnað forgang varðandi hvaða viðhaldsstarfsmönnum er úthlutað til að ljúka verkbeiðnum við tímasetningu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e18f5-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="e18f5-105">Notkun þessarar virkni er valkvæð, en hún getur hjálpað þér að velja fyrir hæfasta viðhaldsstarfsmanninn til að ljúka verki, byggt á færni og hæfni starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e18f5-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="e18f5-106">Þess vegna er uppsetningin í **Forgangsstarfsmenn viðhalds** í verkbeiðniáætlun notuð til að ákvarða hvort tiltekinn viðhaldsstarfsmaður eða starfsmannahópur skuli áætlaðir fyrir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e18f5-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="e18f5-107">Aðeins viðhaldsstarfsmenn sem eru tiltækir, þegar áætlun er gerð, verða áætlaðir.</span><span class="sxs-lookup"><span data-stu-id="e18f5-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="e18f5-108">Ef valin uppsetning viðhaldsstarfsmanna passar við verkbeiðni við tímasetningu, en viðhaldsstarfsmanni er úthlutað til annarra starfa, verður verkbeiðnin áætluð fyrir annan tiltækan viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="e18f5-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="e18f5-109">Áður en þú getur sett upp forgangsstarfsmenn viðhalds verður þú fyrst að setja upp viðhaldsstarfsmenn og hópa starfsmanna viðhalds sem ættu að vera tiltækir fyrir val.</span><span class="sxs-lookup"><span data-stu-id="e18f5-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="e18f5-110">Sjá [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) fyrir lýsingu á hvernig setja skuli upp viðhaldsstarfsmenn og starfsmannahópa.</span><span class="sxs-lookup"><span data-stu-id="e18f5-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="e18f5-111">Setja upp forgangsstarfskrafta</span><span class="sxs-lookup"><span data-stu-id="e18f5-111">Set up preferred workers</span></span>

<span data-ttu-id="e18f5-112">Forgangsviðhaldsstarfsmaður eða starfsmannahópur getur verið skyldur tilteknum</span><span class="sxs-lookup"><span data-stu-id="e18f5-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="e18f5-113">Viðskipti</span><span class="sxs-lookup"><span data-stu-id="e18f5-113">trade</span></span>  
- <span data-ttu-id="e18f5-114">afbrigði viðhaldsverkgerðar</span><span class="sxs-lookup"><span data-stu-id="e18f5-114">maintenance job type variant</span></span>  
- <span data-ttu-id="e18f5-115">gerð viðhaldsverks</span><span class="sxs-lookup"><span data-stu-id="e18f5-115">maintenance job type</span></span>  
- <span data-ttu-id="e18f5-116">tegund viðhaldsverkgerðar</span><span class="sxs-lookup"><span data-stu-id="e18f5-116">maintenance job type category</span></span>  
- <span data-ttu-id="e18f5-117">fastafjármunur</span><span class="sxs-lookup"><span data-stu-id="e18f5-117">asset</span></span>  
- <span data-ttu-id="e18f5-118">gerð eignar</span><span class="sxs-lookup"><span data-stu-id="e18f5-118">asset type</span></span>  

<span data-ttu-id="e18f5-119">eða sambland af þessum valkostum.</span><span class="sxs-lookup"><span data-stu-id="e18f5-119">or a combination of those selections.</span></span> <span data-ttu-id="e18f5-120">Því meira val sem þú gerir fyrir sömu skrá, því nákvæmari verður uppsetningin.</span><span class="sxs-lookup"><span data-stu-id="e18f5-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="e18f5-121">Smelltu á **Eignastjórnun** > **Uppsetning** > **Starfskraftar** > **Forgangstarfsmenn viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="e18f5-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="e18f5-122">Smelltu á **Nýtt** til að stofna nýja færslu.</span><span class="sxs-lookup"><span data-stu-id="e18f5-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="e18f5-123">Byrjaðu á því að búa til „sjálfgefinn“ viðhaldsmann eða starfsmannahópsuppsetningu sem hefur engin val í reitunum sem sýndir eru í áherslulistanum hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="e18f5-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="e18f5-124">Þetta þýðir að þú gerir aðeins val í reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="e18f5-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="e18f5-125">Á myndinni hér að neðan sérðu dæmi í fyrstu skránni þar sem „Beiðnir“ eru valdar sem valinn hópur starfsmanna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="e18f5-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="e18f5-126">Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar við tímasetningu verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="e18f5-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="e18f5-127">Endurtaktu skref 2 til að stofna nýja færslu.</span><span class="sxs-lookup"><span data-stu-id="e18f5-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="e18f5-128">Taktu nauðsynlegar ákvarðanir, eftir því smáatriðastigi fyrir valinn starfsmann eða starfsmannahóp.</span><span class="sxs-lookup"><span data-stu-id="e18f5-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="e18f5-129">*Dæmi:* Á myndinni hér að neðan, í sjöttu skránni, er viðhaldsstarfsmaðurinn Shawn Richardson valinn valinn starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="e18f5-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="e18f5-130">Hann verður sjálfkrafa valinn við tímasetningu verkbeiðni sem felur í sér eignina „CH-BP1-03-02 og viðhaldsvinnutegundin„ Aðstöðumat “, ef hann er tiltækur á tilsettum tíma.</span><span class="sxs-lookup"><span data-stu-id="e18f5-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="e18f5-131">Almennt þegar valinn viðhaldsstarfsmaður er valinn meðan á tímasetningu vinnu stendur fer eignastýring í gegnum allar **Forgangsstarfsmenn viðhalds** skrár til að leita að mögulegri samsvörun, athugaðu alltaf sérstaka samsetningu fyrst.</span><span class="sxs-lookup"><span data-stu-id="e18f5-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="e18f5-132">Ef engin samsvörun er að finna, er „sjálfgefna“ skráin með valinu í annaðhvort reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds** notuð.</span><span class="sxs-lookup"><span data-stu-id="e18f5-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Mynd 1](media/02-work-order-scheduling.png)

<span data-ttu-id="e18f5-134">Þú getur líka sett upp ábyrga viðhaldsstarfsmenn sem hægt er að velja þegar viðhaldsbeiðni eða verkbeiðni er búin til.</span><span class="sxs-lookup"><span data-stu-id="e18f5-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="e18f5-135">Í **Öllum verkbeiðnum** og **Öllum viðhaldsbeiðnum** er hægt að breyta valinu, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="e18f5-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="e18f5-136">Sjá [Ábyrgir viðhaldsstarfsmenn](../setup-for-maintenance-requests/responsible-workers.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e18f5-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="e18f5-137">Við tímatökuáætlun verkbeiðni eru mismunandi stig reiknuð út til að ákvarða hvaða starfsmenn ættu að ljúka störfum sem tengjast verkbeiðni (þessi stig eru sett upp í tenglinum **Færibreytur eignastýringar** > **Tímasetningar verkbeiðni**).</span><span class="sxs-lookup"><span data-stu-id="e18f5-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="e18f5-138">Ef tveir eða fleiri forgangsviðhaldsstarfsmenn eða ábyrgir starfsmenn við viðhald fá sömu einkunn við tímasetningu verkbeiðni er einn starfsmaður valinn af handahófi.</span><span class="sxs-lookup"><span data-stu-id="e18f5-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="e18f5-139">Annars er það alltaf starfsmaðurinn með hæstu einkunn sem er úthlutað til að ljúka verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e18f5-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

