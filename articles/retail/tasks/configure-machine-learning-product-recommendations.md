--- 
title: " Skilgreina ráðleggingar um afurðir sem byggir á vélnámi"
description: "Þetta ferli endurnýjar gögnin í einingaverslun sem er notuð af machine-learning kerfinu sem knýr ráðleggingar um vörur, og virkjar svo ráðleggingar vöru á biðlurum Sölustaðar."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="1f6c9-103"> Skilgreina ráðleggingar um afurðir sem byggir á vélnámi</span><span class="sxs-lookup"><span data-stu-id="1f6c9-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1f6c9-104">Þetta ferli endurnýjar gögnin í einingaverslun sem er notuð af machine-learning kerfinu sem knýr ráðleggingar um vörur, og virkjar svo ráðleggingar vöru á biðlurum Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="1f6c9-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1f6c9-106">Fara í Kerfisstjórnun > Uppsetning > Eining verslun.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="1f6c9-107">Í listanum skal finna og velja skrána 'RetailSales'.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="1f6c9-108">Smellið á Endurnýja.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-108">Click Refresh.</span></span>
4. <span data-ttu-id="1f6c9-109">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-109">Click OK.</span></span>
5. <span data-ttu-id="1f6c9-110">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-110">Close the page.</span></span>
6. <span data-ttu-id="1f6c9-111">Farið í Smásala og viðskipti > Uppsetning höfuðstöðva > Færibreytur > Smásölufæribreytur.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="1f6c9-112">Smellið á flipann Machine-learning.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="1f6c9-113">Velja skal Já í svæðinu virkja ráðleggingar vöru.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="1f6c9-114">Ef tekið er við skilaboðin "ekki tókst að sækja ráðleggingarlíkön", er þar vegna þess að þú uppfærðir einingaverslun mjög nýlega og kerfið hefur hugsanlega ekki lokið því að samhæfa nýju gögnin.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="1f6c9-115">Bíða 2-3 tímar og reyna aftur.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="1f6c9-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-116">Click Save.</span></span>
10. <span data-ttu-id="1f6c9-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f6c9-117">Close the page.</span></span>


