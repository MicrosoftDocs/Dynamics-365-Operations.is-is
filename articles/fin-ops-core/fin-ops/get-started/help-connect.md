---
title: Skilgreining hjálparupplifunar fyrir Finance and Operations-forrit
description: Þetta efnisatriði lýsir þáttum hjálparkerfisins fyrir sum Microsoft Dynamics 365-forrit. Það útskýrir einnig hvernig á að tengja þessi forrit og býður upp á samantekt yfir ferlið til að búa til sérstillta hjálp.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
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
ms.openlocfilehash: 827d4cd14f497b79c85fb084a6295af13c5eb0c7
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367385"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="740c2-104">Skilgreining hjálparupplifunar fyrir Finance and Operations-forrit</span><span class="sxs-lookup"><span data-stu-id="740c2-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="740c2-105">Í þessu efnisatriði er að finna yfirlit yfir þætti hjálparkerfisins fyrir Finance and Operations-forrit á borð við Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="740c2-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="740c2-106">Efnisatriðið útskýrir einnig hvernig á að tengja þessa þætti og býður upp á samantekt yfir ferlið til að búa til sérstillta hjálp.</span><span class="sxs-lookup"><span data-stu-id="740c2-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="740c2-107">Högun Hjálpar</span><span class="sxs-lookup"><span data-stu-id="740c2-107">Help architecture</span></span>

<span data-ttu-id="740c2-108">Finance and Operations-forrit innihalda almenn yfirlit og önnur efnisatriði sem eru birt á vefsvæðinu [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="740c2-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="740c2-109">Þetta efni er svo hægt að nálgast á **hjálparsvæði** vörunnar.</span><span class="sxs-lookup"><span data-stu-id="740c2-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="740c2-110">Eftirfarandi skýringarmynd sýnir hluta hjálparkerfisins.</span><span class="sxs-lookup"><span data-stu-id="740c2-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="740c2-111">[![Högun Hjálpar](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="740c2-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="740c2-112">Hjálparkerfi vörunnar sækir greinar á docs.microsoft.com og önnur tengd vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="740c2-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="740c2-113">Það sækir einnig verkleiðbeiningar sem eru vistaðar í viðskiptaferlavinnslunni (BPM) í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="740c2-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="740c2-114">Verkefnaleiðbeiningum bætt við</span><span class="sxs-lookup"><span data-stu-id="740c2-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="740c2-115">Flipinn **Verkefnaleiðbeiningar** er ekki til staðar í „Human Resources“ eða „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="740c2-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="740c2-116">Hins vegar eru verkefnaleiðbeiningarnar „Hafist handa“ í „Human Resources“ til staðar og þar er að finna upplýsingar um grunnvirknina.</span><span class="sxs-lookup"><span data-stu-id="740c2-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="740c2-117">Hjálparleiðbeiningar eru í boði á vefsvæðinu [https://docs.microsoft.com/dynamics365](/dynamics365/) fyrir bæði „Human Resources“ og „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="740c2-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="740c2-118">Á síðunni **Kerfisfæribreytur** geta kerfisstjórar skilgreint aðgang að viðeigandi verkleiðbeiningasöfnum fyrir innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="740c2-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="740c2-119">Til að grunnstilla hjálpina þarf notandi að skrá sig inn með því að nota lykil hjá sama leigjanda og leigjandanum þar sem forritið er virkjað.</span><span class="sxs-lookup"><span data-stu-id="740c2-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="740c2-120">Ekki er hægt að tengja LCS-safn úr tilviki forritsins sem er keyrt á staðbundnu sýndardrifi (VHD).</span><span class="sxs-lookup"><span data-stu-id="740c2-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="740c2-121">[![Skjámynd kerfisfæribreyta með stillingum hjálparkerfis](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="740c2-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="740c2-122">Til að skilgreina verkefnaleiðbeiningar fyrir lausn skal fylgja þessum skrefum á síðunni **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="740c2-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="740c2-123">Í fyrsta skipti er sem þú opnar flipann **Hjálp** verður þú að tengjast Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="740c2-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="740c2-124">Gætið þess að velja tengil í miðri skjámyndinni, bíða eftir tengingu, loka svarglugga og velja **Í lagi** til að komast á síðuna **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="740c2-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="740c2-125">[![Tengjast við LCS](./media/connect-to-lcs-crop-1024x365.png "Tengjast við LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="740c2-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="740c2-126">Veljið Lifecycle Services verk til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="740c2-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="740c2-127">Veljið BPM söfn (innan valins verks) til að sækja verkskráningu úr .</span><span class="sxs-lookup"><span data-stu-id="740c2-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="740c2-128">Velja birtingarröð BPM safna.</span><span class="sxs-lookup"><span data-stu-id="740c2-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="740c2-129">Birtingarröðin ákvarðar í hvaða röð verkskráningar úr söfnunum birtast á svæðinu **Hjálp**.</span><span class="sxs-lookup"><span data-stu-id="740c2-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="740c2-130">Eftir að þessum skrefum hefur verið lokið, er hægt að opna rúðuna **Hjálp** og velja flipann **Verkleiðbeiningar**. Nú sérðu verkefnaleiðbeiningar sem eiga við um síðuna sem þú ert á í Finance and Operations forritum.</span><span class="sxs-lookup"><span data-stu-id="740c2-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="740c2-131">Ef engin verkefnaleiðbeiningar finnast er hægt að færa inn lykilorð til þess að fínstilla leitina.</span><span class="sxs-lookup"><span data-stu-id="740c2-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="740c2-132">Sýnir þýddar leiðbeiningar verkefninu</span><span class="sxs-lookup"><span data-stu-id="740c2-132">Showing translated task guides</span></span>

<span data-ttu-id="740c2-133">Þýddar verkefnaleiðbeiningar voru gefnar út í maíútgáfu APQC Unified Library 2016, og í safninu „Hafist handa“.</span><span class="sxs-lookup"><span data-stu-id="740c2-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="740c2-134">Til að skoða staðfærðar verkleiðbeiningar hjálpar þarf að ganga úr skugga um að Dynamics 365-lausnin sé tengd við útgáfu safnsins frá maí 2016.</span><span class="sxs-lookup"><span data-stu-id="740c2-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="740c2-135">Notendur geta breytt tungumálinu sem verkefnaleiðbeiningar birtast á með því að breyta tungumálastillingum undir **Valkostir** &gt; **Kjörstillingar**.</span><span class="sxs-lookup"><span data-stu-id="740c2-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="740c2-136">Þrátt fyrir að margar verkefnaleiðbeiningar hafi verið þýddar sýnir biðlarinn ekki heiti þýddra verkleiðbeininga, eins og er.</span><span class="sxs-lookup"><span data-stu-id="740c2-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="740c2-137">Í maíútgáfu safnsins 2016 verða auk þess þýðingar eingöngu í boði fyrir verkleiðbeiningar sem gefnar voru út í febrúar 2016.</span><span class="sxs-lookup"><span data-stu-id="740c2-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="740c2-138">Microsoft mun gefa út uppfært safn sem inniheldur fleiri þýðingar.</span><span class="sxs-lookup"><span data-stu-id="740c2-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="740c2-139">Ef verkefnaleiðbeiningar hefur verið þýdd, þegar þú opnar þessi verkefnaleiðbeiningar birtist allan texta þeirra í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="740c2-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="740c2-140">Ef verkefnaleiðbeiningar hefur ekki enn verið þýdd, þegar þú opnar það, bara nokkrar af textanum (Texti stjórnbúnaðar) munu birtast í valið tungumál.</span><span class="sxs-lookup"><span data-stu-id="740c2-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="740c2-141">Sérsniðinni hjálp bætt við</span><span class="sxs-lookup"><span data-stu-id="740c2-141">Adding custom Help</span></span>

<span data-ttu-id="740c2-142">Hægt er að nota verkefnaleiðbeiningar til að stofna sérsniðna hjálp eða tengja vefsvæði við **hjálparsvæðið**.</span><span class="sxs-lookup"><span data-stu-id="740c2-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="740c2-143">Stofna sérsniðna hjálp með því að nota verkefnaleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="740c2-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="740c2-144">Hægt er að stofna sérsniðna hjálp fyrir studd forrit með því að stofna verkskráningar sem endurspegla innleiðingu og vista þær í viðskiptaferlissafni í LCS.</span><span class="sxs-lookup"><span data-stu-id="740c2-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="740c2-145">Ekki er hægt að búa til sérsniðnar verkefnaleiðbeiningar fyrir „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="740c2-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="740c2-146">Fyrir samstarfsaðila, ef þú færir safn inn í fyrirtækissafn og hefur það með í lausn, verður það tiltækt viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="740c2-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="740c2-147">Einnig er hægt að taka afrit af APQC Unified Library og opna síðan verkskráningarnar í afritinu, breyta þeim og vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="740c2-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="740c2-148">Nánari upplýsingar er að finna [Tilföng verkskráningar](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="740c2-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="740c2-149">Tengja sérstillt hjálparsvæði</span><span class="sxs-lookup"><span data-stu-id="740c2-149">Connect a custom Help site</span></span>

<span data-ttu-id="740c2-150">Finance and Operations-forrit eru sjaldan notuð eins og þau eru afhent.</span><span class="sxs-lookup"><span data-stu-id="740c2-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="740c2-151">Þess í stað er lausnin sérsniðin og útvíkkuð til að passa við þarfir fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="740c2-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="740c2-152">Einnig er hægt að sérsníða og víkka út hjálparupplifunina.</span><span class="sxs-lookup"><span data-stu-id="740c2-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="740c2-153">Til dæmis er hægt að bæta við sérsniðinni hjálp á **hjálparsvæðið**.</span><span class="sxs-lookup"><span data-stu-id="740c2-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="740c2-154">Microsoft hefur gefið út verkfærasett til að auðvelda uppsetningu og teningu sérsniðinnar hjálpar á **hjálparsvæðinu**.</span><span class="sxs-lookup"><span data-stu-id="740c2-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="740c2-155">Frekari upplýsingar um hvernig hægt er að setja upp sérsniðna hjálparlausn sem er tengd við **hjálparsvæðið** er finna í [Sérsniðið hjálparyfirlit](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="740c2-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="740c2-156">Ef óskað er eftir samstarfi við Microsoft í tengslum við verkfæri og ferli til að sérsnið hjálpar skal fylla út eyðublaðið á [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="740c2-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="740c2-157">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="740c2-157">See also</span></span>

[<span data-ttu-id="740c2-158">Hjálparkerfi</span><span class="sxs-lookup"><span data-stu-id="740c2-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="740c2-159">Sérsniðið hjálparyfirlit</span><span class="sxs-lookup"><span data-stu-id="740c2-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="740c2-160">Tilföng verkskráningar</span><span class="sxs-lookup"><span data-stu-id="740c2-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="740c2-161">Búa til fylgiskjöl eða þjálfun með verkskráningu</span><span class="sxs-lookup"><span data-stu-id="740c2-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="740c2-162">Sérsniðin hjálp GitHub-geymslu</span><span class="sxs-lookup"><span data-stu-id="740c2-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
