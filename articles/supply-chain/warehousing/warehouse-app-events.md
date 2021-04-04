---
title: Viðburðir vöruhúsaforrits
description: Þetta efnisatriði lýsir úrvinnslu á viðburðum vöruhúsaforrits sem notaðir eru til að vinna úr skilaboðum um viðburð vöruhúsaforrits sem hluti af runuvinnslu.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248644"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="f029d-103">Vinnsla viðburða í vöruhúsaforriti</span><span class="sxs-lookup"><span data-stu-id="f029d-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f029d-104">Runuvinnslur sem keyra í Supply Chain Management geta notað gögn úr þessari biðröð til að vinna úr viðburðum sem vöruhúsaforritið gefur út til að bregðast við tilkynntum viðburðum eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f029d-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="f029d-105">Þessi eiginleiki bætir viðeigandi viðburðum við biðröðina sem svar við tilteknum gerðum aðgerða sem starfsmenn sem nota forritið grípa til.</span><span class="sxs-lookup"><span data-stu-id="f029d-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="f029d-106">Dæmi er þegar verið er að nota eiginleikann **Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti**, verða haus og línur flutningspöntunar stofnaðar og uppfærðar í bakvinnslunni þegar kerfið keyrir runuvinnsluna **Vinna úr viðburðum vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="f029d-107">Virkja eiginleikann fyrir „Vinna úr viðburðum vöruhúsaforrits“</span><span class="sxs-lookup"><span data-stu-id="f029d-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="f029d-108">Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f029d-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="f029d-109">Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f029d-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="f029d-110">Eiginleikinn fyrir „Vinna úr viðburðum vöruhúsaforrits“ er sýndur sem:</span><span class="sxs-lookup"><span data-stu-id="f029d-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="f029d-111">**Eining** - Vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f029d-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="f029d-112">**Heiti eiginleika** - Vinna úr viðburðum vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="f029d-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="f029d-113">Setja upp runuvinnslu til að vinna úr viðburðum vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="f029d-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="f029d-114">Vinna úr viðburðum vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="f029d-114">Process warehouse app events</span></span>

<span data-ttu-id="f029d-115">Setjið upp áætlaða runuvinnslu til að vinna úr viðburðum í vöruhúsaforriti fyrir stofnun flutningspöntunar og línuuppfærslur.</span><span class="sxs-lookup"><span data-stu-id="f029d-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="f029d-116">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr viðburðum vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="f029d-117">Svarglugginn fyrir „Vinna úr viðburðum vöruhúsaforrits“ opnast.</span><span class="sxs-lookup"><span data-stu-id="f029d-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="f029d-118">Stækkið flýtiflipann **Keyra í bakgrunni** og stillið **Runuvinnsla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f029d-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="f029d-119">Í flýtiflipanum **Keyra í bakgrunni** skal velja **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="f029d-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="f029d-120">Svarglugginn **Skilgreina endurtekningu** opnast.</span><span class="sxs-lookup"><span data-stu-id="f029d-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="f029d-121">Stillið keyrslu áætlunar eftir þörfum fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f029d-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="f029d-122">Veljið **Í lagi** til að fara aftur í svargluggann **Vinna úr viðburðum vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="f029d-123">Veljið **Í lagi** í svarglugganum **Vinna úr viðburðum vöruhúsaforrits** til að bæta runuvinnslunni við runuröðina.</span><span class="sxs-lookup"><span data-stu-id="f029d-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="f029d-124">Fyrirspurn um viðburði vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="f029d-124">Query warehouse app events</span></span>

<span data-ttu-id="f029d-125">Hægt er að skoða viðburðaröðina og viðburðaskilaboðin sem vöruhúsaforritið býr til með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="f029d-126">Hefðbundin vinnsla á viðburðaröð</span><span class="sxs-lookup"><span data-stu-id="f029d-126">The standard event queue process</span></span>

<span data-ttu-id="f029d-127">Viðburðaröð vöruhúsaforrits er yfirleitt notuð með eftirfarandi tegundum flæðis:</span><span class="sxs-lookup"><span data-stu-id="f029d-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="f029d-128">Viðburði verður bætt við biðröðina með skilaboði fyrir viðburðinn.</span><span class="sxs-lookup"><span data-stu-id="f029d-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="f029d-129">Nýju skilaboðin eru upphaflega með viðburðarstöðuna á **Í bið**, sem þýðir að runuvinnslan **Vinna úr viðburðum vöruhúsaforrits** nær ekki í og vinnur úr þessum skilaboðum.</span><span class="sxs-lookup"><span data-stu-id="f029d-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="f029d-130">Um leið og staða viðburðar er uppfærð í **Í biðröð**, mun runuvinnsla viðburða **Vinna úr viðburðum vöruhúsaforrits** sækja og vinna úr viðburði.</span><span class="sxs-lookup"><span data-stu-id="f029d-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="f029d-131">Runuvinnslan uppfærir stöðu viðburðarins í annaðhvort **Lokið** eða **Tókst ekki**, fer eftir því hvort umbeðin vinnsla var möguleg.</span><span class="sxs-lookup"><span data-stu-id="f029d-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="f029d-132">Þegar öllum tengdum skilaboðum viðburðar er **Lokið**, er viðburðinum eytt úr biðröðinni.</span><span class="sxs-lookup"><span data-stu-id="f029d-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="f029d-133">Til að sjá ítarlegt dæmi skal fara í [Stofna flutningspöntun úr vinnslu vöruhúsaforrits](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="f029d-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="f029d-134">Meðhöndla villur í atburðum</span><span class="sxs-lookup"><span data-stu-id="f029d-134">Handle event errors</span></span>

<span data-ttu-id="f029d-135">Sem hluti af úrvinnslu viðburða vöruhúss, getur verið að umbeðin aðgerð skilaboðanna fái ekki úrvinnslu frá runuvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="f029d-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="f029d-136">Í þessu tilfelli breytist skilaboð viðburðarins í **Tókst ekki**.</span><span class="sxs-lookup"><span data-stu-id="f029d-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="f029d-137">Hægt er að nota upplýsingarnar **Runukladdi** til að komast að ástæðunni og grípa til nauðsynlegra aðgerða til að leysa vandamálið.</span><span class="sxs-lookup"><span data-stu-id="f029d-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="f029d-138">Til að sjá ítarlegt dæmi skal fara í [Stofna flutningspöntun úr vöruhúsaforriti](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="f029d-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="f029d-139">Til að endurstilla mislukkuð viðburðarskilaboð vöruhúsaforrits:</span><span class="sxs-lookup"><span data-stu-id="f029d-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="f029d-140">Farið í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="f029d-141">Í flýtiflipanum **Viðburðarskilaboð vöruhúsaforrits** skal finna og velja viðeigandi viðburð sem sýnir **Tókst ekki** í dálknum **Staða viðburðar**.</span><span class="sxs-lookup"><span data-stu-id="f029d-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="f029d-142">Veljið **Endurstilla** í tækjastikunni **Viðburðarskilaboð vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="f029d-143">Vinnið áfram þar til öll viðeigandi skilaboð eru endurstillt.</span><span class="sxs-lookup"><span data-stu-id="f029d-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="f029d-144">Einnig er hægt að fjarlægja **tókst ekki** viðburðarskilaboð með því að nota **Eyða** valkostinn í tækjastikunni **Viðburðarskilaboð vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="f029d-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]