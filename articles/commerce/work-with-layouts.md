---
title: Vinna með forstillt útlit
description: Þetta efni lýsir því hvernig á að vinna með forstillt skipulag í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413177"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="ccea7-103">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="ccea7-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ccea7-104">Þetta efni lýsir því hvernig á að vinna með forstillt skipulag í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ccea7-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ccea7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ccea7-105">Overview</span></span>

<span data-ttu-id="ccea7-106">Áður en þú lýkur við ferlin í þessu efni skaltu passa að lesa [Forstillt og sérsniðið skipulag](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="ccea7-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="ccea7-107">Fyrir almenna yfirsýn skal sjá [Yfirlit yfir sniðmát og skipulag](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ccea7-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="ccea7-108">Búa til nýtt forstillt skipulag</span><span class="sxs-lookup"><span data-stu-id="ccea7-108">Create a new preset layout</span></span>

<span data-ttu-id="ccea7-109">Tvær aðferðir eru við að stofna forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="ccea7-110">Þú getur vistað núverandi sérsniðið skipulag sem nýtt forstillt skipulag, eða þú getur búið til forstillt skipulag frá grunni.</span><span class="sxs-lookup"><span data-stu-id="ccea7-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="ccea7-111">Búðu til forstillt skipulag úr núverandi sérsniðnu skipulagi</span><span class="sxs-lookup"><span data-stu-id="ccea7-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="ccea7-112">Til að stofna forstillt skipulag úr núverandi sérsniðnu skipulagi skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="ccea7-113">Opnaðu fyrirliggjandi síðu sem notar ekki forstillt skipulag eins og er og sem er með einingarskipulag sem þú vilt endurnýta fyrir aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ccea7-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="ccea7-114">Veldu **Breyta** til að skoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="ccea7-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="ccea7-115">Veldu **Vista sem nýtt útlit**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-115">Select **Save as new layout**.</span></span> <span data-ttu-id="ccea7-116">Valmyndin **Vista sem nýtt skipulag** birtist.</span><span class="sxs-lookup"><span data-stu-id="ccea7-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="ccea7-117">Sláðu inn heiti og lýsingu fyrir forstillta skipulagið.</span><span class="sxs-lookup"><span data-stu-id="ccea7-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="ccea7-118">Gildin sem þú slærð inn verða sýnd öðrum höfundum þegar þeir búa til nýjar síður úr útliti þínu eða skipta yfir í það.</span><span class="sxs-lookup"><span data-stu-id="ccea7-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="ccea7-119">Sláðu því inn gildi sem munu nýtast síðuhöfundum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="ccea7-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-120">Select **OK**.</span></span>

<span data-ttu-id="ccea7-121">Forstillt skipulag verður nú tiltækt þegar þú býrð til nýjar síður eða velur annað skipulag fyrir síðu í sama stigveldi sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="ccea7-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="ccea7-122">Til að sjá fljótt hvort tiltekin síða er nú bundin við forstillt skipulag velurðu síðuna á síðulistaskjánum og skoðar lýsigögn skipulagsins í eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="ccea7-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="ccea7-123">Búa til nýtt forstillt skipulag</span><span class="sxs-lookup"><span data-stu-id="ccea7-123">Create a new preset layout</span></span>

<span data-ttu-id="ccea7-124">Til að stofna forstillt skipulag frá byrjun skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="ccea7-125">Í stýriglugganum vinstra megin velurðu **Skipulag**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="ccea7-126">Veldu **Nýtt skipulag**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-126">Select **New Layout**.</span></span> <span data-ttu-id="ccea7-127">Valmyndin **Nýtt skipulag** birtist.</span><span class="sxs-lookup"><span data-stu-id="ccea7-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="ccea7-128">Veldu sniðmát sem á að nota fyrir forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="ccea7-129">Sláðu inn heiti og lýsingu fyrir forstillta skipulagið.</span><span class="sxs-lookup"><span data-stu-id="ccea7-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="ccea7-130">Gildin sem þú slærð inn verða sýnd öðrum höfundum þegar þeir búa til nýjar síður úr útliti þínu eða skipta yfir í það.</span><span class="sxs-lookup"><span data-stu-id="ccea7-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="ccea7-131">Sláðu því inn gildi sem munu nýtast síðuhöfundum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="ccea7-132">Veldu **Í lagi** til að búa til nýtt forstillt skipulag og opnaðu skipulagsritilinn.</span><span class="sxs-lookup"><span data-stu-id="ccea7-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="ccea7-133">Í skipulagsritlinum bætirðu við og stillir einingar með útlínutrénu til vinstri og eiginleikaglugganum til hægri.</span><span class="sxs-lookup"><span data-stu-id="ccea7-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="ccea7-134">(Ferlið líkist ferlinu til að bæta við og stilla einingar fyrir sniðmát í sniðmát ritstjórans.) Fyrirkomulag eininga og allar læstar sjálfgefnar stillingar verða miðstýrð einingastilling fyrir allar síður sem nota þetta forstillta skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="ccea7-135">Breyta forstilltu skipulagi</span><span class="sxs-lookup"><span data-stu-id="ccea7-135">Modify a preset layout</span></span>

<span data-ttu-id="ccea7-136">Til að breyta forstilltu skipulagi skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="ccea7-137">Í stýriglugganum vinstra megin velurðu **Skipulag**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="ccea7-138">Í skipulagsritlinum í útlínutrénu til vinstri velurðu eininguna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="ccea7-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="ccea7-139">Fylgdu síðan einhverju af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ccea7-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="ccea7-140">Til að færa einingu upp eða niður í yfireiningu hennar skaltu velja úrfellingarhnappinn (**...**) fyrir eininguna og veldu síðan **Færa upp** eða **Færa niður**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="ccea7-141">Til að breyta sjálfgefnum stillingum einingar skaltu nota eiginleikagluggann til að slá inn sjálfgefin gildi og læsa þeim mögulega fyrir allar forstreymissíður.</span><span class="sxs-lookup"><span data-stu-id="ccea7-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="ccea7-142">Til að bæta nýjum einingum eða brotum við gámaeiningar velurðu úrfellingarhnappinn og síðan **Bæta við einingu** eða **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="ccea7-143">Til að fjarlægja einingu úr skipulaginu skaltu velja úrfellingarhnappinn og velja síðan **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="ccea7-144">Breyta forstilltu skipulagsþema</span><span class="sxs-lookup"><span data-stu-id="ccea7-144">Change a preset layout theme</span></span>

<span data-ttu-id="ccea7-145">Dæmigerð framkvæmd er að setja sjálfgefið þema fyrir allar síður sem nota forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="ccea7-146">Fylgdu þessum skrefum til að stilla eða breyta þema fyrir allar undirsíður sem nota forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="ccea7-147">Í skipulagsritlinum í útlínutrénu til vinstri velurðu síðugámseininguna.</span><span class="sxs-lookup"><span data-stu-id="ccea7-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="ccea7-148">(Venjulega er þessi eining annar hnúturinn og heitir hann **Sjálfgefin síða**.)</span><span class="sxs-lookup"><span data-stu-id="ccea7-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="ccea7-149">Í eiginleikaglugganum hægra megin, í reitnum **Þema**, velurðu þema.</span><span class="sxs-lookup"><span data-stu-id="ccea7-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="ccea7-150">Vistaðu, skráðu inn, forskoðaðu og birtu forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="ccea7-151">Til að vista og skrá inn forstillt skipulag skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ccea7-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="ccea7-152">Veldu **Vista** efst í skipulagsritli.</span><span class="sxs-lookup"><span data-stu-id="ccea7-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="ccea7-153">Vistaðar breytingar hafa ekki áhrif á forstreymissíðum fyrr en þær eru skráðar inn.</span><span class="sxs-lookup"><span data-stu-id="ccea7-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="ccea7-154">Veldu **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-154">Select **Finish editing**.</span></span> <span data-ttu-id="ccea7-155">Nú er hægt að uppgötva breytingarnar fyrir forstreymisflæði.</span><span class="sxs-lookup"><span data-stu-id="ccea7-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="ccea7-156">Til að forskoða breytingarnar skaltu annaðhvort opna fyrirliggjandi síðu sem notar forstillt skipulag eða búa til nýja síðu úr skipulaginu.</span><span class="sxs-lookup"><span data-stu-id="ccea7-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="ccea7-157">Eftir að þú hefur forskoðað breytingarnar á forstilltu skipulagi skaltu fylgja einu af þessum skrefum til að birta skipulagið á lifandi vefsvæði:</span><span class="sxs-lookup"><span data-stu-id="ccea7-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="ccea7-158">Farðu í **Skipulag**, veldu skipulagið og veldu síðan **Birta**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="ccea7-159">Veldu útlitsheiti til að opna útlitsritil og veldu svo **Birta**.</span><span class="sxs-lookup"><span data-stu-id="ccea7-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="ccea7-160">Birta síðu sem vísar til óbirta skipulagsins.</span><span class="sxs-lookup"><span data-stu-id="ccea7-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="ccea7-161">Skipulagið verður sjálfkrafa birt.</span><span class="sxs-lookup"><span data-stu-id="ccea7-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="ccea7-162">Með mörgum síðum er hægt að vísa í forstillt skipulag.</span><span class="sxs-lookup"><span data-stu-id="ccea7-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="ccea7-163">Þegar þú birtir forstillt skipulag þarftu að hafa í huga að þú gætir haft áhrif á skipulag margra síðna.</span><span class="sxs-lookup"><span data-stu-id="ccea7-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ccea7-164">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ccea7-164">Additional resources</span></span>

[<span data-ttu-id="ccea7-165">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="ccea7-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="ccea7-166">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="ccea7-166">Work with templates</span></span>](work-with-templates.md)
