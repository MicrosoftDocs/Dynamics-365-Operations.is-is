---
title: Tengja hjálparkerfið
description: Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561976"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="b8b68-103">Tengja hjálparkerfið</span><span class="sxs-lookup"><span data-stu-id="b8b68-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8b68-104">Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b8b68-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b8b68-105">Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.</span><span class="sxs-lookup"><span data-stu-id="b8b68-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="b8b68-106">Högun Hjálpar</span><span class="sxs-lookup"><span data-stu-id="b8b68-106">Help architecture</span></span>

<span data-ttu-id="b8b68-107">Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b8b68-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="b8b68-108">Hjálparkerfi innan vörunnar sækir greinar úr svæði Finance and Operations á https://docs.microsoft.com, auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b8b68-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="b8b68-109">Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.</span><span class="sxs-lookup"><span data-stu-id="b8b68-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="b8b68-110">[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="b8b68-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="b8b68-111">Tenging við hjálparkerfi</span><span class="sxs-lookup"><span data-stu-id="b8b68-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="b8b68-112">Flipinn **Verkleiðbeiningar** er ekki í boði eins og stendur í Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="b8b68-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="b8b68-113">Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="b8b68-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="b8b68-114">Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni.</span><span class="sxs-lookup"><span data-stu-id="b8b68-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="b8b68-115">Leiðbeiningar fyrir aðstoð er einnig að finna á docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) fyrir bæði Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="b8b68-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="b8b68-116">Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="b8b68-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="b8b68-117">[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="b8b68-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="b8b68-118">Á síðunni **Kerfisfæribreytur** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="b8b68-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8b68-119">Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="b8b68-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="b8b68-120">Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="b8b68-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="b8b68-121">[![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="b8b68-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="b8b68-122">Veljið Lifecycle Services verk til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="b8b68-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="b8b68-123">Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .</span><span class="sxs-lookup"><span data-stu-id="b8b68-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="b8b68-124">Fyrir Finance and Operations, fyrir Microsoft efni, skal velja nýjasta APQU Unified Library fyrir Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b8b68-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="b8b68-125">Safn verður gefið út fyrir Retail í nánustu framtíð.</span><span class="sxs-lookup"><span data-stu-id="b8b68-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="b8b68-126">Þú þarft ekki að velja safn fyrir Talent — búið er að setja tengingu við rétt safn fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="b8b68-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="b8b68-127">Velja birtingarröð BPM safna.</span><span class="sxs-lookup"><span data-stu-id="b8b68-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="b8b68-128">Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.</span><span class="sxs-lookup"><span data-stu-id="b8b68-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="b8b68-129">Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b8b68-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="b8b68-130">Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.</span><span class="sxs-lookup"><span data-stu-id="b8b68-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="b8b68-131">Sýnir þýddar leiðbeiningar verkefninu</span><span class="sxs-lookup"><span data-stu-id="b8b68-131">Showing translated task guides</span></span>

<span data-ttu-id="b8b68-132">Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started).</span><span class="sxs-lookup"><span data-stu-id="b8b68-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="b8b68-133">Ef þú notar Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí.</span><span class="sxs-lookup"><span data-stu-id="b8b68-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="b8b68-134">Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.</span><span class="sxs-lookup"><span data-stu-id="b8b68-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="b8b68-135">Þó að margar verkefnaleiðbeiningar hafi verið þýddar sýnir Finance and Operations-biðlarinn ekki þýdd heiti verkefnaleiðbeininga eins og er.</span><span class="sxs-lookup"><span data-stu-id="b8b68-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="b8b68-136">Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu.</span><span class="sxs-lookup"><span data-stu-id="b8b68-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="b8b68-137">Við munum gefa út uppfærða safn með fleiri þýðingum.</span><span class="sxs-lookup"><span data-stu-id="b8b68-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="b8b68-138">Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="b8b68-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="b8b68-139">Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="b8b68-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="b8b68-140">Stofnun sérsniðinnar hjálpar</span><span class="sxs-lookup"><span data-stu-id="b8b68-140">Creating custom help</span></span>

<span data-ttu-id="b8b68-141">Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="b8b68-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="b8b68-142">Stofna sérsniðna hjálp með verkefnaleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="b8b68-142">Create custom help with task guides</span></span>

<span data-ttu-id="b8b68-143">Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations og fyrir Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library.</span><span class="sxs-lookup"><span data-stu-id="b8b68-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="b8b68-144">Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="b8b68-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="b8b68-145">Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="b8b68-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="b8b68-146">Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum.</span><span class="sxs-lookup"><span data-stu-id="b8b68-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="b8b68-147">Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="b8b68-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="b8b68-148">Tengja sérsniðið svæði</span><span class="sxs-lookup"><span data-stu-id="b8b68-148">Connect a custom site</span></span>

<span data-ttu-id="b8b68-149">Microsoft hefur útvegað hvítbók og sýnikóða sem lýsa því hvernig á að stofna og tengja sérsniðið svæði hjálpar við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="b8b68-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="b8b68-150">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="b8b68-150">For more information, see:</span></span>

- [<span data-ttu-id="b8b68-151">Stofna sérsniðna hjálp fyrir Finance and Operations (hvítbók)</span><span class="sxs-lookup"><span data-stu-id="b8b68-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="b8b68-152">Sérsniðin hjálp GitHub-geymslu</span><span class="sxs-lookup"><span data-stu-id="b8b68-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="b8b68-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b8b68-153">Additional resources</span></span>

[<span data-ttu-id="b8b68-154">Hjálparyfirlit</span><span class="sxs-lookup"><span data-stu-id="b8b68-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="b8b68-155">yfirlit verkskráningar</span><span class="sxs-lookup"><span data-stu-id="b8b68-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="b8b68-156">Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun</span><span class="sxs-lookup"><span data-stu-id="b8b68-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
