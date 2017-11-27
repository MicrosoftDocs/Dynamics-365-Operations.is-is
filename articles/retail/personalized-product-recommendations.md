---
title: "Yfirlit yfir sérsniðnar afurðarráðleggingar"
description: "Þetta efnisatriði inniheldur upplýsingar ráðleggingar fyrir Dynamics 365 for Retail vörur sem hægt er að birta í sölustaðartæki."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 942d6225a46b108ea39d3b8e4376b644c128ae6d
ms.contentlocale: is-is
ms.lasthandoff: 11/14/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="4a178-103">Yfirlit yfir sérsniðnar afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="4a178-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="4a178-104">Þessi eiginleiki er aðeins til staðar í sandkassa og framleiðsluefnissviðum.</span><span class="sxs-lookup"><span data-stu-id="4a178-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="4a178-105">Í Dynamics 365 for Retail er hægt að birta ráðleggingar um vörur í sölustaðartæki.</span><span class="sxs-lookup"><span data-stu-id="4a178-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="4a178-106">Ráðleggingar eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum.</span><span class="sxs-lookup"><span data-stu-id="4a178-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="4a178-107">Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum að finna vörur.</span><span class="sxs-lookup"><span data-stu-id="4a178-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="4a178-108">Með því að sýna afurðir miðað við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og krosssölu og hægt er að auka varðveisla viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="4a178-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="4a178-109">Í Dynamics 365 for Retail eru ráðleggingar um vörur knúnar með Cognitive Services og vélanámi Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a178-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="4a178-110">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="4a178-110">Scenarios</span></span>
---------

<span data-ttu-id="4a178-111">Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="4a178-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="4a178-112">Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="4a178-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="4a178-113">Á síðunni **Upplýsingar um afurð**:</span><span class="sxs-lookup"><span data-stu-id="4a178-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="4a178-114">Ef aðili tengdur verslun opnar í **Upplýsingar um afurð** síðuna þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur vélin upp á fleiri vörum sem eru líklegar til að vera keyptar saman.</span><span class="sxs-lookup"><span data-stu-id="4a178-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="4a178-115">Ef aðili tengdur versluninni bætir viðskiptavini við færsluna og hann heimsækir síðuna **Upplýsingar um afurð** stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="4a178-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="4a178-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="4a178-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="4a178-117">Á síðunni **Færsla**:</span><span class="sxs-lookup"><span data-stu-id="4a178-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="4a178-118">Ráðlögð vél stingur upp á vörum byggt á öllum vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="4a178-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="4a178-119">Ef aðili tengdur versluninni bætir viðskiptavini við færsluna stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins og vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="4a178-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="4a178-120">Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="4a178-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="4a178-121">Sleppa verður stýringunni **Ráðleggingar** á síðunni **Færsla**.</span><span class="sxs-lookup"><span data-stu-id="4a178-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="4a178-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="4a178-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="4a178-123">Á síðunni **Upplýsingar um viðskiptamann**:</span><span class="sxs-lookup"><span data-stu-id="4a178-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="4a178-124">Ráðlögð vél stingur stingur upp á vörum byggt á notandakenninu og vörum á óskalista viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="4a178-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="4a178-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="4a178-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="4a178-126">Skilgreina Dynamics 365 for Retail þannig að kveikt sé á ráðleggingum á sölustað</span><span class="sxs-lookup"><span data-stu-id="4a178-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="4a178-127">Til að setja upp ráðleggingar vöru þarf að gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="4a178-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="4a178-128">Gangið úr skugga um að réttur **Lögaðili** sé valinn.</span><span class="sxs-lookup"><span data-stu-id="4a178-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="4a178-129">Farið í **Einingaverslun** veljið **Smásala** og smellið á **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="4a178-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="4a178-130">Þá eru sýnigögn (eða þín eigin gögn) notuð úr virknifyrirtækisins og þau færð í einingaverslun.</span><span class="sxs-lookup"><span data-stu-id="4a178-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="4a178-131">Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið í **Útlit Skjás**útlit skjás valið **Útlitshönnuður afgreiðsluskjás** opnaður, og svo sleppt stýringunni **leiðbeiningar** þar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="4a178-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="4a178-132">Farið í **Smásölufæribreytir**, veljið **Vélnám** svo **Já** undir **virkja ráðleggingar sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="4a178-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="4a178-133">Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**.</span><span class="sxs-lookup"><span data-stu-id="4a178-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="4a178-134">Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.</span><span class="sxs-lookup"><span data-stu-id="4a178-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="4a178-135">[]()Hvernig virkar það?</span><span class="sxs-lookup"><span data-stu-id="4a178-135">[]()How does it work?</span></span>
<span data-ttu-id="4a178-136">Þegar **Einingarverslun** einingin er uppfær eiga eftirfarandi aðgerðir sér stað.</span><span class="sxs-lookup"><span data-stu-id="4a178-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="4a178-137">Gögn á sniði sem krafist er af Cognitive Services eru fengin úr Dynamics 365 for Retail virknigagnagrunninum og send í einingaverslunina.</span><span class="sxs-lookup"><span data-stu-id="4a178-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="4a178-138">Gögnin eru notuð af Azure Data Factory (ADF) til að hreinsa gögnin með Hive-forskriftum sem hluta af ADF verkþáttum.</span><span class="sxs-lookup"><span data-stu-id="4a178-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="4a178-139">Hreinsuð gögn eru geymd í blob-geymslu.</span><span class="sxs-lookup"><span data-stu-id="4a178-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="4a178-140">Gögn úr blob-geymslu eru notuð af API vitsmunaþjónustu til að þjálfa ráðlögð líkan.</span><span class="sxs-lookup"><span data-stu-id="4a178-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="4a178-141">Þegar kveikt er á **Virkja ráðleggingar** og skilgreiningarvinnslur eru keyrðar eiga eftirfarandi aðgerðir sér stað.</span><span class="sxs-lookup"><span data-stu-id="4a178-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="4a178-142">Líkanaskilríki og kenni eru sótt úr API og geymd í Dynamics 365 for Retail virknigagnagrunninum í web.config -skránni fyrir AOS og einnig á smásöluþjóni.</span><span class="sxs-lookup"><span data-stu-id="4a178-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="4a178-143">Líkanaskilríki og kenni eru gerð tiltæk á CRT þannig að hægt sé að vinna ráðleggingarbeiðnir vara úr sölukerfi í skýinu og MPOS í nettengdri stillingu.</span><span class="sxs-lookup"><span data-stu-id="4a178-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="4a178-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4a178-144">See also</span></span>
--------

[<span data-ttu-id="4a178-145">Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki</span><span class="sxs-lookup"><span data-stu-id="4a178-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




