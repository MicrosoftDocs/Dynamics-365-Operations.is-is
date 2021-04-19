---
title: Kanna vörugæði
description: Þetta efni útskýrir hvernig á að vinna úr gæðapöntun.
author: perlynne
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e7156e5c57d5f983564cc966b4108f1180ff8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825916"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="ad747-103">Kanna vörugæði</span><span class="sxs-lookup"><span data-stu-id="ad747-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad747-104">Þetta efni útskýrir hvernig á að vinna úr gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="ad747-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="ad747-105">Hægt er að keyra þessari handbók sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="ad747-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="ad747-106">Áður en byrjað er á þessu dæmaferli, þarf að staðfesta innkaupapöntun „000016” og bóka innhreyfingarskjal afurða.</span><span class="sxs-lookup"><span data-stu-id="ad747-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="ad747-107">Þetta stofna sjálfkrafa gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="ad747-107">This will automatically create a quality order.</span></span> <span data-ttu-id="ad747-108">Gæðaeftirlit eru yfirleitt framkvæmd með því að starfsmaður á sviði gæða.</span><span class="sxs-lookup"><span data-stu-id="ad747-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ad747-109">Velja gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="ad747-109">Select a quality order</span></span>
1. <span data-ttu-id="ad747-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastjórnun > Reglubundin verkefni > Gæðastjórnun > Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="ad747-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="ad747-111">Veljið gæðapöntun var stofnuð áður en þetta ferli er hafið.</span><span class="sxs-lookup"><span data-stu-id="ad747-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="ad747-112">Skrá niðurstöðu prófunar</span><span class="sxs-lookup"><span data-stu-id="ad747-112">Record test results</span></span>
1. <span data-ttu-id="ad747-113">Veldu **Niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="ad747-113">Select **Results**.</span></span>
2. <span data-ttu-id="ad747-114">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ad747-114">Select **Edit**.</span></span>
3. <span data-ttu-id="ad747-115">Í reitnum **Niðurstöðumagn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="ad747-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="ad747-116">Í reitnum **Útkoma** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="ad747-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="ad747-117">Í þessu dæmi niðurstaðan er byggt á fyrirframskilgreindu útkomu.</span><span class="sxs-lookup"><span data-stu-id="ad747-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="ad747-118">Vanalega væri skráð nákvæmari niðurstöður prófana, til dæmis stærð eða öðrum vídd.</span><span class="sxs-lookup"><span data-stu-id="ad747-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="ad747-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ad747-119">Select **Save**.</span></span>
6. <span data-ttu-id="ad747-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ad747-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="ad747-121">Villuprófa gæðapöntunina</span><span class="sxs-lookup"><span data-stu-id="ad747-121">Validate the quality order</span></span>
1. <span data-ttu-id="ad747-122">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="ad747-122">Select **Validate**.</span></span>
2. <span data-ttu-id="ad747-123">Í reitnum **Staðfest af** veldu notandann sem framkvæmir skoðunina í fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="ad747-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="ad747-124">Smellið á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="ad747-124">Click **Select**.</span></span>
4. <span data-ttu-id="ad747-125">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ad747-125">Select **OK**.</span></span>
5. <span data-ttu-id="ad747-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ad747-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]