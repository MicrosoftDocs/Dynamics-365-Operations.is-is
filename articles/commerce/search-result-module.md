---
title: Leitarniðurstöðueining
description: Þetta efnisatriði fjallar um leitarniðurstöðueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 645022000d8746db3793a8a8611ab8f17c7bcc6e
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117134"
---
# <a name="search-results-module"></a><span data-ttu-id="17cdb-103">Leitarniðurstöðueining</span><span class="sxs-lookup"><span data-stu-id="17cdb-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="17cdb-104">Þetta efnisatriði fjallar um leitarniðurstöðueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17cdb-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="17cdb-105">Leitarniðurstöðueiningin skilar leitarniðurstöðum afurðar og lista yfir viðeigandi afmarkanir fyrir afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="17cdb-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="17cdb-106">Hægt er að nota leitarniðurstöðueiningar á svæðinu Dynamics 365 Commerce til að birta síður fyrir eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="17cdb-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="17cdb-107">Leitarniðurstöður sem koma til vegna leitar notanda</span><span class="sxs-lookup"><span data-stu-id="17cdb-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="17cdb-108">Leitarniðurstöður sem sýna tiltekið safn afurða á borð við „Versla svipaðar vörur“</span><span class="sxs-lookup"><span data-stu-id="17cdb-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="17cdb-109">Afurðalistar sem tilheyra flokki</span><span class="sxs-lookup"><span data-stu-id="17cdb-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="17cdb-110">Frekari upplýsingar um síður flokka og leitarniðurstaðna er að finna í [Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="17cdb-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="17cdb-111">Eftirfarandi mynd sýnir dæmi um leitarniðurstöðusíðu fyrir flokk á Fabrikam-svæðinu.</span><span class="sxs-lookup"><span data-stu-id="17cdb-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Dæmi um leitarniðurstöðusíðu á Fabrikam-svæðinu](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="17cdb-113">Eiginleikar leitarniðurstöðueiningar</span><span class="sxs-lookup"><span data-stu-id="17cdb-113">Search results module properties</span></span>

<span data-ttu-id="17cdb-114">Í eftirfarandi töflu er listi yfir eiginleika leitarniðurstöðueininga, ásamt gildum þeirra og lýsingum.</span><span class="sxs-lookup"><span data-stu-id="17cdb-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="17cdb-115">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="17cdb-115">Property</span></span> | <span data-ttu-id="17cdb-116">Gildi</span><span class="sxs-lookup"><span data-stu-id="17cdb-116">Values</span></span> | <span data-ttu-id="17cdb-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="17cdb-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="17cdb-118">Vörur á síðu</span><span class="sxs-lookup"><span data-stu-id="17cdb-118">Items per page</span></span> | <span data-ttu-id="17cdb-119">Heiltala</span><span class="sxs-lookup"><span data-stu-id="17cdb-119">Integer</span></span> | <span data-ttu-id="17cdb-120">Fjöldi vara sem á að sýna á hverri síðu.</span><span class="sxs-lookup"><span data-stu-id="17cdb-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="17cdb-121">Leyfa aftur á PDP</span><span class="sxs-lookup"><span data-stu-id="17cdb-121">Allow back on PDP</span></span> | <span data-ttu-id="17cdb-122">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="17cdb-122">**True** or **False**</span></span> | <span data-ttu-id="17cdb-123">Ef þessi eiginleiki er stilltur á **Satt**, þegar notandi velur afurð á leitarniðurstöðusíðunni, mun brauðmylsnuleiðsögnin á upplýsingasíðu afurðar sem er opnuð sýna tengil fyrir „Aftur í niðurstöður“.</span><span class="sxs-lookup"><span data-stu-id="17cdb-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="17cdb-124">Fjölga afmörkunum</span><span class="sxs-lookup"><span data-stu-id="17cdb-124">Expand Refiners</span></span> | <span data-ttu-id="17cdb-125">**Allt**, **1**, **2**, **3** eða **4**</span><span class="sxs-lookup"><span data-stu-id="17cdb-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="17cdb-126">Fjöldi afmarkana efst sem á að víkka út þegar síða er hlaðin.</span><span class="sxs-lookup"><span data-stu-id="17cdb-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="17cdb-127">Ef þessi eiginleiki er til dæmis stilltur á **3** verða fyrstu þrjár afmarkanir á síðunni víkkaðar út.</span><span class="sxs-lookup"><span data-stu-id="17cdb-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="17cdb-128">Fela tegundastigveldi</span><span class="sxs-lookup"><span data-stu-id="17cdb-128">Hide category hierarchy display</span></span> | <span data-ttu-id="17cdb-129">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="17cdb-129">**True** or **False**</span></span> | <span data-ttu-id="17cdb-130">Ef þessi eiginleiki er stilltur á **Satt** verður tegundastigveldið sem sýnt er á síðunni falið.</span><span class="sxs-lookup"><span data-stu-id="17cdb-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="17cdb-131">Þennan eiginleika ætti að stilla á **Satt** ef notuð er [brauðmylsnueiningin](add-breadcrumb.md) til að sýna tegundastigveldið.</span><span class="sxs-lookup"><span data-stu-id="17cdb-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="17cdb-132">Hafa afurðareigindir með í leitarniðurstöðum</span><span class="sxs-lookup"><span data-stu-id="17cdb-132">Include product attributes in search results</span></span> | <span data-ttu-id="17cdb-133">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="17cdb-133">**True** or **False**</span></span> | <span data-ttu-id="17cdb-134">Ef þessi eiginleiki er stilltur á **Satt** verður eigindum skilað fyrir afurðirnar í leitarniðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="17cdb-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="17cdb-135">Þrátt fyrir að hægt sé að sýna þessar eigindir á Commerce-svæði er þörf á viðbót.</span><span class="sxs-lookup"><span data-stu-id="17cdb-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="17cdb-136">Sýna tengsl verðs</span><span class="sxs-lookup"><span data-stu-id="17cdb-136">Show affiliation prices</span></span> | <span data-ttu-id="17cdb-137">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="17cdb-137">**True** or **False**</span></span> | <span data-ttu-id="17cdb-138">Ef þessi eiginleiki er stilltur á **Satt** verða tengd verð afurðanna sýnd í leitarniðurstöðum þegar innskráður notandi skoðar síðuna.</span><span class="sxs-lookup"><span data-stu-id="17cdb-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |
| <span data-ttu-id="17cdb-139">Uppfæra afmörkunarsvæði</span><span class="sxs-lookup"><span data-stu-id="17cdb-139">Update refiner panel</span></span> | <span data-ttu-id="17cdb-140">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="17cdb-140">**True** or **False**</span></span> | <span data-ttu-id="17cdb-141">Ef þessi eiginleiki er stilltur á **Satt** verður afmörkunarsvæðið uppfært þegar afmarkanir eru valdar.</span><span class="sxs-lookup"><span data-stu-id="17cdb-141">If this property is set to **True**, the refiner panel will be updated when refiners are selected.</span></span> <span data-ttu-id="17cdb-142">Í þessari stillingu virka sumar fjölvalsafmarkanir eins og einvalsafmarkanir þegar afmörkunarsvæðið er uppfært.</span><span class="sxs-lookup"><span data-stu-id="17cdb-142">In this mode, some multiple-selection refiners will behave like single-selection refiners when the refiner panel is updated.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="17cdb-143">Í Commerce útgáfu 10.0.16 eða nýrri er hægt að nota skilgreininguna **Sýna tengsl verðs** til að sýna verðtengsl á síðunni.</span><span class="sxs-lookup"><span data-stu-id="17cdb-143">In the Commerce version 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>
>
> <span data-ttu-id="17cdb-144">Í Commerce útgáfu 10.0.20 og nýrri er hægt að nota skilgreininguna **Uppfæra afmörkunarsvæði** til að uppfæra afmörkunarsvæðið við val á afmörkun.</span><span class="sxs-lookup"><span data-stu-id="17cdb-144">In the Commerce version 10.0.20 release and later, the **Update refiner panel** configuration can be used to update the refiner panel during refiner selection.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="17cdb-145">Studdar einingar</span><span class="sxs-lookup"><span data-stu-id="17cdb-145">Supported modules</span></span>

<span data-ttu-id="17cdb-146">Leitarniðurstöðueiningin styður [flýtiskoðunareininguna](quick-view-module.md), sem gerir notendum kleift að skoða afurðarupplýsingar og bæta vörum við körfuna úr síðu leitarniðurstaðna.</span><span class="sxs-lookup"><span data-stu-id="17cdb-146">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="17cdb-147">Bæta leitarniðurstöðueiningu við flokkasíðu</span><span class="sxs-lookup"><span data-stu-id="17cdb-147">Add a search results module to a category page</span></span>

<span data-ttu-id="17cdb-148">Til að bæta leitarniðurstöðueiningu við flokkasíðu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="17cdb-148">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="17cdb-149">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="17cdb-149">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="17cdb-150">Í svarglugganum **Nýtt sniðmát** skal slá inn heitið **Leitarniðurstöður** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-150">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="17cdb-151">Í hólfinu **Meginmál** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-151">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="17cdb-152">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-152">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="17cdb-153">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-153">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="17cdb-154">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-154">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="17cdb-155">Í hólfinu **Hólf** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-155">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="17cdb-156">Í svarglugganum **Bæta við einingu** skal velja eininguna **Brauðmylsna** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-156">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="17cdb-157">Á eiginleikasvæðinu **Brauðmylsna** skal færa inn gildið **1** fyrir **Lágmark atvika**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-157">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="17cdb-158">Í hólfinu **Hólf** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-158">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="17cdb-159">Í glugganum **Bæta við einingu** skal velja eininguna **Leitarniðurstöður** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-159">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="17cdb-160">Á eiginleikasvæðinu **Leitarniðurstöður** skal slá inn gildið **1** fyrir **Lágmark atvika** og síðan stilla alla aðra nauðsynlega eiginleika fyrir leitarniðurstöðueininguna.</span><span class="sxs-lookup"><span data-stu-id="17cdb-160">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="17cdb-161">Með því að stilla þessa eiginleika í sniðmátinu er gengið úr skugga um að allar sérstillingar á tiltekinni flokkasíðu muni sjálfkrafa hafa með þessar stillingar.</span><span class="sxs-lookup"><span data-stu-id="17cdb-161">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="17cdb-162">Veldu **Ljúka við breytingar** og síðan **Birta** til að birta sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="17cdb-162">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="17cdb-163">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="17cdb-163">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="17cdb-164">Í glugganum **Velja sniðmát** skal velja sniðmátið **Leitarniðurstöður** sem var búið til, slá inn **Flokkasíða** fyrir **Síðuheit** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="17cdb-164">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="17cdb-165">Þar sem öll gildin eru stillt í sniðmátinu er síðan tilbúin til birtingar.</span><span class="sxs-lookup"><span data-stu-id="17cdb-165">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="17cdb-166">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="17cdb-166">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17cdb-167">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="17cdb-167">Additional resources</span></span>

[<span data-ttu-id="17cdb-168">Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="17cdb-168">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="17cdb-169">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="17cdb-169">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="17cdb-170">Flýtiskoðunareining</span><span class="sxs-lookup"><span data-stu-id="17cdb-170">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
