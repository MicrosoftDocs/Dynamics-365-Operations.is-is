---
title: Nota stillingar mælieiningar
description: Í efnisatriði er fjallað um stillingar mælieininga og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 7d338ba207c9a101f5e224ca66555b16a457bcbc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271402"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="e9a1c-103">Nota stillingar mælieiningar</span><span class="sxs-lookup"><span data-stu-id="e9a1c-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9a1c-104">Í efnisatriði er fjallað um stillingar mælieininga og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e9a1c-105">Hægt er að selja vöru í mismunandi einingum, eins og „hver“, „par“ og „tugir“.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="e9a1c-106">Í Commerce Headquarters er hægt að skilgreina hverja mælieiningu fyrir sig fyrir vöru og sýna hana á svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="e9a1c-107">Ef söluaðili selur vöru bæði í stökum einingum og í tugum er hægt að sýna tiltækar mælieiningar ásamt öðrum vöruupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="e9a1c-108">Í dæminu á eftirfarandi mynd hefur verið stillt á vöru í mælieiningu **ea** (hverjr) í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Dæmi um vöru sem er stillt með mælieiningu í Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="e9a1c-110">Stuðningur við að sækja og sýna mælieininguna er tiltækur frá og með Commerce útgáfu 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="e9a1c-111">Stillingar mælieiningar</span><span class="sxs-lookup"><span data-stu-id="e9a1c-111">Unit of measure settings</span></span>

<span data-ttu-id="e9a1c-112">Skjástillingar mælieininga eru skilgreindar í vefsmið Commerce á **Stillingar vefsvæðis \> Viðbætur \> Birta mælieiningu fyrir afurðir**.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="e9a1c-113">Þrjár stillingar eru studdar:</span><span class="sxs-lookup"><span data-stu-id="e9a1c-113">There are three supported settings:</span></span>

- <span data-ttu-id="e9a1c-114">**Ekki birta** – Þegar þessi stillingu er valin mun vefsvæði netverslunar ekki sýna mælieiningu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="e9a1c-115">Þessi hegðun er sjálfgefin hegðun.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="e9a1c-116">**Birta í kaupupplifun afurðar** – Þegar þessi stilling er valin er mælieiningin sýnd á síðum afurðaupplýsinga, körfu, greiðsluferlis, pöntunarferils og pöntunarupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="e9a1c-117">**Birta í afurðaflettingu og kaupupplifun** – Þegar þessi stilling er valin er mælieiningin sýnd á síðum kaupupplifunar fyrir afurð og einnig í flettingarupplifun afurðar.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="e9a1c-118">Mælieiningar eru sýndar í leitarniðurstöðum og vörusafnseiningum sem hluti af þessari hegðun.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9a1c-119">Skjástillingar mælieiningar er í boði frá og með Commerce útgáfu 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="e9a1c-120">Ef verið er að uppfæra úr eldri útgáfu af Commerce verður að uppfæra appsettings.json-skrána handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="e9a1c-121">Leiðbeiningar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="e9a1c-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="e9a1c-122">Einingar sem nota stillingar mælieiningar</span><span class="sxs-lookup"><span data-stu-id="e9a1c-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="e9a1c-123">Einingar sem nota mælieiningarstillingarnar eru kaupkassar, óskalisti, karfa, körfutákn, leitarniðurstöðuílát, vörusöfnun, greiðslu- og pöntunarupplýsingaeiningar.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="e9a1c-124">Í dæminu á eftirfarandi mynd sýnir upplýsingar um afurð (PDP) mælieininguna (**ea**) fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Dæmi um vörusafnseiningu sem sýnir mælieininguna](./media/Productunit-PDP.png)

<span data-ttu-id="e9a1c-126">Í dæminu á eftirfarandi mynd sýnir vörusafnseining mælieininguna (**ea**) fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="e9a1c-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Dæmi um vörusafnseiningu sem sýnir mælieininguna](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="e9a1c-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e9a1c-128">Additional resources</span></span>

[<span data-ttu-id="e9a1c-129">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="e9a1c-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e9a1c-130">Körfueining</span><span class="sxs-lookup"><span data-stu-id="e9a1c-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e9a1c-131">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="e9a1c-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e9a1c-132">Síður og einingar fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="e9a1c-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="e9a1c-133">Uppfærslur á SDK og einingasafni</span><span class="sxs-lookup"><span data-stu-id="e9a1c-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
