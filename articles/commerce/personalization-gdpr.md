---
title: Afþakka sérsniðnar tillögur
description: Þetta efnisatriði útskýrir hvernig hægt er að leyfa viðskiptavinum afþakka móttöku sérsniðinna tillagna í Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e65fc54f87664caec95b2bc2c579d0820ae08c0f
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477685"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="9417b-103">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="9417b-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9417b-104">Þetta efnisatriði útskýrir hvernig hægt er að leyfa viðskiptavinum afþakka móttöku sérsniðinna tillagna í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9417b-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9417b-105">Við stofnun reiknings eru nýir viðskiptavinir sjálfkrafa settir upp til að fá persónulega ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="9417b-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="9417b-106">Hins vegar Dynamics 365 Commerce veitir smásöluaðilum ýmsar leiðir til að láta notendur afþakka að fá þessar ráðleggingar og takmarka vinnslu persónuupplýsinga sinna.</span><span class="sxs-lookup"><span data-stu-id="9417b-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="9417b-107">Sannvottir notendur sem afþakka að fá persónulegar ráðleggingar hætta strax að sjá persónulega lista.</span><span class="sxs-lookup"><span data-stu-id="9417b-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="9417b-108">Að auki verða öll persónuleg gögn sem safnað er til að sérsníða verða fjarlægð úr persónulegum ráðleggingalíkönum.</span><span class="sxs-lookup"><span data-stu-id="9417b-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="9417b-109">Nánari upplýsingar um persónulegar afurðaráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9417b-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="9417b-110">Leiðir fyrir smásala til að innleiða afþakkunarupplifun</span><span class="sxs-lookup"><span data-stu-id="9417b-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="9417b-111">Smásalar hafa þrjár leiðir til að innleiða afökkunarupplifun.</span><span class="sxs-lookup"><span data-stu-id="9417b-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="9417b-112">Að afþakka fyrir hönd notenda</span><span class="sxs-lookup"><span data-stu-id="9417b-112">Opting out on behalf of users</span></span>

<span data-ttu-id="9417b-113">Í reikningsstjórnun í bakvinnslu Commerce geta smásalar afþakkað fyrir hönd notenda.</span><span class="sxs-lookup"><span data-stu-id="9417b-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="9417b-114">Leitaðu að á heimasíðu bakvinnslu **allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="9417b-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="9417b-115">Leitaðu að og veldu viðskiptavin og veldu síðan flýtiflipann **Retail**.</span><span class="sxs-lookup"><span data-stu-id="9417b-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Flýtireiturinn Retail](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="9417b-117">Undir **Persónuvernd**, stilltu **Slökkva á sérstillingu** kostur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9417b-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Öryggisstillingar](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="9417b-119">Veljið **Vista** og lokið skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9417b-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="9417b-120">Eining byggð á afþakkunarreynslu</span><span class="sxs-lookup"><span data-stu-id="9417b-120">Module-based opt-out experience</span></span>

<span data-ttu-id="9417b-121">Söluaðilar geta látið staðfesta notendur afþakka sérsniðnar ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="9417b-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="9417b-122">Til að bjóða upp á þessa afþakkunarupplifun skaltu bæta við afþakkunareiningunni fyrir notendur á prófílsíðum viðskiptavinarreiknings.</span><span class="sxs-lookup"><span data-stu-id="9417b-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="9417b-123">Sérsniðnar viðbætur</span><span class="sxs-lookup"><span data-stu-id="9417b-123">Custom extensions</span></span>

<span data-ttu-id="9417b-124">Söluaðilar geta búið til sínar eigin viðbætur til að stjórna afþreyingarupplifun fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="9417b-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="9417b-125">Fyrir frekari upplýsingar, sjá [Hringdu í smáforritaskil smásölumiðlara](e-commerce-extensibility/call-retail-server-apis.md) og [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="9417b-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="9417b-126">Fáðu stafrænt afrit af persónulegum ráðleggingagögnum fyrir hönd staðfestra notanda</span><span class="sxs-lookup"><span data-stu-id="9417b-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="9417b-127">Viðskiptavinir gætu viljað fá stafrænt afrit af persónulegum gögnum sínum og einnig séð útflutt mynd af niðurstöðum ráðlegginga.</span><span class="sxs-lookup"><span data-stu-id="9417b-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="9417b-128">Ef viðskiptavinur óskar eftir þessum upplýsingum verður smásalinn að búa til sérsniðna viðbyggingu sem kallar forritunarviðmót smáforritsþjónustunnar (API) og fyrirspurnir fyrir fullan árangur frá **Velur fyrir þig** listi, byggður á auðkenni viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="9417b-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="9417b-129">Síðan er hægt að flytja niðurstöðurnar með kommu-aðgreindu gildi (CSV) og deila með viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="9417b-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="9417b-130">Eftirfarandi dæmi sýnir hvernig smásala getur sinnt þessu verkefni.</span><span class="sxs-lookup"><span data-stu-id="9417b-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="9417b-131">Söluaðilinn býr til sérsniðna viðbót til að draga persónulegar ráðleggingargögn fyrir hönd notandans.</span><span class="sxs-lookup"><span data-stu-id="9417b-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="9417b-132">Nánari upplýsingar um hvernig á að búa til einingar, klóna núverandi einingar, hringja í API fyrir smásala netþjóns og aðgerðir til að hringja í gögn, sjá [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="9417b-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="9417b-133">Sérsniðna viðbótin hringir í **fá tilmæli** kjarna gagnaaðgerð og miðlar nauðsynlegum upplýsingum til þeirra, byggðar á kröfum listans.</span><span class="sxs-lookup"><span data-stu-id="9417b-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="9417b-134">Í tilviki **Velur fyrir þig** listanum verður viðbótin að gefa réttan listaheiti og kenni viðskiptavina yfir í gagnaaðgerðina.</span><span class="sxs-lookup"><span data-stu-id="9417b-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="9417b-135">Ein leið til að búa til sérsniðna viðbót er að klóna núverandi vöruöflunareining sem er notuð til að skila niðurstöðum meðmæla.</span><span class="sxs-lookup"><span data-stu-id="9417b-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="9417b-136">Með því að klóna þessa núverandi einingu getur smásali breytt núverandi kóða og bætt við nýjum hnappi sem flytur niðurstöður ráðlegginganna yfir í CSV skjal.</span><span class="sxs-lookup"><span data-stu-id="9417b-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="9417b-137">Frekari upplýsingar er að finna í [Klóna einingar einingasafns](e-commerce-extensibility/clone-starter-module.md) og [Afurðasafnseiningar](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9417b-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="9417b-138">Sjá heildarskoðun á API-bókasafni smásöluþjónsins [API og viðskiptavinir smásölumiðstöðva og neytenda](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="9417b-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="9417b-139">Eftir að sérsniðna viðbótin er búin til getur smásalinn flutt út CSV-skrá yfir allar niðurstöður meðmæla, byggðar á sérstöku viðskiptavinaauðkenni auðkennds notanda.</span><span class="sxs-lookup"><span data-stu-id="9417b-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="9417b-140">Söluaðilinn getur deilt útfluttu CSV-skjalinu sem inniheldur fullan persónulega lista yfir ráðlagðar vörur með staðfestum notanda.</span><span class="sxs-lookup"><span data-stu-id="9417b-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9417b-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9417b-141">Additional resources</span></span>

[<span data-ttu-id="9417b-142">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9417b-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9417b-143">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="9417b-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9417b-144">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="9417b-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9417b-145">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="9417b-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9417b-146">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="9417b-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9417b-147">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="9417b-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9417b-148">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="9417b-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9417b-149">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="9417b-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9417b-150">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9417b-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9417b-151">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="9417b-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9417b-152">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="9417b-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
