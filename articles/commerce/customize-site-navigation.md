---
title: Sérstilla yfirlit svæðis
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur þínar til að vafra á Microsoft Dynamics 365 Commerce síðunni.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413144"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="ac0a3-103">Sérstilla yfirlit svæðis</span><span class="sxs-lookup"><span data-stu-id="ac0a3-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac0a3-104">Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur þínar til að vafra á Microsoft Dynamics 365 Commerce síðunni.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="ac0a3-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ac0a3-105">Overview</span></span>

<span data-ttu-id="ac0a3-106">Vefverslanir á netinu láta viðskiptavini gjarnan uppgötva og skoða vörur með því að fletta í gegnum vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="ac0a3-107">Þessi geta er yfirleitt til staðar með flipum efst á síðunni eða með stýristiku vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="ac0a3-108">Í Dynamics 365 Commerce geturðu stofnað og stjórnað stigveldisskipulagi flokksleiðsagnar þinna og vörunum sem eru í ýmsum flokkum.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ac0a3-109">Stofna yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="ac0a3-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="ac0a3-110">Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ac0a3-111">Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="ac0a3-112">Veldu **Tegundastigveldi** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="ac0a3-113">Gefðu stigveldinu heiti.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac0a3-114">Efsti flokkurinn sem þú býrð til er hnútur rótarflokksins.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="ac0a3-115">Hann verður ekki sýndur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-115">It won't be shown on your site.</span></span> <span data-ttu-id="ac0a3-116">Til að búa til flokkunarstigveldi þar sem einn efsti stigs hnút er sýndur á síðunni skaltu stofna og nefna flokkinn sem undirgildi af rótarflokknum.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="ac0a3-117">Veldu **Nýr tegundahnútur** og gefðu flokknum heiti.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="ac0a3-118">Haltu áfram að stofna systkina- og undirflokka eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="ac0a3-119">Núna geturðu úthlutað vörum í hvern flokk sem þú bjóst til undir efsta stigs flokknum.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="ac0a3-120">Sérsniðið röðun flokka</span><span class="sxs-lookup"><span data-stu-id="ac0a3-120">Customize the order of categories</span></span>

<span data-ttu-id="ac0a3-121">Sjálfgefið er að flokkarnir sem þú skilgreinir munu birtast í stafrófsröð á síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="ac0a3-122">Hins vegar getur þú einnig sérsniðið birtingarröð flokka.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="ac0a3-123">Úthluta gerð tegundastigveldis</span><span class="sxs-lookup"><span data-stu-id="ac0a3-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="ac0a3-124">Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="ac0a3-125">Veldu **Tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="ac0a3-126">Í aðgerðarúðunni á flipanum **Tegundastigveldi** í flokknum **Uppsetning** skal velja **Tengja stigveldisgerð**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="ac0a3-127">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-127">Select **New**.</span></span>
1. <span data-ttu-id="ac0a3-128">Í reitnum **Gerð tegundastigveldis** velurðu **Yfirlitsstigveldi rásar**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="ac0a3-129">Í reitnum **Tegundastigveldi** velurðu yfirlitsstigveldi rásarinnar sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="ac0a3-130">Birta ný eða uppfærð yfirlitsstigveldi</span><span class="sxs-lookup"><span data-stu-id="ac0a3-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="ac0a3-131">Fylgdu þessum skrefum til að gera yfirlitsstigveldið aðgengilegt fyrir netverslunina.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="ac0a3-132">Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="ac0a3-133">Veldu netverslunina þína í trénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="ac0a3-134">Veldu **Birta uppfærslur rásar**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="ac0a3-135">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="ac0a3-136">Á listanum finnurðu og velur **Vinnslu 1040**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="ac0a3-137">Veljið **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-137">Select **Run now**.</span></span>
1. <span data-ttu-id="ac0a3-138">Endurtaktu skref 5 og 6 fyrir vinnslur 1070 og 1150.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="ac0a3-139">Sýna flokka á síðunni þinni</span><span class="sxs-lookup"><span data-stu-id="ac0a3-139">Show categories on your site</span></span>

<span data-ttu-id="ac0a3-140">Til að sýna flokkunarveldi í netverslun þinni verður þú að bæta við yfirlitseiningunni á viðeigandi stað í sniðmáti eða broti.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="ac0a3-141">Eining yfirlitsvalmyndar mun síðan sýna yfirlitsstigveldi, að því tilskildu að þú hafir birt yfirlitsstigveldi þitt á rásinni sem vefsvæðið er bundið við.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="ac0a3-142">Valmyndareiningin sem fylgir með í einingarsafninu gerir notendum aðeins kleift að skoða flokka sem eru ekki með undirflokka.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="ac0a3-143">Ef viðskiptavinir þínir ættu að geta farið í flokka sem eru með undirflokka verður þú að sérsníða valmyndareininguna.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="ac0a3-144">Bæta við sérsniðnum yfirlitsvalkostum</span><span class="sxs-lookup"><span data-stu-id="ac0a3-144">Add custom navigation options</span></span>

<span data-ttu-id="ac0a3-145">Á yfirlitsvalmyndinni geturðu bætt við yfirlitsvalkostum sem eru ekki hluti af tegundastigveldi afurðar.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="ac0a3-146">Til dæmis, í lok lista yfir vöruflokka getur þú bætt við liðnum **Hafa samband** sem bendir á tengiliðasíðu sem þú hefur smíðað fyrir síðuna.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="ac0a3-147">Fylgdu þessum skrefum til að bæta við sérsniðnum yfirlitsvalkostum fyrir yfirlitsvalmynd.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="ac0a3-148">Í sniðmátinu eða brotinu sem þú vilt sérsníða velurðu eininguna yfir yfirlitsvalmyndina.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="ac0a3-149">Í einingaglugganum, á flipanum **Gögn**, velurðu **Bæta hlut við** til að búa til nýjan yfirlitslið efnisstjórnunarkerfi (CMS).</span><span class="sxs-lookup"><span data-stu-id="ac0a3-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="ac0a3-150">Sláðu inn tenglatexta og slóð.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="ac0a3-151">Endurtaktu skref 2 og 3 til að bæta við fleiri sérsniðnum leiðsöguvalkostum.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="ac0a3-152">Þegar þessu er lokið skaltu velja **Vista** til að vista sniðmátið eða hlutann og velja **Ljúka við breytingar** til að skrá það inn.</span><span class="sxs-lookup"><span data-stu-id="ac0a3-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac0a3-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ac0a3-153">Additional resources</span></span>

[<span data-ttu-id="ac0a3-154">Yfirlit yfir sniðmát og útlit</span><span class="sxs-lookup"><span data-stu-id="ac0a3-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="ac0a3-155">Vinna með sniðmát</span><span class="sxs-lookup"><span data-stu-id="ac0a3-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ac0a3-156">Vinna með forstillt útlit</span><span class="sxs-lookup"><span data-stu-id="ac0a3-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="ac0a3-157">Vinna með brot</span><span class="sxs-lookup"><span data-stu-id="ac0a3-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="ac0a3-158">Vinna með einingar</span><span class="sxs-lookup"><span data-stu-id="ac0a3-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="ac0a3-159">Búa til síðuvefslóð</span><span class="sxs-lookup"><span data-stu-id="ac0a3-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="ac0a3-160">Unnið með birta hópa</span><span class="sxs-lookup"><span data-stu-id="ac0a3-160">Work with publish groups</span></span>](publish-groups.md)
