---
title: Þekjustillingar
description: Þetta efnisatriði veitir upplýsingar um þekjustillingar sem aðalröðun notar til að reikna út vöruþarfir.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9a170ee07da27977fd65ef8f01f3bb87b7ef8b4
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887115"
---
# <a name="coverage-settings"></a><span data-ttu-id="7dd71-103">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="7dd71-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dd71-104">Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="7dd71-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="7dd71-105">Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:</span><span class="sxs-lookup"><span data-stu-id="7dd71-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="7dd71-106">Tilgreina þekjustillingar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="7dd71-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="7dd71-107">Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn.</span><span class="sxs-lookup"><span data-stu-id="7dd71-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="7dd71-108">Til að stofna þekjuflokk skal opna **Aðaláætlanagerð &gt; Uppsetning &gt; Þekja &gt; Þekjuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="7dd71-109">Hægt er að tengja þekjuflokk við vöru.</span><span class="sxs-lookup"><span data-stu-id="7dd71-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="7dd71-110">Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="7dd71-111">Sé tengillinn almennur, án tillits til afurðarvídda, skal nota reitinn **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="7dd71-112">Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð sem sjálfgildi almennan þekjuflokk sem tilgreindur er á síðunni **Færibreytur áætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="7dd71-113">Tilgreinið þekjustillingar fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="7dd71-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="7dd71-114">Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="7dd71-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="7dd71-115">Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="7dd71-116">Veljið afurðina og síðan í Aðgerðarrúðu á flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja** til að opna síðuna **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="7dd71-117">Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="7dd71-118">Þekjustillingar á síðunni **Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="7dd71-119">Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="7dd71-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="7dd71-120">Leiðsagnarforritið leiðir þig skref fyrir skref í gegnum ferlið við að setja upp færibreytur fyrir helstu vöruþekjuna.</span><span class="sxs-lookup"><span data-stu-id="7dd71-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="7dd71-121">Á síðunni **Vöruþekja**, í aðgerðarúðunni, er valið **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="7dd71-122">Tilgreinið þekjustillingar fyrir víddarflokk.</span><span class="sxs-lookup"><span data-stu-id="7dd71-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="7dd71-123">Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="7dd71-124">Á síðunni **Upplýsingar um losaðar afurðir** á flýtiflipanum **Almennt**, í hlutanum **Stjórnun**, er smellt á tengilinn í reitnum **Geymsluvíddarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="7dd71-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="7dd71-125">Á síðunni **Geymsluvíddarflokkur** skal velja gátreitinn **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="7dd71-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="7dd71-126">Velja verður reitinn **Þekjuáætlun eftir vídd** fyrir allar afurðarvíddir, t.d. skilgreiningu, lit, stærð og stíl.</span><span class="sxs-lookup"><span data-stu-id="7dd71-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="7dd71-127">Þekjukóðar</span><span class="sxs-lookup"><span data-stu-id="7dd71-127">Coverage codes</span></span>

<span data-ttu-id="7dd71-128">Hægt er að stilla aðalskipulagningu til að nota mismunandi áfyllingaraðferðir.</span><span class="sxs-lookup"><span data-stu-id="7dd71-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="7dd71-129">Áfyllingaraðferðirnar eða lotustærðaraðferðirnar eru aðferðirnar sem kerfið notar til að ákvarða runustærð fyrir keyptar eða framleiddar vörur.</span><span class="sxs-lookup"><span data-stu-id="7dd71-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="7dd71-130">Hverri áfyllingaraðferð er úthlutað einum af eftirfarandi umfjöllunarkóðum:</span><span class="sxs-lookup"><span data-stu-id="7dd71-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="7dd71-131">**Handbók** - Lotustærðaraðferðin þar sem kerfið bendir ekki til kaupa, flutnings eða framleiðslupantana fyrir hlutinn.</span><span class="sxs-lookup"><span data-stu-id="7dd71-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="7dd71-132">Skipuleggjandi fyrir hlutinn mun sjá um að búa til nauðsynlegar pantanir fyrir áfyllingu hlutarins.</span><span class="sxs-lookup"><span data-stu-id="7dd71-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="7dd71-133">**Eftir þörfum** - Lotustærðaraðferðin þar sem kerfið býr til fyrirhugaða innkaupa-, flutnings- eða framleiðslupöntun eftir þörfum fyrir hlutinn.</span><span class="sxs-lookup"><span data-stu-id="7dd71-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="7dd71-134">Þetta er almennt notað fyrir dýrar vörur með óreglulega eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="7dd71-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="7dd71-135">**Á hvert tímabil** - Lotustærðaraðferðin sem sameinar alla eftirspurnina á tímabili í eina pöntun á vörunni.</span><span class="sxs-lookup"><span data-stu-id="7dd71-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="7dd71-136">Pöntunin verður áætluð fyrir fyrsta dag tímabilsins og magn hennar uppfyllir nettókröfur á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="7dd71-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="7dd71-137">Tímabilið byrjar með fyrstu eftirspurn eftir vörunni og nær yfir skilgreinda tímalengd.</span><span class="sxs-lookup"><span data-stu-id="7dd71-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="7dd71-138">Næsta tímabil byrjar með næstu eftirspurn eftir vörunni.</span><span class="sxs-lookup"><span data-stu-id="7dd71-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="7dd71-139">**Lágm./Hám.** - Lotustærðaraðferðin sem inniheldur áfyllingu birgða upp að vissu marki þegar spáð lagermagn er undir viðmiðunarmörkum.</span><span class="sxs-lookup"><span data-stu-id="7dd71-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="7dd71-140">Áfyllingarmagnið verður munurinn á milli hámarksstigs og spáðs stigs lagermagns.</span><span class="sxs-lookup"><span data-stu-id="7dd71-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7dd71-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7dd71-141">Additional resources</span></span>

[<span data-ttu-id="7dd71-142">Yfirlit aðaláætlana</span><span class="sxs-lookup"><span data-stu-id="7dd71-142">Master plans overview</span></span>](master-plans.md)
