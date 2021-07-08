---
title: Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði lýsir því hvernig vinnuálag framkvæmdar framleiðslu starfar með kvörðunareiningum skýja og jaðra.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1e2006c0d9b9effe331a644aaaa9fa33ff2fb7c
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270536"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="e1163-103">Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra</span><span class="sxs-lookup"><span data-stu-id="e1163-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]

> [!WARNING]
> <span data-ttu-id="e1163-104">Vinnuálag framkvæmd framleiðslu er í forskoðun eins og er.</span><span class="sxs-lookup"><span data-stu-id="e1163-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="e1163-105">Tiltekin virkni fyrirtækisins er ekki studd að fullu í almennu forskoðuninni þegar kvörðunareiningar skýja og jaðra eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="e1163-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="e1163-106">Í framkvæmd framleiðslu bjóða einingarkvarðar upp á eftirfarandi möguleika:</span><span class="sxs-lookup"><span data-stu-id="e1163-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="e1163-107">Stjórnandi véla og eftirlitsmenn vinnusalar fá aðgang að framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="e1163-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="e1163-108">Stjórnendur vél geta uppfært áætlunina með því að keyra afmarkað og verk framleiðsluferlis.</span><span class="sxs-lookup"><span data-stu-id="e1163-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="e1163-109">Umsjónarmaður vinnusalar getur breytt starfsáætluninni.</span><span class="sxs-lookup"><span data-stu-id="e1163-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="e1163-110">Starfskraftar geta opnað tíma og viðveru til innstimplunar og útstimplunar á jaðrinum til að tryggja réttan útreikning launa starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e1163-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="e1163-111">Þetta efnisatriði lýsir því hvernig vinnuálag framkvæmdar framleiðslu starfar með kvörðunareiningum skýja og jaðra.</span><span class="sxs-lookup"><span data-stu-id="e1163-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="e1163-112">Stuðningstími framleiðslu</span><span class="sxs-lookup"><span data-stu-id="e1163-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="e1163-113">Eins og eftirfarandi skýringarmynd sýnir er stuðningstíma framleiðslu skipt í þrjá áfanga: *Áætlun*, *Keyrslu* og *Lok*.</span><span class="sxs-lookup"><span data-stu-id="e1163-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="e1163-114">[![Áfangar framkvæmdar framleiðslu þegar stakt umhverfi er notað](media/mes-phases.png "Áfangar framkvæmdar framleiðslu þegar stakt umhverfi er notað")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="e1163-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="e1163-115">Áfanginn _Áætlun_ felur í sér skilgreiningu afurðar, áætlanagerð, stofnun og áætlun afurðar og losun.</span><span class="sxs-lookup"><span data-stu-id="e1163-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="e1163-116">Útgáfuskrefið tilgreinir skiptin úr áfanganum _Áætlun_ yfir í áfangann _Keyrsla_.</span><span class="sxs-lookup"><span data-stu-id="e1163-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="e1163-117">Þegar framleiðslupöntun er losuð verða verk framleiðslupöntunar sýnileg á framleiðslugólfinu og tilbúnar til framkvæmdar.</span><span class="sxs-lookup"><span data-stu-id="e1163-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="e1163-118">Þegar framleiðsluverk er merkt sem lokið, færist verkið úr áfanganum _Keyrsla_ yfir í áfangann _Lok_.</span><span class="sxs-lookup"><span data-stu-id="e1163-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="e1163-119">Í áfanganum _Lok_ fara skráningarnar úr áfanganum *Keyrsla* í gegnum samþykktarverkflæði og eru reiknaðar, samþykktar og fluttar.</span><span class="sxs-lookup"><span data-stu-id="e1163-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="e1163-120">Á þeim tímapunkti er framleiðslupöntuninni lokið.</span><span class="sxs-lookup"><span data-stu-id="e1163-120">At that point, the production order is completed.</span></span> <span data-ttu-id="e1163-121">Þar af leiðandi er myndaður grunnur fyrir laun starfskrafta.</span><span class="sxs-lookup"><span data-stu-id="e1163-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="e1163-122">Skipta áfanganum Keyrsla í aðskilið vinnuálag</span><span class="sxs-lookup"><span data-stu-id="e1163-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="e1163-123">Eins og sýnt er á eftirfarandi skýringarmynd, þegar notast er við kvörðunareiningar, er áfanganum _Keyrsla_ skipt niður sem aðskilið vinnuálag.</span><span class="sxs-lookup"><span data-stu-id="e1163-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="e1163-124">[![Áfangar framkvæmdar framleiðslu þegar kvörðunareiningar eru notaðar](media/mes-phases-workloads.png "Áfangar framkvæmdar framleiðslu þegar kvörðunareiningar eru notaðar")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="e1163-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="e1163-125">Líkanið færist nú frá stakri uppsetningu yfir í líkan sem er byggt á miðstöðinni og kvörðunareiningunum.</span><span class="sxs-lookup"><span data-stu-id="e1163-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="e1163-126">Áfangarnir _Áætlun_ og _Lok_ keyra sem aðgerðir bakvinnslu á miðstöðinni og vinnuálag framkvæmdar framleiðslu er keyrð á kvörðunareiningunum.</span><span class="sxs-lookup"><span data-stu-id="e1163-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="e1163-127">Gögn eru flutt á ósamstilltan hátt á milli miðstöðvarinnar og kvörðunareininganna.</span><span class="sxs-lookup"><span data-stu-id="e1163-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="e1163-128">Þegar framleiðslupöntun er losuð í miðstöðinni verða öll gögn sem þarf til að vinna úr framleiðsluverkum flutt yfir í kvörðunareininguna.</span><span class="sxs-lookup"><span data-stu-id="e1163-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="e1163-129">Þessi gögn fela í sér framleiðslupantanir, framleiðsluleiðir, uppskriftir og afurðir.</span><span class="sxs-lookup"><span data-stu-id="e1163-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="e1163-130">Gögn sem eru ekki tengd framleiðslupöntun (svo sem óbeinir verkþættir, fjarvistarkóðar og færibreytur framleiðslu) eru einnig flutt frá miðstöðinni yfir í kvörðunareininguna.</span><span class="sxs-lookup"><span data-stu-id="e1163-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="e1163-131">Gögn sem koma frá miðstöðinni og eru flutt yfir í kvörðunareininguna er að jafnaði einungis hægt að stofna eða uppfæra á miðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="e1163-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="e1163-132">Ekki er t.d. hægt að stofna nýjan fjarvistakóða eða óbeinan verkþátt á kvörðunareiningu&mdash;sem þeir geta aðeins notað fyrir skráningu.</span><span class="sxs-lookup"><span data-stu-id="e1163-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="e1163-133">Skráningarnar sem gerðar eru á kvörðunareiningunni við keyrslu eru síðan fluttar í miðstöðina, þar sem unnið er úr samþykki á tíma og viðveru, birgðum og fjárhagslegum uppfærslum.</span><span class="sxs-lookup"><span data-stu-id="e1163-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="e1163-134">Verk framkvæmdar framleiðslu sem keyra má á vinnuálagi</span><span class="sxs-lookup"><span data-stu-id="e1163-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="e1163-135">Hægt er að keyra eftirfarandi verk framkvæmdar framleiðslu á vinnuálagi þegar kvörðunareiningar eru notaðar:</span><span class="sxs-lookup"><span data-stu-id="e1163-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="e1163-136">Innstimplun, innskráning, útstimplun og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="e1163-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="e1163-137">Ræsa vinnslu</span><span class="sxs-lookup"><span data-stu-id="e1163-137">Start job</span></span>
- <span data-ttu-id="e1163-138">Sameina vinnslur</span><span class="sxs-lookup"><span data-stu-id="e1163-138">Bundle jobs</span></span>
- <span data-ttu-id="e1163-139">Gera framvinduskýrslu</span><span class="sxs-lookup"><span data-stu-id="e1163-139">Report progress</span></span>
- <span data-ttu-id="e1163-140">Tilkynna rýrnun</span><span class="sxs-lookup"><span data-stu-id="e1163-140">Report scrap</span></span>
- <span data-ttu-id="e1163-141">Óbeinn verkþáttur</span><span class="sxs-lookup"><span data-stu-id="e1163-141">Indirect activity</span></span>
- <span data-ttu-id="e1163-142">Hlé</span><span class="sxs-lookup"><span data-stu-id="e1163-142">Break</span></span>
- <span data-ttu-id="e1163-143">Tilkynna sem lokið og ganga frá (krefst þess að þú keyrir einnig vinnuálag vöruhúsakeyrslu á einingakvarðanum þínum, sjá einnig [Tilkynna sem lokið og ganga frá á einingakvarða](#RAF))</span><span class="sxs-lookup"><span data-stu-id="e1163-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="e1163-144">Unnið með vinnuálag framkvæmdar framleiðslu í miðstöðinni</span><span class="sxs-lookup"><span data-stu-id="e1163-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="e1163-145">Yfirleitt eru áskilin ferli til keyrslu vinnuálags framkvæmdar framleiðslu keyrð sjálfkrafa til að halda miðstöðinni og öllum kvörðunareiningunum samstilltum eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="e1163-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="e1163-146">Þegar þú lendir í vandræðum er hins vegar hægt að ræsa handvirkt vinnslu á hráum skráningum sem mótteknar eru frá vinnuálagi og/eða athuga vinnslukladda hrárrar skráningar.</span><span class="sxs-lookup"><span data-stu-id="e1163-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="e1163-147">Vinna handvirkt úr hráum skráningum</span><span class="sxs-lookup"><span data-stu-id="e1163-147">Manually process raw registrations</span></span>

<span data-ttu-id="e1163-148">Runuvinnsla í Supply Chain Management keyrir sjálfkrafa til að vinna úr öllum skráningum sem hafa verið mótteknar úr vinnuálaginu.</span><span class="sxs-lookup"><span data-stu-id="e1163-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="e1163-149">Þessi vinnsla stofnar nauðsynlegar framleiðslubækur og færslubókarfærslur þegar skráning er unnin fyrir vinnslu sem er lokið á vinnuálaginu.</span><span class="sxs-lookup"><span data-stu-id="e1163-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="e1163-150">Þrátt fyrir að vinnslan sé yfirleitt keyrð sjálfkrafa er hægt að keyra hana handvirkt hvenær sem er með því að skrá þig inn á miðstöðina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinna úr hráum skráningum**.</span><span class="sxs-lookup"><span data-stu-id="e1163-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="e1163-151">Athugun á vinnslukladda hrárra skráningar</span><span class="sxs-lookup"><span data-stu-id="e1163-151">Check the raw registration processing log</span></span>

<span data-ttu-id="e1163-152">Þegar endurskoða á vinnslukladda skráningar skal skrá sig inn á miðstöðina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinnslukladdi hrárrar skráningar**.</span><span class="sxs-lookup"><span data-stu-id="e1163-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="e1163-153">Síðan **Vinnslukladdi hrárrar skráningar** sýnir lista yfir unnar hráar skráningar og stöðu hverrar skráningar fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="e1163-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="e1163-154">![Vinnslukladdasíða hrárrar skráningar](media/mes-processing-log.png "Vinnslukladdasíða hrárrar skráningar")</span><span class="sxs-lookup"><span data-stu-id="e1163-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="e1163-155">Hægt er að vinna með allar skráningar á listanum með því að velja skráningu og síðan smella á einn af eftirfarandi hnöppum á aðgerðasvæðinu:</span><span class="sxs-lookup"><span data-stu-id="e1163-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="e1163-156">**Vinnsla** – Vinna handvirkt úr valinni skráningu.</span><span class="sxs-lookup"><span data-stu-id="e1163-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="e1163-157">Þessi aðgerð getur komið sér vel ef vinnslan _Úrvinnsla hrárra skráninga_ var ekki keyrt eða það mistókst.</span><span class="sxs-lookup"><span data-stu-id="e1163-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="e1163-158">**Hætta við** – Hætta við völdu skráninguna.</span><span class="sxs-lookup"><span data-stu-id="e1163-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="e1163-159">Unnið með vinnuálag framkvæmdar framleiðslu í kvarðaeiningu</span><span class="sxs-lookup"><span data-stu-id="e1163-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="e1163-160">Yfirleitt eru áskilin ferli til keyrslu vinnuálags framkvæmdar framleiðslu keyrð sjálfkrafa til að halda miðstöðinni og öllum kvörðunareiningunum samstilltum eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="e1163-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="e1163-161">Þegar þú lendir í vandræðum getur þú athugað feril pantana sem hefur verið unnið úr í kvörðunareiningu eða keyrt handvirkt vinnsluna _Skilaboðaúrvinnsla framleiðslumiðstöðvar til einingarkvarða_.</span><span class="sxs-lookup"><span data-stu-id="e1163-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="e1163-162">Skoða feril framleiðsluvinnslu sem hefur verið unnin á kvörðunareiningu</span><span class="sxs-lookup"><span data-stu-id="e1163-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="e1163-163">Þegar endurskoða á framleiðsluvinnslu sem hefur verið unnin á kvörðunareiningu skal skrá sig inn í kvörðunareiningavélina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinnsluferill framleiðsluvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="e1163-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="e1163-164">**Vinnsluferill framleiðsluvinnslu** sýnir vinnsluferil framleiðslupantana í kvörðunareiningunni.</span><span class="sxs-lookup"><span data-stu-id="e1163-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="e1163-165">Hægt er að vinna í öllum framleiðslupöntunum á listanum með því að velja framleiðslupöntun og smella síðan á einn af eftirfarandi hnöppum á aðgerðasvæði:</span><span class="sxs-lookup"><span data-stu-id="e1163-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="e1163-166">**Vinnsla** – Vinna handvirkt úr valinni framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="e1163-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="e1163-167">**Hætta við** – Hætta við völdu framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="e1163-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="e1163-168">Skilaboðaúrvinnsla framleiðslumiðstöðvar til vinnslu kvörðunareiningar</span><span class="sxs-lookup"><span data-stu-id="e1163-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="e1163-169">Vinnslan _Skilaboðaúrvinnsla framleiðslumiðstöðvar til kvörðunareiningar_ vinnur úr gögnum frá miðstöðinni til kvörðunareiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="e1163-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="e1163-170">Þessi vinnsla hefst sjálfkrafa um leið og vinnuálag framkvæmdar framleiðslu er keyrt.</span><span class="sxs-lookup"><span data-stu-id="e1163-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="e1163-171">Hins vegar er hægt að keyra slíkt handvirkt hvenær sem er með því að opna **Framleiðslustýringu \> Reglubundin verk \> Stjórnun vinnuálags í bakvinnslu \> Skilaboðaúrvinnsla framleiðslumiðstöðvar til kvörðunareiningar**.</span><span class="sxs-lookup"><span data-stu-id="e1163-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="e1163-172">Tilkynna sem lokið og ganga frá á einingakvarða</span><span class="sxs-lookup"><span data-stu-id="e1163-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="e1163-173">Í núverandi útgáfu eru aðgerðirnar tilkynna sem lokið og frágangur (fyrir tilbúnar afurðir, aukaafurðir og hliðarafurðir) studdar af [vinnuálagi vöruhúsakeyrslu](cloud-edge-workload-warehousing.md) (ekki vinnuálagi framleiðslukeyrslu).</span><span class="sxs-lookup"><span data-stu-id="e1163-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="e1163-174">Til að nota þessa virkni þegar tengst er við einingakvarða þarf því að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e1163-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="e1163-175">Settu upp bæði vinnuálag vöruhúsakeyrslu og vinnuálag framleiðslukeyrslu í einingakvarðanum.</span><span class="sxs-lookup"><span data-stu-id="e1163-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="e1163-176">Notaðu farsímaforrit Warehouse Management til að skrá sem tilbúið og vinna úr frágangsverkinu.</span><span class="sxs-lookup"><span data-stu-id="e1163-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="e1163-177">Keyrsluviðmót framleiðslugólfs styður ekki þessi ferli eins og er.</span><span class="sxs-lookup"><span data-stu-id="e1163-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
