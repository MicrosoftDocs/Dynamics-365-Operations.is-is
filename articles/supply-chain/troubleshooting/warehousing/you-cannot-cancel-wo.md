---
title: Ekki er hægt að hætta við vinnu sem er skráð á notanda
description: Ekki er hægt að hætta við vinnu sem er skráð á notanda
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924402"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="a9814-103">Ekki er hægt að hætta við vinnu sem er skráð á notanda</span><span class="sxs-lookup"><span data-stu-id="a9814-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="a9814-104">Villukóði WAX708</span><span class="sxs-lookup"><span data-stu-id="a9814-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="a9814-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="a9814-105">Symptoms</span></span>

<span data-ttu-id="a9814-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="a9814-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a9814-107">Ekki er hægt að hætta við vinnu sem er skráð á notanda.</span><span class="sxs-lookup"><span data-stu-id="a9814-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="a9814-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="a9814-108">Cause</span></span>

<span data-ttu-id="a9814-109">Verki er læst af notanda og er ekki hægt að hætta við.</span><span class="sxs-lookup"><span data-stu-id="a9814-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="a9814-110">Opnaðu vinnukennið og opnaðu svo flipann **Almennt** til að staðfesta þetta. Ef verkið er læst verður reiturinn **Staða verks** stilltur á *Í vinnslu* og reiturinn **Læst af** stilltur á notandakenni.</span><span class="sxs-lookup"><span data-stu-id="a9814-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="a9814-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="a9814-111">Resolution</span></span>

<span data-ttu-id="a9814-112">Til að hætta við verkið skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="a9814-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="a9814-113">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="a9814-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a9814-114">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.</span><span class="sxs-lookup"><span data-stu-id="a9814-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="a9814-115">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a9814-115">Select **OK**.</span></span>
1. <span data-ttu-id="a9814-116">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="a9814-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="a9814-117">Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="a9814-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
