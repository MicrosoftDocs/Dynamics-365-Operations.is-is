---
title: Áætla stofnun vinnu í bylgju
description: Þetta efnisatriði lýsir því hvernig á að setja upp og nota vinnsluaðferð bylgju fyrir áætla stofnun vinnu.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501223"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="46043-103">Áætla stofnun vinnu í bylgju</span><span class="sxs-lookup"><span data-stu-id="46043-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="46043-104">Notið eiginleikann *Áætla stofnun vinnu* sem hluta af bylgjuferlinu til að auka gegnumstreymi bylgjuvinnslu með því að láta kerfið stofna vinnu með samhliða vinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="46043-105">Þegar aðgerðin er virkjuð verður áætluð vinna stofnuð sjálfkrafa sem kerfið mun að lokum vinna úr til að stofna raunverulega vinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="46043-106">Ef fjöldi hleðslulína bylgju nær fyrirframskilgreindum þröskuldi mun kerfið stofna raunverulega vinnu á fljótlegri hátt með því að nota samhliða, ósamstillta vinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="46043-107">Virkja eiginleikann Áætlun stofnun vinnu</span><span class="sxs-lookup"><span data-stu-id="46043-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="46043-108">Virkjun eiginleika í eiginleikastjórnun</span><span class="sxs-lookup"><span data-stu-id="46043-108">Enable the feature in feature management</span></span>

<span data-ttu-id="46043-109">Áður en hægt er að nota eiginleikann *Áætla stofnun vinnu* verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="46043-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="46043-110">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="46043-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="46043-111">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="46043-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="46043-112">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="46043-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="46043-113">**Heiti eiginleika:** *Áætla stofnun vinnu*</span><span class="sxs-lookup"><span data-stu-id="46043-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="46043-114">Eiginleikinn *Vinnulokun fyrir allt fyrirtækið* verður að vera virkur áður en hægt er að virkja *Áætla stofnun vinnu*.</span><span class="sxs-lookup"><span data-stu-id="46043-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="46043-115">Virkja handvirkt runuvinnslur fyrir bylgjur</span><span class="sxs-lookup"><span data-stu-id="46043-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="46043-116">Til að nýta sér samhliða ósamstillta aðferð til að stofna vöruhúsavinnu verður bylgjuferlið að vera keyrt í runu.</span><span class="sxs-lookup"><span data-stu-id="46043-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="46043-117">Til að setja þetta upp:</span><span class="sxs-lookup"><span data-stu-id="46043-117">To set this up:</span></span>

1. <span data-ttu-id="46043-118">Farðu í  **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="46043-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="46043-119">Í flipanum **Almennt** skal stilla **Vinna bylgjur í runu** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="46043-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="46043-120">Einnig er hægt að velja sérstakan **Runuflokk bylgjuvinnslu** til að koma í veg fyrir að úrvinnsla runubiðraðar verði keyrð á sama tíma og önnur ferli.</span><span class="sxs-lookup"><span data-stu-id="46043-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="46043-121">Stillið **Biðtími læsingar (ms)** sem verður notaður þegar kerfið vinnur úr nokkrum bylgjum samtímis.</span><span class="sxs-lookup"><span data-stu-id="46043-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="46043-122">Fyrir flest stærri bylgjuferli er mælt með gildinu *60000*.</span><span class="sxs-lookup"><span data-stu-id="46043-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="46043-123">Virkja nýja bylgjuskrefsaðferð handvirkt fyrir fyrirliggjandi bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="46043-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="46043-124">Byrjið á því að stofna nýja bylgjuskrefsaðferð og virkið hana fyrir ósamstillta verkvinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="46043-125">Farið í  **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.</span><span class="sxs-lookup"><span data-stu-id="46043-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="46043-126">Veljið  **Endurgera aðferð** og athugið að *WHSScheduleWorkCreationWaveStepMethod* hefur verið bætt við listann yfir aðferðir bylgjuferlis sem hægt er að nota í bylgjusniðmátum sendingar.</span><span class="sxs-lookup"><span data-stu-id="46043-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="46043-127">Veljið færsluna með **Heiti aðferðar** *WHSScheduleWorkCreationWaveStepMethod* og veljið **Verkskilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="46043-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="46043-128">Til að bæta nýrri línu við hnitanetið skal velja **Ný** á aðgerðasvæðinu og nota eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="46043-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="46043-129">**Vöruhús** - Veljið vöruhúsið sem nota á til að tímasetja vinnslu á stofnun vinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="46043-130">**Hámarksfjöldi runuverka** - Tilgreinið hámarksfjölda runuverka.</span><span class="sxs-lookup"><span data-stu-id="46043-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="46043-131">Í flestum tilfellum ætti þetta gildi að vera á bilinu 8-16, hins vegar mælum við með því að þið prófið ykkur áfram til að finna út bestu stillinguna fyrir ykkar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="46043-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="46043-132">**Runuflokkur bylgjuvinnslu** - Veljið sérstakan runuflokk bylgjuvinnslu til að fínstilla vinnslu runubiðraðar.</span><span class="sxs-lookup"><span data-stu-id="46043-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="46043-133">Nú er hægt að uppfæra fyrirliggjandi bylgjusniðmát (eða búa til nýtt) til að nota bylgjuvinnsluaðferðina *Áætla stofnun vinnu*.</span><span class="sxs-lookup"><span data-stu-id="46043-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="46043-134">Fara í  **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="46043-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="46043-135">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="46043-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="46043-136">Á listasvæðinu skal velja bylgjusniðmátið sem á að uppfæra (ef verið er að prófa með sýnigögnum, þá er hægt að nota *24 Sjálfgefin sending*).</span><span class="sxs-lookup"><span data-stu-id="46043-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="46043-137">Stækkið flýtiflipann **Aðferðir** og veljið línuna með **Heitinu** *Áætla stofnun vinnu* í hnitanetinu **Eftirstandandi aðferðir**.</span><span class="sxs-lookup"><span data-stu-id="46043-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="46043-138">Veljið örina sem vísar í **Valdar aðferðir** til að fara valda línu í þeim dálki.</span><span class="sxs-lookup"><span data-stu-id="46043-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="46043-139">(Aðeins er hægt að hafa eina valda aðferð í einu sem notar annaðhvort *WHSScheduleWorkCreationWaveStepMethod* eða *createWork* þannig að fyrirliggjandi lína með **Heiti aðferðar** *createWork* færist sjálfkrafa í hnitanetið **Eftirstandandi aðferðir**.)</span><span class="sxs-lookup"><span data-stu-id="46043-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="46043-140">Stilla þröskuldsgögn fyrir úrvinnslu bylgjuverks</span><span class="sxs-lookup"><span data-stu-id="46043-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="46043-141">Kerfið stofnar sjálfgefin þröskuldsgögn fyrir úrvinnslu bylgjuverks í fyrsta skipti sem bylgjuferli er keyrt með því að nota einhverja verktengda vinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="46043-142">Gögnin eru notuð til að stjórna því hvenær bylgjuvinnsla mun keyra ósamstillt og vera tengd verki, sem gerir henni kleift að vinna úr og stofna vinnu samhliða.</span><span class="sxs-lookup"><span data-stu-id="46043-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="46043-143">Sjálfgefin gögn munu í upphafi nota þröskuldsgildið 15 fyrir lágmarksfjölda hleðslulína (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="46043-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="46043-144">Þetta þýðir að þegar kerfið vinnur úr bylgju með fleiri en 15 hleðslulínum notar það ósamstæða verkvinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="46043-145">Hægt er að setja inn/uppfæra þessi gögn handvirkt í töflunni **WHSWaveTaskProcessingThresholdParameters** í prófunarumhverfinu, en ef breyta þarf þessari stillingu í vinnsluumhverfi verður að hafa samskipti við notendaþjónustu Microsoft til að óska eftir uppfærslunni.</span><span class="sxs-lookup"><span data-stu-id="46043-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="46043-146">Unnið með eiginleikann</span><span class="sxs-lookup"><span data-stu-id="46043-146">Work with the feature</span></span>

<span data-ttu-id="46043-147">Þegar aðgerðin *Áætla stofnun vinnu* er virkjuð mun bylgjuvinnsla stofna áætlaða vinnu sem verður á endanum notuð af nýju stofnferli vinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="46043-148">Við stofnun vinnu verður lokað fyrir vinnu með því að nota eiginleikann *Vinnulokun fyrir allt fyrirtækið*.</span><span class="sxs-lookup"><span data-stu-id="46043-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="46043-149">Eftirfarandi flæðirit sýnir hvernig áætluð vinna er stofnuð við bylgjuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Áætla stofnun vinnu](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="46043-151">áætluð vinna</span><span class="sxs-lookup"><span data-stu-id="46043-151">Planned work</span></span>

<span data-ttu-id="46043-152">Síðan **Upplýsingar um áætlaða vinnu** (**Vöruhúsakerfi \> Vinna \> Upplýsingar um áætlaða vinnu**) sýnir upplýsingar um áætlaða vinnu sem er upphaflega stofnuð í bylgjuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="46043-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="46043-153">Eftirtalin **Staða ferlis** gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="46043-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="46043-154">**Í biðröð** - Áætluð vinna bíður þess að vera notuð til að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="46043-155">**Lokið** – Áætluð vinna hefur verið notuð til að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="46043-156">**Mistókst** – Ekki tókst að vinna bylgjuna.</span><span class="sxs-lookup"><span data-stu-id="46043-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="46043-157">Athugið að áætluð vinna getur verið í stöðu sem **Mistókst** með eða án tengdrar raunvinnu.</span><span class="sxs-lookup"><span data-stu-id="46043-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="46043-158">Þegar stofnferli raunverulegrar vinnu tekst ekki helst raunveruleg vinna í stöðunni *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="46043-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="46043-159">Runuvinnsla fyrir stofnferli vinnu</span><span class="sxs-lookup"><span data-stu-id="46043-159">Batch job for the work creation process</span></span>

<span data-ttu-id="46043-160">Til að skoða runuvinnslur fyrir vinnslubylgjur skal velja **Runuvinnslur** á aðgerðasvæðinu á **Allar bylgjur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="46043-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="46043-161">Héðan er hægt að skoða allar upplýsingar um runuverk fyrir hvert runuvinnslukenni.</span><span class="sxs-lookup"><span data-stu-id="46043-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]