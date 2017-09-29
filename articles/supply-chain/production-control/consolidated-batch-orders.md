---
title: "Sameinaðar runupantanir"
description: "Þessi grein lýsir hugtakinu á bakvið samsteyptur runupöntun."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="ee52d-103">Sameinaðar runupantanir</span><span class="sxs-lookup"><span data-stu-id="ee52d-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ee52d-104">Þessi grein lýsir hugtakinu á bakvið samsteyptur runupöntun.</span><span class="sxs-lookup"><span data-stu-id="ee52d-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="ee52d-105">Fjöldavara°sem er framleidd er talin yfirvara, og pökkuð vara er talin undirvara.</span><span class="sxs-lookup"><span data-stu-id="ee52d-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="ee52d-106">Tengsl á milli fjöldavöru og pakkaðrar vöru er sýnd í umreikningi fjöldavöru.</span><span class="sxs-lookup"><span data-stu-id="ee52d-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="ee52d-107">Þessi umreikningur fjöldavöru er skilgreindur í fjöldavörunni sjálfri.</span><span class="sxs-lookup"><span data-stu-id="ee52d-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="ee52d-108">Pökkuðum vörum getur verið pakkað í umbúðir fyrir eina vöru eða í umbúðir sem innihalda fleiri vörur en eru taldar sem ein eining.</span><span class="sxs-lookup"><span data-stu-id="ee52d-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="ee52d-109">Þegar pantanir eru sameinaðar,í fjöldavöru er hægt að skoða allar tengdar runupantanir í einni skjámynd til að auðvelda þér að ákvarða eftirstöðvar vinnu sem verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="ee52d-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="ee52d-110">Sameinaðri runupöntun getur innihaldið samsetningu af eftirfarandi pantanir:</span><span class="sxs-lookup"><span data-stu-id="ee52d-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="ee52d-111">Ein fjöldapöntun og margar pakkapantanir</span><span class="sxs-lookup"><span data-stu-id="ee52d-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="ee52d-112">Margar fjöldapantanir og margar pakkapantanir</span><span class="sxs-lookup"><span data-stu-id="ee52d-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="ee52d-113">Margar fjöldapantanir og ein pakkapöntun</span><span class="sxs-lookup"><span data-stu-id="ee52d-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="ee52d-114">Aðeins pakkapantanir</span><span class="sxs-lookup"><span data-stu-id="ee52d-114">Only packed orders</span></span>





