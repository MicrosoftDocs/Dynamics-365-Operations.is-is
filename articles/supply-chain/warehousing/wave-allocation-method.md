---
title: Bylgjuúthlutun
description: Þetta efnisatriði lýsir hvernig á að setja upp skref bylgjuúthlutunar, þ.á.m. hvernig á að virkja hliðstæðu vinnslu fyrir hana.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: feee33a7d4ea3f0d9c4d671210293a28aac14f61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823168"
---
# <a name="wave-allocation"></a><span data-ttu-id="ddc9e-103">Bylgjuúthlutun</span><span class="sxs-lookup"><span data-stu-id="ddc9e-103">Wave allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddc9e-104">Bylgjuvinnsla getur reynst tímafrek og meirihluti vinnslutímans fer í úthlutunarskrefið og stofnskref vinnunnar.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-104">Wave processing can be time consuming, and most of the processing time is spent in the allocation step and in the work creation step.</span></span>

<span data-ttu-id="ddc9e-105">Nú er hægt að keyra skrefin samhliða, sem getur aukið afköst bylgjuvinnslunnar og opnað fyrir meira gegnumstreymi af bylgjum í sama vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-105">It is now possible to run each of these steps in parallel, which can improve the performance of the wave processing, and allow for a larger throughput of waves in the same warehouse.</span></span> <span data-ttu-id="ddc9e-106">Þetta efnisatriði útskýrir hvernig á að setja upp úthlutunaraðferð bylgjunnar til að keyra samhliða.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-106">This topic explains how to set up the wave allocation method to run in parallel.</span></span> <span data-ttu-id="ddc9e-107">Frekari upplýsingar um hvernig á að setja upp stofnun vinnu fyrir samhliða keyrslu er að finna í [Áætla stofnun vinnu í bylgju](configure-wave-schedule-work-creation.md).</span><span class="sxs-lookup"><span data-stu-id="ddc9e-107">For more information about how to set up work creation to run in parallel, see [Schedule work creation during wave](configure-wave-schedule-work-creation.md).</span></span>

<span data-ttu-id="ddc9e-108">Áður fyrr var aðeins hægt að úthluta einni bylgju í einu í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-108">Previously it was only possible to allocate one wave at a warehouse at a time.</span></span> <span data-ttu-id="ddc9e-109">Þessi takmörkun hefur verið fjarlægð og skipt út fyrir nýja takmörkun sem aðeins læsir vörunni og víddunum sem eru fyrir ofan staðsetninguna í frátekningarstigveldinu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-109">This constraint has been removed and replaced by a new constraint that only locks the item and dimensions that are above location in the reservation hierarchy.</span></span> <span data-ttu-id="ddc9e-110">Víddir fyrir ofan staðsetninguna eru alltaf með afurðarvíddir.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-110">Dimensions above the location always include product dimensions.</span></span> <span data-ttu-id="ddc9e-111">Til dæmis ef vara er skilgreind með því að nota *Lit*, þá er hægt að vinna samhliða úr afbrigðum fyrir *Rauða*, *Bláa* og *Gula*.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-111">For example, if an item is configured using *Color*, then variants for *Red*, *Blue*, and *Yellow* could each be processed in parallel.</span></span>

<span data-ttu-id="ddc9e-112">Þetta þýðir að ef verið er að úthluta sömu vörunni með sömu víddirnar fyrir ofan staðsetninguna af einni bylgju þurfa aðrar bylgjur að bíða til að fá læsingu á sömu vöru og víddum.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-112">This means that if the same item with the same dimensions above the location is being allocated by one wave, other waves will have to wait to acquire a lock on the same item and dimensions.</span></span> <span data-ttu-id="ddc9e-113">Ef ekki er hægt að fá læsinguna í tíma mun villa koma upp og bylgjuvinnslan mistakast.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-113">If the lock can't be acquired in a timely manner, an error will occur and the wave processing will fail.</span></span>

<span data-ttu-id="ddc9e-114">Bylgjan verður að keyra í runu til að geta notað hliðstæða vinnslu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-114">In order to utilize parallel processing, the wave must run in batch.</span></span>

## <a name="performance-improvements"></a><span data-ttu-id="ddc9e-115">Bætt afköst</span><span class="sxs-lookup"><span data-stu-id="ddc9e-115">Performance improvements</span></span>

<span data-ttu-id="ddc9e-116">Ávinningur afkasta vegna hliðstæðrar vinnslu fellur í tvo flokka:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-116">Performance benefits of parallel processing fall in two categories:</span></span>

- <span data-ttu-id="ddc9e-117">**Bætt gegnumstreymi** – Gegnstreymi á bylgjum eykst yfirleitt jafnvel þótt hliðstæð vinnsla sé ekki skilgreind, sérstaklega í aðstæðum þar sem engin skörun á vörum innan bylgjanna.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-117">**Improved throughput** - The throughput of waves will typically improve even if parallel processing isn't configured, especially for scenarios where there is no overlap of items within the waves.</span></span>
- <span data-ttu-id="ddc9e-118">**Endurbætur á úthlutun fyrir eina bylgju** – Prófanir á gögnum viðskiptavina hafa sýnt nærri 50% bætingu á afköstum þegar skipt er yfir í hliðstæða úthlutun.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-118">**Improvement of the allocation for a single wave** - Testing on customer data has shown a near 50% performance improvement after switching to parallel allocation.</span></span> <span data-ttu-id="ddc9e-119">Hliðstæða vinnslan er gerð eftir vörum og víddum fyrir ofan staðsetninguna þannig að bætingar fara eftir því hversu margar mismunandi vörur bylgja inniheldur, tiltæku tölvukerfi og tímalengd úthlutunar í samanburði við tímann sem tekur að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-119">The parallel processing is done per items and dimensions above the location, so the improvements depend on how many different items a wave contains, the infrastructure available, and the duration of the allocation versus the duration of the work creation.</span></span>

## <a name="configure-parallel-allocation"></a><span data-ttu-id="ddc9e-120">Skilgreina hliðstæða úthlutun</span><span class="sxs-lookup"><span data-stu-id="ddc9e-120">Configure parallel allocation</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="ddc9e-121">Færibreytur vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="ddc9e-121">Warehouse management parameters</span></span>

<span data-ttu-id="ddc9e-122">Til að nota hliðstætt úthlutunarferli skal fara í **Vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis**, opna flipann **Bylgjuvinnsla** og stilla eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-122">To use parallel allocation processing, go to **Warehouse management > Setup > Warehouse management parameters**, open the **Wave processing** tab, and make the following settings:</span></span>

- <span data-ttu-id="ddc9e-123">**Runuflokkur bylgjuvinnslu** – Veljið runuflokkinn sem upprunaleg vinnsla bylgjanna á að nota.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-123">**Wave processing batch group** - Select the batch group that the initial processing of the waves should use.</span></span> <span data-ttu-id="ddc9e-124">Vinnsla úthlutunar sem fylgir í kjölfarið verður hægt að gera með því að nota mismunandi runuflokka.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-124">The subsequent processing of allocation can be done using different batch groups.</span></span>
- <span data-ttu-id="ddc9e-125">**Vinna bylgjur í runu** – Stillið þetta á *Já* til að nota hliðstæða vinnslu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-125">**Process waves in batch** - Set this to *Yes* to use parallel processing.</span></span>
- <span data-ttu-id="ddc9e-126">**Bíða eftir læsingu (ms)** – Sláið inn tímann í millisekúndum sem úthlutunarskref mun bíða eftir tilfangi kerfis sem er læst af öðru úthlutunarskrefi.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-126">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="ddc9e-127">Þegar farið er yfir þennan tíma er ekki unnið úr bylgjunni og villuboð birtist.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-127">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span> <span data-ttu-id="ddc9e-128">Mælt er með að láta a.m.k. nokkrar sekúndur líða til að leyfa úthlutun á einni röklegri einingu að klárast.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-128">We recommend that you allow at least a few seconds to allow for allocation of one logical unit to finish.</span></span>

<span data-ttu-id="ddc9e-129">Frekari upplýsingar um þessa og aðra valkosti bylgjuvinnslu á síðunni **Færibreytur vöruhúsakerfis** er að finna í [Færibreytur vöruhúss fyrir bylgjuvinnslu](wave-warehouse-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ddc9e-129">For information about these and other wave processing options on the **Warehouse management parameters** page, see [Warehouse parameters for wave processing](wave-warehouse-parameters.md).</span></span>

## <a name="wave-process-methods"></a><span data-ttu-id="ddc9e-130">Vinnsluaðferðir bylgju</span><span class="sxs-lookup"><span data-stu-id="ddc9e-130">Wave process methods</span></span>

<span data-ttu-id="ddc9e-131">Til að setja upp hliðstæða vinnslu:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-131">To set up parallel processing:</span></span>

1. <span data-ttu-id="ddc9e-132">Farið í **Vöruhúsakerfi > Uppsetning > Bylgjur > Aðferðir bylgjuvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-132">Go to **Warehouse Management > Setup > Waves > Wave process methods**.</span></span>
1. <span data-ttu-id="ddc9e-133">Veljið `allocateWave` aðferðina í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-133">Select the `allocateWave` method in the grid.</span></span>
1. <span data-ttu-id="ddc9e-134">Á aðgerðasvæðinu skal velja **Skilgreining verks**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-134">On the Action Pane, select **Task configuration**.</span></span>
1. <span data-ttu-id="ddc9e-135">Þá opnast síðan **Skilgreining verks eftir bókunaraðferð bylgju**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-135">The **Wave post method task configuration** page opens.</span></span> <span data-ttu-id="ddc9e-136">Þetta hnitanet sýnir hvert vöruhús fyrir sig þar sem `allocateWave` aðferðin hefur verið skilgreind.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-136">This grid lists each warehouse where you have configured the `allocateWave` method.</span></span> <span data-ttu-id="ddc9e-137">Hliðstæð vinnsla verður aðeins notuð fyrir vöruhús sem eru skráð.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-137">Parallel processing will only be used for warehouses that are listed.</span></span> <span data-ttu-id="ddc9e-138">Notið hnappa aðgerðasvæðisins til að bæta við eða fjarlægja vöruhús úr hnitanetinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-138">Use the Action Pane buttons to add or remove warehouses from the grid as needed.</span></span> 
1. <span data-ttu-id="ddc9e-139">Fyrir hvert vöruhús skaltu velja eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-139">For each warehouse, make the following settings:</span></span>
    - <span data-ttu-id="ddc9e-140">**Hámarksfjöldi runuverka** – Tilgreinið fjölda runuverka sem á að nota fyrir úthlutunina fyrir valið vöruhús.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-140">**Maximum number of batch tasks** - Specify the number of batch tasks that should be used for the allocation for the selected warehouse.</span></span> <span data-ttu-id="ddc9e-141">Ákjósanlegur fjöldi runuverka fer eftir tölvukerfinu og öðrum runuvinnslum sem verið að vinna úr á þjóninum.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-141">The optimal number of batch tasks depends on the infrastructure available and what other batch jobs are being processed on the server.</span></span> <span data-ttu-id="ddc9e-142">Prófanir á fjögurra kjarna umhverfi sem einblíndi á bylgjuvinnslu sýndu fram á að góðar niðurstöður fengust með því að nota átta verk.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-142">Tests done on a four core environment that was dedicated to wave processing showed that using eight tasks produced good results.</span></span>
    - <span data-ttu-id="ddc9e-143">**Runuflokkur bylgjuvinnslu** – Hægt er að nota ákveðna runuflokka fyrir mismunandi vöruhús til að leyfa úthlutunarferlinu að laga sig að hverju vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-143">**Wave processing batch group** - Specific batch groups can be used for different warehouses to allow the allocation processing to scale out per warehouse.</span></span>

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a><span data-ttu-id="ddc9e-144">Kveikja eða slökkva á hliðstæðri vinnslu í öllum lögaðilum</span><span class="sxs-lookup"><span data-stu-id="ddc9e-144">Enable or disable parallelization across all legal entities</span></span>

<span data-ttu-id="ddc9e-145">Mælt er með að stilla `allocateWave` aðferðina á að keyra hliðstætt yfir alla lögaðila vegna þess að það stuðlar að auknum afköstum bylgjuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-145">We recommend that you set the `allocateWave` method to run in parallel across all legal entities because this helps to improve the performance of the wave processing.</span></span> <span data-ttu-id="ddc9e-146">Frá og með Supply Chain Management útgáfu 10.0.7 verður eiginleikinn *Hliðstæð vinnsla bylgju fyrir aðferð bylgjuúthlutunar* virkjaður að sjálfgefnu fyrir allar nýjar og uppfærðar uppsetningar og ekki verður hægt að slökkva á þeim aftur.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-146">Starting in Supply Chain Management version 10.0.17, the *Wave parallelization for Allocate Wave method* feature is enabled by default for all new and updated installations, and can't be turned off again.</span></span> <span data-ttu-id="ddc9e-147">Þegar þessi eiginleiki hefur verið virkjaður gerist eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-147">After enabling this feature, the following occurs:</span></span>

- <span data-ttu-id="ddc9e-148">Aðferð `allocateWave` er uppfærð til að hafa með stillingu verkskilgreiningar sem gerir kleift að nota síðuna **Aðferðir bylgjuvinnslu** til að skilgreina fjölda verka sem munu keyra samtímis, sem jafngildir fjölda hliðstæðra vinnsla.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-148">The `allocateWave` method is updated to include a task configuration setting that lets you use the **Wave process methods** page to define the number of tasks that will run simultaneously, equivalent to the number of parallel processes.</span></span> <span data-ttu-id="ddc9e-149">Fyrir vikið er tíminn sem notaður er í skrefi bylgjuúthlutunar (sem er yfirleitt 30% til 60% af heildarvinnslutímanum) styttur um því sem nemur í grófum dráttum fjölda verka.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-149">As a result, the time used on the allocate-wave step (which is typically 30% to 60% of the total processing time) is reduced by a factor roughly equivalent to the number of tasks.</span></span> <span data-ttu-id="ddc9e-150">Einnig er hægt að velja hvaða runu verður úthlutað til að vinna úr þessum verkum.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-150">It's also possible to select which batch will be assigned to process these tasks.</span></span> <span data-ttu-id="ddc9e-151">Mikilvægt er að hafa í huga að allir lögaðilar verða grunnstilltir til að vinna úr bylgjum í runu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-151">It's important to note that all of your legal entities will be configured to process waves in batch.</span></span> <span data-ttu-id="ddc9e-152">Fyrir vöruhúsin sem eru þegar skilgreind til að vinna úr bylgjum í runu og fyrir vöruhúsin sem eru þegar skilgreind til að nota `allocateWave` aðferðina í hliðstæðri vinnslu, verður fyrirliggjandi skilgreiningu haldið.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-152">For the warehouses that are already configured to process waves in batch, and for the warehouses that are already configured to use the `allocateWave` method in parallel, the existing configuration will be kept.</span></span>
- <span data-ttu-id="ddc9e-153">Sjálfgefið er að allir nýju lögaðilarnir séu grunnstilltar til að vinna úr bylgjum í runu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-153">By default, all the new legal entities are configured to process waves in batch.</span></span> <span data-ttu-id="ddc9e-154">Öll ný vöruhús með valkostinn **Ferli vöruhúsakerfis** virkjaðan verða með `allocateWave` aðferðina skilgreinda til að keyra í hliðstæðri vinnslu að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-154">All new warehouses with the **Warehouse management processes** option enabled will have the `allocateWave` method configured to run in parallel by default.</span></span>
- <span data-ttu-id="ddc9e-155">Á síðunni **Færibreytur vöruhúsakerfis** er **Vinna úr bylgjum í runu** stillt á *Já* og **Bíða eftir læsingu (ms)** er stillt á 15 sekúndur að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-155">On the **Warehouse management parameters** page, **Process saves in batch** is set to *Yes* and  **Wait for lock (ms)** set to a default 15 seconds.</span></span> <span data-ttu-id="ddc9e-156">Þetta þýðir að allar bylgjur verða keyrðar í runu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-156">This means that all waves will be executed in batch.</span></span> <span data-ttu-id="ddc9e-157">Þegar bylgja er keyrð fær hún læsingu á vörunni og víddunum fyrir ofan staðsetningu í úthlutunarskrefinu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-157">When a wave is running, it acquires a lock on the item and dimensions above location during the allocation step.</span></span> <span data-ttu-id="ddc9e-158">Þegar annað bylgjuvinnsluverk reynir að fá sömu læsingu fyrir sömu færslu er lokað á það þar til núverandi vinnslu er lokið.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-158">When another wave processing task tries to acquire the same lock for the identical record, it is blocked until the current process is finished.</span></span> <span data-ttu-id="ddc9e-159">Stillingarnar **Bíða eftir læsingu (ms)** setja á hámarkstíma sem kerfið mun bíða áður en læsingin er opnuð.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-159">The **Wait for lock (ms)** settings establishes the maximum time the system will wait before the lock is released.</span></span>

<span data-ttu-id="ddc9e-160">Samhliða úthlutunarferli krefst þess að bylgjuvinnsla keyri í runu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-160">Parallel allocation processing requires wave processing to run in batch.</span></span> <span data-ttu-id="ddc9e-161">Þess vegna verða afköst bylgjuvinnslunnar minnkuð ef slökkt er á stillingunni **Vinna bylgjur í runu**, sérstaklega ef bylgjuvinnsla notar hliðstætt ferli eins og skilgreint er af verkskilgreiningunni fyrir viðeigandi bylgjuaðferðir.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-161">Therefore, you will reduce your wave processing performance if you turn off the **Process saves in batch** setting, especially if wave processing is using a parallel process as defined by the task configuration for the relevant wave methods.</span></span>

<span data-ttu-id="ddc9e-162">Ef þörf krefur er hægt að afturkalla hverja sjálfgefna stillingu fyrir sig þegar eiginleikinn *Samhliða bylgja fyrir úthlutunaraðferð bylgju* er sjálfkrafa virkjaður fyrir tilvikið.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-162">If necessary, you can undo each of the settings made by default when the *Wave parallelization for Allocate Wave method* feature is automatically enabled for your instance.</span></span> <span data-ttu-id="ddc9e-163">Til að gera þetta:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-163">To do this:</span></span>

- <span data-ttu-id="ddc9e-164">Farðu í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-164">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="ddc9e-165">Í flipanum **Bylgjuvinnsla** skal nota æskileg gildi fyrir **Vinna bylgjur í runu** og **Bíða eftir læsingu (ms)**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-165">On the **Wave processing** tab, apply your preferred values for **Process waves in batch** and **Wait for lock (ms)**.</span></span>
- <span data-ttu-id="ddc9e-166">Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-166">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span> <span data-ttu-id="ddc9e-167">Veljið `allocateWave` aðferðina.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-167">Select the `allocateWave` method.</span></span> <span data-ttu-id="ddc9e-168">Á aðgerðasvæðinu skal velja **Skilgreining verks** til að opna síðu sem sýnir hvert vöruhús þar sem aðferðin er stillt á að keyra í hliðstæðri vinnslu.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-168">On the Action Pane, select **Task configuration** to open a page that lists each warehouse where the method is set to run in parallel.</span></span> <span data-ttu-id="ddc9e-169">Breytið eða eyðið fjölda runuverka og úthlutuðum runuflokki fyrir hvert birt vöruhús eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-169">Modify or delete the number of batch tasks and the assigned wave group for each listed warehouse as needed.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ddc9e-170">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="ddc9e-170">Troubleshooting</span></span>

### <a name="troubleshoot-using-the-infolog"></a><span data-ttu-id="ddc9e-171">Úrræðaleit með upplýsingaskránni</span><span class="sxs-lookup"><span data-stu-id="ddc9e-171">Troubleshoot using the Infolog</span></span>

<span data-ttu-id="ddc9e-172">Þars sem runurammi er notaður verða villur sem koma upp í bylgjuvinnslu sóttar sem hluti af upplýsingaskrám runuvinnslanna.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-172">Because the batch framework is used, errors that occur during wave processing will be captured as part of the batch jobs Infologs.</span></span> <span data-ttu-id="ddc9e-173">Til að lesa runuvinnslur sem tengjast bylgju:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-173">To read the batch jobs related to a wave:</span></span>

1. <span data-ttu-id="ddc9e-174">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-174">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="ddc9e-175">Veljið bylgjuna sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-175">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="ddc9e-176">Á aðgerðasvæðinu skal opna flipann **Bylgja** og úr flokknum **Bylgja** skal velja **Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-176">On the Action Pane, open the **Wave** tab and, from the **Wave** group, select **Batch jobs**.</span></span>

<span data-ttu-id="ddc9e-177">Bylgjuvinnsla leiðréttir sig sjálf þannig að allar villur sem vinnslan greinir eiga að vera tilkynntar með upplýsingaskránni.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-177">Wave processing is self-correcting, so any error detected during processing should be reported using the Infolog.</span></span>

<span data-ttu-id="ddc9e-178">Dæmigerð villa sem tengist hliðstæðri vinnslu gæti verið að tvær bylgjur reyni að úthluta sömu vörunni samtímis og önnur þeirra klárast ekki þannig að hin bylgjan getur ekki fengið læsingu innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-178">A typical error related to parallel processing could be that two waves try to allocate the same item at the same time and one does not complete so that the other wave is unable to acquire a lock within the specified time.</span></span> <span data-ttu-id="ddc9e-179">Ef þetta kemur upp mun skrá runuvinnslanna innihalda upplýsingar sem gefa til kynna að ekki hafi verið hægt að sækja læsingu fyrir vöruna, sem þýðir að það þarf að vinna aftur bylgjuna sem tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-179">If this situation occurs, the batch jobs log will contain information stating that the lock for the item could not be acquired, in which case the wave that failed must be processed again.</span></span>

<span data-ttu-id="ddc9e-180">Vegna þess að vinnslan er í gangi í hliðstæðri vinnslu þarf að viðhalda gögnum í öðrum töflum til að rekja stöðu vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-180">Because the processing is happening in parallel, data must be maintained in different tables to track the state of the processing.</span></span> <span data-ttu-id="ddc9e-181">Þetta þýðir skrárnar fyrir runuvinnslurnar gætu innihaldið villur á borð við tvítekinn lykil.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-181">This means that the logs for the batch jobs might contain errors such as duplicate key errors.</span></span>

<span data-ttu-id="ddc9e-182">Villurnar í runuverkunum eru einnig hluti af skrá runuvinnslanna.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-182">The errors from the batch tasks are also part of the batch jobs log.</span></span> <span data-ttu-id="ddc9e-183">Mikilvægustu upplýsingarnar eru yfirleitt neðst.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-183">The most important information is typically at the bottom.</span></span>

<span data-ttu-id="ddc9e-184">Í sjaldgæfum tilfellum, til dæmis ef SQL-tenging rofnaði, er möguleiki á að bylgjuvinnslan endi í ósamkvæmri stöðu þar sem runuvinnslan virðist vera í gangi en vinnslan hefur stöðvast.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-184">In rare cases, for example if the SQL connection ended, it is possible for the wave processing to end in an inconsistent state where the batch job appears to be running but the processing is stopped.</span></span> <span data-ttu-id="ddc9e-185">Bylgjan ræður ekki við villur á borð við þessa, þannig að tilraunir til að hreinsa upp mislukkaðar bylgjur er gerð þegar næsta bylgja er keyrð.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-185">The wave can't handle errors like this, so an attempt to clean up failed waves is done when the next wave runs.</span></span> <span data-ttu-id="ddc9e-186">Annars, ef núverandi bylgja er í ósamkvæmri stöðu, skal fara í gegnum eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-186">Alternatively, if the current wave is in an inconsistent state, perform the following steps:</span></span>

1. <span data-ttu-id="ddc9e-187">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-187">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="ddc9e-188">Veljið bylgjuna sem þarf að hreinsa.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-188">Select the wave you need to clean up.</span></span>
1. <span data-ttu-id="ddc9e-189">Á aðgerðasvæðinu skal opna flipann **Bylgja** og í flokknum **Bylgja** skal velja **Hreinsa bylgjugögn**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-189">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Cleanup wave data**.</span></span>

### <a name="troubleshoot-using-the-wave-progress-log"></a><span data-ttu-id="ddc9e-190">Úrræðaleit með framvindukladda bylgju</span><span class="sxs-lookup"><span data-stu-id="ddc9e-190">Troubleshoot using the wave progress log</span></span>

<span data-ttu-id="ddc9e-191">Ef valkosturinn **Stofna kladda fyrir framvindu bylgju** er virkjaður á síðunni **Færibreytur vöruhúsakerfis**, þá er kladdafærsla búin til í hvert skipti sem úthlutun vöru og vídda hennar hefst og lýkur.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-191">If the **Create wave progress log** option is enabled on the **Warehouse management parameters** page, then a log record is created every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="ddc9e-192">Aðeins ætti að virkja þennan kladda þegar þess gerist þörf, til dæmis við fyrstu prófun eða fyrir úrræðaleit.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-192">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="ddc9e-193">Þegar þessi valkostur er virkjaður er hægt að skoða kladdann með því að gera eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="ddc9e-193">When this option is enabled, you can view the log by taking the following steps:</span></span>

1. <span data-ttu-id="ddc9e-194">Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-194">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="ddc9e-195">Veljið bylgjuna sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-195">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="ddc9e-196">Á aðgerðasvæðinu skal opna flipann **Bylgja** og í flokknum **Bylgja** skal velja **Framvinda**.</span><span class="sxs-lookup"><span data-stu-id="ddc9e-196">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Progress**.</span></span>