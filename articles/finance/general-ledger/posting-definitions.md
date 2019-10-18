---
title: Bókunarskilgreiningar
description: Þessi grein veitir upplýsingar um bókunarskilgreiningar og hvernig skuli skilgreina þær og búa til tengla í. Fyrir studdar bókunargerðir og skjöl, er hægt að nota bókunarskilgreiningar í stað bókunarreglur til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76bae24a975c922ea49ee2584e87cf43ccca61c7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178233"
---
# <a name="posting-definitions"></a><span data-ttu-id="20e02-104">Bókunarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="20e02-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20e02-105">Þessi grein veitir upplýsingar um bókunarskilgreiningar og hvernig skuli skilgreina þær og búa til tengla í.</span><span class="sxs-lookup"><span data-stu-id="20e02-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="20e02-106">Fyrir studdar bókunargerðir og skjöl, er hægt að nota bókunarskilgreiningar í stað bókunarreglur til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur.</span><span class="sxs-lookup"><span data-stu-id="20e02-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="20e02-107">Hægt er að skoða skjöl og gerðir bókana á í **bókunarskilgreiningar Færslna** síðu.</span><span class="sxs-lookup"><span data-stu-id="20e02-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="20e02-108">Til að byrja að nota bókunarskilgreiningar, í **Nota bókunarskilgreiningar** valkostinn á í **fjárhagsfæribreytur** síðu.</span><span class="sxs-lookup"><span data-stu-id="20e02-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="20e02-109">Jafnvel þegar nota bókunarskilgreiningar, enn þarf að skilgreina bókunarreglur fyrir upphaflegar færslur og ekki studdar bókunargerðir og skjöl.</span><span class="sxs-lookup"><span data-stu-id="20e02-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="20e02-110">Þú verður að nota Bókunarskilgreiningar til að styðja bókhald fjárúthlutunar innkaupapantana og áætlaða fjárúthlutun fyrir innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="20e02-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="20e02-111">Skilgreina Bókunarskilgreining</span><span class="sxs-lookup"><span data-stu-id="20e02-111">Defining posting definitions</span></span>
<span data-ttu-id="20e02-112">Nota skal **Bókunarskilgreiningar** síðu til að tilgreina skilyrði jöfnunar og færslur sem á að mynda þegar samsvörun verður.</span><span class="sxs-lookup"><span data-stu-id="20e02-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="20e02-113">Samsvörunarskilyrði eru metnar fyrir upphaflegar færslur og dreifingar á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="20e02-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="20e02-114">Á **Bókunarskilgreiningar** síðu má einnig tengja forgangstölur á línur til að stýra röðinni sem línurnar eru metnar í.</span><span class="sxs-lookup"><span data-stu-id="20e02-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="20e02-115">Línur sem hafa lægsta forgangsnúmer eru metnar fyrst.</span><span class="sxs-lookup"><span data-stu-id="20e02-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="20e02-116">Til dæmis allar línur sem hafa forgang 1 eru metin og síðan línur sem hafa forgang yfir 2 o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="20e02-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="20e02-117">Þegar samsvörun finnst eru önnur skilyrði fyrir samsvörun hunsuð.</span><span class="sxs-lookup"><span data-stu-id="20e02-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="20e02-118">Þar að auki, Einnig geta aðeins skilyrði í flokknum sem samsvara upprunalegu færslunni stofna myndaðrar færslur.</span><span class="sxs-lookup"><span data-stu-id="20e02-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="20e02-119">Hægt er að villuleita bókunarskilgreiningar með í **Prófa bókunarskilgreining** leiðsagnarforritið.</span><span class="sxs-lookup"><span data-stu-id="20e02-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="20e02-120">Þegar búið er að skilgreina dæmi um upprunafærslu bókunarskilgreiningar , sérðu myndaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="20e02-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="20e02-121">Hægt er að nota útgáfur bókunarskilgreiningar með gildisdagsetningum.</span><span class="sxs-lookup"><span data-stu-id="20e02-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="20e02-122">Til dæmis er hægt að stofna síðari útgáfum af bókunarskilgreiningu til að bóka í annan fjárhagslykil í nýtt fjárhagsár.</span><span class="sxs-lookup"><span data-stu-id="20e02-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="20e02-123">Nota skal **bókunarskilgreiningar Færslna** síðu til að tengja bókunarskilgreiningar við færslugerðir.</span><span class="sxs-lookup"><span data-stu-id="20e02-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="20e02-124">Tenging Bókunarskilgreininga</span><span class="sxs-lookup"><span data-stu-id="20e02-124">Linking posting definitions</span></span>
<span data-ttu-id="20e02-125">Hægt er að tengja úr einni bókunarskilgreiningu til annarar þegar bókunarskilgreiningar eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="20e02-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="20e02-126">Skilyrði fyrir skilgreiningu sem er tengd eru tekin til greina auk skilyrði fyrir núverandi bókunarskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="20e02-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="20e02-127">Þessi eiginleiki auðveldar að spara tíma, því ekki þarf að færa aftur inn skilyrði á **Færslur** flýtiflipi á í **Bókunarskilgreiningar** síðunni fyrir núverandi bókunarskilgreiningu ef þegar er færður inn þessar línur fyrir aðra skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="20e02-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="20e02-128">Taka með alla tengla í skýringarmyndu eða töflum sem væri að nota.</span><span class="sxs-lookup"><span data-stu-id="20e02-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="20e02-129">Til að forðast árekstra með núverandi bókunarskilgreiningu, ganga úr skugga um að línurnar í hverri bókunarskilgreiningar sem tengt er í séu einkvæmir.</span><span class="sxs-lookup"><span data-stu-id="20e02-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="20e02-130">Eftirfarandi takmarkanir eiga við þegar stofnaðir eru tengla í bókunarskilgreiningar:</span><span class="sxs-lookup"><span data-stu-id="20e02-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="20e02-131">Tiltekið bókunarskilgreiningu getur annað hvort tengja aðra bókunarskilgreiningu eða tengja úr aðra bókunarskilgreiningu, en ekki bæði.</span><span class="sxs-lookup"><span data-stu-id="20e02-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="20e02-132">Hins vegar getur bókunarskilgreiningu tengja margar bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="20e02-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="20e02-133">Hægt er að setja upp tengla aðeins milli bókunarskilgreiningar sem eru í sömu einingunni.</span><span class="sxs-lookup"><span data-stu-id="20e02-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="20e02-134">Hægt er að úthluta bókunarskilgreiningu á hvaða færslugerð sem er, en færslugerð verður að vera í sömu einingunni og bókunarskilgreiningin.</span><span class="sxs-lookup"><span data-stu-id="20e02-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="20e02-135">Nota skal **bókunarskilgreiningar Færslna** síðu til að sjá af hvaða tegund færsla er í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="20e02-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="20e02-136">Frekari upplýsingar eru í [Dæmi um bókunarskilgreiningar](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="20e02-136">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


