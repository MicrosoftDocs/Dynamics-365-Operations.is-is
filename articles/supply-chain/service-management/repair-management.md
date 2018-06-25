---
title: "Viðgerðarstjórnun"
description: "Flokkaðu vandamál á kerfisbundinn hátt til auðvelda tillögur að lausnum sem hafa gengið vel áður."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a><span data-ttu-id="6feda-103">Viðgerðarstjórnun</span><span class="sxs-lookup"><span data-stu-id="6feda-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6feda-104">Fyrir viðgerðarstjórnun geturðu flokkað vandamál kerfisbundið.</span><span class="sxs-lookup"><span data-stu-id="6feda-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="6feda-105">Þetta er til að hjálpa með tillögur að lausnum sem hafa gengið vel áður.</span><span class="sxs-lookup"><span data-stu-id="6feda-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="6feda-106">Þú setur upp stillingar einkenna, greiningar og úrlausnar.</span><span class="sxs-lookup"><span data-stu-id="6feda-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="6feda-107">Hægt er að nota þær allar seinna þegar þú færð svipaða vöru til viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="6feda-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="6feda-108">Þú getur einnig sett upp viðgerðarstig sem geta fylgst með framvindu viðgerðarverkefnis.</span><span class="sxs-lookup"><span data-stu-id="6feda-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="6feda-109">Uppsetning viðgerðarstjórnar</span><span class="sxs-lookup"><span data-stu-id="6feda-109">Setting up repair management</span></span>

<span data-ttu-id="6feda-110">Notaðu eftirfarandi skjámyndir uppsetningar til að slá inn upplýsingar sem nota skal til að tilgreina einkenni, greiningu og úrlausn viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="6feda-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="6feda-111">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="6feda-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="6feda-112">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Einkennasvæði**.</span><span class="sxs-lookup"><span data-stu-id="6feda-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="6feda-113">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Greiningarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="6feda-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="6feda-114">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Úrlausnir**.</span><span class="sxs-lookup"><span data-stu-id="6feda-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="6feda-115">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Viðgerðarstig**.</span><span class="sxs-lookup"><span data-stu-id="6feda-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="6feda-116">Einkenni og skilyrði</span><span class="sxs-lookup"><span data-stu-id="6feda-116">Symptoms and conditions</span></span>

<span data-ttu-id="6feda-117">Einkenni eru hvernig viðskiptavinurinn lýsir vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="6feda-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="6feda-118">Einkenni eru athuganir viðskiptavinar sem gefa til kynna þörf fyrir viðgerð.</span><span class="sxs-lookup"><span data-stu-id="6feda-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="6feda-119">Hægt er að setja upp einkennasvæði, einkennakóða og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="6feda-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="6feda-120">Einkennasvæðið nær yfir bilunarþáttinn og einkenniskóðinn nær yfir bilunareinkennin.</span><span class="sxs-lookup"><span data-stu-id="6feda-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="6feda-121">Skilyrðin lýsa kringumstæðum eða umhverfi sem er til staðar þegar vandamálið kemur fram.</span><span class="sxs-lookup"><span data-stu-id="6feda-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="6feda-122">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="6feda-122">**Example**</span></span>

<span data-ttu-id="6feda-123">Komið er með tölvu í viðgerð vegna þess að harði diskurinn bilar eftir langan notkunartíma.</span><span class="sxs-lookup"><span data-stu-id="6feda-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="6feda-124">Bilun á harða disknum veldur villu með bláum skjá.</span><span class="sxs-lookup"><span data-stu-id="6feda-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="6feda-125">Tæknimaðurinn sem fær tölvuna færir inn eftirfarandi einkenni og skilyrði:</span><span class="sxs-lookup"><span data-stu-id="6feda-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="6feda-126">Einkennasvæðið er harði diskurinn</span><span class="sxs-lookup"><span data-stu-id="6feda-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="6feda-127">Einkennakóðinn er villan með bláum skjá</span><span class="sxs-lookup"><span data-stu-id="6feda-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="6feda-128">Skilyrðin eru að diskurinn bilar eftir langvarandi notkun</span><span class="sxs-lookup"><span data-stu-id="6feda-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="6feda-129">Greining og lausnir</span><span class="sxs-lookup"><span data-stu-id="6feda-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="6feda-130">Svæðin greining og lausnir eru yrðingar frá sjónarhorni viðgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="6feda-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="6feda-131">Þetta eru skrefin sem tæknimaður fór í gegnum til þess að kanna vandamálið.</span><span class="sxs-lookup"><span data-stu-id="6feda-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="6feda-132">Greiningarsvæðið nær yfir aðgerðina sem verður að eiga sér stað til þess að leysa viðfangsefnið.</span><span class="sxs-lookup"><span data-stu-id="6feda-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="6feda-133">Greiningarkóðinn sýnir hvernig vandamálið var meðhöndlað og lausn vandamálsins gæti falist í viðgerð vöru, að henni sé skipt út eða því að viðskiptavinur hætti við pöntunina.</span><span class="sxs-lookup"><span data-stu-id="6feda-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="6feda-134">Til dæmis, ef gert er við tölvuna, gæti greiningarsvæðið verið „gallaður hluti“, greiningarkóðinn gæti verið „nýtt skjákort sett upp“ og úrlausnin gæti verið „skipt um“.</span><span class="sxs-lookup"><span data-stu-id="6feda-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="6feda-135">Viðgerðarstig</span><span class="sxs-lookup"><span data-stu-id="6feda-135">Repair stages</span></span>

<span data-ttu-id="6feda-136">Viðgerðarstig taka fram hver framvindan er í viðgerðarferlinu.</span><span class="sxs-lookup"><span data-stu-id="6feda-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="6feda-137">Viðgerðarstigið er með útskráningarfæribreytuna **Lokið** sem gefur til kynna að viðgerðarlínunni sé lokið og lokadagsetning og tími hefur verið skráður.</span><span class="sxs-lookup"><span data-stu-id="6feda-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="6feda-138">Notkun viðgerðarstjórnunar</span><span class="sxs-lookup"><span data-stu-id="6feda-138">Applying repair management</span></span>

<span data-ttu-id="6feda-139">Til þess að nota viðgerðarstjórnun á vöru, verður að setja vöruna upp með þjónustuhlutatengslum í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6feda-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="6feda-140">Úr þjónustupöntuninni er síðan hægt að stofna viðgerðarlínu með upplýsingum um núverandi verkefni.</span><span class="sxs-lookup"><span data-stu-id="6feda-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="6feda-141">Í viðgerðarlínunni er þjónustuhluturinn sem er í viðgerð síðan skilgreindur og upplýsingar gefnar um einkenni, greiningu og framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="6feda-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="6feda-142">Einnig er hægt að stofna athugasemd í viðgerðarlínuna.</span><span class="sxs-lookup"><span data-stu-id="6feda-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="6feda-143">Hægt er að stofna viðhaldslínur fyrir hvert skref í viðgerðarferlinu.</span><span class="sxs-lookup"><span data-stu-id="6feda-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="6feda-144">Stofna viðgerðarlínu í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="6feda-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="6feda-145">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="6feda-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6feda-146">Veljið þjónustupöntunina með þjónustuhlutnum sem þarfnast viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="6feda-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="6feda-147">Smelltu á **Viðgerð** \> **Viðgerðarlínur** til að opna skjámyndina **Viðgerðarlínur**.</span><span class="sxs-lookup"><span data-stu-id="6feda-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="6feda-148">Stutt á CTRL+N til að stofna nýja línu.</span><span class="sxs-lookup"><span data-stu-id="6feda-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="6feda-149">Velja þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="6feda-149">Select a service object.</span></span> <span data-ttu-id="6feda-150">Hægt er að velja hvaða þjónustuhlut sem settur hefur verið upp með hlutatengslum í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6feda-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="6feda-151">Veldu eitthvað af forstilltum einkennum, greiningum og framkvæmdargildi sem eru viðeigandi í viðgerðarlínunni og smelltu síðan á flipann **Athuga** til að búa til minnismiða á viðgerðarlínunni, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="6feda-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="6feda-152">Styðjið á CTRL+S til þess að vista nýju viðgerðarlínuna.</span><span class="sxs-lookup"><span data-stu-id="6feda-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="6feda-153">Reiturinn **Stofna dagsetningu og tíma** á flipanum **Almennt** í skjámyndinni **Viðgerðarlínur** er uppfærður þegar vistun á sér stað.</span><span class="sxs-lookup"><span data-stu-id="6feda-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="6feda-154">Að fylgjast með framvindu og finna úrlausn á viðgerðarverkefni</span><span class="sxs-lookup"><span data-stu-id="6feda-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="6feda-155">Hægt er að stilla viðgerðarstig viðgerðarlínu til að fylgjast með framvindu viðgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="6feda-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="6feda-156">Þegar viðgerðarverkefni er leyst er hægt að loka viðgerðarlínunni.</span><span class="sxs-lookup"><span data-stu-id="6feda-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="6feda-157">Setjið viðgerðarstigið á stig með **Lokið** eiginleikann virkan.</span><span class="sxs-lookup"><span data-stu-id="6feda-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="6feda-158">Núverandi dagsetning og tími er skráður sem tími viðgerðarloka í línuna.</span><span class="sxs-lookup"><span data-stu-id="6feda-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="6feda-159">Loka viðgerðarlínu fyrir leyst verkefni</span><span class="sxs-lookup"><span data-stu-id="6feda-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="6feda-160">Opnaðu skjámyndina **Viðgerðarlínur**.</span><span class="sxs-lookup"><span data-stu-id="6feda-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="6feda-161">Fylgdu ferlinu fyrr í þessu efnisatriði til að búa til viðgerðarlínu.</span><span class="sxs-lookup"><span data-stu-id="6feda-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="6feda-162">Velja viðgerðarlínu með viðgerðarverkefni sem ætlunin er að loka.</span><span class="sxs-lookup"><span data-stu-id="6feda-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="6feda-163">Í reitnum **Viðgerðarsvið** skal velja stig með eiginleikann **Lokið** virkan.</span><span class="sxs-lookup"><span data-stu-id="6feda-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  


