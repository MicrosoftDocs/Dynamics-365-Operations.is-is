---
title: Stjórna niðurstöðum afurðartillagna sem byggjast á AI-ML
description: Þetta efni útskýrir hvernig á að sníða niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770071"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="fd621-103">Stjórna niðurstöðum afurðartillagna sem byggjast á AI-ML</span><span class="sxs-lookup"><span data-stu-id="fd621-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fd621-104">Þetta efni útskýrir hvernig á að sníða niðurstöður afurðatillagna byggt á námi gervigreindarvéla (AI-ML) að fyrirtæki þínu.</span><span class="sxs-lookup"><span data-stu-id="fd621-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="fd621-105">Eftir að hafa gert afurðatillögur virkar munu sjálfgefnar stillingar taka gildi; þessar færibreytur munu vinna fyrir geta unnið fyrir margar þarfir.</span><span class="sxs-lookup"><span data-stu-id="fd621-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="fd621-106">Best er að skipuleggja að eyða tíma í að meta hvort árangurinn passi við söluhreyfingu afurða.</span><span class="sxs-lookup"><span data-stu-id="fd621-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="fd621-107">Við mælum með að meta niðurstöður í nokkra daga áður en færibreytum er breytt eftir þörfum áður en prófað er aftur.</span><span class="sxs-lookup"><span data-stu-id="fd621-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="fd621-108">Að skilja færibreytur tillögulista</span><span class="sxs-lookup"><span data-stu-id="fd621-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="fd621-109">Áður en færibreytuum er breytt skaltu læra hvernig þær hafa áhrif á niðurstöðurnar hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="fd621-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="fd621-110">Vinsæll afurðalisti</span><span class="sxs-lookup"><span data-stu-id="fd621-110">Trending product list</span></span>

<span data-ttu-id="fd621-111">Afurðalistinn **Vinsælt** hefur tvær færibreytur sem hægt er að breyta: ![Dæmi um lista yfir vinsælan lista yfir sjálfgefnar færibreytur](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="fd621-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="fd621-112">**Láta fylgja með nýjar afurðir frá síðustu X dögum** - Vörur sem hefur verið bætt við innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að velja afurðatillögur.</span><span class="sxs-lookup"><span data-stu-id="fd621-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="fd621-113">Sjálfgefið gildi á myndinni bendir til þess að hægt sé að nota afurðir sem eru orðnar 180 daga gamlar í vinsælum afurðalistanum.</span><span class="sxs-lookup"><span data-stu-id="fd621-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="fd621-114">**Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="fd621-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="fd621-115">Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir vinsælar afurðir.</span><span class="sxs-lookup"><span data-stu-id="fd621-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="fd621-116">Listi yfir mest seldar afurðir</span><span class="sxs-lookup"><span data-stu-id="fd621-116">Best selling product list</span></span>

<span data-ttu-id="fd621-117">Það fer eftir viðskiptum þínum, en Mest selt getur skilað öðrum árangri en stefna, jafnvel þó að þeir noti bæði viðskiptatilvik til að panta vörur.</span><span class="sxs-lookup"><span data-stu-id="fd621-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="fd621-118">Þar sem Mest selt er ekki með nein lok miðað við dagsetningu úrvals getur Mest selt samt bent á mjög vinsælar, eldri vörur sem gætu hafa verið felldar af listanum Vinsælt.</span><span class="sxs-lookup"><span data-stu-id="fd621-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="fd621-119">Afurðalistinn **Mest selt** er með eina færibreytu sem hægt er að breyta:</span><span class="sxs-lookup"><span data-stu-id="fd621-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Dæmi um sjálfgefna færibreytu fyrir mest selt](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="fd621-121">**Láta fylgja með nýjar sölu frá síðustu X dögum** - Sölufærslur sem hafa orðið innan tiltekins fjölda daga fyrir núverandi dagsetningu má nota til að panta afurðirnar.</span><span class="sxs-lookup"><span data-stu-id="fd621-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="fd621-122">Sjálfgefið gildi hér að ofan bendir til þess að öll innkaup, sem gerð hafa verið á vöru síðustu 30 daga, verði notuð til að ákvarða staðsetningu vörunnar í lista yfir mest seldar afurðir.</span><span class="sxs-lookup"><span data-stu-id="fd621-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="fd621-123">Bættu við eða fjarlægðu vörur handvirkt af tillagnalistum</span><span class="sxs-lookup"><span data-stu-id="fd621-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="fd621-124">Fyrir Nýtt, Vinsælt eða Mest selt</span><span class="sxs-lookup"><span data-stu-id="fd621-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="fd621-125">Farðu í **Retail** > **Afurðatillögur** > **Tillögufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="fd621-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="fd621-126">Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.</span><span class="sxs-lookup"><span data-stu-id="fd621-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="fd621-127">Veldu listann sem á að bæta við eða fjarlægja afurðir af.</span><span class="sxs-lookup"><span data-stu-id="fd621-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="fd621-128">Til að bæta afurðum við töfluna skaltu velja **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="fd621-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="fd621-129">Undir afurðadálkinum leitarðu að afurð eftir **Heiti** eða **Vörunúmeri.**
![Dæmi um leit að afurð á Nýja vörulistanum](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="fd621-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="fd621-130">Veldu einn af tveimur valkostum undir dálknum Línugerð:</span><span class="sxs-lookup"><span data-stu-id="fd621-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="fd621-131">**Hafa með** - þvingar afurð fremst á listanum</span><span class="sxs-lookup"><span data-stu-id="fd621-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="fd621-132">**Útiloka** - fjarlægir afurð frá því að birtast á listanum ![Dæmi um að hafa með eða útiloka vöru af lista yfir nýja vöru](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="fd621-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="fd621-133">Ef **Sýna röð** er breytt breytir það röðinni sem afurðir merktar **hafa með** birtast í á listanum.</span><span class="sxs-lookup"><span data-stu-id="fd621-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="fd621-134">Ef tvær vörur hafa sama gildi **birta röð**, þá getur endanleg röð þessara tveggja niðurstaðna verið frábrugðin bakforritinu.</span><span class="sxs-lookup"><span data-stu-id="fd621-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="fd621-135">Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="fd621-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="fd621-136">Fyrir listana Fólki líkar einnig eða Oft keypt saman</span><span class="sxs-lookup"><span data-stu-id="fd621-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="fd621-137">Í samhengi listanna **Oft keypt saman** eða **Fólki líkar einnig** er vélanám notað til að greina kaupmynstur neytenda til að mæla með skyldum vörum sem oftast eru keyptar saman fyrir einstaka grunnvöru.</span><span class="sxs-lookup"><span data-stu-id="fd621-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="fd621-138">**Grunnafurð** er afurðin sem þú vilt búa til niðurstöður fyrir.</span><span class="sxs-lookup"><span data-stu-id="fd621-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="fd621-139">Í tengslum við að breyta tillagnalistum handvirkt ertu að bæta við eða fjarlægja niðurstöður fyrir þessa afurð.</span><span class="sxs-lookup"><span data-stu-id="fd621-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="fd621-140">Fylgdu þessum skrefum til að bæta við eða fjarlægja niðurstöður fyrir grunnafurð handvirkt:</span><span class="sxs-lookup"><span data-stu-id="fd621-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="fd621-141">Velja **Grunnafurð**.</span><span class="sxs-lookup"><span data-stu-id="fd621-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="fd621-142">Undir dálkinum **Afurð** leitarðu að afurð eftir **Heiti** eða **Vörunúmeri.**
![Dæmi um leit að afurð á listanum Oft keypt saman](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="fd621-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="fd621-143">Veldu einn af tveimur valkostum undir dálknum **Línugerð**:</span><span class="sxs-lookup"><span data-stu-id="fd621-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="fd621-144">**Hafa með** - þvingar afurð fremst á listanum</span><span class="sxs-lookup"><span data-stu-id="fd621-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="fd621-145">**Útiloka** - fjarlægir afurð frá því að birtast á listanum</span><span class="sxs-lookup"><span data-stu-id="fd621-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="fd621-146">![Dæmi um að hafa með eða útiloka afurð á listanum Oft keypt saman](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="fd621-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="fd621-147">Til að fjarlægja vörur af töflunni: veldu línuna sem á að fjarlægja og veldu Fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="fd621-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fd621-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fd621-148">Additional resources</span></span>

[<span data-ttu-id="fd621-149">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="fd621-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fd621-150">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="fd621-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fd621-151">Bæta við listum með afurðartillögum við síður</span><span class="sxs-lookup"><span data-stu-id="fd621-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
