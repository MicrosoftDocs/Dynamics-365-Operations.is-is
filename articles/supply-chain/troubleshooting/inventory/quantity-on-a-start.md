---
title: Magn í biðgeymslupöntun í vinnslu uppfærist ekki þegar pöntuninni er skipt
description: Þegar biðgeymslupöntun er stofnuð og reynt að skipta henni er pöntunarmagnið ekki uppfært í það magn sem eftir er af pöntuninni.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026622"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="54160-103">Magn í biðgeymslupöntun í vinnslu uppfærist ekki þegar pöntuninni er skipt</span><span class="sxs-lookup"><span data-stu-id="54160-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="54160-104">KB númer: 4613113</span><span class="sxs-lookup"><span data-stu-id="54160-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="54160-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="54160-105">Symptoms</span></span>

<span data-ttu-id="54160-106">Þegar biðgeymslupöntun er stofnuð og reynt að skipta henni er pöntunarmagnið ekki uppfært í eftirstöðvarnar eftir skiptinguna.</span><span class="sxs-lookup"><span data-stu-id="54160-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="54160-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="54160-107">Resolution</span></span>

<span data-ttu-id="54160-108">Kerfið breytir ekki upprunalegu magni úr biðgeymslupöntun til að tryggja að hægt sé að rekja upprunalegt magn sem búið var til fyrir þá biðgeymslupöntun.</span><span class="sxs-lookup"><span data-stu-id="54160-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="54160-109">Kerfið fylgist hins vegar ekki með magninu sem skipt er úr biðgeymslupöntun.</span><span class="sxs-lookup"><span data-stu-id="54160-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="54160-110">Þetta er gert með gagnagrunnsreit sem kallast `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="54160-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="54160-111">Þessi reitur er þó ekki sýnilegur í notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="54160-111">However, this field isn't visible in the user interface (UI).</span></span>
