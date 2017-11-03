---
title: "Uppfæra staðalkostnað í framleiðsluumhverfis"
description: "Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðsluumhverfi."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="fbae1-103">Uppfæra staðalkostnað í framleiðsluumhverfis</span><span class="sxs-lookup"><span data-stu-id="fbae1-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fbae1-104">Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="fbae1-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="fbae1-105">Uppfærslur geta endurspeglað nýjar vörur, kostnaðartegundir eða óbeinar formúlur kostnaðarútreiknings.</span><span class="sxs-lookup"><span data-stu-id="fbae1-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="fbae1-106">Þeir geta einnig endurspeglað leiðréttingar og breytingar á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="fbae1-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="fbae1-107">Uppfærslugerðin mun hafa áhrif á þau skref sem eru nauðsynleg til að uppfæra staðalkostnað eins og sýnt er í eftirfarandi tilfellum.</span><span class="sxs-lookup"><span data-stu-id="fbae1-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="fbae1-108">Færið inn þær staðalkostnaðarbreytingar sem búist er við fyrir keyptar vörur og breytið svo stöðu kostnaðarfærslu vörunnar **í virkt** á viðeigandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fbae1-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="fbae1-109">En ekki endurreikna samt kostnað framleiddra vara sem nota keyptu vörurnar.</span><span class="sxs-lookup"><span data-stu-id="fbae1-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="fbae1-110">Færið inn staðalkostnað fyrir nýja keypta vöru en ekki endurreikna kostnað framleiddra vara með uppskriftarútgáfu sem inniheldur keyptu vöruna sem þátt.</span><span class="sxs-lookup"><span data-stu-id="fbae1-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="fbae1-111">Leiðréttið eða breytið kostnaði keyptu vörunnar eða breytið kostnaðarflokknum sem er úthlutaður keyptu vörunni og reiknið út kostnað allra framleiddra vara með víxilsútgáfu sem inniheldur keyptu vöruna sem þátt.</span><span class="sxs-lookup"><span data-stu-id="fbae1-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="fbae1-112">Breytið kostnaði kostnaðartegundar og reiknið út kostnað allra framleiddra vara með leiðarútgáfu sem inniheldur leiðaraðgerðir sem nota kostnaðartegundina.</span><span class="sxs-lookup"><span data-stu-id="fbae1-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="fbae1-113">Breytið kostnaðartegundunum sem eru úthlutaðar leiðaraðgerðum eða kostnaðarflokknum sem er úthlutaður kostnaðartegundum.</span><span class="sxs-lookup"><span data-stu-id="fbae1-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="fbae1-114">Reiknið síðan út kostnað allra framleiddra vara með leiðarútgáfu sem inniheldur leiðaraðgerðir sem nota kostnaðartegundina.</span><span class="sxs-lookup"><span data-stu-id="fbae1-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="fbae1-115">Breytið óbeinni jöfnu kostnaðarútreiknings og reiknið út kostnaðinn fyrir allar framleiddar vörur sem verða fyrir áhrifum vegna breytingarinnar.</span><span class="sxs-lookup"><span data-stu-id="fbae1-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="fbae1-116">Breytið eða bætið við framleiðslustað fyrir framleidda vöru og reiknið út framleiðslukostnað vörunnar fyrir staðinn.</span><span class="sxs-lookup"><span data-stu-id="fbae1-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="fbae1-117">Reiknið út (eða endurreiknið) kostnaðinn við framleidda vörur og endurreiknið kostnaðinn við allar framleiddar vörur með víxilútgáfu sem inniheldur framleiddu vöruna sem þátt.</span><span class="sxs-lookup"><span data-stu-id="fbae1-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="fbae1-118">Reiknið út kostnað við nýja framleidda vöru á grundvelli skilgreindra, samþykktra og virkra víxils- og leiðarupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="fbae1-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="fbae1-119">Hvert tilfelli krefst ítarlegrar umhugsunar um það hvernig eigi að uppfæra staðalkostnað.</span><span class="sxs-lookup"><span data-stu-id="fbae1-119">Each case requires careful consideration about how to update standard costs.</span></span>




