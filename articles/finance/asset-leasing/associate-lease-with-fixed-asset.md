---
title: Tengja eignir við leigu
description: Efnið útskýrir hvernig á að tengja fyrirliggjandi eign við nýja leigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444586"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="01856-103">Tengja eignir við leigu</span><span class="sxs-lookup"><span data-stu-id="01856-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01856-104">Efnið útskýrir hvernig á að tengja fyrirliggjandi eign við nýja leigu.</span><span class="sxs-lookup"><span data-stu-id="01856-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="01856-105">Þegar eign er tengd við leigu verður eignarvirði afnotaréttar af eign (ROU) við fyrstu viðurkenningu kaupverð eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="01856-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="01856-106">Áður en hægt er að tengja eign við leigusamning þarf að stofna færslu fyrir eignina í „Eignir“.</span><span class="sxs-lookup"><span data-stu-id="01856-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="01856-107">Á síðunni **Samantekt leigu** þarf að stofna leigusamning og tengja eignina við viðkomandi leigusamning.</span><span class="sxs-lookup"><span data-stu-id="01856-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="01856-108">Bætið við leigu með því að fylgja eftirfarandi skrefum í [Bæta við eða afrita leigusamninga](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="01856-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="01856-109">Á síðunni **Bæta við leigusamningi**, í reitnum **Númer eignar** , skal velja eignina sem hefur ekki enn verið keypt.</span><span class="sxs-lookup"><span data-stu-id="01856-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="01856-110">Veljið **Bækur** og staðfestið greiðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="01856-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="01856-111">Veljið **Upphafleg skráning**.</span><span class="sxs-lookup"><span data-stu-id="01856-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="01856-112">Veljið **Færslubækur eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="01856-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="01856-113">Upphafleg bókarfærsla fyrir leigusamning debetfærir eignina fyrir þá upphæð sem venjulega er debetfærð á reikning ROU-eignar.</span><span class="sxs-lookup"><span data-stu-id="01856-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="01856-114">Nú er hægt að skoða færslugerðina og bókina fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="01856-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="01856-115">Veljið **Færslubókarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="01856-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="01856-116">Veljið **Línur** til að skoða stakar línur fyrir bókarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="01856-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="01856-117">Veljið færslubókarlínuna sem inniheldur eignina og veljið svo flipann **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="01856-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="01856-118">Flipinn **Eignir** sýnir færslugerðina og bókina.</span><span class="sxs-lookup"><span data-stu-id="01856-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="01856-119">Sjálfgefið er að reiturinn **færslugerð** sé stilltur á **kaup** og reiturinn **bók** sé stilltur á núverandi bók fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="01856-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="01856-120">Þegar búið er að bóka upphaflegu bókarfærsluna birtist færslan sem kaupfærsla fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="01856-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="01856-121">Til að skoða færslutöflu skal fara á **Eignir \> Eignir \> Eignir**, velja viðeigandi eign og velja síðan **Mat**.</span><span class="sxs-lookup"><span data-stu-id="01856-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="01856-122">Þú ættir að sjá að upphaflega bókarfærslan hafi stofnað kaupfærslu fyrir tilgreinda eign.</span><span class="sxs-lookup"><span data-stu-id="01856-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="01856-123">Nú er hægt að afskrifa eignina með því að nota staðlaða afskriftarvirkni í eignum.</span><span class="sxs-lookup"><span data-stu-id="01856-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="01856-124">Frekari upplýsingar um afskriftir eru í [Afskriftaaðferðir og hefðir](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="01856-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="01856-125">Ef eign er tengd við leigusamning eru hnapparnir **Afskrift eigna** og **Virðisrýrnun leigusamnings** óvirkir í eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="01856-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="01856-126">Hægt er að skoða færslur fyrir afskriftir eigna og virðisrýrnun leigusamninga úr eignum.</span><span class="sxs-lookup"><span data-stu-id="01856-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="01856-127">Hnappurinn **Eignarfærslur**, sem opnar fyrirspurnarskjámynd er einnig gerður óvirkur.</span><span class="sxs-lookup"><span data-stu-id="01856-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="01856-128">Einnig er hægt að opna **Eignarfærslur** fyrirspurnarskjámyndina í Eignir.</span><span class="sxs-lookup"><span data-stu-id="01856-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  