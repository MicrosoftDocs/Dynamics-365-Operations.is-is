---
title: "Tenging við hjálpargögnin"
description: "Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations og veitir yfirlit yfir hvernig eigi að tengja þá og yfirlit yfir hvernig eigi að stofna sérsniðna hjálp."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="2e9af-103">Tenging við hjálpargögnin</span><span class="sxs-lookup"><span data-stu-id="2e9af-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e9af-104">Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e9af-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2e9af-105">Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.</span><span class="sxs-lookup"><span data-stu-id="2e9af-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="2e9af-106">Högun Hjálpar</span><span class="sxs-lookup"><span data-stu-id="2e9af-106">Help architecture</span></span>
<span data-ttu-id="2e9af-107">Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e9af-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="2e9af-108">Hjálparkerfi innan vörunnar sækir greinar úr svæði Finance and Operations á https://docs.microsoft.com auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2e9af-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="2e9af-109">Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.</span><span class="sxs-lookup"><span data-stu-id="2e9af-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="2e9af-110">[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="2e9af-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="2e9af-111">Tenging við hjálparkerfi</span><span class="sxs-lookup"><span data-stu-id="2e9af-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="2e9af-112">Flipinn **Verkefnaleiðbeiningar** er ekki tiltækur eins og er í Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="2e9af-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="2e9af-113">Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="2e9af-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="2e9af-114">Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni.</span><span class="sxs-lookup"><span data-stu-id="2e9af-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="2e9af-115">Einnig er hægt að fá aðgerðahjálp á svæðinu docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) fyrir bæði Retail og Talent</span><span class="sxs-lookup"><span data-stu-id="2e9af-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="2e9af-116">Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="2e9af-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="2e9af-117">[![Snið kerfisfæribreyta með Stillingar fyrir hjálp ](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) á **kerfisfæribreytum** síðunni, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2e9af-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e9af-118">Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="2e9af-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="2e9af-119">Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.[![Tengjast LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="2e9af-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="2e9af-120">Veljið Lifecycle Services verk til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="2e9af-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="2e9af-121">Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .</span><span class="sxs-lookup"><span data-stu-id="2e9af-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="2e9af-122">Ef þú notar Finance and Operations, fyrir Microsoft efni, skaltu velja febrúar 2017 QPC Unified Library fyrir Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e9af-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="2e9af-123">Við munum gefa út safn í júlí fyrir Retail.</span><span class="sxs-lookup"><span data-stu-id="2e9af-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="2e9af-124">Þú þarft ekki að velja safn fyrir Talent — búið er að setja tengingu við rétt safn fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="2e9af-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="2e9af-125">Velja birtingarröð BPM safna.</span><span class="sxs-lookup"><span data-stu-id="2e9af-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="2e9af-126">Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.</span><span class="sxs-lookup"><span data-stu-id="2e9af-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="2e9af-127">Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="2e9af-128">Nú sérðu verkefnaleiðbeiningar sem eiga við þá síðu sem þú ert á í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e9af-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="2e9af-129">Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.</span><span class="sxs-lookup"><span data-stu-id="2e9af-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="2e9af-130">Sýnir þýddar leiðbeiningar verkefninu</span><span class="sxs-lookup"><span data-stu-id="2e9af-130">Showing translated task guides</span></span>

<span data-ttu-id="2e9af-131">Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started).</span><span class="sxs-lookup"><span data-stu-id="2e9af-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="2e9af-132">Ef þú notar Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí.</span><span class="sxs-lookup"><span data-stu-id="2e9af-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="2e9af-133">Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2e9af-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2e9af-134">Þó að margar verkefnaleiðbeiningar hafi verið þýddar sýnir Finance and Operations-biðlarinn ekki þýdd heiti verkefnaleiðbeininga eins og er.</span><span class="sxs-lookup"><span data-stu-id="2e9af-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="2e9af-135">Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu.</span><span class="sxs-lookup"><span data-stu-id="2e9af-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="2e9af-136">Við munum gefa út uppfærða safn með fleiri þýðingum.</span><span class="sxs-lookup"><span data-stu-id="2e9af-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="2e9af-137">Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="2e9af-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="2e9af-138">Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="2e9af-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="2e9af-139">Stofnun sérsniðinnar hjálpar</span><span class="sxs-lookup"><span data-stu-id="2e9af-139">Creating custom help</span></span>
<span data-ttu-id="2e9af-140">Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations og fyrir Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library.</span><span class="sxs-lookup"><span data-stu-id="2e9af-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="2e9af-141">Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="2e9af-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="2e9af-142">Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="2e9af-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="2e9af-143">Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum.</span><span class="sxs-lookup"><span data-stu-id="2e9af-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="2e9af-144">Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="2e9af-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="2e9af-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2e9af-145">See also</span></span>
--------

[<span data-ttu-id="2e9af-146">Hjálparyfirlit</span><span class="sxs-lookup"><span data-stu-id="2e9af-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="2e9af-147">yfirlit verkskráningar</span><span class="sxs-lookup"><span data-stu-id="2e9af-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="2e9af-148">Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun</span><span class="sxs-lookup"><span data-stu-id="2e9af-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





