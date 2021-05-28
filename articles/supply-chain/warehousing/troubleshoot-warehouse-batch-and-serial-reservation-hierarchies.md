---
title: Úrræðaleit fyrir keyrslur vöruhúss og frátekningastigveldi raða
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með frátekningastigveldi sem nota runu- eða raðnúmeravíddir.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022547"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="c43ad-103">Úrræðaleit fyrir keyrslur vöruhúss og frátekningastigveldi raða</span><span class="sxs-lookup"><span data-stu-id="c43ad-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c43ad-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með frátekningastigveldi sem nota runu- eða raðnúmeravíddir.</span><span class="sxs-lookup"><span data-stu-id="c43ad-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="c43ad-105">Frekari upplýsingar er að finna í [Sveigjanleg frátektarregla á vídd vöruhúsastigs](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="c43ad-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="c43ad-106">Frátekningastigveldi vöru segir til um kröfur geymsluvídda sem þarf að uppfylla til að úthluta staðsetningu á eftirspurnarpöntun.</span><span class="sxs-lookup"><span data-stu-id="c43ad-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="c43ad-107">Hægt er að lýsa þessum víddum sem *víddum fyrir ofan staðsetningu* fyrir allar víddirnar sem þarf að uppfylla áður en staðsetningu er úthlutað og *víddir fyrir neðan staðsetningu* fyrir víddir sem hægt er að úthluta eftir að staðsetningu hefur verið úthlutað á eftirspurnarpöntunina.</span><span class="sxs-lookup"><span data-stu-id="c43ad-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="c43ad-108">Þessi frátekningastigveldi eru einnig þekkt sem *runa fyrir ofan* og *runa fyrir neðan* frátekningastigveldi, eða *raðnúmer fyrir ofan* og *raðnúmer fyrir neðan* frátekningastigveldi.</span><span class="sxs-lookup"><span data-stu-id="c43ad-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="c43ad-109">Aðeins er hægt að úthluta birgðum ef engar eyður eru í víddunum fyrir ofan staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c43ad-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="c43ad-110">Til dæmis má búast við að í *runa fyrir ofan* frátekningarstigveldi séu víddirnar **Svæði**, **Vöruhús** og **Rununúmer** tilgreindar í eftirspurnarpöntuninni.</span><span class="sxs-lookup"><span data-stu-id="c43ad-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="c43ad-111">Ef einhverjar af þessum víddum vantar mun úthlutunarferlið mistakast.</span><span class="sxs-lookup"><span data-stu-id="c43ad-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="c43ad-112">Hins vegar, í *runa fyrir neðan* eða *raðnúmer fyrir neðan* frátekningastigveldi gæti runu- eða raðnúmer verið tilgreint í eftirspurnarpöntuninni, en úthlutunarferlið krefst þess ekki.</span><span class="sxs-lookup"><span data-stu-id="c43ad-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="c43ad-113">Ég fæ eftirfarandi villuboð: „Til að úthluta bylgju verða hleðslulínur að tilgreina víddirnar fyrir ofan staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="c43ad-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="c43ad-114">Til að úthluta þessum víddum skal taka hleðslulínuna frá og endurgera hana.“</span><span class="sxs-lookup"><span data-stu-id="c43ad-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c43ad-115">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="c43ad-115">Issue description</span></span>

<span data-ttu-id="c43ad-116">Þegar notuð er vara með *runa fyrir ofan* frátekningastigveldi mun skipunin **Losa í vöruhús** á síðunni **Vinnusvæði hleðsluáætlunar** ekki virka ef reynt er að losa hleðslu fyrir hlutamagn.</span><span class="sxs-lookup"><span data-stu-id="c43ad-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="c43ad-117">Þessi villuskilaboð berast og engin vinna er stofnuð fyrir hlutamagnið.</span><span class="sxs-lookup"><span data-stu-id="c43ad-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="c43ad-118">Hins vegar, þegar notuð er vara sem er með *runa fyrir neðan* frátekningastigveldi, er hægt að losa hleðslu fyrir hlutamagn á síðunni **Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="c43ad-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c43ad-119">Ástæða vandamáls</span><span class="sxs-lookup"><span data-stu-id="c43ad-119">Issue cause</span></span>

<span data-ttu-id="c43ad-120">Þegar vídd er fyrir ofan víddina **Staðsetning** er sett upp í frátekningarstigveldi verður að tilgreina hana áður en hún er losuð í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="c43ad-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="c43ad-121">Ekki er hægt að losa hlutamagn ef ein eða fleiri vídd fyrir ofan **Staðsetning** eru ekki tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="c43ad-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="c43ad-122">Kvaðning sjálfvirkrar frátekningar fyrir rununúmer er sett í gang þó að tiltækar birgðir séu í boði.</span><span class="sxs-lookup"><span data-stu-id="c43ad-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c43ad-123">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="c43ad-123">Issue description</span></span>

<span data-ttu-id="c43ad-124">Þegar notuð er vara sem er með *runa fyrir ofan* frátekningastigveldi í vöruhúsi sem hefur ekki virkjað vöruhúsaferla og sjálfvirk frátekning er virkjuð, birtist kvaðning sjálfvirkrar frátekningar fyrir rununúmer þótt aðeins ein runa er tiltæk fyrir tiltekt.</span><span class="sxs-lookup"><span data-stu-id="c43ad-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="c43ad-125">Hins vegar þegar sama varan er notuð í vöruhúsi þar sem vöruhúsaferli eru virkjuð, er kvaðning sjálfvirkrar frátekningar ekki sýnd.</span><span class="sxs-lookup"><span data-stu-id="c43ad-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c43ad-126">Ástæða vandamáls</span><span class="sxs-lookup"><span data-stu-id="c43ad-126">Issue cause</span></span>

<span data-ttu-id="c43ad-127">Ef frátekningastigveldi er skilgreint sem *runa fyrir ofan* eða *raðnúmer fyrir ofan* verður alltaf að tilgreina vídd sem vísað er í (**Rununúmer** eða **Raðnúmer**) í eftirspurnarpöntunum.</span><span class="sxs-lookup"><span data-stu-id="c43ad-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="c43ad-128">Vöruhúsaferli gætu lokið upplýsingunum ef ein runa eða raðnúmer er í boði.</span><span class="sxs-lookup"><span data-stu-id="c43ad-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="c43ad-129">En þar sem vöruhúsið er ekki virkjað fyrir vöruhúsaferli, verður notandinn alltaf að tilgreina allar víddir fyrir ofan **Staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="c43ad-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="c43ad-130">Hólfasniðmát sem eru með hólfaskilyrðið Íhuga magn í birgðum taka ekki til greina núverandi lagerbirgðir fyrir runuvirkar vörur.</span><span class="sxs-lookup"><span data-stu-id="c43ad-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="c43ad-131">Frekari upplýsingar er að finna í [Hólfaskipting vöruhúss](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="c43ad-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="c43ad-132">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="c43ad-132">Issue description</span></span>

<span data-ttu-id="c43ad-133">Hólfasniðmát sem eru með hólfaskilyrðið *Íhuga magn í birgðum* taka ekki til greina núverandi lagerbirgðir fyrir *runu fyrir ofan* vörur.</span><span class="sxs-lookup"><span data-stu-id="c43ad-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="c43ad-134">Þau taka þær aðeins til greina ef rununúmerið er tilgreint í sölupöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="c43ad-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="c43ad-135">En þegar notuð er *runa fyrir ofan* vörur verða núverandi lagerbirgðir teknar til greina eins og vænta má.</span><span class="sxs-lookup"><span data-stu-id="c43ad-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c43ad-136">Ástæða vandamáls</span><span class="sxs-lookup"><span data-stu-id="c43ad-136">Issue cause</span></span>

<span data-ttu-id="c43ad-137">Hægt er að skilgreina haus hólfasniðmáts fyrir eftirspurnarleiðina *Pantað*, *Frátekið* eða *Losað*.</span><span class="sxs-lookup"><span data-stu-id="c43ad-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="c43ad-138">Fyrir eftirspurnarleiðina *Pantað* eiga sömu kröfur um frátekningastigveldi við og gilda um frátekningu eða losun í vöruhúsaferli.</span><span class="sxs-lookup"><span data-stu-id="c43ad-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="c43ad-139">Þar af leiðandi, fyrir vörur sem eru með *runa fyrir ofan* og *raðnúmer fyrir neðan* frátekningastigveldi, þarf að tilgreina runu eða raðnúmer í eftirspurnarpöntuninni (sölu eða flutning).</span><span class="sxs-lookup"><span data-stu-id="c43ad-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="c43ad-140">Annars er hægt að nota eftirspurnarleiðina *Frátekið* til að velja runu eða raðnúmer áður en eftirspurn eftir hólfaskiptingu í vöruhúsi er búin til.</span><span class="sxs-lookup"><span data-stu-id="c43ad-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
