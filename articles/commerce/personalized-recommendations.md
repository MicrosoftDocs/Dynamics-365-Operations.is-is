---
title: Virkja sérsniðnar afurðaráðleggingar
description: Þetta efnisatriði lýsir því hvernig á að gera sérsniðnar afurðatillögur tiltækar fyrir viðskiptavini í Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804430"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="6be58-103">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="6be58-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6be58-104">Þetta efnisatriði lýsir því hvernig á að gera sérsniðnar afurðatillögur tiltækar fyrir viðskiptavini í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be58-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6be58-105">Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar.</span><span class="sxs-lookup"><span data-stu-id="6be58-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="6be58-106">Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="6be58-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="6be58-107">Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="6be58-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="6be58-108">Forsendur sérstillingar</span><span class="sxs-lookup"><span data-stu-id="6be58-108">Personalization prerequisites</span></span>

<span data-ttu-id="6be58-109">Áður en þú gerir persónulegar ráðleggingar um vörur tiltækar fyrir viðskiptavini skaltu hafa í huga að tillögur um vöru eru aðeins studdar notendum viðskiptamanna sem hafa flutt geymslu sína til Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6be58-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="6be58-110">Áður en viðskiptavinir geta fengið persónulegar ráðleggingar um vöru verða smásalar að gera það [kveikja á ráðleggingum um vörur](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6be58-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6be58-111">Með því að kveikja á tilmælum til vara kveikirðu líka á sérsniðinni.</span><span class="sxs-lookup"><span data-stu-id="6be58-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="6be58-112">Hins vegar, ef þú slekkur á sérstillingu, slekkurðu ekki á öðrum tegundum ráðlegginga um vöru.</span><span class="sxs-lookup"><span data-stu-id="6be58-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="6be58-113">Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6be58-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="6be58-114">Kveikja á aðlögun</span><span class="sxs-lookup"><span data-stu-id="6be58-114">Turn on personalization</span></span>

<span data-ttu-id="6be58-115">Fylgdu þessum skrefum til að kveikja á persónuaðlögun.</span><span class="sxs-lookup"><span data-stu-id="6be58-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="6be58-116">Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="6be58-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="6be58-117">Veljið **Allir** til að sjá lista yfir tiltæka eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6be58-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="6be58-118">Í leitarreitnum skal slá inn **Ráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="6be58-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="6be58-119">Velja eiginleikann **Sérsniðnar afurðarráðleggingar**.</span><span class="sxs-lookup"><span data-stu-id="6be58-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="6be58-120">Á svæðinu **Sérsniðnar afurðaráðleggingar** skal velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="6be58-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Kveikt á aðlögun](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="6be58-122">Þegar þú kveikir á sérsniðinni er ferlið við að búa til sérsniðna vöru meðmæla lista byrjað.</span><span class="sxs-lookup"><span data-stu-id="6be58-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="6be58-123">Allt að einn dagur gæti verið nauðsynlegur áður en þessir listar eru tiltækir og sýnilegir á netinu og í POS.</span><span class="sxs-lookup"><span data-stu-id="6be58-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="6be58-124">Sérsniðnir listar</span><span class="sxs-lookup"><span data-stu-id="6be58-124">Personalized lists</span></span>

<span data-ttu-id="6be58-125">Auk þess að gera ráð fyrir að sérsníða fyrirliggjandi vélalista, gera ráðleggingarþjónustan kleift að sérsníða reynslu af uppgötvun vöru bæði á netinu og í POS.</span><span class="sxs-lookup"><span data-stu-id="6be58-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="6be58-126">Eftir að kveikt er á sérstillingu geta smásalar sýnt kaupendum persónulega „Tillögur fyrir þig“ lista á netinu eða „Mælt með fyrir viðskiptavini“ lista á POS skautanna.</span><span class="sxs-lookup"><span data-stu-id="6be58-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="6be58-127">Að auki geta smásalar beitt sérsniðningu á fyrirliggjandi vörumælalista og útvegað Almennu persónuverndarreglugerðina (GDPR) uppljóstrunarupplifun fyrir staðfesta notendur.</span><span class="sxs-lookup"><span data-stu-id="6be58-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="6be58-128">Ef þú slekkur á sérsniðinni, slekkurðu einnig á þessum eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="6be58-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="6be58-129">Listar yfir „Tillögur fyrir þig“ á netinu</span><span class="sxs-lookup"><span data-stu-id="6be58-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="6be58-130">„Tillögur fyrir þig“ listi er listi yfir gervigreindarvélar (AI-ML) sem sýnir staðfestum notanda persónulega lista yfir fyrirhugaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="6be58-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="6be58-131">Þessi listi er byggður á fjölrása kaupsögu notandans.</span><span class="sxs-lookup"><span data-stu-id="6be58-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="6be58-132">Sérsniðnar ráðleggingar eru uppfærðar með virkum hætti þegar notandinn gerir fleiri kaup.</span><span class="sxs-lookup"><span data-stu-id="6be58-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="6be58-133">Þessi tegund af lista styður einnig flokkun sía, svo að smásalar geti sýnt helstu val, byggðar á stigveldum siglinga.</span><span class="sxs-lookup"><span data-stu-id="6be58-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="6be58-134">Áður en „Tillögur fyrir þig“ listinn getur birst á hvaða e-Commerce síðu sem er þarf að uppfylla eftirfarandi notendakröfur:</span><span class="sxs-lookup"><span data-stu-id="6be58-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="6be58-135">Notendur verða að vera skráðir inn.</span><span class="sxs-lookup"><span data-stu-id="6be58-135">Users must be signed in.</span></span> <span data-ttu-id="6be58-136">Nafnlausir notendur munu ekki sjá persónulegar tillögur.</span><span class="sxs-lookup"><span data-stu-id="6be58-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="6be58-137">Notendur verða að hafa að minnsta kosti eina kaup á reikningi sínum.</span><span class="sxs-lookup"><span data-stu-id="6be58-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="6be58-138">Notendur verða að taka þátt í að fá persónulegar ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="6be58-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="6be58-139">Eftirfarandi mynd sýnir dæmi um „Tillögur fyrir þig“ á netverslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="6be58-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Listar yfir „Tillögur fyrir þig“ á netinu](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="6be58-141">Listar með „Mælt með fyrir viðskiptavini“ í POS</span><span class="sxs-lookup"><span data-stu-id="6be58-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="6be58-142">Til að auka upplifun viðskiptavinarins geta smásalar sérsniðið núverandi upplýsingasíður viðskiptavina með því að bæta við samhengislistann „Mælt með fyrir viðskiptavini“.</span><span class="sxs-lookup"><span data-stu-id="6be58-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="6be58-143">Eftirfarandi mynd sýnir dæmi um „Mælt með fyrir viðskiptavini“ á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="6be58-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Listinn Mællt með fyrir viðskiptavini í POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="6be58-145">Notaðu persónugervingu á fyrirliggjandi meðmæla lista</span><span class="sxs-lookup"><span data-stu-id="6be58-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="6be58-146">Söluaðilar geta beitt sérsniðum á fyrirliggjandi ráðleggingalista, svo sem „Nýtt“, „Væntanlegt“, „Mest selt“, „Fólk kann líka vel við“ og „Oft keypt saman.“</span><span class="sxs-lookup"><span data-stu-id="6be58-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="6be58-147">Þegar sérstillingu er beitt á núverandi lista eru hlutir sem skráður notandi keypti áður keyptir af þessum listum.</span><span class="sxs-lookup"><span data-stu-id="6be58-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="6be58-148">Fyrir bæði nafnlausa notendur og notendur sem hafa afþakkað að fá persónulegar ráðleggingar, eru sjálfgefnar útgáfur af núverandi listum sýndar.</span><span class="sxs-lookup"><span data-stu-id="6be58-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="6be58-149">Þess vegna þurfa smásalar ekki að hafa sérstaka síðureynslu handvirkt.</span><span class="sxs-lookup"><span data-stu-id="6be58-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="6be58-150">Til dæmis hefur skráður notandi þegar keypt svarta úrið og brúnu vinnuskóna sem birtast á listanum „Vinsælt - sjálfgildi“ á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="6be58-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="6be58-151">Þess vegna mun notandinn sjá nýjar vörur í stað þessara vara, eins og sýnt er í listanum „Vinsælt - sérsniðið“.</span><span class="sxs-lookup"><span data-stu-id="6be58-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Að beita sérsniðum](./media/applypersonalization.png)

<span data-ttu-id="6be58-153">Fylgdu þessum skrefum til að beita sérsniðun á fyrirliggjandi meðmælalista í vefsvæðishönnuði Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be58-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6be58-154">Opnaðu núverandi síðu byggingarsíðu sem inniheldur vörusöfnunareiningu.</span><span class="sxs-lookup"><span data-stu-id="6be58-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="6be58-155">Í vinstri stýriglugganum velurðu vörusafnseininguna.</span><span class="sxs-lookup"><span data-stu-id="6be58-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="6be58-156">Í hægri stýriglugganum undir **Afurðir** velurðu listann.</span><span class="sxs-lookup"><span data-stu-id="6be58-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="6be58-157">Í **Veldu stillingu vörulistans** valmynd, undir **Gerð**, veldu gerð listans.</span><span class="sxs-lookup"><span data-stu-id="6be58-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="6be58-158">Veldu **Notaðu sérsnið** merktu við reitinn og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6be58-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Notkun sérsniðs á vinsældalista](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="6be58-160">Vistaðu síðuna, ljúktu við að breyta því og birtu hana síðan.</span><span class="sxs-lookup"><span data-stu-id="6be58-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="6be58-161">Eftir að síðunni er birt munu innskráðir notendur sjá sérsniðna vinsældalista.</span><span class="sxs-lookup"><span data-stu-id="6be58-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6be58-162">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6be58-162">Additional resources</span></span>

[<span data-ttu-id="6be58-163">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6be58-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="6be58-164">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="6be58-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6be58-165">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="6be58-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6be58-166">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="6be58-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="6be58-167">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="6be58-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="6be58-168">Bæta afurðaráðleggingum við sölustað</span><span class="sxs-lookup"><span data-stu-id="6be58-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="6be58-169">Bæta við tillögum á færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="6be58-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="6be58-170">Aðlagaðu niðurstöður AI-ML</span><span class="sxs-lookup"><span data-stu-id="6be58-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6be58-171">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6be58-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6be58-172">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="6be58-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="6be58-173">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="6be58-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
