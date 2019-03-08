---
title: " Skilgreiningar færibreyta fyrir smásöluyfirlit"
description: Þetta ferli sýnir skilgreiningar fyrir smásölufæribreytur sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "352621"
---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="5f877-103"> Skilgreiningar færibreyta fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="5f877-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5f877-104">Þetta ferli sýnir skilgreiningar fyrir smásölufæribreytur sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="5f877-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="5f877-105">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5f877-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="5f877-106">Farið í Smásala og viðskipti > Uppsetning höfuðstöðva > Færibreytur > Smásölufæribreytur.</span><span class="sxs-lookup"><span data-stu-id="5f877-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="5f877-107">Smellt er á flipann Bókun</span><span class="sxs-lookup"><span data-stu-id="5f877-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="5f877-108">Veljið "Já" ef óskað er að bóka upphæðir tímabundins afsláttar sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="5f877-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="5f877-109">Veljið "Venjulegur" til að nota sjálfgefna fjárhagslykla eða veldu "Reglubundið" ef óskað er að skilgreina hvaða lykill sem nota á fyrir hverja tímabundins afsláttar.</span><span class="sxs-lookup"><span data-stu-id="5f877-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="5f877-110">Veljið "Samantekt" ef ætti að leggja saman línur birgða þegar unnt er.</span><span class="sxs-lookup"><span data-stu-id="5f877-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="5f877-111">Veljið "Já" ef Reikninga og Greiðslur skuli sjálfkrafa jafnaður sem hluti af Uppgjör bókunarferli.</span><span class="sxs-lookup"><span data-stu-id="5f877-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="5f877-112">Veljið "Já" ef færsla peningaflutnings í öryggisskáp ætti að lagt saman.</span><span class="sxs-lookup"><span data-stu-id="5f877-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="5f877-113">Veljið "Já" ef færsla peningaflutningur í banka ætti að lagt saman.</span><span class="sxs-lookup"><span data-stu-id="5f877-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="5f877-114">Veljið "Já" til að kveikja á uppsöfnun fyrir bókun Uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="5f877-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="5f877-115">Veljið "Já" til að stofna og vinna sölupantanir samhliða þegar yfirlit eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="5f877-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="5f877-116">Færið inn hámark pantana sem þarf að vinna í hverri runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="5f877-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="5f877-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5f877-117">Click Save.</span></span>

