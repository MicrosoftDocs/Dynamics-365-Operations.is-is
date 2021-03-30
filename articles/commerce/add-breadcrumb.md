---
title: Brauðmylsnueining
description: Þetta efnisatriði fjallar um brauðmylsnueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 06f8ffdecd1f77468ed88043929f29b6957c2e6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206560"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="08777-103">Brauðmylsnueining</span><span class="sxs-lookup"><span data-stu-id="08777-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08777-104">Þetta efnisatriði fjallar um brauðmylsnueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="08777-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="08777-105">Brauðmylsnueiningar eru notaðar til að bjóða upp á aukaleiðsögn á vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="08777-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="08777-106">Þær eru venjulega sýndar efst á síðunni, undir hausnum.</span><span class="sxs-lookup"><span data-stu-id="08777-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="08777-107">Þrátt fyrir að hægt sé að bæta brauðmylsnueiningum við hvaða síðu sem er, eru þær oftast notaðar upplýsingasíðum afurða til að sýna tegundastigveldi afurðar og bjóða upp á styttri leið til að flakka um svæði.</span><span class="sxs-lookup"><span data-stu-id="08777-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="08777-108">Einnig er hægt að nota brauðmylsnueininguna til að sýna tengilinn „Aftur í niðurstöður“ þegar notendur opna upplýsingasíðu afurðar af leitar- eða listasíðu.</span><span class="sxs-lookup"><span data-stu-id="08777-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="08777-109">Á þennan hátt geta notendur á fljótlegan hátt farið aftur á síuðu listasíðuna til að halda áfram að versla.</span><span class="sxs-lookup"><span data-stu-id="08777-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="08777-110">Á síðum sem eru með samhengi afurðategunda, t.d. upplýsingasíður afurða og flokkasíður, sýna brauðmylsnueiningar tegundastigveldið.</span><span class="sxs-lookup"><span data-stu-id="08777-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="08777-111">Á síðum sem eru ekki með flokkasamhengi, sýna brauðmylsnueiningar sjálfgefið **&lt;Rót svæðis&gt; / &lt;Núverandi síða&gt;**.</span><span class="sxs-lookup"><span data-stu-id="08777-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="08777-112">Einnig er hægt að skilgreina brauðmylsnueiningar handvirkt á öðrum gerðum svæðissíðna til að sýna tengla á ákveðnar síður á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="08777-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="08777-113">Brauðmylsnueiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="08777-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="08777-114">Eftirfarandi mynd sýnir dæmi um brauðmylsnueiningu sem sýnir tegundastigveldi á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Dæmi um brauðmylsnueiningu](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="08777-116">Stillingar brauðmylsnueiningar</span><span class="sxs-lookup"><span data-stu-id="08777-116">Breadcrumb module settings</span></span>

<span data-ttu-id="08777-117">Brauðmylsnueiningin er háð stillingunni **Birtingargerð brauðmylsnu á upplýsingasíðu afurðar** sem er skilgreind í **Stillingar svæðis \> Viðbætur** í svæðissmið.</span><span class="sxs-lookup"><span data-stu-id="08777-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="08777-118">Þessi stilling er með þrjú möguleg gildi:</span><span class="sxs-lookup"><span data-stu-id="08777-118">This setting has three possible values:</span></span>

- <span data-ttu-id="08777-119">**Sýna tegundastigveldi** – Þegar þetta gildi er valið sýnir brauðmylsnueiningin allt tegundastigveldi afurðarinnar sem er sýnt á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="08777-120">**Sýna aftur í niðurstöður** - Þegar þetta gildi er valið mun brauðmylsnueiningin sýna „Aftur í niðurstöður“ tengil á upplýsingasíðu afurðar ef notandinn opnaði upplýsingasíðu afurðar úr einingunni sem leyfir tengil fyrir „Aftur í niðurstöður“.</span><span class="sxs-lookup"><span data-stu-id="08777-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="08777-121">Þessi virkni er í boði þegar notendur fara úr flokka-, leitar-, lista- og tillögulistasíðum.</span><span class="sxs-lookup"><span data-stu-id="08777-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="08777-122">Til að styðja þessa virkni eru einingar vörusafns og leitarniðurstaðna með eiginleika sem heitir **Leyfa aftur í niðurstöður á upplýsingasíðu afurðar**.</span><span class="sxs-lookup"><span data-stu-id="08777-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="08777-123">Þessi eiginleiki gefur sveigjanleika til að skilgreina hvaða einingar eigi að styðja virknina fyrir tengil „Aftur í niðurstöður“ á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="08777-124">Til dæmis þegar **Sýna aftur í niðurstöður** er valið fyrir stillinguna **Birtingargerð brauðmylsna á upplýsingasíðu afurðar** á brauðmylsnueiningunni og **Leyfa aftur í niðurstöður á upplýsingasíðu afurðar** er valið fyrir einingu leitarniðurstaðna leitarsíðu, er tengill fyrir „Aftur í niðurstöður“ sýndur þegar notendur fara frá leitarsíðunni til upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="08777-125">**Sýna tegundastigveldi og aftur í niðurstöður** – Þetta gildi er samsetning fyrri tveggja.</span><span class="sxs-lookup"><span data-stu-id="08777-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="08777-126">Þegar þetta gildi er valið sýnir brauðmylsnueiningin bæði allt tegundastigveldið og tengilinn „Aftur í niðurstöður“ (ef hann er skilgreindur) á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08777-127">Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="08777-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="08777-128">Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="08777-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="08777-129">Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="08777-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="08777-130">Eiginleikar brauðmylsnueiningar</span><span class="sxs-lookup"><span data-stu-id="08777-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="08777-131">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="08777-131">Property name</span></span> | <span data-ttu-id="08777-132">Gildi</span><span class="sxs-lookup"><span data-stu-id="08777-132">Values</span></span> | <span data-ttu-id="08777-133">lýsing</span><span class="sxs-lookup"><span data-stu-id="08777-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="08777-134">Rót</span><span class="sxs-lookup"><span data-stu-id="08777-134">Root</span></span> | <span data-ttu-id="08777-135">Texti eða tengill</span><span class="sxs-lookup"><span data-stu-id="08777-135">Text or link</span></span>| <span data-ttu-id="08777-136">Þessi valfrjálsi eiginleiki sýnir texta tengils og viðtökustað tengils fyrir rót brauðmylsnusvæðis.</span><span class="sxs-lookup"><span data-stu-id="08777-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="08777-137">Ef þessi eiginleiki er ekki stilltur verður engin rót skilgreind.</span><span class="sxs-lookup"><span data-stu-id="08777-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="08777-138">Brauðmylsnutengill</span><span class="sxs-lookup"><span data-stu-id="08777-138">Breadcrumb link</span></span> | <span data-ttu-id="08777-139">Tengill</span><span class="sxs-lookup"><span data-stu-id="08777-139">Link</span></span> | <span data-ttu-id="08777-140">Þessi valfrjálsi eiginleiki sýnir tengla fyrir handvirkt stillta brauðmylsnu ef þessir tenglar eru nauðsynlegir.</span><span class="sxs-lookup"><span data-stu-id="08777-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="08777-141">Tenglar birtast í þeirri röð sem þeir eru sýndir.</span><span class="sxs-lookup"><span data-stu-id="08777-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="08777-142">Bæta brauðmylsnueiningu við nýja síðu</span><span class="sxs-lookup"><span data-stu-id="08777-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="08777-143">Til að bæta brauðmylsnueiningu við upplýsingasíðu afurðar og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="08777-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="08777-144">Farið í **Stillingar svæðis \> Viðbætur** og síðan, fyrir stillinguna **Birtingargerð brauðmylsnu á upplýsingasíðu afurðar**, skal velja **Sýna tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="08777-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="08777-145">Opnið **Sniðmát** og veljið sniðmát upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="08777-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="08777-146">Í hólfinu **Geymsla** sem inniheldur kaupgluggaeininguna skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="08777-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="08777-147">Í svarglugganum **Bæta við einingu** skal velja eininguna **Brauðmylsna** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08777-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="08777-148">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="08777-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="08777-149">Farið á **Síður**, og Opnið PDP sem notar PDP-sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="08777-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="08777-150">Ef PDP er ekki til staðar skal stofna eitt.</span><span class="sxs-lookup"><span data-stu-id="08777-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="08777-151">Í hólfinu **Geymsla** sem inniheldur kaupgluggaeininguna skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="08777-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="08777-152">Í svarglugganum **Bæta við einingu** skal velja eininguna **Brauðmylsna** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08777-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="08777-153">Á eiginleikasvæði hólfsins **Brauðmylsna**, undir **Rót**, skal velja **Texti tengils**.</span><span class="sxs-lookup"><span data-stu-id="08777-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="08777-154">Í svarglugganum **Texti tengils** skal slá inn **Heim** og síðan, undir **Viðtökustaður tengils**, skal velja **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="08777-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="08777-155">Í svarglugganum **Bæta við tengli** skal velja tengil fyrir brauðmylsnurótina og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="08777-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="08777-156">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="08777-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="08777-157">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="08777-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08777-158">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="08777-158">Additional resources</span></span>

[<span data-ttu-id="08777-159">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="08777-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="08777-160">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="08777-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="08777-161">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="08777-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="08777-162">Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="08777-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="08777-163">Afurðasafnseiningar</span><span class="sxs-lookup"><span data-stu-id="08777-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="08777-164">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="08777-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="08777-165">Uppfærslur á SDK og kjarnasafni</span><span class="sxs-lookup"><span data-stu-id="08777-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]