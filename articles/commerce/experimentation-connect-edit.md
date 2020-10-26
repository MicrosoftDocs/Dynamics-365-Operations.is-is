---
title: Tengja tilraun og breyta afbrigðum
description: Þetta efnisatriði lýsir því hvernig á að tengja tilraun í þjónustu þriðja aðila við Dynamics 365 Commerce og hvernig á að breyta afbrigðum fyrir tilraunina.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930222"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="76e09-103">Tengja tilraun og breyta afbrigðum</span><span class="sxs-lookup"><span data-stu-id="76e09-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="76e09-104">Þetta efnisatriði lýsir því hvernig á að tengja tilraunina í Commerce og gera breytingar á afbrigðum þannig að þau samræmist tilgátunni.</span><span class="sxs-lookup"><span data-stu-id="76e09-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="76e09-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="76e09-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="76e09-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="76e09-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="76e09-107">[ ![Tilraunastarfssemi notanda - Tengja og breyta](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="76e09-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="76e09-108">Þegar [búið er að setja upp tilraunina](experimentation-setup.md) í þjónustu þriðja aðila skal tengja tilraunina við Dynamics 365 Commerce og breyta afbrigðum tilraunarinnar.</span><span class="sxs-lookup"><span data-stu-id="76e09-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="76e09-109">Athugunarefni við gerð verkefnaáætlunar</span><span class="sxs-lookup"><span data-stu-id="76e09-109">Planning considerations</span></span>

<span data-ttu-id="76e09-110">Áður en þú tengir tilraunina þína í Commerce þarftu að taka nokkrar ákvarðanir sem hafa áhrif á það hvernig Commerce hefur umsjón með efninu þínu.</span><span class="sxs-lookup"><span data-stu-id="76e09-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="76e09-111">Ákvarða umfang tilraunarinnar</span><span class="sxs-lookup"><span data-stu-id="76e09-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="76e09-112">Þegar tilraun er tengd er beðið um að skilgreina umfang tilraunarinnar.</span><span class="sxs-lookup"><span data-stu-id="76e09-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="76e09-113">Tilraunir eru skilgreindar með umfang **að hluta** eða **allt** .</span><span class="sxs-lookup"><span data-stu-id="76e09-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="76e09-114">Veljið **að hluta** ef framkvæma á tilraun á tilteknum hluta síðu.</span><span class="sxs-lookup"><span data-stu-id="76e09-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="76e09-115">Ef þessi valkostur er valinn verður að auðkenna hvaða einingar eru teknar með í tilrauninni.</span><span class="sxs-lookup"><span data-stu-id="76e09-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="76e09-116">Breytingar sem eru gerðar á hlutum sjálfgefinnar síðu eða broti sem er ekki tengt tilrauninni eru sjálfkrafa samstillt á milli afbrigða.</span><span class="sxs-lookup"><span data-stu-id="76e09-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="76e09-117">Veljið **allt** ef framkvæma á tilraun á heilli síðu eða broti.</span><span class="sxs-lookup"><span data-stu-id="76e09-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="76e09-118">Aðskilin afrit af sjálfgefinni síðu eða hluta eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="76e09-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="76e09-119">Ekki þarf að velja hvaða einingar eru hafðar með í tilrauninni vegna þess að hægt er að breyta öllu útlitinu.</span><span class="sxs-lookup"><span data-stu-id="76e09-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="76e09-120">Hægt er að bæta við, eyða og endurraða einingum eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="76e09-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="76e09-121">Ef einhverjar breytingar eru hins vegar gerðar á sjálfgefinni síðu eða broti sem tilraunin tengist verða þessar breytingar að vera samstilltar handvirkt yfir öll afbrigðin.</span><span class="sxs-lookup"><span data-stu-id="76e09-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="76e09-122">Ef þú tengir tilraunina þína við síðu sem notar útlit er aðeins hægt að stilla umfang tilraunarinnar á **allt**.</span><span class="sxs-lookup"><span data-stu-id="76e09-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="76e09-123">Ákveða hvort eigi að tímasetja hvenær tilraunin verður gefin út</span><span class="sxs-lookup"><span data-stu-id="76e09-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="76e09-124">Ef ætlunin er að tímasetja hvenær tilraunin er birt á lifandi svæðinu, skal ganga úr skugga um efnið sem tengja á við tilraunina sé tiltækt í birtingarhóp *áður en* þú tengir tilraunina.</span><span class="sxs-lookup"><span data-stu-id="76e09-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="76e09-125">Frekari upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="76e09-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="76e09-126">Tengja tilraun</span><span class="sxs-lookup"><span data-stu-id="76e09-126">Connect your experiment</span></span>
<span data-ttu-id="76e09-127">Til að tengja tilraunina þarf að ræsa leiðsagnarforritið **Tengja tilraun**.</span><span class="sxs-lookup"><span data-stu-id="76e09-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="76e09-128">Leiðsagnarforritið fer með þér í gegnum skrefin sem þarf til að tengja tilraunina.</span><span class="sxs-lookup"><span data-stu-id="76e09-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="76e09-129">Þegar leiðsagnarforritinu er lokið er tillraunin tengd og afbrigði eru búin til og þau tilbúin fyrir breytingar.</span><span class="sxs-lookup"><span data-stu-id="76e09-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="76e09-130">Til að ræsa leiðsagnarforritið skal velja flipann **Tilraunir** í vefsmiðnum og síðan velja **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="76e09-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="76e09-131">Að öðrum kosti er hægt að opna leiðsagnarforritið í gegnum ritil síðu eða brots.</span><span class="sxs-lookup"><span data-stu-id="76e09-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="76e09-132">Í breytingastillingu skal velja **Tengja tilraun** í skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="76e09-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="76e09-133">Síða getur aðeins verið tengd við eina tilraun í einu.</span><span class="sxs-lookup"><span data-stu-id="76e09-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="76e09-134">Til að tengja síðu við aðra tilraun skal fyrst eyða tilrauninni sem síðan er tengd við.</span><span class="sxs-lookup"><span data-stu-id="76e09-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="76e09-135">Veldu síðuna eða hlutann sem þú vilt keyra tilraunina þína á.</span><span class="sxs-lookup"><span data-stu-id="76e09-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="76e09-136">Stilltu umfang tilraunir á **að hluta** eða **allt** samkvæmt valinu þínu í hlutanum [Ákvarða umfang tilraunarinnar](#determine-the-scope-of-your-experiment) hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="76e09-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="76e09-137">Virkja verður flagg eiginleikans **Tilraun á síðum eða broti** ef ætlunin er að gera tilraun á heilli síðu eða síðubroti.</span><span class="sxs-lookup"><span data-stu-id="76e09-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="76e09-138">Frekari upplýsingar er að finna í efnisatriðinu [Tilraunir í Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76e09-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="76e09-139">Í lokaskrefi leiðsagnarforritsins skal velja **Búa til afbrigði og hætta í leiðsagnarforritinu**.</span><span class="sxs-lookup"><span data-stu-id="76e09-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="76e09-140">Afbrigði eru búin til fyrir tilraunina.</span><span class="sxs-lookup"><span data-stu-id="76e09-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="76e09-141">Breyta afbrigðum</span><span class="sxs-lookup"><span data-stu-id="76e09-141">Edit your variations</span></span>
<span data-ttu-id="76e09-142">Þegar farið er út úr leiðsagnarforritinu eru afbrigði stofnuð fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="76e09-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="76e09-143">Því næst skaltu breyta afbrigðunum þannig að þau endurspegli valkostina sem þú þarft að sannprófa í tilgátu tilraunarinnar.</span><span class="sxs-lookup"><span data-stu-id="76e09-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="76e09-144">Veldu eina af eftirfarandi ferlum sem samsvarar umfanginu sem þú valdir fyrir tilraun þína í hlutanum [Ákvarða umfang tilraunarinnar](#determine-the-scope-of-your-experiment) hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="76e09-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="76e09-145">Breyta afbrigðum fyrir tilraunir með umfang að hluta til</span><span class="sxs-lookup"><span data-stu-id="76e09-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="76e09-146">Fylgið eftirfarandi skrefum ef umfang tilraunarinnar var skilgreint sem **að hluta** í leiðsagnarforritinu **Tengja tilraun**.</span><span class="sxs-lookup"><span data-stu-id="76e09-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="76e09-147">Í yfirliti ritils skal nota fellivalmynd afbrigðanna fyrir neðan skipanastikuna til að breyta hverju afbrigði fyrir sig samkvæmt upprunalegu tilgátunni.</span><span class="sxs-lookup"><span data-stu-id="76e09-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="76e09-148">Þú gætir einnig viljað setja upp samanburðar- eða grunnafbrigði með því að skilja eitt þessarar afbrigða eftir óbreytt.</span><span class="sxs-lookup"><span data-stu-id="76e09-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="76e09-149">Veldu eininguna sem á að gera tilraunir á, veldu úrfellingarmerkið (...) og veldu síðan **Bæta við tilraun**.</span><span class="sxs-lookup"><span data-stu-id="76e09-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="76e09-150">Breyta afbrigðum fyrir tilraunir með fullt umfang</span><span class="sxs-lookup"><span data-stu-id="76e09-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="76e09-151">Ef þú skilgreindir umfang tilraunarinnar sem **allt** í leiðsagnarforritinu **Tengja tilraun**, skaltu í yfirliti ritils skal nota fellivalmynd afbrigðanna fyrir neðan skipanastikuna til að breyta hverju afbrigði fyrir sig samkvæmt upprunalegu tilgátunni.</span><span class="sxs-lookup"><span data-stu-id="76e09-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="76e09-152">Hvort sem verður fyrir valinu, gætir þú einnig viljað setja upp samanburðar- eða grunnafbrigði með því að skilja eitt þessarar afbrigða eftir óbreytt.</span><span class="sxs-lookup"><span data-stu-id="76e09-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="76e09-153">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="76e09-153">Previous step</span></span>
[<span data-ttu-id="76e09-154">Setja upp tilraun</span><span class="sxs-lookup"><span data-stu-id="76e09-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="76e09-155">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="76e09-155">Next step</span></span>
[<span data-ttu-id="76e09-156">Forskoða og birta tilraun</span><span class="sxs-lookup"><span data-stu-id="76e09-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)