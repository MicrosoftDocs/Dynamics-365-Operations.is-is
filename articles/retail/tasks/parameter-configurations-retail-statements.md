--- 
title: " Skilgreiningar færibreyta fyrir smásöluyfirlit"
description: "Þetta ferli sýnir skilgreiningar fyrir smásölufæribreytur sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 61540297a2ebbbc76657734140b8add009db67ca
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="9b97c-103"> Skilgreiningar færibreyta fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="9b97c-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9b97c-104">Þetta ferli sýnir skilgreiningar fyrir smásölufæribreytur sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="9b97c-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="9b97c-105">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="9b97c-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9b97c-106">Farið í Smásala og viðskipti > Uppsetning höfuðstöðva > Færibreytur > Smásölufæribreytur.</span><span class="sxs-lookup"><span data-stu-id="9b97c-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="9b97c-107">Smellt er á flipann Bókun</span><span class="sxs-lookup"><span data-stu-id="9b97c-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="9b97c-108">Veljið "Já" ef óskað er að bóka upphæðir tímabundins afsláttar sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="9b97c-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="9b97c-109">Veljið "Venjulegur" til að nota sjálfgefna fjárhagslykla eða veldu "Reglubundið" ef óskað er að skilgreina hvaða lykill sem nota á fyrir hverja tímabundins afsláttar.</span><span class="sxs-lookup"><span data-stu-id="9b97c-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="9b97c-110">Veljið "Samantekt" ef ætti að leggja saman línur birgða þegar unnt er.</span><span class="sxs-lookup"><span data-stu-id="9b97c-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="9b97c-111">Veljið "Já" ef Reikninga og Greiðslur skuli sjálfkrafa jafnaður sem hluti af Uppgjör bókunarferli.</span><span class="sxs-lookup"><span data-stu-id="9b97c-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="9b97c-112">Veljið "Já" ef færsla peningaflutnings í öryggisskáp ætti að lagt saman.</span><span class="sxs-lookup"><span data-stu-id="9b97c-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="9b97c-113">Veljið "Já" ef færsla peningaflutningur í banka ætti að lagt saman.</span><span class="sxs-lookup"><span data-stu-id="9b97c-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="9b97c-114">Veljið "Já" til að kveikja á uppsöfnun fyrir bókun Uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="9b97c-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="9b97c-115">Veljið "Já" til að stofna og vinna sölupantanir samhliða þegar yfirlit eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="9b97c-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="9b97c-116">Færið inn hámark pantana sem þarf að vinna í hverri runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="9b97c-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="9b97c-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9b97c-117">Click Save.</span></span>


