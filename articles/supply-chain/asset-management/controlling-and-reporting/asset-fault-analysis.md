---
title: Bilanagreining eignar
description: Þetta efni skýrir greiningu eignabilunar í eignastýringu.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a26ee80eb52e40b60ace9b1494b3512d85f04cfe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837874"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="6946a-103">Bilanagreining eignar</span><span class="sxs-lookup"><span data-stu-id="6946a-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6946a-104">Í eignastýringu er hægt að greina skráningar eignabilana til að fá yfirsýn yfir heildarfjölda bilana sem eru skráðir á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="6946a-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="6946a-105">Hægt er að greina bilanaskráningar frá mismunandi sjónarhornum, til dæmis með áherslu á eignir, eignagerðir, virkar staðsetningar, bilunareinkenni eða bilanagerðir.</span><span class="sxs-lookup"><span data-stu-id="6946a-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="6946a-106">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Greiningu eignabilunar**.</span><span class="sxs-lookup"><span data-stu-id="6946a-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="6946a-107">Í glugganum **Útreikningur á greiningu eignabilunar** geturðu notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að eignabilanalínurnar séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="6946a-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="6946a-108">Til dæmis, ef þú setur inn töluna „1“ í reitinn, og þú ert með fjölþrepa skipulag virkra staðsetninga, verða allar eignabilanalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að bæta tímunum á línunni við af virkum staðsetningum sem eru staðsettar á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="6946a-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="6946a-109">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar eignabilanalínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="6946a-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="6946a-110">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar, bilunarástæður og bilunarúrræði á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="6946a-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="6946a-111">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="6946a-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="6946a-112">Á flipanum **Eignabilanagreining** smellirðu á hnappana **Flokka eftir...** til að birta smáatriðastigið sem þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="6946a-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="6946a-113">Virkjaðir hnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="6946a-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="6946a-114">Virkjaður eða afvirkjaðu hnappa með því að smella á þá.</span><span class="sxs-lookup"><span data-stu-id="6946a-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="6946a-115">Smelltu á **Uppfæra útreikninga** til að sýna val þitt á skjánum.</span><span class="sxs-lookup"><span data-stu-id="6946a-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="6946a-116">Í hvert skipti sem þú virkjar eða afvirkjar hnapp **Flokka eftir** skaltu muna að smella á hnappinn **Uppfæra útreikninga**.</span><span class="sxs-lookup"><span data-stu-id="6946a-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="6946a-117">Þetta er nauðsynlegt vegna þess að mikið magn af gögnum er unnið þar sem þú ert að endurreikna villulíkindi.</span><span class="sxs-lookup"><span data-stu-id="6946a-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="6946a-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6946a-118">Examples</span></span>

<span data-ttu-id="6946a-119">Það eru margar leiðir til að greina skráningar á bilunum.</span><span class="sxs-lookup"><span data-stu-id="6946a-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="6946a-120">Þessi kafli er með fimm dæmi um hvernig mismunandi gagnaval getur veitt meiri innsýn og smáatriði við greiningu á skráningum eignabilana.</span><span class="sxs-lookup"><span data-stu-id="6946a-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="6946a-121">Flokka eftir einkennum</span><span class="sxs-lookup"><span data-stu-id="6946a-121">Group by symptoms</span></span>

<span data-ttu-id="6946a-122">Í skjámyndinni hér að neðan er aðeins hnappurinn **Einkenni** valinn.</span><span class="sxs-lookup"><span data-stu-id="6946a-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="6946a-123">Bilanaskráningar hafa verið gerðar á þremur bilunareinkennum: „Loftleka“, „Sprungið öryggi“ og „Búnaður fastur“.</span><span class="sxs-lookup"><span data-stu-id="6946a-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="6946a-124">Í dálknum **Líkindi %** leggjast allar prósentur saman að 100%.</span><span class="sxs-lookup"><span data-stu-id="6946a-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="6946a-125">Líkindi eru byggð á öllum skráningum **Einkenna** í þessari bilagreiningu.</span><span class="sxs-lookup"><span data-stu-id="6946a-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Mynd 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="6946a-127">Flokka eftir einkennum og tímabili</span><span class="sxs-lookup"><span data-stu-id="6946a-127">Group by symptoms and time period</span></span>

<span data-ttu-id="6946a-128">Í skjámyndinni hér að neðan er **Ári** og **Mánuði** bætt við til að sýna hvernig hægt er að skoða bilanaskráningar á völdu tímabili.</span><span class="sxs-lookup"><span data-stu-id="6946a-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="6946a-129">Bilunareinkennin eru nú sýnd sem skráningar á ári/mánuði.</span><span class="sxs-lookup"><span data-stu-id="6946a-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="6946a-130">Í dálknum **Líkindi %**, ef þú bætir við öllum prósentum fyrir hvern mánuð, leggjast þær saman upp að 100%.</span><span class="sxs-lookup"><span data-stu-id="6946a-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="6946a-131">Líkindi eru byggð á skráningum **Einkenna** í þessari bilagreiningu.</span><span class="sxs-lookup"><span data-stu-id="6946a-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="6946a-132">Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunareinkenni til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunareinkenni.</span><span class="sxs-lookup"><span data-stu-id="6946a-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Mynd 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="6946a-134">Flokka eftir margfeldi einkenna og eigna</span><span class="sxs-lookup"><span data-stu-id="6946a-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="6946a-135">Samsetning eigna og eignategund er notuð til grundvallar við útreikninga sem sýndir eru í þremur skjámyndunum hér að neðan sem munu aukast í smáatriðum.</span><span class="sxs-lookup"><span data-stu-id="6946a-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="6946a-136">Almennt innihalda hnapparnir í **Flokka eftir dagsetningu**, **Flokka eftir eign**, **Flokka eftir virkri staðsetningu** aðgerðasvæðinu, sem og **Villa** hnappurinn (bilunarkenni), tímabil eða eignatengsl.</span><span class="sxs-lookup"><span data-stu-id="6946a-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="6946a-137">Hnapparnir **Einkenni**, **Svæði**, **Gerð**, **Orsök** og **Úrræði** eru flokkanir sem notaðar eru í bilunastjórnun til að greina skráningu eignabilana og finna vandamálasvið.</span><span class="sxs-lookup"><span data-stu-id="6946a-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="6946a-138">**Flokka eftir einkennum, eignum og eignategundum**</span><span class="sxs-lookup"><span data-stu-id="6946a-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="6946a-139">Í skjámyndinni hér að neðan var **Eignir** og **Gerð eigna** bætt við til að veita nánari upplýsingar varðandi skráningar á bilunum.</span><span class="sxs-lookup"><span data-stu-id="6946a-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="6946a-140">Bilunareinkennunum er nú skipt upp í samsetningarnar **Eignir** / **Gerð eigna** / **Einkenni**.</span><span class="sxs-lookup"><span data-stu-id="6946a-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="6946a-141">Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** í þessari röð verður útkoman 100%.</span><span class="sxs-lookup"><span data-stu-id="6946a-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="6946a-142">Líkindi eru byggð á skráningum **Einkenna** í þessari bilagreiningu.</span><span class="sxs-lookup"><span data-stu-id="6946a-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="6946a-143">Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunareinkenni til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunareinkenni.</span><span class="sxs-lookup"><span data-stu-id="6946a-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Mynd 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="6946a-145">**Flokka eftir tveimur einkennum, eignum og eignategundum**</span><span class="sxs-lookup"><span data-stu-id="6946a-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="6946a-146">Í skjámyndinni hér að neðan var **Svæði** bætt við **Einkenni**, **Eign** og **Gerð eigna** til að veita nánari upplýsingar varðandi skráningar á bilunum.</span><span class="sxs-lookup"><span data-stu-id="6946a-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="6946a-147">Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** á eign verður útkoman 100%.</span><span class="sxs-lookup"><span data-stu-id="6946a-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="6946a-148">Líkindi eru byggð á samsetningunni **Einkenni** og **Svæði** í þessari bilagreiningu.</span><span class="sxs-lookup"><span data-stu-id="6946a-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="6946a-149">Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunarsvæði til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunarsvæði.</span><span class="sxs-lookup"><span data-stu-id="6946a-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Mynd 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="6946a-151">**Flokka eftir þremur einkennum, eignum og eignategundum**</span><span class="sxs-lookup"><span data-stu-id="6946a-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="6946a-152">Í skjámyndinni hér að neðan var **Gerð** bætt við og ítarlegasti útreikningurinn í þessu dæmi er sýndur.</span><span class="sxs-lookup"><span data-stu-id="6946a-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="6946a-153">Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** á eign verður útkoman 100%.</span><span class="sxs-lookup"><span data-stu-id="6946a-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="6946a-154">Líkindi eru byggð á samsetningunni **Einkenni**, **Svæði** og **Gerð** í þessari bilagreiningu.</span><span class="sxs-lookup"><span data-stu-id="6946a-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="6946a-155">Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunargerð til að skoða betur til að finna leið til að takmarka fjölda skráninga á þeirri bilunargerð.</span><span class="sxs-lookup"><span data-stu-id="6946a-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Mynd 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="6946a-157">Til að fá yfirlit yfir allar bilanaskráningar sem stofnaðar eru í verkbeiðnum og viðhaldsbeiðnum smellirðu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna**.</span><span class="sxs-lookup"><span data-stu-id="6946a-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="6946a-158">Á síðunni **Bilanir eigna** skaltu velja eignarbilunarskráningu og stækka gluggann **Tengdar upplýsingar** til að sjá upplýsingar varðandi tengda verkbeiðni eða viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="6946a-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]