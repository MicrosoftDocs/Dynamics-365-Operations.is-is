---
title: Breyta síðu svæðis sem þegar er til
description: Þetta efni lýsir því hvernig á að breyta fyrirliggjandi svæði í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413239"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="71d9b-103">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="71d9b-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="71d9b-104">Þetta efni lýsir því hvernig á að breyta fyrirliggjandi svæði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71d9b-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="71d9b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="71d9b-105">Overview</span></span>

<span data-ttu-id="71d9b-106">Þegar þú verður að breyta síðu er fyrsta skrefið að opna hana í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="71d9b-107">Farðu á svæðið sem inniheldur síðuna þína og finndu síðan síðuna sem þú vilt á lista með síðum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="71d9b-108">Ef þú finnur ekki síðuna geturðu notað ríka leitarmöguleika höfundartækisins.</span><span class="sxs-lookup"><span data-stu-id="71d9b-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="71d9b-109">Annaðhvort slærðu nákvæmlega inn nafn síðunnar eða sláðu inn fyrstu stafina í því og síðan stjörnu (\*).</span><span class="sxs-lookup"><span data-stu-id="71d9b-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="71d9b-110">Síaður listi yfir síður birtist.</span><span class="sxs-lookup"><span data-stu-id="71d9b-110">A filtered list of pages appears.</span></span> <span data-ttu-id="71d9b-111">Þú getur notað þennan lista til að finna síðuna sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="71d9b-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="71d9b-112">Þegar þú hefur fundið rétta síðu skaltu velja heiti síðunnar til að opna síðuna í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="71d9b-113">Ef síðan þín er sýnileg í síðuskoðun geturðu valið **Breyta** og skoðað síðuna áður en þú opnar hana í síðuritlinum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="71d9b-114">Á þennan hátt geturðu skoðað margar síður á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="71d9b-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="71d9b-115">Eftir að síðan er opin í ritlinum verður þú að ganga úr skugga um að hún sé skráðu út til þín.</span><span class="sxs-lookup"><span data-stu-id="71d9b-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="71d9b-116">Skipanastikan í höfundatólinu er kvik, samhengisnæm og tekur tillit til stöðu.</span><span class="sxs-lookup"><span data-stu-id="71d9b-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="71d9b-117">Þess vegna sýnir það aðeins aðgerðir sem þú getur framkvæmt á síðunni núna.</span><span class="sxs-lookup"><span data-stu-id="71d9b-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="71d9b-118">Til dæmis, ef síðan er ekki merkt þér birtast hnapparnir **Vista** og **Ljúka við breytingar** ekki á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="71d9b-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="71d9b-119">Staða síðunnar er einnig sýnd hægra megin í glugganum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="71d9b-120">Ef síðan er ekki merkt þér skaltu velja **Breyta** á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="71d9b-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="71d9b-121">Skipunarstikan breytist til að endurspegla nýja stöðu síðunnar.</span><span class="sxs-lookup"><span data-stu-id="71d9b-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="71d9b-122">Þú færð einnig tilkynningu þar sem fram kemur að síðan hafi verið skráð út á þig.</span><span class="sxs-lookup"><span data-stu-id="71d9b-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="71d9b-123">Næsta skref er að gera raunverulegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="71d9b-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="71d9b-124">Oft notarðu útlínutré síðunnar til vinstri til að finna og velja eininguna sem þú vilt breyta og gera síðan breytingar í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="71d9b-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="71d9b-125">Hins vegar gæti breyting þín stundum falið í sér viðbót eða fjarlægingu líkana eða brota.</span><span class="sxs-lookup"><span data-stu-id="71d9b-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="71d9b-126">Til að bæta við broti eða einingunni skaltu nota útlitsgreinatréð til að finna raufina sem þú vilt bæta einingunni eða brotinu við og veldu síðan úrfellingarhnappinn (**...**) fyrir það hólf.</span><span class="sxs-lookup"><span data-stu-id="71d9b-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="71d9b-127">Valmynd birtist sem inniheldur skipanir til að bæta við einingu eða broti.</span><span class="sxs-lookup"><span data-stu-id="71d9b-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="71d9b-128">Til að fjarlægja einingu eða brot, finndu og veldu það í útlitsstré síðunnar, veldu úrfellingarhnappinn og veldu síðan skipunina til að eyða einingunni eða brotinu.</span><span class="sxs-lookup"><span data-stu-id="71d9b-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="71d9b-129">Einnig er hægt að skoða og breyta eiginleikum fyrir einingu sem er sýnileg í forskoðun sýnilegs síðuhönnuðar með því að velja hana með beinum hætti.</span><span class="sxs-lookup"><span data-stu-id="71d9b-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="71d9b-130">Eftir að þú ert búinn að gera breytingar þínar og forskoða áhrif þeirra skaltu merkja við síðuna með því að velja **Ljúka við breytingar** á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="71d9b-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="71d9b-131">Til að birta breytingarnar þínar strax velurðu **Birta** á skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="71d9b-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="71d9b-132">Síðasta innskráða útgáfan af síðunni sem þú breyttir er birt og verður tiltæk utanaðkomandi notendum sem skoða síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="71d9b-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="71d9b-133">Dæmi: Breyttu myndskeiðinu á heimasíðunni</span><span class="sxs-lookup"><span data-stu-id="71d9b-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="71d9b-134">Eftirfarandi dæmi sýnir hvernig á að breyta heimasíðunni með því að breyta myndbandinu sem birtist í einingunni.</span><span class="sxs-lookup"><span data-stu-id="71d9b-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="71d9b-135">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="71d9b-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="71d9b-136">Í stýriglugganum vinstra megin velurðu **Síður**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="71d9b-137">Finndu og veldu heimasíðuna til að opna hana í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="71d9b-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="71d9b-138">Á skipanastikunni velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="71d9b-139">Í síðuútlínu velurðu hólfið **Aðal**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="71d9b-140">Undir hólfinu **Aðal** stækkarðu allar einingar vökvaílátsins.</span><span class="sxs-lookup"><span data-stu-id="71d9b-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="71d9b-141">Finndu og veldu vídeóspilarann.</span><span class="sxs-lookup"><span data-stu-id="71d9b-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="71d9b-142">Í eiginleikaglugganum til hægri velurðu eiginleikann **myndskeið**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="71d9b-143">Eignarval birtist.</span><span class="sxs-lookup"><span data-stu-id="71d9b-143">The asset picker appears.</span></span>
1. <span data-ttu-id="71d9b-144">Í eignavali velurðu myndskeiðseignina eða velur **Hlaða upp nýrri eign** til að hlaða upp nýrri myndskeiðseign.</span><span class="sxs-lookup"><span data-stu-id="71d9b-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="71d9b-145">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-145">Select **OK**.</span></span>
1. <span data-ttu-id="71d9b-146">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="71d9b-147">Í reitnum **Athugasemdir** slærðu inn **Myndskeiði breytt** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="71d9b-148">Veldu **Forskoða** til að forskoða uppfærða síðu.</span><span class="sxs-lookup"><span data-stu-id="71d9b-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="71d9b-149">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="71d9b-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="71d9b-150">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="71d9b-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71d9b-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="71d9b-151">Additional resources</span></span>

[<span data-ttu-id="71d9b-152">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="71d9b-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="71d9b-153">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="71d9b-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="71d9b-154">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="71d9b-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="71d9b-155">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="71d9b-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="71d9b-156">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="71d9b-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="71d9b-157">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="71d9b-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="71d9b-158">Staðfesta aðgengi síðuinnihalds</span><span class="sxs-lookup"><span data-stu-id="71d9b-158">Verify page content accessibility</span></span>](verify-accessibility.md)
