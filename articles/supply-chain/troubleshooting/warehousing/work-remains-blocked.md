---
title: Áfram er lokað á vinnu
description: Áfram er lokað á vinnu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924131"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="c0009-103">Áfram er lokað á vinnu</span><span class="sxs-lookup"><span data-stu-id="c0009-103">Work remains blocked</span></span>

<span data-ttu-id="c0009-104">Villukóði: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="c0009-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="c0009-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="c0009-105">Symptoms</span></span>

<span data-ttu-id="c0009-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="c0009-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c0009-107">Vinna %1 er áfram útilokuð vegna þess að tengd bylgja %2 er með stöðuna %3.</span><span class="sxs-lookup"><span data-stu-id="c0009-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="c0009-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="c0009-108">Cause</span></span>

<span data-ttu-id="c0009-109">Vinnan er í bylgjuvinnslu og ekki er hægt að opna hana, eins og tilgreint er með einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="c0009-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="c0009-110">Á flipanum **Ástæður lokana** er reiturinn **Ástæða fyrir vinnulokun** fyrir eina eða fleiri línur stilltur á *Bylgjuvinnsla*.</span><span class="sxs-lookup"><span data-stu-id="c0009-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="c0009-111">Þegar þú velur **Bylgja** í flokknum **Tengdar upplýsingar** á flipanum **Tengdar upplýsingar** í aðgerðasvæðinu er **Staða bylgju** stillt á *Vinnsla*.</span><span class="sxs-lookup"><span data-stu-id="c0009-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c0009-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="c0009-112">Resolution</span></span>

<span data-ttu-id="c0009-113">Á aðgerðasvæðinu, í flipanum **Tengdar upplýsingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgja**.</span><span class="sxs-lookup"><span data-stu-id="c0009-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="c0009-114">Á síðunni **Bylgjur**, á aðgerðasvæðinu, á flipanum **Bylgja** í **Bylgja** hópnum skal síðan velja **Hreinsa bylgjugögn**.</span><span class="sxs-lookup"><span data-stu-id="c0009-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="c0009-115">Hjáleið</span><span class="sxs-lookup"><span data-stu-id="c0009-115">Workaround</span></span>

<span data-ttu-id="c0009-116">Ef fyrri skrefin leystu ekki úr vandanum er hægt að hætta við verkið með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c0009-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="c0009-117">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="c0009-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="c0009-118">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.</span><span class="sxs-lookup"><span data-stu-id="c0009-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="c0009-119">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c0009-119">Select **OK**.</span></span>
1. <span data-ttu-id="c0009-120">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="c0009-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="c0009-121">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="c0009-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
