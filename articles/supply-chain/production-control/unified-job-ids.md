---
title: Samræmd númeraröð fyrir vinnslukenni
description: Þessi eiginleiki býður upp á eina samræmda númeraröð sem býr til vinnslukenni fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824943"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="7181d-103">Samræmd númeraröð fyrir vinnslukenni</span><span class="sxs-lookup"><span data-stu-id="7181d-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7181d-104">Þessi eiginleiki býður upp á eina samræmda númeraröð sem býr til vinnslukenni fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru.</span><span class="sxs-lookup"><span data-stu-id="7181d-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="7181d-105">Áður var hægt að velja mismunandi númeraröð fyrir hverja einingu fyrir sig, sem gat leitt til vinnslukenna sem stönguðust á ef tvær eða fleiri þessara raða notuðu eins snið.</span><span class="sxs-lookup"><span data-stu-id="7181d-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="7181d-106">Slíkur árekstur getur skemmt gögn.</span><span class="sxs-lookup"><span data-stu-id="7181d-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="7181d-107">Kveikja á þessum eiginleika fyrir kerfið</span><span class="sxs-lookup"><span data-stu-id="7181d-107">Turn on this feature for your system</span></span>

<span data-ttu-id="7181d-108">Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Samræmd númeraröð fyrir vinnslukenni*.</span><span class="sxs-lookup"><span data-stu-id="7181d-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="7181d-109">Setja upp samræmda númeraröð fyrir vinnslukenni</span><span class="sxs-lookup"><span data-stu-id="7181d-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="7181d-110">Þegar þessi eiginleiki hefur verið virkjaður, verða fyrirliggjandi númeraraðastillingar fyrir **Auðkenningu vinnslu**, sem staðsettar eru á færibreytusíðum fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru úreldar og nýjum reit **Samræmds vinnslukennis** verður bætt við.</span><span class="sxs-lookup"><span data-stu-id="7181d-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="7181d-111">Allar þrjár einingarnar samnýta gildið fyrir **Samræmt vinnslukenni** sem fyrir vikið tryggir að allar einingarnar vísi í sömu númeraröðina.</span><span class="sxs-lookup"><span data-stu-id="7181d-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="7181d-112">Vinnslukenni verða þar af leiðand einkvæm yfir allar þrjár einingarnar og árekstrar því úr sögunni.</span><span class="sxs-lookup"><span data-stu-id="7181d-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="7181d-113">Til að setja upp samræmda númeraröð fyrir vinnslukenni:</span><span class="sxs-lookup"><span data-stu-id="7181d-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="7181d-114">Kveikið á eiginleikanum eins og lýst er í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="7181d-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="7181d-115">Annaðhvort skal benda á númeraröðina sem á að nota fyrir samræmd vinnslukenni eða stofna nýja.</span><span class="sxs-lookup"><span data-stu-id="7181d-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="7181d-116">Frekari upplýsingar er að finna í [Yfirlit númeraraða](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7181d-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="7181d-117">Farið á síðuna **Færibreytur framleiðslustýringar**, **Færibreytur framleiðsluframkvæmdar** eða **Færibreytur tíma og viðveru**.</span><span class="sxs-lookup"><span data-stu-id="7181d-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="7181d-118">Það skiptir ekki máli hvað er valið þegar þessi stilling er gerð á einhverri af þessum síðum þar sem allar aðrar síður uppfærast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="7181d-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="7181d-119">Opnið **Númeraraðir** flipann á valinni færibreytusíðu.</span><span class="sxs-lookup"><span data-stu-id="7181d-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="7181d-120">Úthlutið **Númeraraðarkóðanum** sem gerð var grein fyrir áður í línunni **Samræmd vinnslukenni** í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="7181d-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
