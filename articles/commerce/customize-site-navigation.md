---
title: Sérstilla yfirlit svæðis
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur fyrir vafra á Microsoft Dynamics 365 Commerce svæðinu.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799350"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="7a9de-103">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="7a9de-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a9de-104">Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur fyrir vafra á Microsoft Dynamics 365 Commerce svæðinu.</span><span class="sxs-lookup"><span data-stu-id="7a9de-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="7a9de-105">Vefverslanir á netinu láta viðskiptavini gjarnan uppgötva og skoða vörur með því að fletta í gegnum vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="7a9de-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="7a9de-106">Þessi geta er yfirleitt til staðar með flipum efst á síðunni eða með stýristiku vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="7a9de-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="7a9de-107">Í Dynamics 365 Commerce geturðu stofnað og stjórnað stigveldisskipulagi flokksleiðsagnar þinna og vörunum sem eru í ýmsum flokkum.</span><span class="sxs-lookup"><span data-stu-id="7a9de-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="7a9de-108">Stofna yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="7a9de-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="7a9de-109">Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="7a9de-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7a9de-110">Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="7a9de-111">Veldu **Tegundastigveldi** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="7a9de-112">Gefðu stigveldinu heiti.</span><span class="sxs-lookup"><span data-stu-id="7a9de-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a9de-113">Efsti flokkurinn sem þú býrð til er hnútur rótarflokksins.</span><span class="sxs-lookup"><span data-stu-id="7a9de-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="7a9de-114">Hann verður ekki sýndur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="7a9de-114">It won't be shown on your site.</span></span> <span data-ttu-id="7a9de-115">Til að búa til flokkunarstigveldi þar sem einn efsti stigs hnút er sýndur á síðunni skaltu stofna og nefna flokkinn sem undirgildi af rótarflokknum.</span><span class="sxs-lookup"><span data-stu-id="7a9de-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="7a9de-116">Veldu **Nýr tegundahnútur** og gefðu flokknum heiti.</span><span class="sxs-lookup"><span data-stu-id="7a9de-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="7a9de-117">Haltu áfram að stofna systkina- og undirflokka eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7a9de-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="7a9de-118">Núna geturðu úthlutað vörum í hvern flokk sem þú bjóst til undir efsta stigs flokknum.</span><span class="sxs-lookup"><span data-stu-id="7a9de-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="7a9de-119">Sérsniðið röðun flokka</span><span class="sxs-lookup"><span data-stu-id="7a9de-119">Customize the order of categories</span></span>

<span data-ttu-id="7a9de-120">Sjálfgefið er að flokkarnir sem þú skilgreinir munu birtast í stafrófsröð á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="7a9de-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="7a9de-121">Hins vegar getur þú einnig sérsniðið birtingarröð flokka.</span><span class="sxs-lookup"><span data-stu-id="7a9de-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="7a9de-122">Úthluta gerð tegundastigveldis</span><span class="sxs-lookup"><span data-stu-id="7a9de-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="7a9de-123">Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="7a9de-124">Veldu **Tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="7a9de-125">Í aðgerðarúðunni á flipanum **Tegundastigveldi** í flokknum **Uppsetning** skal velja **Tengja stigveldisgerð**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="7a9de-126">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-126">Select **New**.</span></span>
1. <span data-ttu-id="7a9de-127">Í reitnum **Gerð tegundastigveldis** velurðu **Yfirlitsstigveldi rásar**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="7a9de-128">Í reitnum **Tegundastigveldi** velurðu yfirlitsstigveldi rásarinnar sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="7a9de-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="7a9de-129">Birta ný eða uppfærð yfirlitsstigveldi</span><span class="sxs-lookup"><span data-stu-id="7a9de-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="7a9de-130">Fylgdu þessum skrefum til að gera yfirlitsstigveldið aðgengilegt fyrir netverslunina.</span><span class="sxs-lookup"><span data-stu-id="7a9de-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="7a9de-131">Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="7a9de-132">Veldu netverslunina þína í trénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="7a9de-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="7a9de-133">Veldu **Birta uppfærslur rásar**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="7a9de-134">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="7a9de-135">Á listanum finnurðu og velur **Vinnslu 1040**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="7a9de-136">Veljið **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="7a9de-136">Select **Run now**.</span></span>
1. <span data-ttu-id="7a9de-137">Endurtaktu skref 5 og 6 fyrir vinnslur 1070 og 1150.</span><span class="sxs-lookup"><span data-stu-id="7a9de-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="7a9de-138">Sýna flokka á síðunni þinni</span><span class="sxs-lookup"><span data-stu-id="7a9de-138">Show categories on your site</span></span>

<span data-ttu-id="7a9de-139">Til að sýna flokkunarveldi í netverslun þinni verður þú að bæta við yfirlitseiningunni á viðeigandi stað í sniðmáti eða broti.</span><span class="sxs-lookup"><span data-stu-id="7a9de-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="7a9de-140">Eining yfirlitsvalmyndar mun síðan sýna yfirlitsstigveldi, að því tilskildu að þú hafir birt yfirlitsstigveldi þitt á rásinni sem vefsvæðið er bundið við.</span><span class="sxs-lookup"><span data-stu-id="7a9de-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="7a9de-141">Valmyndareiningin sem fylgir með í einingarsafninu gerir notendum aðeins kleift að skoða flokka sem eru ekki með undirflokka.</span><span class="sxs-lookup"><span data-stu-id="7a9de-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="7a9de-142">Ef viðskiptavinir þínir ættu að geta farið í flokka sem eru með undirflokka verður þú að sérsníða valmyndareininguna.</span><span class="sxs-lookup"><span data-stu-id="7a9de-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="7a9de-143">Bæta við sérsniðnum yfirlitsvalkostum</span><span class="sxs-lookup"><span data-stu-id="7a9de-143">Add custom navigation options</span></span>

<span data-ttu-id="7a9de-144">Á yfirlitsvalmyndinni geturðu bætt við yfirlitsvalkostum sem eru ekki hluti af tegundastigveldi afurðar.</span><span class="sxs-lookup"><span data-stu-id="7a9de-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="7a9de-145">Til dæmis, í lok lista yfir vöruflokka getur þú bætt við liðnum **Hafa samband** sem bendir á tengiliðasíðu sem þú hefur smíðað fyrir síðuna.</span><span class="sxs-lookup"><span data-stu-id="7a9de-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="7a9de-146">Fylgdu þessum skrefum til að bæta við sérsniðnum yfirlitsvalkostum fyrir yfirlitsvalmynd.</span><span class="sxs-lookup"><span data-stu-id="7a9de-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="7a9de-147">Í sniðmátinu eða brotinu sem þú vilt sérsníða velurðu eininguna yfir yfirlitsvalmyndina.</span><span class="sxs-lookup"><span data-stu-id="7a9de-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="7a9de-148">Í einingaglugganum, á flipanum **Gögn**, velurðu **Bæta hlut við** til að búa til nýjan yfirlitslið efnisstjórnunarkerfi (CMS).</span><span class="sxs-lookup"><span data-stu-id="7a9de-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="7a9de-149">Sláðu inn tenglatexta og slóð.</span><span class="sxs-lookup"><span data-stu-id="7a9de-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="7a9de-150">Endurtaktu skref 2 og 3 til að bæta við fleiri sérsniðnum leiðsöguvalkostum.</span><span class="sxs-lookup"><span data-stu-id="7a9de-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="7a9de-151">Þegar þessu er lokið skaltu velja **Vista** til að vista sniðmátið eða hlutann og velja **Ljúka við breytingar** til að skrá það inn.</span><span class="sxs-lookup"><span data-stu-id="7a9de-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a9de-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7a9de-152">Additional resources</span></span>

[<span data-ttu-id="7a9de-153">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="7a9de-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="7a9de-154">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="7a9de-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="7a9de-155">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="7a9de-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="7a9de-156">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="7a9de-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="7a9de-157">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="7a9de-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="7a9de-158">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="7a9de-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="7a9de-159">Unnið með birta hópa</span><span class="sxs-lookup"><span data-stu-id="7a9de-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
