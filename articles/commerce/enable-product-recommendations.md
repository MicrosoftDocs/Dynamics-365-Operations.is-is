---
title: Virkja ráðleggingar um afurðir
description: Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: d3b970c3b93d8be12886b1c5a6bf91f0b33726dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2020
ms.locfileid: "3700843"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ee3f0-103">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="ee3f0-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee3f0-104">Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ee3f0-105">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ee3f0-106">Ráðleggingar fyrir skoðun</span><span class="sxs-lookup"><span data-stu-id="ee3f0-106">Recommendations pre-check</span></span>

<span data-ttu-id="ee3f0-107">Áður en er virkjað skal hafa í huga að afurðartillögur eru aðeins studdar fyrir Commerce-viðskiptavini sem hafa flutt geymsluna sína til að nota Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="ee3f0-108">Eftirfarandi stillingar verða að vera gerðar virkar í bakvinnslunni áður en ráðleggingar eru virkjaðar:</span><span class="sxs-lookup"><span data-stu-id="ee3f0-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="ee3f0-109">Gakktu úr skugga um að Azure Data Lake Storage hafi verið keypt og staðfest í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="ee3f0-110">Frekari upplýsingar er að finna í [Gakktu úr skugga um að Azure Data Lake Storage hafi verið keypt og staðfest í umhverfinu](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="ee3f0-111">Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið gerð sjálfvirk.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="ee3f0-112">Fyrir frekari upplýsingar, sjá [Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið sjálfvirk](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="ee3f0-113">Staðfestu að Azure AD auðkennisstilling innihaldi færslu fyrir tillögur.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="ee3f0-114">Nánari upplýsingar um framkvæmd þessarar aðgerðar eru hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="ee3f0-115">Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ee3f0-116">Til að læra meira um þetta uppsetningarferli, sjá [Vinna með mælingar](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="ee3f0-117">Azure AD auðkennisskilgreining</span><span class="sxs-lookup"><span data-stu-id="ee3f0-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="ee3f0-118">Þetta skref er nauðsynlegt fyrir alla viðskiptavini sem reka innra skipulag sem þjónustustillingu (IaaS).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="ee3f0-119">Fyrir viðskiptavini sem keyra á Service Fabric (SF) ætti þetta skref að vera sjálfvirkt og við mælum með að staðfesta að stillingin sé stillt eins og vænst er.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="ee3f0-120">Setja upp</span><span class="sxs-lookup"><span data-stu-id="ee3f0-120">Setup</span></span>

1. <span data-ttu-id="ee3f0-121">Úr bakvinnslunni leitarðu að síðunni **Azure Active Directory forrit**.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="ee3f0-122">Staðfestu hvort færsla sé fyrir hendi fyrir „RecommendationSystemApplication-1“.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="ee3f0-123">Ef færslan er ekki til skaltu bæta við nýrri færslu með eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="ee3f0-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="ee3f0-124">**Biðlarakenni** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="ee3f0-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="ee3f0-125">**Heiti** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="ee3f0-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="ee3f0-126">**Notandakenni** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ee3f0-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="ee3f0-127">Vistið og lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="ee3f0-128">Kveikja á tillögum</span><span class="sxs-lookup"><span data-stu-id="ee3f0-128">Turn on recommendations</span></span>

<span data-ttu-id="ee3f0-129">Til að kveikja á afurðatillögum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ee3f0-130">Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="ee3f0-131">Veljið **Allir** til að sjá lista yfir tiltæka eiginleika.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="ee3f0-132">Í leitarreitnum skal slá inn **Ráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="ee3f0-133">Veljið eiginleikann **Afurðaráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="ee3f0-134">Á eiginleikasvæðinu **Afurðaráðleggingar** skal velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Kveikt á tillögum](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="ee3f0-136">Þetta ferli hefur ferlið við að mynda afurðatillögulista.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ee3f0-137">Það getur tekið nokkrar klukkustundir áður en listarnir verða tiltækir og sjást á sölustað (POS) eða í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ee3f0-138">Stilla færibreytur tillögulista</span><span class="sxs-lookup"><span data-stu-id="ee3f0-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="ee3f0-139">Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ee3f0-140">Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ee3f0-141">Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ee3f0-142">Sýna tillögur um POS tæki</span><span class="sxs-lookup"><span data-stu-id="ee3f0-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="ee3f0-143">Eftir að hafa gert tillögur í bakvinnslu Commerce virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ee3f0-144">Til að fræðast um þetta ferli, sjá [Bættu ráðleggingastjórnun við viðskiptaskjáinn á POS tækjum](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ee3f0-145">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="ee3f0-145">Enable personalized recommendations</span></span>

<span data-ttu-id="ee3f0-146">Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="ee3f0-147">Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="ee3f0-148">Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="ee3f0-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="ee3f0-149">Til að læra meira um persónulegar ráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ee3f0-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee3f0-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ee3f0-150">Additional resources</span></span>

[<span data-ttu-id="ee3f0-151">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ee3f0-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ee3f0-152">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="ee3f0-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ee3f0-153">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="ee3f0-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ee3f0-154">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="ee3f0-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ee3f0-155">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="ee3f0-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ee3f0-156">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="ee3f0-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ee3f0-157">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="ee3f0-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ee3f0-158">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="ee3f0-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ee3f0-159">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ee3f0-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ee3f0-160">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="ee3f0-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ee3f0-161">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="ee3f0-161">Product recommendations FAQ</span></span>](faq-recommendations.md)

