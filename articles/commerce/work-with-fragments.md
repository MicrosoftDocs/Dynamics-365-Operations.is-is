---
title: Vinna með brot
description: Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698097"
---
# <a name="work-with-fragments"></a><span data-ttu-id="7d73c-103">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="7d73c-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7d73c-104">Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d73c-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d73c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="7d73c-105">Overview</span></span>

<span data-ttu-id="7d73c-106">Brot gera ráð fyrir miðlægri höfundarupplifun fyrir einingasamsetningar sem þarf að endurnýta á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="7d73c-107">Til dæmis eru fyrirsagnir, síðufætur og borðar oft stilltir sem brot því þeim er deilt á margar síður.</span><span class="sxs-lookup"><span data-stu-id="7d73c-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="7d73c-108">Þú getur hugsað um brot sem litlar vefsíður sem hægt er að setja inn á aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="7d73c-109">Brot hafa sinn eigin líftíma.</span><span class="sxs-lookup"><span data-stu-id="7d73c-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="7d73c-110">Með öðrum orðum, þau eru búin til, vísað til, uppfærð og þeim eytt sem sjálfstæðum aðilum í höfundatólunum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="7d73c-111">Eftir að brot eru stillt er hægt að nota þau alls staðar sem hægt er að nota einingar í vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="7d73c-112">Hægt er að vísa í brot á síðum, í skipulagi, í sniðmátum og í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="7d73c-113">Brot geta verið ívafin í allt að sjö stig djúpt inni í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="7d73c-114">Til dæmis, ef þú vilt auglýsa árstíðabundinn viðburð yfir margar síður á svæðinu okkar, geturðu notað brot.</span><span class="sxs-lookup"><span data-stu-id="7d73c-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="7d73c-115">Fyrsta skrefið í því ferli að búa til nýtt brot er að velja gerð einingar sem þú vilt byrja á.</span><span class="sxs-lookup"><span data-stu-id="7d73c-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="7d73c-116">Fyrir þetta dæmi er hægt að smíða brot úr hetjueiningunni.</span><span class="sxs-lookup"><span data-stu-id="7d73c-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="7d73c-117">Brot er hægt að smíða úr hvaða einingagerð sem er.</span><span class="sxs-lookup"><span data-stu-id="7d73c-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="7d73c-118">Þú getur síðan stillt hetjubrotið með sérstöku kynningarinnihaldinu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="7d73c-119">Þú getur líka staðfært það eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="7d73c-119">You can also localize it as you require.</span></span> <span data-ttu-id="7d73c-120">Nýja sjálfstæða hetjubrotið er síðan hægt að nota sem forstillta einingu á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="7d73c-121">Þú getur auðveldlega bætt því við sniðmát, á tilteknar síður eða í önnur brot sem geta innihaldið hetjueiningar.</span><span class="sxs-lookup"><span data-stu-id="7d73c-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="7d73c-122">Allir staðirnir þar sem brotinu er bætt við eru tilvísanir í miðlægahetjubrotið sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="7d73c-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="7d73c-123">Ef þú birtir breytingar á brotinu endurspeglast þessar breytingar strax á öllum þeim stöðum þar sem vísað er í brotið á vefnum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="7d73c-124">Þess vegna veita brot öflug og skilvirk leið til að endurnýta og stjórna miðlægum stillingum á vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="7d73c-125">Með því að nota þau á áhrifaríkan hátt geturðu aukið lipurð verulega og hjálpað til við að draga úr kostnaði sem fylgir stjórnun á innihaldi vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="7d73c-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="7d73c-126">Eftirfarandi mynd sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á e-verslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Mynd sem sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á netverslunarsíðu.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="7d73c-128">Stofna brot</span><span class="sxs-lookup"><span data-stu-id="7d73c-128">Create a fragment</span></span>

<span data-ttu-id="7d73c-129">Þú getur annaðhvort búið til nýtt brot eða vistað fyrirliggjandi einingarstillingu sem brot.</span><span class="sxs-lookup"><span data-stu-id="7d73c-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="7d73c-130">Stofna nýtt brot</span><span class="sxs-lookup"><span data-stu-id="7d73c-130">Create a new fragment</span></span>

<span data-ttu-id="7d73c-131">Fylgið eftirfarandi skrefum til að stofna nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="7d73c-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="7d73c-132">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7d73c-133">Veljið **Nýtt síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="7d73c-134">Gluggi birtist sem sýnir allar tiltækar gerðir eininga.</span><span class="sxs-lookup"><span data-stu-id="7d73c-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="7d73c-135">Eins og áður var getið er hægt að búa til brot úr hvaða einingartegund sem er.</span><span class="sxs-lookup"><span data-stu-id="7d73c-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="7d73c-136">Veldu gerð einingar fyrir brotið þitt og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="7d73c-137">Með því að velja almenna gámaeiningagerð færðu mestan sveigjanleika þegar þú verður að uppfæra og stilla brotið þitt seinna.</span><span class="sxs-lookup"><span data-stu-id="7d73c-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="7d73c-138">Vistaðu núverandi einingarstillingu sem brot</span><span class="sxs-lookup"><span data-stu-id="7d73c-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="7d73c-139">Fylgdu þessum skrefum til að umbreyta áður uppsettri einingu í endurnýtanlegt brot.</span><span class="sxs-lookup"><span data-stu-id="7d73c-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="7d73c-140">Opnaðu síðu eða sniðmát sem inniheldur eininguna sem þú vilt breyta í brot.</span><span class="sxs-lookup"><span data-stu-id="7d73c-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="7d73c-141">Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn (**...**) við hliðina á heiti einingarinnar og síðan velurðu **Vista sem brot**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="7d73c-142">Svargluggi birtist.</span><span class="sxs-lookup"><span data-stu-id="7d73c-142">A dialog box appears.</span></span>
1. <span data-ttu-id="7d73c-143">Sláðu inn heiti og lýsigögn fyrir brotið.</span><span class="sxs-lookup"><span data-stu-id="7d73c-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="7d73c-144">Veldu **Í lagi** til að vista einingastillinguna sem brot sem hægt er að bæta við aðrar síður.</span><span class="sxs-lookup"><span data-stu-id="7d73c-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="7d73c-145">Bættu við, fjarlægðu eða breyttu brotum á síðu</span><span class="sxs-lookup"><span data-stu-id="7d73c-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="7d73c-146">Eftirfarandi aðferðir lýsa því hvernig á að bæta við, fjarlægja og breyta einingum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="7d73c-147">Bæta við broti</span><span class="sxs-lookup"><span data-stu-id="7d73c-147">Add a fragment</span></span>

<span data-ttu-id="7d73c-148">Til að bæta broti við síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="7d73c-149">Í útlínuglugganum til vinstri velurðu gám eða hólf sem hægt er að bæta undireiningum við.</span><span class="sxs-lookup"><span data-stu-id="7d73c-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="7d73c-150">Veldu úrfellingarhnappinn við hliðina á heiti gámsins eða hólfsins og velur síðan **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="7d73c-151">Svargluggi birtist.</span><span class="sxs-lookup"><span data-stu-id="7d73c-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d73c-152">Ef gámurinn eða hólfið styðja ekki nýjar undireiningar er valkosturinn **Bæta við broti** er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="7d73c-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="7d73c-153">Leitaðu að og veldu broti til að bæta við í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="7d73c-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="7d73c-154">Ef engin tiltæk brot eru tilgreind gætirðu fyrst þurft að búa til brot úr einingagerð sem valinn gámur eða hólf styður.</span><span class="sxs-lookup"><span data-stu-id="7d73c-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="7d73c-155">Veldu **Í lagi** til að bæta völdu broti við valinn gám eða hólf á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="7d73c-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="7d73c-156">Einingarnar sem eru leyfðar í gámi eða hólfi eru skilgreindar af sniðmáti síðunnar eða eigin skilgreiningum eininganna.</span><span class="sxs-lookup"><span data-stu-id="7d73c-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="7d73c-157">Fjarlægja brot</span><span class="sxs-lookup"><span data-stu-id="7d73c-157">Remove a fragment</span></span>

<span data-ttu-id="7d73c-158">Til að fjarlægja brot úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="7d73c-159">Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti brotanna sem á að fjarlægja og síðan velurðu ruslatunnuhnappinn.</span><span class="sxs-lookup"><span data-stu-id="7d73c-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="7d73c-160">Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja brotið skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="7d73c-161">Þegar þú fjarlægir brot af síðu fjarlægirðu bara tilvísunina til þess af þeirri síðu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="7d73c-162">Þú eyðir brotinu **ekki** af vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7d73c-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="7d73c-163">Til að eyða brotum af vefsvæðinu verðurðu að nota notendaviðmót brotaskoðara.</span><span class="sxs-lookup"><span data-stu-id="7d73c-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="7d73c-164">Þú getur eingöngu eytt brotum af síðu ef ekki er vísað í þau af síðum, sniðmátum eða öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="7d73c-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="7d73c-165">Breyta broti</span><span class="sxs-lookup"><span data-stu-id="7d73c-165">Edit a fragment</span></span>

<span data-ttu-id="7d73c-166">Til að breyta brotum verður þú að nota brotaritilsviðmótið.</span><span class="sxs-lookup"><span data-stu-id="7d73c-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="7d73c-167">Þessi takmörkun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="7d73c-167">This restriction is by design.</span></span> <span data-ttu-id="7d73c-168">Hún hjálpar til við að tryggja að höfundar rugla ekki saman ferlinu við að breyta einingunum fyrir ákveðna síðu og því að breyta brotum sem hægt er að deila á margar síður.</span><span class="sxs-lookup"><span data-stu-id="7d73c-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="7d73c-169">Fylgið eftirfarandi skrefum til að breyta broti.</span><span class="sxs-lookup"><span data-stu-id="7d73c-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="7d73c-170">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="7d73c-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7d73c-171">Undir **Brot** velurðu brotið sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="7d73c-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="7d73c-172">Breyttu einingareiginleikum og uppbyggingu brotsins eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="7d73c-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="7d73c-173">Ferlið líkist ferlinu við að breyta einingum er breytt á blaðsíðu ritstjórans.</span><span class="sxs-lookup"><span data-stu-id="7d73c-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="7d73c-174">Þú getur einnig breytt broti með því að velja það á síðu, í sniðmáti eða í foreldrabroti og síðan velja **Breyta broti** í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="7d73c-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d73c-175">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7d73c-175">Additional resources</span></span>

[<span data-ttu-id="7d73c-176">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="7d73c-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="7d73c-177">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="7d73c-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="7d73c-178">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="7d73c-178">Work with preset layouts</span></span>](work-with-layouts.md)
