---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Í Dynamics 365 for Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
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
ms.openlocfilehash: 8cc05772e7ee125a5ce8603c4d5f8719e8895c73
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851772"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="5990b-104">Gera skiltákn bókhaldslykils einkvæmt</span><span class="sxs-lookup"><span data-stu-id="5990b-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5990b-105">Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi.</span><span class="sxs-lookup"><span data-stu-id="5990b-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="5990b-106">Í Dynamics 365 for Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi.</span><span class="sxs-lookup"><span data-stu-id="5990b-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="5990b-107">Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="5990b-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="5990b-108">Þessi eiginleiki er fáanlegur í:</span><span class="sxs-lookup"><span data-stu-id="5990b-108">This feature is available in:</span></span>
- <span data-ttu-id="5990b-109">Dynamics 365 for Finance and Operations útgáfa 8.0</span><span class="sxs-lookup"><span data-stu-id="5990b-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="5990b-110">Dynamics 365 for Finance and Operations útgáfa 7.1, KB 4094701 Ekki er hægt að slá inn fjárhagsvíddir þegar víddargildin innihalda skiltákn bókhaldslykils</span><span class="sxs-lookup"><span data-stu-id="5990b-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="5990b-111">Dynamics 365 for Finance and Operations útgáfa 7.2, KB 4092967 Ekki er hægt að velja undirverk sem vídd þegar snið undirverks inniheldur víddarskiltákn</span><span class="sxs-lookup"><span data-stu-id="5990b-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="5990b-112">Uppfæra skiltákn</span><span class="sxs-lookup"><span data-stu-id="5990b-112">Update delimiter</span></span>
<span data-ttu-id="5990b-113">Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði.</span><span class="sxs-lookup"><span data-stu-id="5990b-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="5990b-114">Ekki er hægt að breyta öðrum víddarskiltáknum.</span><span class="sxs-lookup"><span data-stu-id="5990b-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="5990b-115">Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu á Finance and Operations í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**.</span><span class="sxs-lookup"><span data-stu-id="5990b-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="5990b-116">Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**.</span><span class="sxs-lookup"><span data-stu-id="5990b-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="5990b-117">Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna</span><span class="sxs-lookup"><span data-stu-id="5990b-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="5990b-118">Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu.</span><span class="sxs-lookup"><span data-stu-id="5990b-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="5990b-119">Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.</span><span class="sxs-lookup"><span data-stu-id="5990b-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
