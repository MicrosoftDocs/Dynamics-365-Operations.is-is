---
title: Leiðrétta niðurstöður afurðartillagna sem byggjast á AI-ML
description: Þetta efni útskýrir hvernig á að sníða niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9e370faed7feb0640959a9fcc4b608f18f9ffc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263947"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="25ae5-103">Leiðrétta niðurstöður afurðartillagna sem byggjast á AI-ML</span><span class="sxs-lookup"><span data-stu-id="25ae5-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="25ae5-104">Þetta efni útskýrir hvernig á að leiðrétta niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu.</span><span class="sxs-lookup"><span data-stu-id="25ae5-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="25ae5-105">Eftir að hafa gert afurðatillögur virkar munu sjálfgefnar stillingar taka gildi; þessar færibreytur munu vinna fyrir geta unnið fyrir margar þarfir.</span><span class="sxs-lookup"><span data-stu-id="25ae5-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="25ae5-106">Best er að skipuleggja að eyða tíma í að meta hvort árangurinn passi við söluhreyfingu afurða.</span><span class="sxs-lookup"><span data-stu-id="25ae5-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="25ae5-107">Við mælum með að meta niðurstöður í nokkra daga áður en færibreytum er breytt eftir þörfum áður en prófað er aftur.</span><span class="sxs-lookup"><span data-stu-id="25ae5-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="25ae5-108">Að skilja færibreytur tillögulista</span><span class="sxs-lookup"><span data-stu-id="25ae5-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="25ae5-109">Áður en færibreytuum er breytt skaltu læra hvernig þær hafa áhrif á niðurstöðurnar hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="25ae5-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="25ae5-110">Afurðalistinn „Vinsælt”</span><span class="sxs-lookup"><span data-stu-id="25ae5-110">"Trending" product list</span></span>

<span data-ttu-id="25ae5-111">Afurðalistinn „Vinsælt” er með tvær færibreytur sem hægt er að breyta:</span><span class="sxs-lookup"><span data-stu-id="25ae5-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Dæmi um sjálfgefna færibreytu fyrir „Vinsælt”](./media/exampletrendingparameters.png)

1. <span data-ttu-id="25ae5-113">**Láta fylgja með nýjar afurðir frá síðustu X dögum** - Vörur sem hefur verið bætt við innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að velja afurðatillögur.</span><span class="sxs-lookup"><span data-stu-id="25ae5-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="25ae5-114">Sjálfgefið gildi á myndinni bendir til þess að hægt sé að nota afurðir sem eru orðnar 180 daga gamlar í vinsælum afurðalistanum.</span><span class="sxs-lookup"><span data-stu-id="25ae5-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="25ae5-115">**Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="25ae5-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="25ae5-116">Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir vinsælar afurðir.</span><span class="sxs-lookup"><span data-stu-id="25ae5-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="25ae5-117">Listi yfir „mest seldar” afurðir</span><span class="sxs-lookup"><span data-stu-id="25ae5-117">"Best selling" product list</span></span>

<span data-ttu-id="25ae5-118">Það fer eftir viðskiptum þínum, en „Mest selt” getur skilað öðrum árangri en stefna, jafnvel þó að þeir noti bæði viðskiptatilvik til að panta vörur.</span><span class="sxs-lookup"><span data-stu-id="25ae5-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="25ae5-119">Þar sem Mest selt er ekki með nein lok miðað við dagsetningu úrvals getur Mest selt samt bent á mjög vinsælar, eldri vörur sem gætu hafa verið felldar af listanum Vinsælt.</span><span class="sxs-lookup"><span data-stu-id="25ae5-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="25ae5-120">Afurðalistinn „Mest selt” er með eina færibreytu sem hægt er að breyta:</span><span class="sxs-lookup"><span data-stu-id="25ae5-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Dæmi um sjálfgefna færibreytu fyrir mest selt](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="25ae5-122">**Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="25ae5-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="25ae5-123">Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir mest seldar afurðir.</span><span class="sxs-lookup"><span data-stu-id="25ae5-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="25ae5-124">Bættu við eða fjarlægðu vörur handvirkt af tillagnalistum</span><span class="sxs-lookup"><span data-stu-id="25ae5-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="25ae5-125">Fyrir listana „Nýtt”, „Vinsælt” eða „Mest selt”</span><span class="sxs-lookup"><span data-stu-id="25ae5-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="25ae5-126">Farðu í **Retail og Commerce** > **Afurðatillögur** > **Færibreytur tillögulista**.</span><span class="sxs-lookup"><span data-stu-id="25ae5-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="25ae5-127">Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.</span><span class="sxs-lookup"><span data-stu-id="25ae5-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="25ae5-128">Veldu listann sem á að bæta við eða fjarlægja afurðir af.</span><span class="sxs-lookup"><span data-stu-id="25ae5-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="25ae5-129">Til að bæta afurðum við töfluna skaltu velja **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="25ae5-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="25ae5-130">Undir vöru dálki, leitaðu að vöru eftir **Nafn** eða **Vörunúmer.**</span><span class="sxs-lookup"><span data-stu-id="25ae5-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Dæmi um leit að vöru á Nýja vörulistanum](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="25ae5-132">Veldu einn af tveimur valkostum undir dálknum Línugerð:</span><span class="sxs-lookup"><span data-stu-id="25ae5-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="25ae5-133">**Hafa með** - þvingar afurð fremst á listanum</span><span class="sxs-lookup"><span data-stu-id="25ae5-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="25ae5-134">**Útiloka** - fjarlægir afurð frá því að birtast á listanum</span><span class="sxs-lookup"><span data-stu-id="25ae5-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Dæmi um að taka með eða útiloka vöru frá Nýja vörulistanum](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="25ae5-136">Ef **Sýna röð** er breytt breytir það röðinni sem afurðir merktar **hafa með** birtast í á listanum.</span><span class="sxs-lookup"><span data-stu-id="25ae5-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="25ae5-137">Ef tvær vörur hafa sama gildi **birta röð**, þá getur endanleg röð þessara tveggja niðurstaðna verið frábrugðin bakforritinu.</span><span class="sxs-lookup"><span data-stu-id="25ae5-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="25ae5-138">Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="25ae5-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="25ae5-139">Fyrir listana „Fólki líkar einnig” eða „Oft keypt saman”</span><span class="sxs-lookup"><span data-stu-id="25ae5-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="25ae5-140">Í samhengi listanna „Oft keypt saman” eða „Fólki líkar einnig” er vélanám notað til að greina kaupmynstur neytenda til að mæla með skyldum vörum sem oftast eru keyptar saman fyrir einstaka grunnvöru.</span><span class="sxs-lookup"><span data-stu-id="25ae5-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="25ae5-141">*Grunnafurð* er afurðin sem þú vilt búa til niðurstöður fyrir.</span><span class="sxs-lookup"><span data-stu-id="25ae5-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="25ae5-142">Í tengslum við að breyta tillagnalistum handvirkt ertu að bæta við eða fjarlægja niðurstöður fyrir þessa afurð.</span><span class="sxs-lookup"><span data-stu-id="25ae5-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="25ae5-143">Fylgdu þessum skrefum til að bæta við eða fjarlægja niðurstöður fyrir grunnafurð handvirkt:</span><span class="sxs-lookup"><span data-stu-id="25ae5-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="25ae5-144">Velja **Grunnafurð**.</span><span class="sxs-lookup"><span data-stu-id="25ae5-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="25ae5-145">Undir dálkinum **Afurð** leitarðu að afurð eftir **Heiti** eða **Vörunúmeri.**
![Dæmi um leit að afurð á listanum Oft keypt saman](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="25ae5-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="25ae5-146">Veldu einn af tveimur valkostum undir dálknum **Línugerð**:</span><span class="sxs-lookup"><span data-stu-id="25ae5-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="25ae5-147">**Hafa með** - þvingar afurð fremst á listanum</span><span class="sxs-lookup"><span data-stu-id="25ae5-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="25ae5-148">**Útiloka** - fjarlægir afurð frá því að birtast á listanum</span><span class="sxs-lookup"><span data-stu-id="25ae5-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="25ae5-149">![Dæmi um að hafa með eða útiloka afurð á listanum Oft keypt saman](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="25ae5-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="25ae5-150">Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu Fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="25ae5-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="25ae5-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="25ae5-151">Additional resources</span></span>

[<span data-ttu-id="25ae5-152">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="25ae5-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="25ae5-153">Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="25ae5-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="25ae5-154">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="25ae5-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="25ae5-155">Kveikja á sérsniðnum tillögum</span><span class="sxs-lookup"><span data-stu-id="25ae5-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="25ae5-156">Afþakka sérsniðnar tillögur</span><span class="sxs-lookup"><span data-stu-id="25ae5-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="25ae5-157">Virkja tillögur um að kaupa svipaða vöru</span><span class="sxs-lookup"><span data-stu-id="25ae5-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="25ae5-158">Bæta við afurðatillögum á sölustað</span><span class="sxs-lookup"><span data-stu-id="25ae5-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="25ae5-159">Bæta tillögum við færsluskjáinn</span><span class="sxs-lookup"><span data-stu-id="25ae5-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="25ae5-160">Búðu til handvirkt myndaðar ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="25ae5-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="25ae5-161">Búðu til tillögur með kynningargögnum</span><span class="sxs-lookup"><span data-stu-id="25ae5-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="25ae5-162">Algengar spurningar um afurðaráðleggingar</span><span class="sxs-lookup"><span data-stu-id="25ae5-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]