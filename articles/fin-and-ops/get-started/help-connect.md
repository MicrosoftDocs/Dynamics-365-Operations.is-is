---
title: "Tenging við hjálpargögnin"
description: "Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations og veitir yfirlit yfir hvernig eigi að tengja þá og yfirlit yfir hvernig eigi að stofna sérsniðna hjálp."
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 87ca6afe817d27de12479f1b7d8155d11d800233
ms.openlocfilehash: a2ca5f5302751ad2c4ddc3c6921a8a9b6c2d57df
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="13c8f-103">Tenging við hjálpargögnin</span><span class="sxs-lookup"><span data-stu-id="13c8f-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13c8f-104">Þetta efnisatriði lýsir þáttum í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13c8f-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="13c8f-105">Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.</span><span class="sxs-lookup"><span data-stu-id="13c8f-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="13c8f-106">Högun Hjálpar</span><span class="sxs-lookup"><span data-stu-id="13c8f-106">Help architecture</span></span>
<span data-ttu-id="13c8f-107">Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13c8f-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="13c8f-108">Hjálparkerfi innan vörunnar sækir greinar úr svæði Finance and Operations á https://docs.microsoft.com, auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="13c8f-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="13c8f-109">Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.</span><span class="sxs-lookup"><span data-stu-id="13c8f-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="13c8f-110">[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="13c8f-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="13c8f-111">Tenging við hjálparkerfi</span><span class="sxs-lookup"><span data-stu-id="13c8f-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="13c8f-112">Flipinn **Verkefnaleiðbeiningar** er ekki tiltækur eins og er í Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="13c8f-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="13c8f-113">Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="13c8f-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="13c8f-114">Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni.</span><span class="sxs-lookup"><span data-stu-id="13c8f-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="13c8f-115">Leiðbeiningar fyrir aðstoð er einnig að finna á docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) fyrir bæði Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="13c8f-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>


<span data-ttu-id="13c8f-116">Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="13c8f-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="13c8f-117">[![Snið kerfisfæribreyta með Stillingar fyrir hjálp ](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) á **kerfisfæribreytum** síðunni, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13c8f-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13c8f-118">Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="13c8f-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="13c8f-119">Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast í **Kerfisfæribreytur** síðuna.[![Tengjast LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="13c8f-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="13c8f-120">Veljið Lifecycle Services verk til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="13c8f-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="13c8f-121">Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .</span><span class="sxs-lookup"><span data-stu-id="13c8f-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="13c8f-122">Fyrir Finance and Operations, fyrir Microsoft efni, skal velja nýjasta APQU Unified Library fyrir Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13c8f-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="13c8f-123">Safn verður gefið út fyrir Retail í nánustu framtíð.</span><span class="sxs-lookup"><span data-stu-id="13c8f-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="13c8f-124">Þú þarft ekki að velja safn fyrir Talent — búið er að setja tengingu við rétt safn fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="13c8f-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="13c8f-125">Velja birtingarröð BPM safna.</span><span class="sxs-lookup"><span data-stu-id="13c8f-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="13c8f-126">Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.</span><span class="sxs-lookup"><span data-stu-id="13c8f-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="13c8f-127">Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Þú sérð verkefnaleiðbeiningar sem eiga við síðu sem þú ert á í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13c8f-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="13c8f-128">Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.</span><span class="sxs-lookup"><span data-stu-id="13c8f-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="13c8f-129">Sýnir þýddar leiðbeiningar verkefninu</span><span class="sxs-lookup"><span data-stu-id="13c8f-129">Showing translated task guides</span></span>

<span data-ttu-id="13c8f-130">Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started).</span><span class="sxs-lookup"><span data-stu-id="13c8f-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="13c8f-131">Ef þú notar Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí.</span><span class="sxs-lookup"><span data-stu-id="13c8f-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="13c8f-132">Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.</span><span class="sxs-lookup"><span data-stu-id="13c8f-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="13c8f-133">Þó að margar verkefnaleiðbeiningar hafi verið þýddar sýnir Finance and Operations-biðlarinn ekki þýdd heiti verkefnaleiðbeininga eins og er.</span><span class="sxs-lookup"><span data-stu-id="13c8f-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="13c8f-134">Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu.</span><span class="sxs-lookup"><span data-stu-id="13c8f-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="13c8f-135">Við munum gefa út uppfærða safn með fleiri þýðingum.</span><span class="sxs-lookup"><span data-stu-id="13c8f-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="13c8f-136">Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="13c8f-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="13c8f-137">Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="13c8f-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="13c8f-138">Stofnun sérsniðinnar hjálpar</span><span class="sxs-lookup"><span data-stu-id="13c8f-138">Creating custom help</span></span>
<span data-ttu-id="13c8f-139">Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="13c8f-139">You can use task guides to create custom help, or connect a website to the Help pane.</span></span> 

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="13c8f-140">Stofna sérsniðna hjálp með verkefnaleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="13c8f-140">Create custom help with task guides</span></span>
<span data-ttu-id="13c8f-141">Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations og fyrir Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library.</span><span class="sxs-lookup"><span data-stu-id="13c8f-141">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="13c8f-142">Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="13c8f-142">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="13c8f-143">Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="13c8f-143">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="13c8f-144">Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum.</span><span class="sxs-lookup"><span data-stu-id="13c8f-144">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="13c8f-145">Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="13c8f-145">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="13c8f-146">Tengja sérsniðið svæði</span><span class="sxs-lookup"><span data-stu-id="13c8f-146">Connect a custom site</span></span>
<span data-ttu-id="13c8f-147">Microsoft hefur útvegað hvítbók og sýnikóða sem lýsa því hvernig á að stofna og tengja sérsniðið svæði hjálpar við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="13c8f-147">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="13c8f-148">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="13c8f-148">For more information, see:</span></span> 
- [<span data-ttu-id="13c8f-149">Stofna sérsniðna hjálp fyrir Finance and Operations (hvítbók)</span><span class="sxs-lookup"><span data-stu-id="13c8f-149">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="13c8f-150">Sérsniðin hjálp GitHub-geymslu</span><span class="sxs-lookup"><span data-stu-id="13c8f-150">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)



<a name="additional-resources"></a><span data-ttu-id="13c8f-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="13c8f-151">Additional resources</span></span>
--------

[<span data-ttu-id="13c8f-152">Hjálparyfirlit</span><span class="sxs-lookup"><span data-stu-id="13c8f-152">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="13c8f-153">yfirlit verkskráningar</span><span class="sxs-lookup"><span data-stu-id="13c8f-153">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="13c8f-154">Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun</span><span class="sxs-lookup"><span data-stu-id="13c8f-154">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





