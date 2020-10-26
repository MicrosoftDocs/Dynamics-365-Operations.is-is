---
title: Vinna með brot
description: Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 07/31/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b3e3299388190f03e761591a0c23164b705db9e8
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961659"
---
# <a name="work-with-fragments"></a><span data-ttu-id="68e6c-103">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="68e6c-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="68e6c-104">Þetta efni lýsir því hvers vegna, hvenær og hvernig skuli nota brot í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68e6c-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="68e6c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="68e6c-105">Overview</span></span>

<span data-ttu-id="68e6c-106">Brot gera ráð fyrir miðlægri höfundarupplifun fyrir einingasamsetningar sem þarf að endurnýta á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="68e6c-107">Til dæmis eru fyrirsagnir, síðufætur og borðar oft stilltir sem brot því þeim er deilt á margar síður.</span><span class="sxs-lookup"><span data-stu-id="68e6c-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="68e6c-108">Þú getur hugsað um brot sem litlar vefsíður sem hægt er að setja inn á aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="68e6c-109">Brot hafa sinn eigin líftíma.</span><span class="sxs-lookup"><span data-stu-id="68e6c-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="68e6c-110">Með öðrum orðum, þau eru búin til, vísað til, uppfærð og þeim eytt sem sjálfstæðum aðilum í höfundatólunum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="68e6c-111">Eftir að brot eru stillt er hægt að nota þau alls staðar sem hægt er að nota einingar í vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="68e6c-112">Hægt er að vísa í brot á síðum, í skipulagi, í sniðmátum og í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="68e6c-113">Brot geta verið ívafin í allt að sjö stig djúpt inni í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="68e6c-114">Til dæmis, ef þú vilt auglýsa árstíðabundinn viðburð yfir margar síður á svæðinu okkar, geturðu notað brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="68e6c-115">Fyrsta skrefið í því ferli að búa til nýtt brot er að velja gerð einingar sem þú vilt byrja á.</span><span class="sxs-lookup"><span data-stu-id="68e6c-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="68e6c-116">Fyrir þetta dæmi er hægt að smíða brot úr hetjueiningunni.</span><span class="sxs-lookup"><span data-stu-id="68e6c-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="68e6c-117">Brot er hægt að smíða úr hvaða einingagerð sem er.</span><span class="sxs-lookup"><span data-stu-id="68e6c-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="68e6c-118">Þú getur síðan stillt hetjubrotið með sérstöku kynningarinnihaldinu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="68e6c-119">Þú getur líka staðfært það eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="68e6c-119">You can also localize it as you require.</span></span> <span data-ttu-id="68e6c-120">Nýja sjálfstæða hetjubrotið er síðan hægt að nota sem forstillta einingu á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="68e6c-121">Þú getur auðveldlega bætt því við sniðmát, á tilteknar síður eða í önnur brot sem geta innihaldið hetjueiningar.</span><span class="sxs-lookup"><span data-stu-id="68e6c-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="68e6c-122">Allir staðirnir þar sem brotinu er bætt við eru tilvísanir í miðlægahetjubrotið sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="68e6c-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="68e6c-123">Ef þú birtir breytingar á brotinu endurspeglast þessar breytingar strax á öllum þeim stöðum þar sem vísað er í brotið á vefnum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="68e6c-124">Þess vegna veita brot öflug og skilvirk leið til að endurnýta og stjórna miðlægum stillingum á vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="68e6c-125">Með því að nota þau á áhrifaríkan hátt geturðu aukið lipurð verulega og hjálpað til við að draga úr kostnaði sem fylgir stjórnun á innihaldi vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="68e6c-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="68e6c-126">Eftirfarandi mynd sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á e-verslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Mynd sem sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á netverslunarsíðu.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="68e6c-128">Stofna brot</span><span class="sxs-lookup"><span data-stu-id="68e6c-128">Create a fragment</span></span>

<span data-ttu-id="68e6c-129">Þú getur annaðhvort búið til nýtt brot eða vistað fyrirliggjandi einingarstillingu sem brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="68e6c-130">Vistaðu núverandi einingarstillingu sem brot</span><span class="sxs-lookup"><span data-stu-id="68e6c-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="68e6c-131">Fylgdu þessum skrefum til að umbreyta áður uppsettri einingu í endurnýtanlegt brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="68e6c-132">Opnaðu síðu eða sniðmát sem inniheldur eininguna sem þú vilt breyta í brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="68e6c-133">Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja eininguna sem var skilgreind áður.</span><span class="sxs-lookup"><span data-stu-id="68e6c-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="68e6c-134">Veljið úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar á annaðhvort yfirlitssvæðinu eða valda tækjastiku einingarinnar í sjónrænum síðuhönnuði.</span><span class="sxs-lookup"><span data-stu-id="68e6c-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="68e6c-135">Velja **Samnýta sem síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-135">Select **Share as Page Fragment**.</span></span> 
1. <span data-ttu-id="68e6c-136">Í svargluggann **Vista sem síðubrot** skal færa inn heiti fyrir síðubrotið.</span><span class="sxs-lookup"><span data-stu-id="68e6c-136">In the **Save as Page Fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="68e6c-137">Veldu **Í lagi** til að vista einingastillinguna sem brot sem hægt er að bæta við aðrar síður.</span><span class="sxs-lookup"><span data-stu-id="68e6c-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="68e6c-138">Eftirfarandi mynd sýnir hvernig vista má einingastillingu sem brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Skjámynd um hvernig á að vista einingastillingu sem brot](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="68e6c-140">Stofna nýtt brot</span><span class="sxs-lookup"><span data-stu-id="68e6c-140">Create a new fragment</span></span>

<span data-ttu-id="68e6c-141">Fylgið eftirfarandi skrefum til að stofna nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="68e6c-142">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="68e6c-143">Veljið **Nýtt síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="68e6c-144">Gluggi birtist sem sýnir allar tiltækar gerðir eininga.</span><span class="sxs-lookup"><span data-stu-id="68e6c-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="68e6c-145">Eins og áður var getið er hægt að búa til brot úr hvaða einingartegund sem er.</span><span class="sxs-lookup"><span data-stu-id="68e6c-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="68e6c-146">Veldu tegund einingar fyrir brotið þitt.</span><span class="sxs-lookup"><span data-stu-id="68e6c-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="68e6c-147">Eftirfarandi mynd sýnir hvar á að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="68e6c-147">The following image shows where to create a new fragment.</span></span>

![Skjámynd um hvar eigi að búa til nýtt brot](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="68e6c-149">Með því að velja almenna gámaeiningagerð færðu mestan sveigjanleika þegar þú þarft að uppfæra og stilla brotið þitt seinna.</span><span class="sxs-lookup"><span data-stu-id="68e6c-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="68e6c-150">Bættu við, fjarlægðu eða breyttu brotum á síðu</span><span class="sxs-lookup"><span data-stu-id="68e6c-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="68e6c-151">Eftirfarandi aðferðir lýsa því hvernig á að bæta við, fjarlægja og breyta einingum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="68e6c-152">Bæta við broti</span><span class="sxs-lookup"><span data-stu-id="68e6c-152">Add a fragment</span></span>

<span data-ttu-id="68e6c-153">Til að bæta broti við síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="68e6c-154">Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja gám eða hólf þar sem bæta á undireiningunum við.</span><span class="sxs-lookup"><span data-stu-id="68e6c-154">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="68e6c-155">Á yfirlitssvæðinu skal velja úrfellingarmerkið (**...**) við hliðina á heiti gámsins eða hólfsins.</span><span class="sxs-lookup"><span data-stu-id="68e6c-155">In the online pane, select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="68e6c-156">Ef sjónrænn síðuhönnuður er notaður, skal velja plústáknið (**+**).</span><span class="sxs-lookup"><span data-stu-id="68e6c-156">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="68e6c-157">Veljið **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-157">Select **Add Fragment**.</span></span>

    ![Skjámynd um hvernig bæta má núverandi broti við rauf eða ílát](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="68e6c-159">Ef gámurinn eða hólfið styðja ekki nýjar undireiningar er valkosturinn **Bæta við broti** er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="68e6c-159">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="68e6c-160">Í svarglugganum **Bæta við broti** skal leita að og velja brot til að bæta við.</span><span class="sxs-lookup"><span data-stu-id="68e6c-160">In the **Add Fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="68e6c-161">Ef engin tiltæk brot eru tilgreind gætirðu fyrst þurft að búa til brot úr einingagerð sem valinn gámur eða hólf styður.</span><span class="sxs-lookup"><span data-stu-id="68e6c-161">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="68e6c-162">Veldu brotið sem þú vilt til að bæta því við gám eða hólf á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="68e6c-162">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Skjámynd af staðfestingaglugga brotavals](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="68e6c-164">Einingarnar sem eru leyfðar í gámi eða hólfi eru skilgreindar af sniðmáti síðunnar eða eigin skilgreiningum eininganna.</span><span class="sxs-lookup"><span data-stu-id="68e6c-164">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="68e6c-165">Fjarlægja brot</span><span class="sxs-lookup"><span data-stu-id="68e6c-165">Remove a fragment</span></span>

<span data-ttu-id="68e6c-166">Til að fjarlægja brot úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-166">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="68e6c-167">Á yfirlitssvæðinu vinstra megin skal velja úrfellingarmerkið (**...**) við hliðina á heiti brotsins sem á að fjarlægja og síðan velja ruslakörfutáknið.</span><span class="sxs-lookup"><span data-stu-id="68e6c-167">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="68e6c-168">Annars er hægt að velja brotið í sjónrænum síðuhönnuði og velja ruslakörfutákni í tækjastiku brotsins.</span><span class="sxs-lookup"><span data-stu-id="68e6c-168">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="68e6c-169">Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja brotið skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-169">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="68e6c-170">Þegar þú fjarlægir brot af síðu fjarlægirðu bara tilvísunina til þess af þeirri síðu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-170">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="68e6c-171">Þú eyðir brotinu **ekki** af vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="68e6c-171">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="68e6c-172">Til að eyða brotum af vefsvæðinu verðurðu að nota notendaviðmót brotaskoðara.</span><span class="sxs-lookup"><span data-stu-id="68e6c-172">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="68e6c-173">Þú getur eingöngu eytt brotum af síðu ef ekki er vísað í þau af síðum, sniðmátum eða öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="68e6c-173">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="68e6c-174">Breyta broti</span><span class="sxs-lookup"><span data-stu-id="68e6c-174">Edit a fragment</span></span>

<span data-ttu-id="68e6c-175">Til að breyta brotum verður þú að nota brotaritilsviðmótið.</span><span class="sxs-lookup"><span data-stu-id="68e6c-175">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="68e6c-176">Þessi takmörkun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="68e6c-176">This restriction is by design.</span></span> <span data-ttu-id="68e6c-177">Hún hjálpar til við að tryggja að höfundar rugla ekki saman ferlinu við að breyta einingunum fyrir ákveðna síðu og því að breyta brotum sem hægt er að deila á margar síður.</span><span class="sxs-lookup"><span data-stu-id="68e6c-177">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="68e6c-178">Fylgið eftirfarandi skrefum til að breyta broti.</span><span class="sxs-lookup"><span data-stu-id="68e6c-178">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="68e6c-179">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="68e6c-179">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="68e6c-180">Undir **Brot** velurðu brotið sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="68e6c-180">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="68e6c-181">Breyttu einingareiginleikum og uppbyggingu brotsins eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="68e6c-181">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="68e6c-182">Ferlið líkist ferlinu við að breyta einingum er breytt á blaðsíðu ritstjórans.</span><span class="sxs-lookup"><span data-stu-id="68e6c-182">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="68e6c-183">Þú getur einnig breytt broti með því að velja það á síðu, í sniðmáti eða í foreldrabroti og síðan velja **Breyta broti** í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="68e6c-183">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68e6c-184">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="68e6c-184">Additional resources</span></span>

[<span data-ttu-id="68e6c-185">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="68e6c-185">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="68e6c-186">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="68e6c-186">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="68e6c-187">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="68e6c-187">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="68e6c-188">Unnið með birta hópa</span><span class="sxs-lookup"><span data-stu-id="68e6c-188">Work with publish groups</span></span>](publish-groups.md)
