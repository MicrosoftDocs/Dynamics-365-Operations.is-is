---
title: Virkja sérsniðnar afurðaráðleggingar
description: Þetta efni lýsir því hvernig hægt er að gera persónulegar ráðleggingar um vöru tiltækar fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413130"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="70859-103">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="70859-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70859-104">Þetta efni lýsir því hvernig hægt er að gera persónulegar ráðleggingar um vöru tiltækar fyrir viðskiptavini Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70859-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="70859-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="70859-105">Overview</span></span>

<span data-ttu-id="70859-106">Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar.</span><span class="sxs-lookup"><span data-stu-id="70859-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="70859-107">Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="70859-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="70859-108">Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="70859-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="70859-109">Forsendur sérstillingar</span><span class="sxs-lookup"><span data-stu-id="70859-109">Personalization prerequisites</span></span>

<span data-ttu-id="70859-110">Áður en þú gerir persónulegar ráðleggingar um vörur tiltækar fyrir viðskiptavini skaltu hafa í huga að tillögur um vöru eru aðeins studdar notendum viðskiptamanna sem hafa flutt geymslu sína til Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70859-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="70859-111">Áður en viðskiptavinir geta fengið persónulegar ráðleggingar um vöru verða smásalar að gera það [kveikja á ráðleggingum um vörur](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="70859-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="70859-112">Með því að kveikja á tilmælum til vara kveikirðu líka á sérsniðinni.</span><span class="sxs-lookup"><span data-stu-id="70859-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="70859-113">Hins vegar, ef þú slekkur á sérstillingu, slekkurðu ekki á öðrum tegundum ráðlegginga um vöru.</span><span class="sxs-lookup"><span data-stu-id="70859-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="70859-114">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="70859-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="70859-115">Kveikja á aðlögun</span><span class="sxs-lookup"><span data-stu-id="70859-115">Turn on personalization</span></span>

<span data-ttu-id="70859-116">Fylgdu þessum skrefum til að kveikja á persónuaðlögun.</span><span class="sxs-lookup"><span data-stu-id="70859-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="70859-117">Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="70859-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="70859-118">Veljið **Allir** til að sjá lista yfir tiltæka eiginleika.</span><span class="sxs-lookup"><span data-stu-id="70859-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="70859-119">Í leitarreitnum skal slá inn **Ráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="70859-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="70859-120">Velja eiginleikann **Sérsniðnar afurðarráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="70859-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="70859-121">Á svæðinu **Sérsniðnar afurðaráðleggingar** skal velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="70859-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Kveikt á aðlögun](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="70859-123">Þegar þú kveikir á sérsniðinni er ferlið við að búa til sérsniðna vöru meðmæla lista byrjað.</span><span class="sxs-lookup"><span data-stu-id="70859-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="70859-124">Allt að einn dagur gæti verið nauðsynlegur áður en þessir listar eru tiltækir og sýnilegir á netinu og í POS.</span><span class="sxs-lookup"><span data-stu-id="70859-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="70859-125">Sérsniðnir listar</span><span class="sxs-lookup"><span data-stu-id="70859-125">Personalized lists</span></span>

<span data-ttu-id="70859-126">Auk þess að gera ráð fyrir að sérsníða fyrirliggjandi vélalista, gera ráðleggingarþjónustan kleift að sérsníða reynslu af uppgötvun vöru bæði á netinu og í POS.</span><span class="sxs-lookup"><span data-stu-id="70859-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="70859-127">Eftir að kveikt er á sérstillingu geta smásalar sýnt kaupendum persónulega „Tillögur fyrir þig“ lista á netinu eða „Mælt með fyrir viðskiptavini“ lista á POS skautanna.</span><span class="sxs-lookup"><span data-stu-id="70859-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="70859-128">Að auki geta smásalar beitt sérsniðningu á fyrirliggjandi vörumælalista og útvegað Almennu persónuverndarreglugerðina (GDPR) uppljóstrunarupplifun fyrir staðfesta notendur.</span><span class="sxs-lookup"><span data-stu-id="70859-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="70859-129">Ef þú slekkur á sérsniðinni, slekkurðu einnig á þessum eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="70859-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="70859-130">Listar yfir „Tillögur fyrir þig“ á netinu</span><span class="sxs-lookup"><span data-stu-id="70859-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="70859-131">„Tillögur fyrir þig“ listi er listi yfir gervigreindarvélar (AI-ML) sem sýnir staðfestum notanda persónulega lista yfir fyrirhugaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="70859-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="70859-132">Þessi listi er byggður á fjölrása kaupsögu notandans.</span><span class="sxs-lookup"><span data-stu-id="70859-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="70859-133">Sérsniðnar ráðleggingar eru uppfærðar með virkum hætti þegar notandinn gerir fleiri kaup.</span><span class="sxs-lookup"><span data-stu-id="70859-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="70859-134">Þessi tegund af lista styður einnig flokkun sía, svo að smásalar geti sýnt helstu val, byggðar á stigveldum siglinga.</span><span class="sxs-lookup"><span data-stu-id="70859-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="70859-135">Áður en „Tillögur fyrir þig“ listinn getur birst á hvaða e-Commerce síðu sem er þarf að uppfylla eftirfarandi notendakröfur:</span><span class="sxs-lookup"><span data-stu-id="70859-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="70859-136">Notendur verða að vera skráðir inn.</span><span class="sxs-lookup"><span data-stu-id="70859-136">Users must be signed in.</span></span> <span data-ttu-id="70859-137">Nafnlausir notendur munu ekki sjá persónulegar tillögur.</span><span class="sxs-lookup"><span data-stu-id="70859-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="70859-138">Notendur verða að hafa að minnsta kosti eina kaup á reikningi sínum.</span><span class="sxs-lookup"><span data-stu-id="70859-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="70859-139">Notendur verða að taka þátt í að fá persónulegar ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="70859-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="70859-140">Eftirfarandi mynd sýnir dæmi um „Tillögur fyrir þig“ á netverslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="70859-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Listar yfir „Tillögur fyrir þig“ á netinu](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="70859-142">Listar með „Mælt með fyrir viðskiptavini“ í POS</span><span class="sxs-lookup"><span data-stu-id="70859-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="70859-143">Til að auka upplifun viðskiptavinarins geta smásalar sérsniðið núverandi upplýsingasíður viðskiptavina með því að bæta við samhengislistann „Mælt með fyrir viðskiptavini“.</span><span class="sxs-lookup"><span data-stu-id="70859-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="70859-144">Eftirfarandi mynd sýnir dæmi um „Mælt með fyrir viðskiptavini“ á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="70859-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Listinn Mællt með fyrir viðskiptavini í POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="70859-146">Notaðu persónugervingu á fyrirliggjandi meðmæla lista</span><span class="sxs-lookup"><span data-stu-id="70859-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="70859-147">Söluaðilar geta beitt sérsniðum á fyrirliggjandi ráðleggingalista, svo sem „Nýtt“, „Væntanlegt“, „Mest selt“, „Fólk kann líka vel við“ og „Oft keypt saman.“</span><span class="sxs-lookup"><span data-stu-id="70859-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="70859-148">Þegar sérstillingu er beitt á núverandi lista eru hlutir sem skráður notandi keypti áður keyptir af þessum listum.</span><span class="sxs-lookup"><span data-stu-id="70859-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="70859-149">Fyrir bæði nafnlausa notendur og notendur sem hafa afþakkað að fá persónulegar ráðleggingar, eru sjálfgefnar útgáfur af núverandi listum sýndar.</span><span class="sxs-lookup"><span data-stu-id="70859-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="70859-150">Þess vegna þurfa smásalar ekki að hafa sérstaka síðureynslu handvirkt.</span><span class="sxs-lookup"><span data-stu-id="70859-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="70859-151">Til dæmis hefur skráður notandi þegar keypt svarta úrið og brúnu vinnuskóna sem birtast á listanum „Vinsælt - sjálfgildi“ á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="70859-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="70859-152">Þess vegna mun notandinn sjá nýjar vörur í stað þessara vara, eins og sýnt er í listanum „Vinsælt - sérsniðið“.</span><span class="sxs-lookup"><span data-stu-id="70859-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Að beita sérsniðum](./media/applypersonalization.png)

<span data-ttu-id="70859-154">Fylgdu þessum skrefum til að beita sérsniðun á fyrirliggjandi meðmælalista í vefsvæðishönnuði Commerce.</span><span class="sxs-lookup"><span data-stu-id="70859-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70859-155">Opnaðu núverandi síðu byggingarsíðu sem inniheldur vörusöfnunareiningu.</span><span class="sxs-lookup"><span data-stu-id="70859-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="70859-156">Í vinstri stýriglugganum velurðu vörusafnseininguna.</span><span class="sxs-lookup"><span data-stu-id="70859-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="70859-157">Í hægri stýriglugganum undir **Afurðir** velurðu listann.</span><span class="sxs-lookup"><span data-stu-id="70859-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="70859-158">Í **Veldu stillingu vörulistans** valmynd, undir **Gerð**, veldu gerð listans.</span><span class="sxs-lookup"><span data-stu-id="70859-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="70859-159">Veldu **Notaðu sérsnið** merktu við reitinn og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="70859-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Notkun sérsniðs á vinsældalista](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="70859-161">Vistaðu síðuna, ljúktu við að breyta því og birtu hana síðan.</span><span class="sxs-lookup"><span data-stu-id="70859-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="70859-162">Eftir að síðunni er birt munu innskráðir notendur sjá sérsniðna vinsældalista.</span><span class="sxs-lookup"><span data-stu-id="70859-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70859-163">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="70859-163">Additional resources</span></span>

[<span data-ttu-id="70859-164">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="70859-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="70859-165">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="70859-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="70859-166">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="70859-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="70859-167">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="70859-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="70859-168">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="70859-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="70859-169">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="70859-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="70859-170">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="70859-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="70859-171">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="70859-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="70859-172">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="70859-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="70859-173">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="70859-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="70859-174">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="70859-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
