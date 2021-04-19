---
title: Áætlanagerð innan samstæðu
description: Þetta efnisatriði lýsir áætlanagerð innan samstæðu og útskýrir hvernig á að skilgreina áætlanagerð innan samstæðu með fínstillingu skipulagningar í Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c9ab724034a9bb40cfe155b748a0c7e25978add
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833354"
---
# <a name="intercompany-planning"></a><span data-ttu-id="b789a-103">Áætlanagerð innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="b789a-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b789a-104">Í sumum fyrirtækjum eru aðgerðir vörustjórnunar háðar öðrum lögaðilum (fyrirtækjum) innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b789a-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="b789a-105">Þessar aðgerðir eru meðhöndlaðar með sölu og innkaupum innan samstæðu, vegna þess að hver lögaðili hefur aðskilda bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="b789a-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="b789a-106">Þetta efnisatriði lýsir áætlanagerð innan samstæðu og útskýrir hvernig á að skilgreina áætlanagerð innan samstæðu með fínstillingu skipulagningar í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b789a-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b789a-107">Í þessu efnisatriði er notast við eftirfarandi mikilvæga samstæðuskilmála:</span><span class="sxs-lookup"><span data-stu-id="b789a-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="b789a-108">**Fyrir ofan** – Afstæð tilvísun í fyrirtæki eða aðfangakeðju.</span><span class="sxs-lookup"><span data-stu-id="b789a-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="b789a-109">Gefur til kynna hreyfingu í áttina að hráefnisbirgi.</span><span class="sxs-lookup"><span data-stu-id="b789a-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="b789a-110">**Fyrir neðan** – Afstæð tilvísun í fyrirtæki eða aðfangakeðju.</span><span class="sxs-lookup"><span data-stu-id="b789a-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="b789a-111">Gefur til kynna hreyfingu í áttina að viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="b789a-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="b789a-112">**Áætluð eftirspurn innan samstæðu** – Áætluð eftirspurn eftir afurð í fyrirtæki miðað við áætlaða eftirspurn afurðarinnar hjá fyrirtæki fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="b789a-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="b789a-113">Við aðaláætlanagerð getur áætlun í einu fyrirtæki falið í sér áætlaða eftirspurn innan samstæðu sem tengist áætluðum pöntunum úr áætlun í öðru fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b789a-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="b789a-114">Þessi eiginleiki er gagnlegur vegna þess að hann býður upp á fullan sýnileika á áætluðum pöntunum milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="b789a-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="b789a-115">Slíkt tryggir einnig að allar nauðsynlegar áætlaðar birgðapantanir séu stofnaðar, en án þess að krefjast þess að áætlaðar pantanir séu staðfestar fyrir eftirspurn innan samstæðunnar.</span><span class="sxs-lookup"><span data-stu-id="b789a-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="b789a-116">Þegar aðaláætlanagerð er keyrð úr aðaláætlun sem inniheldur áætlaða eftirspurn fyrir neðan, verða innkaupatillögur úr tengdum lánardrottnum innan samstæðu teknar með í áætluninni sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="b789a-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="b789a-117">Nauðsynleg uppsetning</span><span class="sxs-lookup"><span data-stu-id="b789a-117">Required setup</span></span>

<span data-ttu-id="b789a-118">Til að nota samstæðuáætlun verður þú að undirbúa kerfið þitt á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b789a-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="b789a-119">Losa verður viðeigandi afurðir í öllum viðeigandi fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="b789a-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="b789a-120">Frekari upplýsingar er að finna í [skilgreina og nota samstæðuviðskipti í Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) á Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="b789a-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="b789a-121">Eftirspurn fyrir neðan verður að svara með innkaupum af lánardrottinn sem er með samstæðutengsl við fyrirtækið fyrir ofan og viðeigandi sjálfgefnar birgðavíddir (svæði og vöruhús) viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="b789a-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="b789a-122">Frekari upplýsingar er að finna í [skilgreina og nota samstæðuviðskipti í Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) á Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="b789a-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="b789a-123">Aðaláætlunin í fyrirtækinu fyrir ofan verður að innihalda áætlaða eftirspurn fyrir neðan og tilgreina verður viðeigandi fyrirtæki og aðaláætlun í áætlunum fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="b789a-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="b789a-124">Þ.m.t. áætluð eftirspurn forstreymis</span><span class="sxs-lookup"><span data-stu-id="b789a-124">Include planned downstream demand</span></span>

<span data-ttu-id="b789a-125">Fylgið eftirfarandi skrefum til að skilgreina aðaláætlunina þannig að hún feli í sér áætlaða eftirspurn fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="b789a-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="b789a-126">Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="b789a-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="b789a-127">Velja eða stofnið aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="b789a-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="b789a-128">Á flýtiflipanum **Samstæðuáætlun** skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b789a-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="b789a-129">**Taka með áætlaða eftirspurn fyrir neðan** – Stillið þennan valkost á *Já* til að virkja áætlanagerð innan samstæðu fyrir aðaláætlunina.</span><span class="sxs-lookup"><span data-stu-id="b789a-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="b789a-130">**Áætlanir fyrir neðan** – Ef þú stillir **Taka með áætlaða eftirspurn fyrir neðan** á *Já* skaltu nota verkfæraslána og hnitanetið til að bæta við aðaláætlunum frá öðrum fyrirtækjum eins og óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b789a-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="b789a-131">Festa milli fyrirtækja með því að nota festingu á mörgum stigum</span><span class="sxs-lookup"><span data-stu-id="b789a-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="b789a-132">Í marglaga þarfarakningu er hægt að skoða þarfarakningu í mörgum fyrirtækjum til að sjá upphaflegan uppruna eftirspurnarinnar sem framboð mætir.</span><span class="sxs-lookup"><span data-stu-id="b789a-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="b789a-133">Fylgdu eftirfarandi skrefum til að skoða marglaga upplýsingar um þarfarakningu.</span><span class="sxs-lookup"><span data-stu-id="b789a-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="b789a-134">Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="b789a-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="b789a-135">Velja eða opna áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="b789a-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="b789a-136">Á aðgerðasvæðinu, í flipanum **Skoða**, í flokknum **Kröfur**, skal velja **Festingu á mörgum stigum**.</span><span class="sxs-lookup"><span data-stu-id="b789a-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="b789a-137">Samstæðudæmi sem inniheldur tvö fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="b789a-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="b789a-138">Í þessu dæmi er áætluð framleiðslupöntun stofnuð í USMF-fyrirtækinu til að mæta sölupöntun DEMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b789a-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="b789a-139">Í USMF er bein eftirspurn áætluð eftirspurn innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="b789a-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="b789a-140">Til að þessi eftirspurn birtist í USMF er aðaláætlanagerð keyrð fyrst í DEMF og síðan í USMF.</span><span class="sxs-lookup"><span data-stu-id="b789a-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="b789a-141">Eftirfarandi mynd sýnir hvernig þetta dæmi kann að birtast á síðunni **margbrotin Þarfarakning** fyrir áætluðu framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="b789a-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Samstæðudæmi sem inniheldur tvö fyrirtæki](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="b789a-143">Dæmi um fyrirtæki innan samstæðu sem felur í sér þrjú fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="b789a-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="b789a-144">Í þessu dæmi er áætluð innkaupatillaga stofnuð í USMF-fyrirtækinu til að mæta sölupöntun FRRT-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b789a-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="b789a-145">Í fyrirtækjunum DEMF og USMF er bein eftirspurn áætluð eftirspurn innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="b789a-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="b789a-146">Til að þessi eftirspurn birtist í USMF er aðaláætlanagerð keyrð fyrst í FRRT, síðan í DEMF og loks í USMF.</span><span class="sxs-lookup"><span data-stu-id="b789a-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="b789a-147">Eftirfarandi mynd sýnir hvernig þetta dæmi kann að birtast á síðunni **margbrotin Þarfarakning** fyrir áætluðu framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="b789a-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Dæmi um fyrirtæki innan samstæðu sem felur í sér þrjú fyrirtæki](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]