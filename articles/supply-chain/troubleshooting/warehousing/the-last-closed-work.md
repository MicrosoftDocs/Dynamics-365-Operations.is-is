---
title: Síðasta lokaða vinnulína verður að vera ganga frá
description: Síðasta lokaða vinnulína verður að vera ganga frá
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924376"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="1a258-103">Síðasta lokaða vinnulína verður að vera ganga frá</span><span class="sxs-lookup"><span data-stu-id="1a258-103">The last closed work line must be a put</span></span>

<span data-ttu-id="1a258-104">Villukóði WAX1285</span><span class="sxs-lookup"><span data-stu-id="1a258-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="1a258-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="1a258-105">Symptoms</span></span>

<span data-ttu-id="1a258-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="1a258-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1a258-107">Síðasta lokaða vinnulína verður að vera Ganga frá.</span><span class="sxs-lookup"><span data-stu-id="1a258-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="1a258-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="1a258-108">Cause</span></span>

<span data-ttu-id="1a258-109">Ekki er hægt að hætta við verkið í núverandi stöðu.</span><span class="sxs-lookup"><span data-stu-id="1a258-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="1a258-110">Í síðustu vinnulínunni er reiturinn **Staða verks** stilltur á *Lokaður*, en reiturinn **Vinnugerð** er ekki stilltur á *Frágangur*.</span><span class="sxs-lookup"><span data-stu-id="1a258-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a258-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="1a258-111">Resolution</span></span>

<span data-ttu-id="1a258-112">Til að hætta við verkið skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="1a258-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="1a258-113">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="1a258-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="1a258-114">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.</span><span class="sxs-lookup"><span data-stu-id="1a258-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="1a258-115">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1a258-115">Select **OK**.</span></span>
1. <span data-ttu-id="1a258-116">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="1a258-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="1a258-117">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="1a258-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
