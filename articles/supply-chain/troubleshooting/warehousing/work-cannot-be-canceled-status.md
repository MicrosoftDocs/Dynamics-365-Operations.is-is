---
title: Ekki er hægt að hætta við vinnu vegna stöðu hennar
description: Ekki er hægt að hætta við vinnu vegna stöðu hennar
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924256"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="d88c8-103">Ekki er hægt að hætta við vinnu vegna stöðu hennar</span><span class="sxs-lookup"><span data-stu-id="d88c8-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="d88c8-104">Villukóði WAX2190</span><span class="sxs-lookup"><span data-stu-id="d88c8-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="d88c8-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="d88c8-105">Symptoms</span></span>

<span data-ttu-id="d88c8-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="d88c8-106">The system shows the following error message:</span></span>

> <span data-ttu-id="d88c8-107">Ekki er hægt að hætta við vinnu %1 því að hún er með stöðuna %2.</span><span class="sxs-lookup"><span data-stu-id="d88c8-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="d88c8-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="d88c8-108">Cause</span></span>

<span data-ttu-id="d88c8-109">Ekki er hægt að hætta við verkið í núverandi stöðu.</span><span class="sxs-lookup"><span data-stu-id="d88c8-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="d88c8-110">Vinnuhaus eða vinnulínur eru ekki með væntanlegt gildi **Vinnustöðu**.</span><span class="sxs-lookup"><span data-stu-id="d88c8-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="d88c8-111">Reiturinn **Vinnustaða** í vinnuhausnum er ekki stilltur á *Opið* eða *Í vinnslu*.</span><span class="sxs-lookup"><span data-stu-id="d88c8-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="d88c8-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="d88c8-112">Resolution</span></span>

<span data-ttu-id="d88c8-113">Til að hætta við verkið skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="d88c8-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="d88c8-114">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="d88c8-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="d88c8-115">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.</span><span class="sxs-lookup"><span data-stu-id="d88c8-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="d88c8-116">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d88c8-116">Select **OK**.</span></span>
1. <span data-ttu-id="d88c8-117">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="d88c8-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="d88c8-118">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="d88c8-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
