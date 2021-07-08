---
title: Vara má ekki hafa uppskrift eða formúlu
description: Þegar reynt er að festa pöntun berast villuboð við staðfestingu vöru. Þar kemur fram að varan má ekki vera með uppskrift eða formúlu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294101"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="dde8d-104">Vara má ekki hafa uppskrift eða formúlu</span><span class="sxs-lookup"><span data-stu-id="dde8d-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="dde8d-105">Villukóði PRO2614</span><span class="sxs-lookup"><span data-stu-id="dde8d-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="dde8d-106">Einkenni</span><span class="sxs-lookup"><span data-stu-id="dde8d-106">Symptoms</span></span>

<span data-ttu-id="dde8d-107">Þegar reynt er að festa pöntun berast eftirfarandi villuboð við staðfestingu vöru:</span><span class="sxs-lookup"><span data-stu-id="dde8d-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="dde8d-108">Vara má hvorki hafa uppskrift né formúlu</span><span class="sxs-lookup"><span data-stu-id="dde8d-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="dde8d-109">Lausn</span><span class="sxs-lookup"><span data-stu-id="dde8d-109">Resolution</span></span>

<span data-ttu-id="dde8d-110">Vörur sem eru með uppskriftir eða formúlu verða að vera af gerðinni *Áætlunarvara*, *Uppskrift* eða *Formúla*.</span><span class="sxs-lookup"><span data-stu-id="dde8d-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="dde8d-111">Til að breyta gerð vörunnar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="dde8d-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="dde8d-112">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="dde8d-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="dde8d-113">Viðeigandi vara er opnuð.</span><span class="sxs-lookup"><span data-stu-id="dde8d-113">Open the relevant product.</span></span>
1. <span data-ttu-id="dde8d-114">Í flýtiflipanum **Hönnuður** skal stilla reitinn **Framleiðslugerð** á *Áætlunarvara*, *Uppskrift* eða *Formúlu*.</span><span class="sxs-lookup"><span data-stu-id="dde8d-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
