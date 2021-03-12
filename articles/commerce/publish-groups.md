---
title: Vinna með birtingarhópa
description: Þetta efni lýsir eiginleikum útgáfuhópa í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0a4f19af0cdf9c72add0ec18be84e36c807af9ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969877"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="b297c-103">Vinna með birtingarhópa</span><span class="sxs-lookup"><span data-stu-id="b297c-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b297c-104">Þetta efni lýsir eiginleikum útgáfuhópa í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b297c-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b297c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b297c-105">Overview</span></span>

<span data-ttu-id="b297c-106">Vefsíður rafrænna viðskipta eru stöðugt uppfærðar með nýju efni allt árið.</span><span class="sxs-lookup"><span data-stu-id="b297c-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="b297c-107">Uppfærslur eru oft gefnar út í runum í kringum upptekna viðburði netverslana eins og frídaga, árstíðabundnar markaðsherferðir eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="b297c-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="b297c-108">Þessar uppfærslur krefjast þess oft að hópar innihalds á vefsíðu (til dæmis síður, myndir, brot og sniðmát) séu stigsettir, staðfestir og gefnir út samtímis í einni aðgerð.</span><span class="sxs-lookup"><span data-stu-id="b297c-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="b297c-109">Getan til að flokka hluti í rökleg sett sem birta hluti saman, þar sem hvert sett hefur sína eigin líftíma, veitir höfundum marga kosti.</span><span class="sxs-lookup"><span data-stu-id="b297c-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="b297c-110">Í Commerce eru þessi röklegu sett þekkt sem útgáfuhópar.</span><span class="sxs-lookup"><span data-stu-id="b297c-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="b297c-111">Þau gera höfundum síðunnar kleift að rekja mengi uppfærslna sem eigin stillanlegar, prófanlegar og birtanlegar einingar.</span><span class="sxs-lookup"><span data-stu-id="b297c-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="b297c-112">Höfundar geta forskoðað uppfærslur í sviðsettum útgáfuhópi án þess að hafa áhrif á lifandi vefinn eða aðra sjálfstæða útgáfuhópa.</span><span class="sxs-lookup"><span data-stu-id="b297c-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="b297c-113">Höfundar geta síðan tímasett útgáfuaðgerðina til að birta samtímis öll atriðin í útgáfnahópnum á lifandi vefinn.</span><span class="sxs-lookup"><span data-stu-id="b297c-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="b297c-114">Getan til að flokka, forskoða og tímasetja uppfærslur er mikilvæg fyrir mörg fyrirtækjastig fyrirtækisins sem skila talsverðum árlegum tekjum í kringum tímamótabundna uppfærslu á vefsvæðum.</span><span class="sxs-lookup"><span data-stu-id="b297c-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="b297c-115">Fyrirtæki geta stofnað til kostnaðar vegna hægfara eða ógildrar útfærslu efnis sem gengur ekki vel.</span><span class="sxs-lookup"><span data-stu-id="b297c-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="b297c-116">Úgtáfuhópar hjálpa til við að tryggja að ræsingar séu skipulagðar, staðfestar og gefnar út á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="b297c-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="b297c-117">Hvort sem þeir eru stórir eða litlir, þá eru útgáfuhópar með dýrmæt verkfæri sem hjálpar höfundum að skipuleggja og einfalda áframhaldandi uppfærsluverk vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="b297c-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="b297c-118">Hvenær á að nota útgáfuhópa</span><span class="sxs-lookup"><span data-stu-id="b297c-118">When to use publish groups</span></span>

<span data-ttu-id="b297c-119">Þú getur notað útgáfuhópa hvenær sem þú verður að stigsetja og birta mörg skjöl saman.</span><span class="sxs-lookup"><span data-stu-id="b297c-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="b297c-120">Til dæmis, ef vefsíðan þín uppfærir efni á hverju tímabili, getur þú búið til útgáfuhópa fyrir þessar árstíðabundnu markaðsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="b297c-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="b297c-121">Útgáfuflokkurinn „Haustárstíðabundin uppfærsla“ gæti innihaldið nýjar árstíðabundnar myndir, brot sem eru með árstíðabundin markaðsskilaboð, síður sem innihalda árstíðabundin vörusöfn eða aðrar árstíðabundnar uppfærslur á vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="b297c-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="b297c-122">Kosturinn við útgáfuhópa er að þú getur stigsett margar uppfærslur samhliða.</span><span class="sxs-lookup"><span data-stu-id="b297c-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="b297c-123">Til dæmis, skömmu eftir uppfærslu fyrir útgáfuhópinn „Haustárstíðabundin uppfærsla“ gæti verið innihaldsuppfærsla fyrir tiltekna fríhelgi.</span><span class="sxs-lookup"><span data-stu-id="b297c-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="b297c-124">Í þessu tilfelli geturðu stigsett efni fyrir útgáfuhópinn „Haustárstíðabundin uppfærsla“ á sama tíma og þú stigsetur efni fyrir síðari útgáfuhóp „Haustfrísuppfærsla“.</span><span class="sxs-lookup"><span data-stu-id="b297c-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="b297c-125">Hver útgáfuflokkur inniheldur sitt eigið einkvæma sett af blaðsíðum, myndum, brotum, sniðmátum og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="b297c-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="b297c-126">Þú getur stigsett, forskoðað og staðfest þessa tvo útgáfuhópa sjálfstætt en samtímis.</span><span class="sxs-lookup"><span data-stu-id="b297c-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="b297c-127">Síðan er hægt að áætla hvern útgáfuflokk til að birtast á vefsvæðinu á ákveðnum dagsetningum og tímum.</span><span class="sxs-lookup"><span data-stu-id="b297c-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="b297c-128">Kveikt á eiginleika útgáfuhópa</span><span class="sxs-lookup"><span data-stu-id="b297c-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="b297c-129">Aðgerðin sem birtir hópa er valfrjáls og kveikja verður á henni fyrir vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="b297c-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="b297c-130">Fylgdu þessum skrefum til að kveikja á útgáfuhópum fyrir vefsvæðið í höfundatækjum Commerce.</span><span class="sxs-lookup"><span data-stu-id="b297c-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="b297c-131">Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="b297c-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="b297c-132">Undir **Svæðisstillingar** velurðu **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="b297c-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b297c-133">Stilltu valkostinn **Útgáfuhópar** **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="b297c-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="b297c-134">Stofna útgáfuflokk</span><span class="sxs-lookup"><span data-stu-id="b297c-134">Create a publish group</span></span>

<span data-ttu-id="b297c-135">Til að stofna útgáfuflokk fyrir vefsvæðið í höfundatólum Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b297c-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="b297c-136">Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b297c-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="b297c-137">Á efstu skipanastikunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b297c-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="b297c-138">Í valmyndinni **Stofna útgáfuflokk**, undir **Birta heiti flokks**, slærðu inn lýsandi heiti.</span><span class="sxs-lookup"><span data-stu-id="b297c-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="b297c-139">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b297c-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="b297c-140">Veldu samhengi höfundar útgáfuhópsins</span><span class="sxs-lookup"><span data-stu-id="b297c-140">Set the publish group authoring context</span></span>

<span data-ttu-id="b297c-141">Í Commerce er sjálfgefið höfundarsamhengi samhengi lifandi vefsvæðis.</span><span class="sxs-lookup"><span data-stu-id="b297c-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="b297c-142">Samhengi höfundar við lifandi vefsvæði er sjálfgefið útlit þar sem þú getur skoðað og gert breytingar beint á vefsíðuna án þess að nota útgáfuhóp.</span><span class="sxs-lookup"><span data-stu-id="b297c-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="b297c-143">Það táknar nýjustu beinar uppfærslur á birtri útgáfu af vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="b297c-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="b297c-144">Ef samhengisstjórnun undir **Útgáfuflokkar** í vinstri stýriglugganum sýnir heitið **Lifandi síða** ertu að vinna í samhengi höfundar við lifandi vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="b297c-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="b297c-145">**Lifandi síða** er sjálfgefið heiti samhengistjórnunar.</span><span class="sxs-lookup"><span data-stu-id="b297c-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="b297c-146">Annars sýnir samhengistjórnun nafn útgáfuhóps.</span><span class="sxs-lookup"><span data-stu-id="b297c-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="b297c-147">Til að vinna í útgáfuhópi verðurðu að skipta yfir í höfundaritunarútgáfuna fyrir það.</span><span class="sxs-lookup"><span data-stu-id="b297c-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="b297c-148">Fylgdu einu af þessum skrefum til að stilla samhengi útgáfuhópsins.</span><span class="sxs-lookup"><span data-stu-id="b297c-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="b297c-149">Í vinstri stýriglugganum velurðu samhengisstjórnunina beint undir **Útgáfuflokkar** og velur síðan heiti útgáfuflokksins af listanum yfir valkosit sem birtist.</span><span class="sxs-lookup"><span data-stu-id="b297c-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="b297c-150">Samhengistjórnuninni er gefið nýtt heiti og sýnir heiti útgáfuhópsins.</span><span class="sxs-lookup"><span data-stu-id="b297c-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="b297c-151">Í vinstri stýriglugganum velurðu **Útgáfuhópar** og síðan, undir **Útgáfuhópar**, velurðu heiti útgáfuhópsins.</span><span class="sxs-lookup"><span data-stu-id="b297c-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="b297c-152">Samhengistjórnuninni er gefið nýtt heiti og sýnir heiti útgáfuhópsins.</span><span class="sxs-lookup"><span data-stu-id="b297c-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="b297c-153">Eftir að þú hefur valið samhengi höfundar við útgáfuhópa vinnur þú í því samhengi við birtingu hópsins þegar þú forskoðar og breytir innihaldi síðunnar.</span><span class="sxs-lookup"><span data-stu-id="b297c-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="b297c-154">Veldu samhengistjórnun til að fara aftur í sjálfgefið samhengi höfundaréttar með höfundarétti og síðan **Lifandi síða**.</span><span class="sxs-lookup"><span data-stu-id="b297c-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="b297c-155">Bættu síðum eða öðrum hlutum við útgáfuhóp</span><span class="sxs-lookup"><span data-stu-id="b297c-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="b297c-156">Eftir að þú hefur valið samhengi höfundar við höfundarútgáfu og samhengistjórnun í vinstri stýriglugganum sýnir nafn þess geturðu búið til efni alveg eins og þú gerir í sjálfgefnu samhengi lifandi vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="b297c-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="b297c-157">Þú getur líka bætt við núverandi síðum eða öðrum hlutum frá öðrum útgáfuflokkum eða frá samhengi lifandi vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="b297c-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="b297c-158">Fylgdu þessum skrefum til að afrita núverandi síður í birtan hóp.</span><span class="sxs-lookup"><span data-stu-id="b297c-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="b297c-159">Veldu höfundarsamhengi sem á að afrita, og veldu síðan í vinstri stýriglugganum **Síður**.</span><span class="sxs-lookup"><span data-stu-id="b297c-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="b297c-160">Veldu síðuna til að bæta við útgáfuhóp.</span><span class="sxs-lookup"><span data-stu-id="b297c-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="b297c-161">Veldu á skipanastikunni **Afrita í útgáfuhóp**.</span><span class="sxs-lookup"><span data-stu-id="b297c-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="b297c-162">Í valmyndinni **Velja útgáfuhóp** velurðu útgáfuhópinn sem á að bæta síðunni við og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b297c-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="b297c-163">Þú getur notað sömu grunnskrefin til að búa til sérsniðnar vörusíður, vefslóðir, sniðmát, skipulag, brot og margmiðlunarbókareignir, eða til að bæta núverandi hluti af þessum gerðum við útgáfuhóp.</span><span class="sxs-lookup"><span data-stu-id="b297c-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="b297c-164">Staðfesta útgáfuflokk</span><span class="sxs-lookup"><span data-stu-id="b297c-164">Validate a publish group</span></span>

<span data-ttu-id="b297c-165">Til að ganga úr skugga um að öll ósjálfstæði í efni birta hópa sé fullnægt og að öll staðfesting sé liðin geturðu keyrt staðfestingu til að bera kennsl á öll mál sem þarf að taka á áður en þú áætlar útgáfuaðgerð.</span><span class="sxs-lookup"><span data-stu-id="b297c-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="b297c-166">Fylgdu þessum skrefum til að staðfesta útgáfuhópinn þinn áður en þú áætlar hann.</span><span class="sxs-lookup"><span data-stu-id="b297c-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="b297c-167">Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b297c-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="b297c-168">Veldu útgáfuhópinn sem á að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="b297c-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="b297c-169">Á efstu skipanastikunni velurðu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="b297c-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="b297c-170">Fullgilding er keyrð á öllu efni í útgáfuhópnum.</span><span class="sxs-lookup"><span data-stu-id="b297c-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="b297c-171">Öll vandamál sem koma í veg fyrir birtingu aðgerða birtast í tilkynningareit sem birtist efst til hægri.</span><span class="sxs-lookup"><span data-stu-id="b297c-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="b297c-172">Villuleit er alltaf keyrð sjálfkrafa þegar útgáfnahópur er áætlaður.</span><span class="sxs-lookup"><span data-stu-id="b297c-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="b297c-173">Hins vegar er hnappurinn **Staðfesta** á skipanastikunni gagnlegur vegna þess að hann hjálpar til við að bera kennsl á vandamál sem verður að laga áður en þú reynir að áætla útgáfuhóp til að fara í gang.</span><span class="sxs-lookup"><span data-stu-id="b297c-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="b297c-174">Áætla útgáfuhóp til að fara í gang</span><span class="sxs-lookup"><span data-stu-id="b297c-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="b297c-175">Fylgdu þessum skrefum til að áætla útgáfuhóp til að fara í gang á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="b297c-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="b297c-176">Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="b297c-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="b297c-177">Undir **Útgáfuhópar** velurðu útgáfuhópinn sem á að áætla.</span><span class="sxs-lookup"><span data-stu-id="b297c-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="b297c-178">Á efstu skipanastikunni velurðu **Breyta áætlun**.</span><span class="sxs-lookup"><span data-stu-id="b297c-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="b297c-179">Valmyndin **Breyta áætlun** birtist.</span><span class="sxs-lookup"><span data-stu-id="b297c-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="b297c-180">Veldu dagsetningu og tíma þegar útgáfuhópurinn ætti að fara í gang og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b297c-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="b297c-181">Fylgdu sömu skrefum til að taka útgáfuhóp úr áætlun, en veldu **Taka útgáfuhóp úr áætlun** í valmyndinni **Breyta áætlun**.</span><span class="sxs-lookup"><span data-stu-id="b297c-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="b297c-182">Mjög stórir útgáfuflokkar geta tekið allt að mínútu eða tvær til að verða gefnir út þegar áætlunartími þeirra rennur upp.</span><span class="sxs-lookup"><span data-stu-id="b297c-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="b297c-183">Hafðu í huga að útgáfuaðgerð er ekki samstundis og að minni útgáfuflokkar verða gefnir út hraðar.</span><span class="sxs-lookup"><span data-stu-id="b297c-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="b297c-184">Algengar spurningar um birtingarhópa</span><span class="sxs-lookup"><span data-stu-id="b297c-184">Publish groups FAQ</span></span>

<span data-ttu-id="b297c-185">**Hve mörg atriði geta verið í útgáfuhóp?**</span><span class="sxs-lookup"><span data-stu-id="b297c-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="b297c-186">Eins og er eru takmörk upp á 2.000 atriði á hvern útgáfuhóp.</span><span class="sxs-lookup"><span data-stu-id="b297c-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="b297c-187">Hafðu í huga að mjög stórir útgáfuflokkar geta tekið nokkrar mínútur til að verða gefnir út þegar áætlunartími þeirra rennur upp.</span><span class="sxs-lookup"><span data-stu-id="b297c-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="b297c-188">**Eru að útgáfuhópar eins og „kóðagreinar“ í hugbúnaðarþróun hugtakanna?**</span><span class="sxs-lookup"><span data-stu-id="b297c-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="b297c-189">Já og nei.</span><span class="sxs-lookup"><span data-stu-id="b297c-189">Yes and no.</span></span> <span data-ttu-id="b297c-190">Hægt er að hugsa um að útgáfuhópa sem kvíslgreindar útgáfur af síðunni.</span><span class="sxs-lookup"><span data-stu-id="b297c-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="b297c-191">Þannig virka þeir eins og greinar.</span><span class="sxs-lookup"><span data-stu-id="b297c-191">In that way, they do act like branches.</span></span> <span data-ttu-id="b297c-192">Hins vegar er ekkert hugtak um sameiningu á stigi einstakra atriða.</span><span class="sxs-lookup"><span data-stu-id="b297c-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="b297c-193">Atriðið sem birt er síðast skrifar bara yfir það sem áður var og nýjasta útgáfuaðgerðin kemur alltaf í stað fyrri útgáfuaðgerða.</span><span class="sxs-lookup"><span data-stu-id="b297c-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="b297c-194">**Get ég tímasett tvo útgáfuhópa til að fara í gang á sama tíma?**</span><span class="sxs-lookup"><span data-stu-id="b297c-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="b297c-195">Nei.</span><span class="sxs-lookup"><span data-stu-id="b297c-195">No.</span></span> <span data-ttu-id="b297c-196">Vegna afkasta og árekstra mun kerfið neyða þig til að dreifa áætlaðum útgáfuhópum með að minnsta kosti fimm mínútna millibili.</span><span class="sxs-lookup"><span data-stu-id="b297c-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="b297c-197">**Get ég notað útgáfuhópa til að skipuleggja alhliða þjónustu á bakvinnslu vara, svo sem afslátt og vöruuppfærslur?**</span><span class="sxs-lookup"><span data-stu-id="b297c-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="b297c-198">Eins og stendur styður eiginleiki útgáfuhópa aðeins innihald vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="b297c-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="b297c-199">Hins vegar Microsoft er meðvitað um að samþætting við bakvinnslu á smásöluaðstæðum getur verið dýrmæt fyrir samhæfingu og sjálfvirkni alhliða kynningarherferðar.</span><span class="sxs-lookup"><span data-stu-id="b297c-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b297c-200">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b297c-200">Additional resources</span></span>

[<span data-ttu-id="b297c-201">Leiðir til að bæta við efni</span><span class="sxs-lookup"><span data-stu-id="b297c-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="b297c-202">Orðalisti síðulíkans</span><span class="sxs-lookup"><span data-stu-id="b297c-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="b297c-203">Staða og líftími skjala</span><span class="sxs-lookup"><span data-stu-id="b297c-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="b297c-204">Virkja og nota deilingu milli rása</span><span class="sxs-lookup"><span data-stu-id="b297c-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="b297c-205">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="b297c-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="b297c-206">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="b297c-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="b297c-207">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="b297c-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b297c-208">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="b297c-208">Customize site navigation</span></span>](customize-site-navigation.md)
