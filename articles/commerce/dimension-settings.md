---
title: Nota skjástillingar fyrir afurðavíddir
description: Í þessu efnisatriði er fjallað um skjástillingar fyrir afurðarvíddir og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117229"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="e50c4-103">Nota skjástillingar fyrir afurðavíddir</span><span class="sxs-lookup"><span data-stu-id="e50c4-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e50c4-104">Í þessu efnisatriði er fjallað um skjástillingar fyrir afurðarvíddir og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e50c4-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e50c4-105">Dynamics 365 Commerce styður stærð, stíl og litvíddir til að greina afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="e50c4-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="e50c4-106">Stærðir eru yfirleitt sýndar sem textagildi, t.d. „Lítið“, „Miðlungs“ og „Stórt“ fyrir stærðir og „Svart“ og „Brúnt“ fyrir liti.</span><span class="sxs-lookup"><span data-stu-id="e50c4-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="e50c4-107">Ef afurð styður hinsvegar mörg afbrigði getur reynst erfitt að leita í afurðarafbrigðum vegna þess að margs konar val er nauðsynlegt til að skoða myndina fyrir hvert afbrigði.</span><span class="sxs-lookup"><span data-stu-id="e50c4-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="e50c4-108">Til að gera það auðveldara að skoða afurðarafbrigði getur útgáfa 10.0.20 af Commerce notað myndir og sextándakerfiskóða til að sýna víddir sem sýnishorn.</span><span class="sxs-lookup"><span data-stu-id="e50c4-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="e50c4-109">Í vefsmið Commerce eru víddastillingar skilgreindar á **Stillingar svæðis \> Viðbætur \> Stillingar víddar**.</span><span class="sxs-lookup"><span data-stu-id="e50c4-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="e50c4-110">Eftirfarandi skýringarmynd sýnir dæmi um víddastillingar í vefsmið.</span><span class="sxs-lookup"><span data-stu-id="e50c4-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Dæmi um svæðisstillingar í vefsmið Commerce](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="e50c4-112">Tvær víddarsamstæður eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="e50c4-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="e50c4-113">**Víddir sem á að birta sem mynd** – Tilgreinið hvaða víddir ættu að birtast sem sýnishorn á svæðum rafrænna viðskipta á borð við upplýsingasíður afurða og listasíður leitarniðurstaða.</span><span class="sxs-lookup"><span data-stu-id="e50c4-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="e50c4-114">Hægt er að sýna hvaða samsetningu sem er af lita-, stærðar- og stílvíddum.</span><span class="sxs-lookup"><span data-stu-id="e50c4-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="e50c4-115">Ef vídd er valin til birtingar sem sýnishorn mun myndþýðingareining Commerce leita að tiltækri skilgreiningu á sýnishorni sextándakerfiskóða.</span><span class="sxs-lookup"><span data-stu-id="e50c4-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="e50c4-116">Ef enginn sextándakerfiskóði er stilltur leita kerfisrök að stillingu á sýnishorni myndaslóðar.</span><span class="sxs-lookup"><span data-stu-id="e50c4-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="e50c4-117">Ef hvorki sextándakerfiskóði né myndaslóð er skilgreind verður texti sýndur.</span><span class="sxs-lookup"><span data-stu-id="e50c4-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="e50c4-118">Eftirfarandi mynd sýnir dæmi þar sem upplýsingasíða afurðar á svæði fyrir rafræn viðskipti inniheldur sýnishorn lita og stærða.</span><span class="sxs-lookup"><span data-stu-id="e50c4-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="e50c4-119">Í þessu dæmi er sextándakerfiskóði skilgreindur fyrir litavíddina.</span><span class="sxs-lookup"><span data-stu-id="e50c4-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="e50c4-120">Því eru sýnishorn sýnd sem litir.</span><span class="sxs-lookup"><span data-stu-id="e50c4-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="e50c4-121">Hinsvegar er hvorki sextándakerfiskóði né myndaslóð stillt fyrir stærðarvíddina.</span><span class="sxs-lookup"><span data-stu-id="e50c4-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="e50c4-122">Því er texti sýndur.</span><span class="sxs-lookup"><span data-stu-id="e50c4-122">Therefore, text is shown.</span></span>

    ![Dæmi um litavíddina sem sýnd er sem sýnishorn á upplýsingasíðu afurðar á rafrænu svæði viðskipta](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="e50c4-124">**Víddir til að birta í afurðarspjaldi** – Tilgreinið hvaða víddir eigi að birtast á afurðarspjöldum sem eru sýnd í listum og á listasíðum.</span><span class="sxs-lookup"><span data-stu-id="e50c4-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="e50c4-125">Áður en vídd getur birst á afurðarspjaldi þarf að virkja þessa stillingu fyrir þá vídd.</span><span class="sxs-lookup"><span data-stu-id="e50c4-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="e50c4-126">Stillingin **Víddir til að birta sem mynd** ætti einnig að vera virk.</span><span class="sxs-lookup"><span data-stu-id="e50c4-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="e50c4-127">Hegðun sýnishornavals á afurðarspjöldum er fínstillt fyrir litavíddina.</span><span class="sxs-lookup"><span data-stu-id="e50c4-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="e50c4-128">Fyrir aðrar víddir gæti skoðunarviðbót verið nauðsynleg til að sérstilla hegðun sýnishornavals.</span><span class="sxs-lookup"><span data-stu-id="e50c4-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="e50c4-129">Eftirfarandi mynd sýnir dæmi þar sem listasíða á svæði rafrænna viðskipta inniheldur afurðarspjöld sem eru með litaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e50c4-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Dæmi um litavíddina sem sýnd er sem litaspjald á listasíðu svæðis fyrir rafræn viðskipti](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="e50c4-131">Upplýsingar um hvernig á að stilla víddir afurða þannig að þau eru birt sem sýnishorn á vefsíðum er að finna í [Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="e50c4-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e50c4-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e50c4-132">Additional resources</span></span>

[<span data-ttu-id="e50c4-133">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="e50c4-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e50c4-134">Leitarniðurstöðueining</span><span class="sxs-lookup"><span data-stu-id="e50c4-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="e50c4-135">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="e50c4-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e50c4-136">Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn</span><span class="sxs-lookup"><span data-stu-id="e50c4-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
