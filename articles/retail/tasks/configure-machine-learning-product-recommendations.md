---
title: " Skilgreina ráðleggingar um afurðir sem byggir á vélnámi"
description: Þetta ferli endurnýjar gögnin í einingaverslun sem er notuð af machine-learning kerfinu sem knýr ráðleggingar um vörur, og virkjar svo ráðleggingar vöru á biðlurum Sölustaðar.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548440"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="f828d-103"> Skilgreina ráðleggingar um afurðir sem byggir á vélnámi</span><span class="sxs-lookup"><span data-stu-id="f828d-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f828d-104">Þetta ferli endurnýjar gögnin í einingaverslun sem er notuð af machine-learning kerfinu sem knýr ráðleggingar um vörur, og virkjar svo ráðleggingar vöru á biðlurum Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="f828d-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="f828d-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="f828d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f828d-106">Fara í Kerfisstjórnun > Uppsetning > Eining verslun.</span><span class="sxs-lookup"><span data-stu-id="f828d-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="f828d-107">Í listanum skal finna og velja skrána 'RetailSales'.</span><span class="sxs-lookup"><span data-stu-id="f828d-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="f828d-108">Smellið á Endurnýja.</span><span class="sxs-lookup"><span data-stu-id="f828d-108">Click Refresh.</span></span>
4. <span data-ttu-id="f828d-109">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f828d-109">Click OK.</span></span>
5. <span data-ttu-id="f828d-110">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f828d-110">Close the page.</span></span>
6. <span data-ttu-id="f828d-111">Farið í Smásala og viðskipti > Uppsetning höfuðstöðva > Færibreytur > Smásölufæribreytur.</span><span class="sxs-lookup"><span data-stu-id="f828d-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="f828d-112">Smellið á flipann Machine-learning.</span><span class="sxs-lookup"><span data-stu-id="f828d-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="f828d-113">Velja skal Já í svæðinu virkja ráðleggingar vöru.</span><span class="sxs-lookup"><span data-stu-id="f828d-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="f828d-114">Ef tekið er við skilaboðin "ekki tókst að sækja ráðleggingarlíkön", er þar vegna þess að þú uppfærðir einingaverslun mjög nýlega og kerfið hefur hugsanlega ekki lokið því að samhæfa nýju gögnin.</span><span class="sxs-lookup"><span data-stu-id="f828d-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="f828d-115">Bíða 2-3 tímar og reyna aftur.</span><span class="sxs-lookup"><span data-stu-id="f828d-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="f828d-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f828d-116">Click Save.</span></span>
10. <span data-ttu-id="f828d-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f828d-117">Close the page.</span></span>

