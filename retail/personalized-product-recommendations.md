---
title: "Yfirlit yfir sérsniðnar afurðarráðleggingar"
description: "Í Dynamics 365 for Retail er hægt að birta ráðleggingar um vörur í sölustaðartæki. Ráðleggingar eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum. Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum að finna vörur. Með því að sýna afurðir miðað við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og krosssölu og hægt er að auka varðveisla viðskiptavinar. Í Dynamics 365 for Retail eru ráðleggingar um vörur knúnar með Cognitive Services og vélanámi Microsoft Azure."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a3a3b5e87a797c29c13b180c248d1782805c4c31
ms.contentlocale: is-is
ms.lasthandoff: 06/29/2017


---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="f46a8-107">Yfirlit yfir sérsniðnar afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="f46a8-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f46a8-108">Í Dynamics 365 for Retail er hægt að birta ráðleggingar um vörur í sölustaðartæki.</span><span class="sxs-lookup"><span data-stu-id="f46a8-108">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="f46a8-109">Ráðleggingar eru vörur sem viðskiptavinurinn kann að hafa áhuga á grundvelli sögu innkaupapantanir, vara á óskalista þeirra og vörur sem aðrir viðskiptavinir keyptu á netinu og í verslunum.</span><span class="sxs-lookup"><span data-stu-id="f46a8-109">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="f46a8-110">Fyrir smásala með stóra vörulista hjálpa sérsniðnar ráðleggingar viðskiptavinum að finna vörur.</span><span class="sxs-lookup"><span data-stu-id="f46a8-110">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="f46a8-111">Með því að sýna afurðir miðað við áhugamál viðskiptavinarins og innkaupavenjur geta vöruráðleggingar aðstoðað smásala við viðbótarsölu og krosssölu og hægt er að auka varðveisla viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f46a8-111">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="f46a8-112">Í Dynamics 365 for Retail eru ráðleggingar um vörur knúnar með Cognitive Services og vélanámi Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f46a8-112">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

<a name="scenarios"></a><span data-ttu-id="f46a8-113">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="f46a8-113">Scenarios</span></span>
---------

<span data-ttu-id="f46a8-114">Vöruráðleggingar eru virkjaðar fyrir eftirfarandi aðstæður sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="f46a8-114">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="f46a8-115">Þær eru tiltækar í sölukerfi í skýinu eða Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f46a8-115">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="f46a8-116">Á síðunni **Upplýsingar um afurð**:</span><span class="sxs-lookup"><span data-stu-id="f46a8-116">On the **Product details** page:</span></span>

-   <span data-ttu-id="f46a8-117">Ef aðili tengdur verslun opnar í **Upplýsingar um afurð** síðuna þegar hann skoðar fyrri færslur þvert á mismunandi rásir stingur vélin upp á fleiri vörum sem eru líklegar til að vera keyptar saman.</span><span class="sxs-lookup"><span data-stu-id="f46a8-117">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="f46a8-118">Ef aðili tengdur versluninni bætir viðskiptavini við færsluna og hann heimsækir síðuna **Upplýsingar um afurð** stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f46a8-118">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="f46a8-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="f46a8-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="f46a8-120">Á síðunni **Færsla**:</span><span class="sxs-lookup"><span data-stu-id="f46a8-120">On the **Transaction** page:</span></span>

-   <span data-ttu-id="f46a8-121">Ráðlögð vél stingur upp á vörum byggt á öllum vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="f46a8-121">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="f46a8-122">Ef aðili tengdur versluninni bætir viðskiptavini við færsluna stingur vélin upp á persónubundnum efni byggt á viðskiptaferli viðskiptavinarins og vörum í körfunni.</span><span class="sxs-lookup"><span data-stu-id="f46a8-122">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

<span data-ttu-id="f46a8-123">**Athugið**  Til að birta ráðleggingar á síðunni **Færsla** þarf smásöluaðilinn að uppfæra skjáútlitið í Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f46a8-123">**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="f46a8-124">Sleppa verður stýringunni **Ráðleggingar** á síðunni **Færsla**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-124">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="f46a8-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="f46a8-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="f46a8-126">Á síðunni **Upplýsingar um viðskiptamann**:</span><span class="sxs-lookup"><span data-stu-id="f46a8-126">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="f46a8-127">Ráðlögð vél stingur stingur upp á vörum byggt á notandakenninu og vörum á óskalista viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f46a8-127">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="f46a8-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="f46a8-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="f46a8-129">Skilgreina Dynamics 365 for Retail þannig að kveikt sé á ráðleggingum á sölustað</span><span class="sxs-lookup"><span data-stu-id="f46a8-129">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="f46a8-130">Til að setja upp ráðleggingar vöru þarf að gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="f46a8-130">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="f46a8-131">Gangið úr skugga um að réttur **Lögaðili** sé valinn.</span><span class="sxs-lookup"><span data-stu-id="f46a8-131">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="f46a8-132">Farið í **Einingaverslun** veljið **Smásala** og smellið á **Uppfæra**.** **Þá eru sýnigögn (eða þín eigin gögn) notuð úr virknifyrirtækisins og þau færð í einingaverslun.</span><span class="sxs-lookup"><span data-stu-id="f46a8-132">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="f46a8-133">Valfrjálst: Til Að birta ráðleggingar á færsluskjánum, er farið ** Útlit Skjás **útlit skjás valið, **Útlitshönnuður afgreiðsluskjás**,** opnaður, ** og svo sleppt ** stýringu leiðbeiningar ** þar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="f46a8-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.</span></span>
4.  <span data-ttu-id="f46a8-134">Farið í **Smásölufæribreytir**, veljið **Vélnám** svo **Já **undir **virkja ráðleggingar sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="f46a8-135">Til að sjá ráðleggingar á sölustað skal keyra altæku vinnsluna **1110**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="f46a8-136">Til að endurspegla breytingar á útlitshönnuði sölustaðar skal keyra skilgreiningarvinnslu rásar **1070**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="f46a8-137">[]()Hvernig virkar það?</span><span class="sxs-lookup"><span data-stu-id="f46a8-137">[]()How does it work?</span></span>
<span data-ttu-id="f46a8-138">Þegar **Einingarverslun** einingin er uppfær eiga eftirfarandi aðgerðir sér stað.</span><span class="sxs-lookup"><span data-stu-id="f46a8-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="f46a8-139">Gögn á sniði sem krafist er af Cognitive Services eru fengin úr Dynamics 365 for Retail virknigagnagrunninum og send í einingaverslunina.</span><span class="sxs-lookup"><span data-stu-id="f46a8-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="f46a8-140">Gögnin eru notuð af Azure Data Factory (ADF) til að hreinsa gögnin með Hive-forskriftum sem hluta af ADF verkþáttum.</span><span class="sxs-lookup"><span data-stu-id="f46a8-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="f46a8-141">Hreinsuð gögn eru geymd í blob-geymslu.</span><span class="sxs-lookup"><span data-stu-id="f46a8-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="f46a8-142">Gögn úr blob-geymslu eru notuð af API vitsmunaþjónustu til að þjálfa ráðlögð líkan.</span><span class="sxs-lookup"><span data-stu-id="f46a8-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="f46a8-143">Þegar kveikt er á **Virkja ráðleggingar** og skilgreiningarvinnslur eru keyrðar eiga eftirfarandi aðgerðir sér stað.</span><span class="sxs-lookup"><span data-stu-id="f46a8-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="f46a8-144">Líkanaskilríki og kenni eru sótt úr API og geymd í Dynamics 365 for Retail virknigagnagrunninum í web.config -skránni fyrir AOS og einnig á smásöluþjóni.</span><span class="sxs-lookup"><span data-stu-id="f46a8-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="f46a8-145">Líkanaskilríki og kenni eru gerð tiltæk á CRT þannig að hægt sé að vinna ráðleggingarbeiðnir vara úr sölukerfi í skýinu og MPOS í nettengdri stillingu.</span><span class="sxs-lookup"><span data-stu-id="f46a8-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="f46a8-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f46a8-146">See also</span></span>
--------

[<span data-ttu-id="f46a8-147">Bæta stýringu ráðleggingar á færslusíðu á sölustaðartæki</span><span class="sxs-lookup"><span data-stu-id="f46a8-147">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




