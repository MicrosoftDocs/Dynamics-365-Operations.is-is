---
title: Vinna með brot
description: Þetta efnisatriði lýsir því hvers vegna, hvenær og hvernig á að nota brot í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793946"
---
# <a name="work-with-fragments"></a><span data-ttu-id="a517c-103">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="a517c-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="a517c-104">Þetta efnisatriði lýsir því hvers vegna, hvenær og hvernig á að nota brot í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a517c-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a517c-105">Brot gera ráð fyrir miðlægri höfundarupplifun fyrir einingasamsetningar sem þarf að endurnýta á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="a517c-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="a517c-106">Til dæmis eru fyrirsagnir, síðufætur og borðar oft stilltir sem brot því þeim er deilt á margar síður.</span><span class="sxs-lookup"><span data-stu-id="a517c-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="a517c-107">Þú getur hugsað um brot sem litlar vefsíður sem hægt er að setja inn á aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a517c-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="a517c-108">Brot hafa sinn eigin líftíma.</span><span class="sxs-lookup"><span data-stu-id="a517c-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="a517c-109">Með öðrum orðum, þau eru búin til, vísað til, uppfærð og þeim eytt sem sjálfstæðum aðilum í höfundatólunum.</span><span class="sxs-lookup"><span data-stu-id="a517c-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="a517c-110">Eftir að brot eru stillt er hægt að nota þau alls staðar sem hægt er að nota einingar í vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a517c-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="a517c-111">Hægt er að vísa í brot á síðum, í skipulagi, í sniðmátum og í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="a517c-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="a517c-112">Brot geta verið ívafin í allt að sjö stig djúpt inni í öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="a517c-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="a517c-113">Til dæmis, ef þú vilt auglýsa árstíðabundinn viðburð yfir margar síður á svæðinu okkar, geturðu notað brot.</span><span class="sxs-lookup"><span data-stu-id="a517c-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="a517c-114">Fyrsta skrefið í því ferli að búa til nýtt brot er að velja gerð einingar sem þú vilt byrja á.</span><span class="sxs-lookup"><span data-stu-id="a517c-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="a517c-115">Fyrir þetta dæmi er hægt að smíða brot úr hetjueiningunni.</span><span class="sxs-lookup"><span data-stu-id="a517c-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="a517c-116">Brot er hægt að smíða úr hvaða einingagerð sem er.</span><span class="sxs-lookup"><span data-stu-id="a517c-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="a517c-117">Þú getur síðan stillt hetjubrotið með sérstöku kynningarinnihaldinu.</span><span class="sxs-lookup"><span data-stu-id="a517c-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="a517c-118">Þú getur líka staðfært það eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="a517c-118">You can also localize it as you require.</span></span> <span data-ttu-id="a517c-119">Nýja sjálfstæða hetjubrotið er síðan hægt að nota sem forstillta einingu á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="a517c-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="a517c-120">Þú getur auðveldlega bætt því við sniðmát, á tilteknar síður eða í önnur brot sem geta innihaldið hetjueiningar.</span><span class="sxs-lookup"><span data-stu-id="a517c-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="a517c-121">Allir staðirnir þar sem brotinu er bætt við eru tilvísanir í miðlægahetjubrotið sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="a517c-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="a517c-122">Ef þú birtir breytingar á brotinu endurspeglast þessar breytingar strax á öllum þeim stöðum þar sem vísað er í brotið á vefnum.</span><span class="sxs-lookup"><span data-stu-id="a517c-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="a517c-123">Þess vegna veita brot öflug og skilvirk leið til að endurnýta og stjórna miðlægum stillingum á vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="a517c-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="a517c-124">Með því að nota þau á áhrifaríkan hátt geturðu aukið lipurð verulega og hjálpað til við að draga úr kostnaði sem fylgir stjórnun á innihaldi vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="a517c-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="a517c-125">Eftirfarandi mynd sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á e-verslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="a517c-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Mynd sem sýnir hvernig brot er hægt að nota til að miðstýra höfundarstillingu samskiptaeininga á netverslunarsíðu.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="a517c-127">Stofna brot</span><span class="sxs-lookup"><span data-stu-id="a517c-127">Create a fragment</span></span>

<span data-ttu-id="a517c-128">Þú getur annaðhvort búið til nýtt brot eða vistað fyrirliggjandi einingarstillingu sem brot.</span><span class="sxs-lookup"><span data-stu-id="a517c-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="a517c-129">Vistaðu núverandi einingarstillingu sem brot</span><span class="sxs-lookup"><span data-stu-id="a517c-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="a517c-130">Til að umbreyta áður stilltri einingu í endurnýtanlegt brot í Commerce síðusmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a517c-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a517c-131">Opnaðu síðu eða sniðmát sem inniheldur eininguna sem þú vilt breyta í brot.</span><span class="sxs-lookup"><span data-stu-id="a517c-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="a517c-132">Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja eininguna sem var skilgreind áður.</span><span class="sxs-lookup"><span data-stu-id="a517c-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="a517c-133">Veljið úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar á annaðhvort yfirlitssvæðinu eða valda tækjastiku einingarinnar í sjónrænum síðuhönnuði.</span><span class="sxs-lookup"><span data-stu-id="a517c-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="a517c-134">Veljið **Deila sem broti**.</span><span class="sxs-lookup"><span data-stu-id="a517c-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="a517c-135">Í svargluggann **Vista sem brot** skal færa inn heiti fyrir síðubrotið.</span><span class="sxs-lookup"><span data-stu-id="a517c-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="a517c-136">Veldu **Í lagi** til að vista einingastillinguna sem brot sem hægt er að bæta við aðrar síður.</span><span class="sxs-lookup"><span data-stu-id="a517c-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="a517c-137">Stofna nýtt brot</span><span class="sxs-lookup"><span data-stu-id="a517c-137">Create a new fragment</span></span>

<span data-ttu-id="a517c-138">Til að búa til nýtt brot í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a517c-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a517c-139">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="a517c-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a517c-140">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a517c-140">Select **New**.</span></span> <span data-ttu-id="a517c-141">Svargluggi fyrir **Nýtt brot** birtist sem sýnir allar tiltæku einingargerðirnar.</span><span class="sxs-lookup"><span data-stu-id="a517c-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="a517c-142">Eins og áður var getið er hægt að búa til brot úr hvaða einingartegund sem er.</span><span class="sxs-lookup"><span data-stu-id="a517c-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="a517c-143">Veldu tegund einingar fyrir brotið þitt.</span><span class="sxs-lookup"><span data-stu-id="a517c-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="a517c-144">Með því að velja almenna gámaeiningagerð færðu mestan sveigjanleika þegar þú þarft að uppfæra og stilla brotið þitt seinna.</span><span class="sxs-lookup"><span data-stu-id="a517c-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="a517c-145">Bættu við, fjarlægðu eða breyttu brotum á síðu</span><span class="sxs-lookup"><span data-stu-id="a517c-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="a517c-146">Eftirfarandi aðferðir lýsa því hvernig á að bæta við, fjarlægja og breyta einingum.</span><span class="sxs-lookup"><span data-stu-id="a517c-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="a517c-147">Bæta við broti</span><span class="sxs-lookup"><span data-stu-id="a517c-147">Add a fragment</span></span>

<span data-ttu-id="a517c-148">Til að breyta broti milli rása í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a517c-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a517c-149">Á yfirlitssvæðinu vinstra megin eða beint á sjónrænum síðuhönnuði skal velja gám eða hólf þar sem bæta á undireiningunum við.</span><span class="sxs-lookup"><span data-stu-id="a517c-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="a517c-150">Veljið úrfellingarmerkið (**...**) við hliðina á heiti gámsins eða hólfsins.</span><span class="sxs-lookup"><span data-stu-id="a517c-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="a517c-151">Ef sjónrænn síðuhönnuður er notaður, skal velja plústáknið (**+**).</span><span class="sxs-lookup"><span data-stu-id="a517c-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="a517c-152">Veljið **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="a517c-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="a517c-153">Ef geymirinn eða hólfið styður ekki nýjar undireiningar er valkosturinn **Bæta broti** ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="a517c-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="a517c-154">Í svarglugganum **Velja brot** skal leita að og velja brot til að bæta við.</span><span class="sxs-lookup"><span data-stu-id="a517c-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="a517c-155">Ef engin tiltæk brot eru tilgreind gætirðu fyrst þurft að búa til brot úr einingagerð sem valinn gámur eða hólf styður.</span><span class="sxs-lookup"><span data-stu-id="a517c-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="a517c-156">Veldu brotið sem þú vilt til að bæta því við gám eða hólf á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="a517c-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="a517c-157">Einingarnar sem eru leyfðar í gámi eða hólfi eru skilgreindar af sniðmáti síðunnar eða eigin skilgreiningum eininganna.</span><span class="sxs-lookup"><span data-stu-id="a517c-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="a517c-158">Fjarlægja brot</span><span class="sxs-lookup"><span data-stu-id="a517c-158">Remove a fragment</span></span>

<span data-ttu-id="a517c-159">Til að fjarlægja brot úr hófli eða gámi á síðu í Commerce síðusmíð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a517c-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a517c-160">Á yfirlitssvæðinu vinstra megin skal velja úrfellingarmerkið (**...**) við hliðina á heiti brotsins sem á að fjarlægja og síðan velja ruslakörfutáknið.</span><span class="sxs-lookup"><span data-stu-id="a517c-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="a517c-161">Annars er hægt að velja brotið í sjónrænum síðuhönnuði og velja ruslakörfutákni í tækjastiku brotsins.</span><span class="sxs-lookup"><span data-stu-id="a517c-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="a517c-162">Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja brotið skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a517c-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a517c-163">Þegar þú fjarlægir brot af síðu fjarlægirðu bara tilvísunina til þess af þeirri síðu.</span><span class="sxs-lookup"><span data-stu-id="a517c-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="a517c-164">Þú eyðir brotinu **ekki** af vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a517c-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="a517c-165">Til að eyða brotum af vefsvæðinu verðurðu að nota notendaviðmót brotaskoðara.</span><span class="sxs-lookup"><span data-stu-id="a517c-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="a517c-166">Þú getur eingöngu eytt brotum af síðu ef ekki er vísað í þau af síðum, sniðmátum eða öðrum brotum.</span><span class="sxs-lookup"><span data-stu-id="a517c-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="a517c-167">Breyta broti</span><span class="sxs-lookup"><span data-stu-id="a517c-167">Edit a fragment</span></span>

<span data-ttu-id="a517c-168">Til að breyta brotum verður þú að nota brotaritilsviðmótið.</span><span class="sxs-lookup"><span data-stu-id="a517c-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="a517c-169">Þessi takmörkun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="a517c-169">This restriction is by design.</span></span> <span data-ttu-id="a517c-170">Hún hjálpar til við að tryggja að höfundar rugla ekki saman ferlinu við að breyta einingunum fyrir ákveðna síðu og því að breyta brotum sem hægt er að deila á margar síður.</span><span class="sxs-lookup"><span data-stu-id="a517c-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="a517c-171">Til að breyta broti milli rása í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a517c-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a517c-172">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="a517c-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a517c-173">Undir **Brot** velurðu brotið sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="a517c-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="a517c-174">Breyttu einingareiginleikum og uppbyggingu brotsins eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="a517c-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="a517c-175">Ferlið líkist ferlinu við að breyta einingum er breytt á blaðsíðu ritstjórans.</span><span class="sxs-lookup"><span data-stu-id="a517c-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="a517c-176">Þú getur einnig breytt broti með því að velja það á síðu, í sniðmáti eða í foreldrabroti og síðan velja **Breyta broti** í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="a517c-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a517c-177">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a517c-177">Additional resources</span></span>

[<span data-ttu-id="a517c-178">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="a517c-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a517c-179">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="a517c-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="a517c-180">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="a517c-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="a517c-181">Unnið með birta hópa</span><span class="sxs-lookup"><span data-stu-id="a517c-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
