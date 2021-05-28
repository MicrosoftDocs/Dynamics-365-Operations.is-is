---
title: Þú getur ekki flutt inn hlut með því að nota eininguna Útgefnar afurðir V2
description: Þú getur ekki flutt inn hlut með því að nota eininguna Útgefnar afurðir V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026601"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="b945f-103">Þú getur ekki flutt inn hlut með því að nota eininguna Útgefnar afurðir V2</span><span class="sxs-lookup"><span data-stu-id="b945f-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="b945f-104">KB númer: 4611825</span><span class="sxs-lookup"><span data-stu-id="b945f-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="b945f-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="b945f-105">Symptoms</span></span>

<span data-ttu-id="b945f-106">Þegar reynt er að flytja inn hlut með því að nota *Útgefnar afurðir V2* birtast villuboð sem líkjast eftirfarandi dæmi:</span><span class="sxs-lookup"><span data-stu-id="b945f-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="b945f-107">Ekki tókst að stofna færslu í atriði - víddarakningarflokkar (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="b945f-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="b945f-108">Vörunúmer: 2040663, Lota.</span><span class="sxs-lookup"><span data-stu-id="b945f-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="b945f-109">Færsla þegar til.</span><span class="sxs-lookup"><span data-stu-id="b945f-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="b945f-110">Upplausn</span><span class="sxs-lookup"><span data-stu-id="b945f-110">Resolution</span></span>

<span data-ttu-id="b945f-111">Til að flytja inn nýjar útgefnar vörur verður að nota eininguna *Útgefin stofnun afurðar V2* í stað einingarinnar *Útgefnar afurðir V2*.</span><span class="sxs-lookup"><span data-stu-id="b945f-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
