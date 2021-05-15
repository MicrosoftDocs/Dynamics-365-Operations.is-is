---
title: Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð
description: Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924280"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="5fdb4-103">Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð</span><span class="sxs-lookup"><span data-stu-id="5fdb4-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="5fdb4-104">Villukóði: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="5fdb4-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="5fdb4-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="5fdb4-105">Symptoms</span></span>

<span data-ttu-id="5fdb4-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5fdb4-107">Ekki er hægt að hætta við vinnu %1 vegna þess að ástæða af gerðinni %2 hefur lokað á hana.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="5fdb4-108">Opna verður vinnuna áður en hægt er að hætta við hana.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="5fdb4-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="5fdb4-109">Cause</span></span>

<span data-ttu-id="5fdb4-110">Verkið er lokað og ekki er hægt að hætta við.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="5fdb4-111">Á síðunni **Vinna**, á flipanum **Almennt**, er valkosturinn **Lokað** stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="5fdb4-112">Þessi stilling gefur til kynna að vinnan sé lokuð.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="5fdb4-113">Flipinn **Ástæður lokunar** sýnir ástæðu þess að lokað var á vinnuna.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="5fdb4-114">Upplausn</span><span class="sxs-lookup"><span data-stu-id="5fdb4-114">Resolution</span></span>

<span data-ttu-id="5fdb4-115">Til að opna fyrir vinnuna skal velja flipann **Lokunarástæður** og fylgja svo einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="5fdb4-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="5fdb4-116">Ef reiturinn **Ástæða fyrir vinnulokun** er stilltur á *Óskilgreind ástæða*: Á aðgerðasvæðinu, í flipanum **Vinna**, í flokknum **Vinna**, skal velja **Opna fyrir verk**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="5fdb4-117">Ef reiturinn **Ástæða fyrir vinnulokun** er stilltur á *Bylgjuvinnsla*: Á aðgerðasvæðinu, í flipanum **Tengdar upplýsingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgja**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="5fdb4-118">Á síðunni **Bylgjur**, á aðgerðasvæðinu, á flipanum **Bylgja** í **Bylgja** hópnum skal síðan velja **Hreinsa bylgjugögn**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="5fdb4-119">Hjáleið</span><span class="sxs-lookup"><span data-stu-id="5fdb4-119">Workaround</span></span>

<span data-ttu-id="5fdb4-120">Ef fyrri skrefin leystu ekki úr vandanum er hægt að hætta við verkið með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="5fdb4-121">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="5fdb4-122">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="5fdb4-123">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-123">Select **OK**.</span></span>
1. <span data-ttu-id="5fdb4-124">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="5fdb4-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="5fdb4-125">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="5fdb4-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
