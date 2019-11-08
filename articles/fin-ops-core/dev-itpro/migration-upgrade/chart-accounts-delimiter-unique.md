---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Þetta efni útskýrir hvernig ekki er hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 5861bcaa42f7bc5ec20916fe1a44418bdd9c2ffe
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550909"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="d6394-104">Gera skiltákn bókhaldslykils einkvæmt</span><span class="sxs-lookup"><span data-stu-id="d6394-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6394-105">Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi.</span><span class="sxs-lookup"><span data-stu-id="d6394-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="d6394-106">Í núverandi útgáfum af Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi.</span><span class="sxs-lookup"><span data-stu-id="d6394-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="d6394-107">Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="d6394-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="d6394-108">Þessi eiginleiki er ekki í boði eftirfarandi útgáfum:</span><span class="sxs-lookup"><span data-stu-id="d6394-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="d6394-109">Finance and Operations, útgáfu 8.0</span><span class="sxs-lookup"><span data-stu-id="d6394-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="d6394-110">Finance and Operations, útgáfu 7.1, KB 4094701 Ekki er hægt að slá inn fjárhagsvíddir þegar víddargildin innihalda skiltákn bókhaldslykils</span><span class="sxs-lookup"><span data-stu-id="d6394-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="d6394-111">Finance and Operations, útgáfu 7.2, KB 4092967 Ekki er hægt að velja undirverk sem vídd þegar snið undirverks inniheldur víddarskiltákn</span><span class="sxs-lookup"><span data-stu-id="d6394-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="d6394-112">Uppfæra skiltákn</span><span class="sxs-lookup"><span data-stu-id="d6394-112">Update delimiter</span></span>
<span data-ttu-id="d6394-113">Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði.</span><span class="sxs-lookup"><span data-stu-id="d6394-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="d6394-114">Ekki er hægt að breyta öðrum víddarskiltáknum.</span><span class="sxs-lookup"><span data-stu-id="d6394-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="d6394-115">Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**.</span><span class="sxs-lookup"><span data-stu-id="d6394-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="d6394-116">Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**.</span><span class="sxs-lookup"><span data-stu-id="d6394-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="d6394-117">Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna</span><span class="sxs-lookup"><span data-stu-id="d6394-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="d6394-118">Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu.</span><span class="sxs-lookup"><span data-stu-id="d6394-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="d6394-119">Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.</span><span class="sxs-lookup"><span data-stu-id="d6394-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
