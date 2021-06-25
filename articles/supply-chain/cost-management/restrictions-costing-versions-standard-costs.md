---
title: Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað
description: Þetta efnisatriði fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d828e2413a20c4e61d162a31d3c2ed2b18718b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187675"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="a3567-103">Takmarkanir á kostnaðarútgáfum fyrir staðalkostnað</span><span class="sxs-lookup"><span data-stu-id="a3567-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3567-104">Þetta efnisatriði fjallar um þær takmarkanir sem gilda um kostnaðarútgáfu fyrir staðalkostnað.</span><span class="sxs-lookup"><span data-stu-id="a3567-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="a3567-105">Eftirfarandi takmarkanir stuðla að því að reglum um staðalkostnað sé fylgt:</span><span class="sxs-lookup"><span data-stu-id="a3567-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="a3567-106">Gjöld verða að vera innifalinn í kostnaði vöru.</span><span class="sxs-lookup"><span data-stu-id="a3567-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="a3567-107">Gjöld vegna framleiddrar vöru standa fyrir afskrifaðan fastan kostnað í uppskriftum (BOM) og leiðarlýsingar.</span><span class="sxs-lookup"><span data-stu-id="a3567-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="a3567-108">Þess vegna verða gjöldin að vera innifalinn í einingarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="a3567-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="a3567-109">Gjöldin vegna keyptra vara eru einnig innifalin í einingarkostnaði vörunnar.</span><span class="sxs-lookup"><span data-stu-id="a3567-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="a3567-110">Útreikningur á staðalkostnaði framleiddrar vöru verður að byggja á kostnaðarfærslum í kostnaðarútgáfu fyrir staðalkostnað.</span><span class="sxs-lookup"><span data-stu-id="a3567-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="a3567-111">Annan uppruna kostnaðargagna er aðeins hægt að nota með kostnaðarútgáfu fyrir áætlaðan kostnað, eins og viðskiptasamningi um innkaupaverð fyrir keyptar vörur.</span><span class="sxs-lookup"><span data-stu-id="a3567-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="a3567-112">Annar uppruni kostnaðargagna er skilgreindur af flokki uppskriftarútreiknings.</span><span class="sxs-lookup"><span data-stu-id="a3567-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="a3567-113">Útreikningar uppskrifta verður að framkvæma með eins stigs niðurbroti.</span><span class="sxs-lookup"><span data-stu-id="a3567-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="a3567-114">Hægt er að afrita kostnaðargögn vöru fyrir staðlaðan kostnað í aðra kostnaðarútgáfu sem inniheldur staðlaðan kostnað eða áætlaðan kostnað.</span><span class="sxs-lookup"><span data-stu-id="a3567-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="a3567-115">Hins vegar er ekki hægt að afrita kostnaðargögn vöru yfir í kostnaðarútgáfu sem inniheldur staðalkostnað, þar sem takmarkanirnar sem er lýst fyrr í þessu efnisatriði eiga ekki við áætlaðan kostnað.</span><span class="sxs-lookup"><span data-stu-id="a3567-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3567-116">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="a3567-116">Related topics</span></span>

[<span data-ttu-id="a3567-117">Yfirlit kostnaðarútgáfa</span><span class="sxs-lookup"><span data-stu-id="a3567-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="a3567-118">Uppfæra staðalkostnað í umhverfi sem er ekki fyrir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="a3567-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="a3567-119">Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur</span><span class="sxs-lookup"><span data-stu-id="a3567-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]