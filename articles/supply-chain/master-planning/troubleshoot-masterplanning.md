---
title: Úrræðaleit fyrir aðaláætlanagerð
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með aðaláætlanagerð.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216106"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="dc2c2-103">Úrræðaleit fyrir aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="dc2c2-103">Troubleshoot master planning</span></span>

<span data-ttu-id="dc2c2-104">Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="dc2c2-105">Niðurbrot uppskriftar hegðar sér á annan hátt fyrir staðfestar framleiðslupantanir og fyrir áætlaðar framleiðslupantanir fyrir vinnu sem er búið að stofna handvirkt.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dc2c2-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dc2c2-106">Issue description</span></span>

<span data-ttu-id="dc2c2-107">Þegar framleiðslupöntun er staðfest eru vörurnar ekki brotnar niður þegar þú brýtur uppskriftirnar niður.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="dc2c2-108">Hins vegar þegar þú stofnar verkbeiðni handvirkt og áætlar síðan framleiðslupöntunina eru vörurnar brotnar niður.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dc2c2-109">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dc2c2-109">Issue resolution</span></span>

<span data-ttu-id="dc2c2-110">Kerfið virkar eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-110">The system is working as expected.</span></span> <span data-ttu-id="dc2c2-111">Niðurbrotið sem verður þegar framleiðslupöntunin er staðfest vísar á áætlaða pöntun en áætlaða pöntunin virðist ekki vera staðfest í þessu tilviki.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="dc2c2-112">Ef framleiðslupöntunin hefur hins vegar verið metin er niðurbrotið ræst af útgefnu framleiðslupöntuninni þegar engin áætluð pöntun er til staðar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="dc2c2-113">Seinkunargildið er ekki uppfært þegar ég enduráætla áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="dc2c2-114">Til að uppfæra seinkun á áætluðum pöntunum skal opna svargluggann **Endurröðun** fyrir áætluðu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="dc2c2-115">Á flýtiflipanum **Niðurbrot** skal ganga úr skugga um að **Framkvæma niðurbrot eftir að endurröðunarvalkosturinn** er stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="dc2c2-116">Framleiðsluröðun tekur ekki til greina öryggismörk sem eru stillt á vöruþekju fyrir fest framboð.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dc2c2-117">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dc2c2-117">Issue description</span></span>

<span data-ttu-id="dc2c2-118">Aðaláætlanagerð áætlar öryggismörk.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="dc2c2-119">Hins vegar eru öryggismörk hunsuð um leið og áætlaðar framleiðslupantanir eru áætlaðar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dc2c2-120">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dc2c2-120">Issue resolution</span></span>

<span data-ttu-id="dc2c2-121">Aðeins er tekið tillit til marka við aðaláætlanagerð, ekki við handvirka áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="dc2c2-122">Mörk eiga að gegna hlutverki biðminnis við áætlunarferlið til að setja tiltekin „mörk“ fyrir raunverulega ferlið.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="dc2c2-123">Til að fá æskilega útkomu er hægt að fjarlægja framlegðina.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="dc2c2-124">Síðan verður að uppfæra leiðina þannig að hún innihaldi tímann sem óskað er eftir (til dæmis, sem biðtími).</span><span class="sxs-lookup"><span data-stu-id="dc2c2-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="dc2c2-125">Bæði aðaláætlanagerð og handvirk röðun ættu þá að búa til sömu niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="dc2c2-126">Áætlaðar pantanir eru myndaðar þrátt fyrir að vörur séu á lager og framleiðslupantanir séu þegar til fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="dc2c2-127">Hugsanlega er hægt að laga vandamálið með því að auka gildið **Jákvæðir dagar** fyrir viðeigandi flokka á síðunni **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="dc2c2-128">Þessi breyting veldur því að kerfið ákveður hvort hægt er að nota lagerbirgðir til að anna eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="dc2c2-129">Þá verður ný áætluð pöntun ekki mynduð fyrir vörurnar sem eru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="dc2c2-130">Aðaláætlanagerð virðist ekki taka mið af takmörkunum afkastagetu og áætlar meira en tiltæk afkastageta.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dc2c2-131">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dc2c2-131">Issue description</span></span>

<span data-ttu-id="dc2c2-132">Þegar aðgerðaröðun er notuð þar sem takmörkuð afkastageta er til staðar og leiðin tilgreinir blöndu af kröfum bæði tilfangaflokks og einstakra tilfanga er möguleiki á ofbókun vegna aðferðarinnar sem algrím notar til að villuleita árekstra í afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="dc2c2-133">Þessi ofbókun getur átt sér stað þegar hjálpartæki eru notuð til að keyra aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="dc2c2-134">Líklegra er að slíkt hendi þegar mörg verk með hlutfallslega stutta keyrslu eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dc2c2-135">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dc2c2-135">Issue resolution</span></span>

<span data-ttu-id="dc2c2-136">Þegar nauðsynlegt að engin ofbókun eigi sér stað við aðgerðaröðun er hægt að gera áætlanahluta aðaláætlanagerðarinnar að stökum þræði með því að kveikja á valkostinum **Nákvæm takmörkuð geta fyrir aðgerðaröðun** á síðunni **Færibreytur aðaláætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="dc2c2-137">Þessi valkostur er ekki tiltækur sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-137">This option isn't available by default.</span></span> <span data-ttu-id="dc2c2-138">Þú verður að bæta henni handvirkt við síðuna með því að nota sérstillingar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="dc2c2-139">Þegar þessi valkostur er notaður verður áætlanagerð keyrð hægar því samhliða keyrsla er ekki til staðar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="dc2c2-140">Það tekur langan tíma að uppfæra áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dc2c2-141">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dc2c2-141">Issue description</span></span>

<span data-ttu-id="dc2c2-142">Þegar þarfamagn og/eða afhendingardagsetning áætlaðrar pöntunar er uppfært tekur a.m.k. 30 sekúndur að vista uppfærsluna á pöntun.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dc2c2-143">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dc2c2-143">Issue resolution</span></span>

<span data-ttu-id="dc2c2-144">Þetta er þekkt vandamál með innbyggðri aðaláætlunarvél.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="dc2c2-145">Slíkt stafar af undirliggjandi, sjálfvirku niðurbroti í skipulagi uppskriftarinnar á meðan breytingar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="dc2c2-146">Slíkt vandamál er leyst með fínstillingu skipulagningar, þar sem áætlun getur uppfært og samþykkt viðeigandi pantanir og þegar þess er óskað, keyrt uppfærslu áætlaðra pantana fyrir undirliggjandi skipan uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="dc2c2-147">Ein leið til að auka afköst með innbyggðri aðaláætlunarvél er að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="dc2c2-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="dc2c2-148">Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="dc2c2-149">Velja áætlun.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-149">Select a plan.</span></span>
1. <span data-ttu-id="dc2c2-150">Víkka út flipann **Tímamörk í dögum**.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="dc2c2-151">Stilltu **Niðurbrot** á *Já* og stilltu svæðið fyrir neðan þessa stillingu á 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="dc2c2-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="dc2c2-152">Slíkt takmarkar framkvæmdartímabil niðurbrota fyrir þessa aðaláætlun við einn dag.</span><span class="sxs-lookup"><span data-stu-id="dc2c2-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]