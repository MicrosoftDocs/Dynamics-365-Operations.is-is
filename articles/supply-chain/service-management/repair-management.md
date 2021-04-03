---
title: Viðgerðarstjórnun
description: Flokkaðu vandamál á kerfisbundinn hátt til auðvelda tillögur að lausnum sem hafa gengið vel áður.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470642"
---
# <a name="repair-management"></a><span data-ttu-id="b3aa9-103">Viðgerðarstjórnun</span><span class="sxs-lookup"><span data-stu-id="b3aa9-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b3aa9-104">Fyrir viðgerðarstjórnun geturðu flokkað vandamál kerfisbundið.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="b3aa9-105">Þetta er til að hjálpa með tillögur að lausnum sem hafa gengið vel áður.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="b3aa9-106">Þú setur upp stillingar einkenna, greiningar og úrlausnar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="b3aa9-107">Hægt er að nota þær allar seinna þegar þú færð svipaða vöru til viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="b3aa9-108">Þú getur einnig sett upp viðgerðarstig sem geta fylgst með framvindu viðgerðarverkefnis.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="b3aa9-109">Uppsetning viðgerðarstjórnar</span><span class="sxs-lookup"><span data-stu-id="b3aa9-109">Setting up repair management</span></span>

<span data-ttu-id="b3aa9-110">Notaðu eftirfarandi skjámyndir uppsetningar til að slá inn upplýsingar sem nota skal til að tilgreina einkenni, greiningu og úrlausn viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="b3aa9-111">Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="b3aa9-112">Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Einkennasvæði**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="b3aa9-113">Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Greiningarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="b3aa9-114">Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Úrlausnir**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="b3aa9-115">Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Viðgerðarstig**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="b3aa9-116">Einkenni og skilyrði</span><span class="sxs-lookup"><span data-stu-id="b3aa9-116">Symptoms and conditions</span></span>

<span data-ttu-id="b3aa9-117">Einkenni eru hvernig viðskiptavinurinn lýsir vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="b3aa9-118">Einkenni eru athuganir viðskiptavinar sem gefa til kynna þörf fyrir viðgerð.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="b3aa9-119">Hægt er að setja upp einkennasvæði, einkennakóða og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="b3aa9-120">Einkennasvæðið nær yfir bilunarþáttinn og einkenniskóðinn nær yfir bilunareinkennin.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="b3aa9-121">Skilyrðin lýsa kringumstæðum eða umhverfi sem er til staðar þegar vandamálið kemur fram.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="b3aa9-122">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b3aa9-122">**Example**</span></span>

<span data-ttu-id="b3aa9-123">Komið er með tölvu í viðgerð vegna þess að harði diskurinn bilar eftir langan notkunartíma.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="b3aa9-124">Bilun á harða disknum veldur villu með bláum skjá.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="b3aa9-125">Tæknimaðurinn sem fær tölvuna færir inn eftirfarandi einkenni og skilyrði:</span><span class="sxs-lookup"><span data-stu-id="b3aa9-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="b3aa9-126">Einkennasvæðið er harði diskurinn</span><span class="sxs-lookup"><span data-stu-id="b3aa9-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="b3aa9-127">Einkennakóðinn er villan með bláum skjá</span><span class="sxs-lookup"><span data-stu-id="b3aa9-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="b3aa9-128">Skilyrðin eru að diskurinn bilar eftir langvarandi notkun</span><span class="sxs-lookup"><span data-stu-id="b3aa9-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="b3aa9-129">Greining og lausnir</span><span class="sxs-lookup"><span data-stu-id="b3aa9-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="b3aa9-130">Svæðin greining og lausnir eru yrðingar frá sjónarhorni viðgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="b3aa9-131">Þetta eru skrefin sem tæknimaður fór í gegnum til þess að kanna vandamálið.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="b3aa9-132">Greiningarsvæðið nær yfir aðgerðina sem verður að eiga sér stað til þess að leysa viðfangsefnið.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="b3aa9-133">Greiningarkóðinn sýnir hvernig vandamálið var meðhöndlað og lausn vandamálsins gæti falist í viðgerð vöru, að henni sé skipt út eða því að viðskiptavinur hætti við pöntunina.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="b3aa9-134">Til dæmis, ef gert er við tölvuna, gæti greiningarsvæðið verið „gallaður hluti“, greiningarkóðinn gæti verið „nýtt skjákort sett upp“ og úrlausnin gæti verið „skipt um“.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="b3aa9-135">Viðgerðarstig</span><span class="sxs-lookup"><span data-stu-id="b3aa9-135">Repair stages</span></span>

<span data-ttu-id="b3aa9-136">Viðgerðarstig taka fram hver framvindan er í viðgerðarferlinu.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="b3aa9-137">Viðgerðarstigið er með útskráningarfæribreytuna **Lokið** sem gefur til kynna að viðgerðarlínunni sé lokið og lokadagsetning og tími hefur verið skráður.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="b3aa9-138">Notkun viðgerðarstjórnunar</span><span class="sxs-lookup"><span data-stu-id="b3aa9-138">Applying repair management</span></span>

<span data-ttu-id="b3aa9-139">Til þess að nota viðgerðarstjórnun á vöru, verður að setja vöruna upp með þjónustuhlutatengslum í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="b3aa9-140">Úr þjónustupöntuninni er síðan hægt að stofna viðgerðarlínu með upplýsingum um núverandi verkefni.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="b3aa9-141">Í viðgerðarlínunni er þjónustuhluturinn sem er í viðgerð síðan skilgreindur og upplýsingar gefnar um einkenni, greiningu og framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="b3aa9-142">Einnig er hægt að stofna athugasemd í viðgerðarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="b3aa9-143">Hægt er að stofna viðhaldslínur fyrir hvert skref í viðgerðarferlinu.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="b3aa9-144">Stofna viðgerðarlínu í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="b3aa9-145">Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b3aa9-146">Veljið þjónustupöntunina með þjónustuhlutnum sem þarfnast viðgerðar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="b3aa9-147">Veljið **Viðgerð** \> **Viðgerðarlínur** til að opna skjámyndina **Viðgerðarlínur**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="b3aa9-148">Veljið **Nýtt** til að stofna nýja línu.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="b3aa9-149">Velja þjónustuhlut.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-149">Select a service object.</span></span> <span data-ttu-id="b3aa9-150">Hægt er að velja hvaða þjónustuhlut sem settur hefur verið upp með hlutatengslum í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="b3aa9-151">Veldu eitthvað af forstilltum einkennum, greiningum og framkvæmdargildi sem eru viðeigandi í viðgerðarlínunni og veldu síðan flipann **Athuga** til að búa til minnismiða á viðgerðarlínunni, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="b3aa9-152">Veljið **Vista** til að vista nýju viðgerðarlínuna.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="b3aa9-153">Reiturinn **Stofna dagsetningu og tíma** á flipanum **Almennt** í skjámyndinni **Viðgerðarlínur** er uppfærður þegar vistun á sér stað.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="b3aa9-154">Að fylgjast með framvindu og finna úrlausn á viðgerðarverkefni</span><span class="sxs-lookup"><span data-stu-id="b3aa9-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="b3aa9-155">Hægt er að stilla viðgerðarstig viðgerðarlínu til að fylgjast með framvindu viðgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="b3aa9-156">Þegar viðgerðarverkefni er leyst er hægt að loka viðgerðarlínunni.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="b3aa9-157">Setjið viðgerðarstigið á stig með **Lokið** eiginleikann virkan.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="b3aa9-158">Núverandi dagsetning og tími er skráður sem tími viðgerðarloka í línuna.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="b3aa9-159">Loka viðgerðarlínu fyrir leyst verkefni</span><span class="sxs-lookup"><span data-stu-id="b3aa9-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="b3aa9-160">Opnaðu skjámyndina **Viðgerðarlínur**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="b3aa9-161">Fylgdu ferlinu fyrr í þessu efnisatriði til að búa til viðgerðarlínu.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="b3aa9-162">Velja viðgerðarlínu með viðgerðarverkefni sem ætlunin er að loka.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="b3aa9-163">Í reitnum **Viðgerðarsvið** skal velja stig með eiginleikann **Lokið** virkan.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]