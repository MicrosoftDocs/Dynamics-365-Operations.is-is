---
title: Hanna viðmótið fyrir framkvæmd á framleiðslugólfi
description: Þetta efnisatriði lýsir því hvernig á að hanna efni í notandaviðmóti fyrir hverja skilgreiningu.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 4e2b3746e690623e347e0319ab1b55f2645a5e23
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814681"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="e9e2e-103">Hanna viðmótið fyrir framkvæmd á framleiðslugólfi</span><span class="sxs-lookup"><span data-stu-id="e9e2e-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9e2e-104">Hægt er að hanna efni í notandaviðmóti fyrir hverja skilgreiningu sem notendaviðmót framleiðslugólfsins notar.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="e9e2e-105">Til dæmis gæti verið að starfskraftar í einum vinnuflokki geti opnað verkleiðbeiningar á framleiðslugólfið, en í öðrum vinnuflokki er ekki þörf á leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="e9e2e-106">Í því tilviki er hægt að stofna tvær grunnstillingar, eina með hnapp til að opna viðhengi skjala og eitt án þessa hnapps.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="e9e2e-107">Hanna flipa</span><span class="sxs-lookup"><span data-stu-id="e9e2e-107">Design a tab</span></span>

<span data-ttu-id="e9e2e-108">Á **grunnstillingarsíðu Framleiðslugluggana** er hægt að stofna og grunnstilla flipa með því að velja **Hanna flipa** á aðgerðasvæði.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="e9e2e-109">Hverjum flipa er skipt í fjóra kafla, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="e9e2e-110">![Flipaútlit](media/pfe-tab-layout.png "Flipaútlit")</span><span class="sxs-lookup"><span data-stu-id="e9e2e-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="e9e2e-111">Eftirfarandi einingar eru sýndar á mynd:</span><span class="sxs-lookup"><span data-stu-id="e9e2e-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="e9e2e-112">Fyrsta tækjastika</span><span class="sxs-lookup"><span data-stu-id="e9e2e-112">Primary toolbar</span></span>
1. <span data-ttu-id="e9e2e-113">Önnur tækjastika</span><span class="sxs-lookup"><span data-stu-id="e9e2e-113">Secondary toolbar</span></span>
1. <span data-ttu-id="e9e2e-114">Aðalyfirlit</span><span class="sxs-lookup"><span data-stu-id="e9e2e-114">Main view</span></span>
1. <span data-ttu-id="e9e2e-115">Ítarlegt yfirlit</span><span class="sxs-lookup"><span data-stu-id="e9e2e-115">Detailed view</span></span>

<span data-ttu-id="e9e2e-116">Til að stofna og skilgreina nýjan flipa skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="e9e2e-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="e9e2e-117">Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-117">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

1. <span data-ttu-id="e9e2e-118">Veljið **Hanna flipa** á aðgerðasvæði til að opna síðuna **Hanna flipa**.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="e9e2e-119">![Síðan „Hanna flipa“](media/pfe-design-tabs.png "Síðan Hanna flipa")</span><span class="sxs-lookup"><span data-stu-id="e9e2e-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="e9e2e-120">Veljið **Nýtt** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="e9e2e-121">Gerið eftirfarandi stillingar í haus síðunnar:</span><span class="sxs-lookup"><span data-stu-id="e9e2e-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="e9e2e-122">**Heiti flipa** - Tilgreindu heiti fyrir flipann</span><span class="sxs-lookup"><span data-stu-id="e9e2e-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="e9e2e-123">**Aðalyfirlit** -Veljið á milli tveggja fyrirfram skilgreindra verklista (*Virk verk*, *Öll verk* eða *Vélin mín*).</span><span class="sxs-lookup"><span data-stu-id="e9e2e-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="e9e2e-124">**Upplýsingayfirlit** -Veldu milli auðra gilda eða **Upplýsingar um starf**.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="e9e2e-125">Ef valið er autt gildi verður engin nákvæm skoðun á flipanum. Ef valið er **Upplýsingar um starf** mun Ítarlegt yfirlit innihalda nákvæma lýsingu á vinnslunni sem er valin í verklistanum í aðalyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="e9e2e-126">Í **aðaltækjastikunni** skal velja hvaða hnappar eiga að vera tiltækir í aðaltækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="e9e2e-127">Dálkurinn **Tiltækar aðgerðir** sýnir lista yfir alla hnappa sem hægt er að bæta við.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="e9e2e-128">Dálkurinn **Valdar aðgerðir** sýnir lista yfir alla hnappa sem eru teknir með í núgildandi skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="e9e2e-129">Notaðu hnappana á milli dálka til að fara valdar vörur á milli dálka eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="e9e2e-130">Notaðu upp- og niðurhnappana við hliðina á **Valdar aðgerðir** til að hafa stjórnina á pöntuninni þar sem hnapparnir eru sýndir í notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="e9e2e-131">Í **Auka** **tækjastiku** er hægt að velja hvaða hnappar eiga að vera tiltækir í aukatækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="e9e2e-132">Dálkurinn **Tiltækar aðgerðir** sýnir lista yfir alla hnappa sem hægt er að bæta við.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="e9e2e-133">Dálkurinn **Valdar aðgerðir** sýnir lista yfir alla hnappa sem eru teknir með í núgildandi skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="e9e2e-134">Notaðu hnappana á milli dálka til að fara valdar vörur á milli dálka eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="e9e2e-135">Notaðu upp- og niðurhnappana við hliðina á **Valdar aðgerðir** til að hafa stjórnina á pöntuninni þar sem hnapparnir eru sýndir í notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="e9e2e-136">Tengja flipa við skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="e9e2e-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="e9e2e-137">Eftir að þú hefur hannað alla flipana sem þú þarft er hægt að tengja þá við skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="e9e2e-138">Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-138">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

    <span data-ttu-id="e9e2e-139">![Grunnstilla framkvæmd á framleiðslugólfi](media/pfe-config-prod-floor-execution.png "Grunnstilla framkvæmd á framleiðslugólfi")</span><span class="sxs-lookup"><span data-stu-id="e9e2e-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="e9e2e-140">Í flýtiflipanum **Val á flipa** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="e9e2e-141">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-141">A new row is added to the grid.</span></span> <span data-ttu-id="e9e2e-142">Fyrir þessa nýju línu skal velja heiti flipa sem bæta á við skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="e9e2e-143">Halda áfram að bæta við öðrum flipum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="e9e2e-144">Notið hnappana **Færa upp** og **Færa niður** á tækjastikunni til að raða flipunum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e9e2e-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="e9e2e-145">Fliparnir birtast frá vinstri til hægri í þeirri röð sem sýnd er í ofangreindri skjámynd (flipinn efst er sýndur hér til vinstri).</span><span class="sxs-lookup"><span data-stu-id="e9e2e-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]