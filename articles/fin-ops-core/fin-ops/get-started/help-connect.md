---
title: Tengja hjálparkerfið
description: Þetta efnisatriði lýsir þætti í hjálparkerfinu fyrir forrit Finance and Operations og veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537856"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="1ed88-103">Tengja hjálparkerfið</span><span class="sxs-lookup"><span data-stu-id="1ed88-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ed88-104">Þetta efni lýsir íhlutum hjálparkerfisins fyrir forrit Finance and Operations, eins og Dynamics 365 Finance, Supply Chain Management, Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="1ed88-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="1ed88-105">Það veitir yfirlit yfir hvernig á að tengja þá og yfirlit yfir hvernig á að stofna sérsniðna hjálp.</span><span class="sxs-lookup"><span data-stu-id="1ed88-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="1ed88-106">Högun Hjálpar</span><span class="sxs-lookup"><span data-stu-id="1ed88-106">Help architecture</span></span>

<span data-ttu-id="1ed88-107">Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins.</span><span class="sxs-lookup"><span data-stu-id="1ed88-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="1ed88-108">Hjálparkerfi innan vörunnar sækir greinar úr https://docs.microsoft.com, auk verkefnaleiðbeininga sem eru geymdar í Viðskiptaferlavinnslu í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1ed88-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="1ed88-109">Aðgerðirnar sem eru listaðar í skýringarmyndinni með stjörnu (\*) eru á vegvísnum, en eru ekki tiltækar enn.</span><span class="sxs-lookup"><span data-stu-id="1ed88-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="1ed88-110">[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="1ed88-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="1ed88-111">Tenging við hjálparkerfi</span><span class="sxs-lookup"><span data-stu-id="1ed88-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="1ed88-112">Flipinn **Verkleiðbeiningar** er ekki í boði eins og stendur í Dynamics 365 Talent eða Retail.</span><span class="sxs-lookup"><span data-stu-id="1ed88-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="1ed88-113">Við erum að vinna í því að virkja þessa aðgerð í útgáfum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="1ed88-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="1ed88-114">Verkefnaleiðbeiningarnar í Hafist handa í Talent eru enn tiltækar og í þeim er farið yfir grunnvirkni.</span><span class="sxs-lookup"><span data-stu-id="1ed88-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="1ed88-115">Málsmeðferð til vinnu er einnig fáanleg á docs.microsoft.com vefsvæðinu fyrir bæði Retail og Talent.</span><span class="sxs-lookup"><span data-stu-id="1ed88-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="1ed88-116">Með skjámyndinni **Kerfisfæribreytur** tengja kerfisstjórar stykki í hjálparkerfinu fyrir innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="1ed88-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="1ed88-117">[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="1ed88-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="1ed88-118">Á síðunni **Kerfisfæribreytur** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="1ed88-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ed88-119">Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="1ed88-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="1ed88-120">Gætið þess að smella á tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og smella á **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="1ed88-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="1ed88-121">[![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="1ed88-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="1ed88-122">Veljið Lifecycle Services verk til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="1ed88-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="1ed88-123">Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .</span><span class="sxs-lookup"><span data-stu-id="1ed88-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="1ed88-124">Velja birtingarröð BPM safna.</span><span class="sxs-lookup"><span data-stu-id="1ed88-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="1ed88-125">Þetta ákvarðar í hvaða röð verkskráning úr í söfn birtast á **Hjálp** rúðunni.</span><span class="sxs-lookup"><span data-stu-id="1ed88-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="1ed88-126">Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og smella á flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1ed88-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="1ed88-127">Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.</span><span class="sxs-lookup"><span data-stu-id="1ed88-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="1ed88-128">Sýnir þýddar leiðbeiningar verkefninu</span><span class="sxs-lookup"><span data-stu-id="1ed88-128">Showing translated task guides</span></span>

<span data-ttu-id="1ed88-129">Þýddar verkefnaleiðbeiningar voru sendar í maí 2016 APQC Unified Library, og í safninu Hafist handa (getting started).</span><span class="sxs-lookup"><span data-stu-id="1ed88-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="1ed88-130">Ef þú notar forrit Finance and Operations og vilt sjá staðbundna verkefnahjálp skaltu ganga úr skugga um að þú sért tengd(ur) við safnið fyrir maí.</span><span class="sxs-lookup"><span data-stu-id="1ed88-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="1ed88-131">Tungumálið sem leiðarvísir fyrir verk birtist í er stjórnað fyrir hvern notanda samkvæmt tungumálastillingar undir **Valkostir** &gt; **> Kjörstillingar**.</span><span class="sxs-lookup"><span data-stu-id="1ed88-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="1ed88-132">Þó margar verkefnaleiðbeiningar hafi verið þýdd, er biðlarinn ekki að sýna þýdd heiti verkefnaleiðbeininga.</span><span class="sxs-lookup"><span data-stu-id="1ed88-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="1ed88-133">Einnig, aðeins verkefnaleiðbeiningar sem voru gefnar út í febrúar 2016 eru í boði í þýðingu í maí safninu.</span><span class="sxs-lookup"><span data-stu-id="1ed88-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="1ed88-134">Við munum gefa út uppfærða safn með fleiri þýðingum.</span><span class="sxs-lookup"><span data-stu-id="1ed88-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="1ed88-135">Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="1ed88-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="1ed88-136">Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="1ed88-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="1ed88-137">Stofnun sérsniðinnar hjálpar</span><span class="sxs-lookup"><span data-stu-id="1ed88-137">Creating custom help</span></span>

<span data-ttu-id="1ed88-138">Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="1ed88-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="1ed88-139">Stofna sérsniðna hjálp með verkefnaleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="1ed88-139">Create custom help with task guides</span></span>

<span data-ttu-id="1ed88-140">Hægt er að stofna sérsniðna hjálp fyrir Finance and Operations, Supply Chain Management og Retail með því að stofna verkskráningar sem endurspegla innleiðingu þína og vista þær í LCS Business Process Library.</span><span class="sxs-lookup"><span data-stu-id="1ed88-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="1ed88-141">Ekki er hægt að stofna sérsniðnar verkefnaleiðbeiningar fyrir Talent.</span><span class="sxs-lookup"><span data-stu-id="1ed88-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="1ed88-142">Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="1ed88-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="1ed88-143">Einnig er hægt gera afrit af APQC Unified global library og síðan opna síðan afritið, opna verkskráningar úr því, breyta þeim og vista skráningar með breytingunum.</span><span class="sxs-lookup"><span data-stu-id="1ed88-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="1ed88-144">Frekari upplýsingar er að finna í efnisatriðinu [Hvernig stofna á verkskráningu sem nota á sem fylgigögn eða þjálfun](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="1ed88-144">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="1ed88-145">Tengja sérsniðið svæði</span><span class="sxs-lookup"><span data-stu-id="1ed88-145">Connect a custom site</span></span>

<span data-ttu-id="1ed88-146">Microsoft hefur útvegað hvítbók og sýnikóða sem lýsa því hvernig á að stofna og tengja sérsniðið svæði hjálpar við hjálparsvæðið.</span><span class="sxs-lookup"><span data-stu-id="1ed88-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="1ed88-147">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="1ed88-147">For more information, see:</span></span>

- [<span data-ttu-id="1ed88-148">Stofna sérsniðna hjálp fyrir forrit Finance and Operations (hvítbók)</span><span class="sxs-lookup"><span data-stu-id="1ed88-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="1ed88-149">Sérsniðin hjálp GitHub-geymslu</span><span class="sxs-lookup"><span data-stu-id="1ed88-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="1ed88-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1ed88-150">Additional resources</span></span>

[<span data-ttu-id="1ed88-151">Hjálparyfirlit</span><span class="sxs-lookup"><span data-stu-id="1ed88-151">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="1ed88-152">yfirlit verkskráningar</span><span class="sxs-lookup"><span data-stu-id="1ed88-152">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="1ed88-153">Stofna verkskráning til að nota sem fylgiskjölum eða þjálfun</span><span class="sxs-lookup"><span data-stu-id="1ed88-153">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
