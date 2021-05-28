---
title: Að afturkalla skýrslu sem er lokið býr til óvænta opna færslu
description: Bakfærsla skýrslu sem lokið sem er með merkingu skapar opna færslu þar sem bakfært magn hefur sömu birgðavíddir og bakfærða færslan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026621"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="37246-103">Að afturkalla skýrslu sem er lokið býr til óvænta opna færslu</span><span class="sxs-lookup"><span data-stu-id="37246-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="37246-104">KB númer: 4612469</span><span class="sxs-lookup"><span data-stu-id="37246-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="37246-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="37246-105">Symptoms</span></span>

<span data-ttu-id="37246-106">Ef þú bakfærir skýrslu sem lokið sem er með merkingu býrð kerfið til opna færslu þar sem bakfærða magnið hefur sömu birgðastærðir og bakfærða færslan.</span><span class="sxs-lookup"><span data-stu-id="37246-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="37246-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="37246-107">Resolution</span></span>

<span data-ttu-id="37246-108">Þegar skýrsla er bakfærð, er birgðavíddin ræstu úr framleiðslubókinni.</span><span class="sxs-lookup"><span data-stu-id="37246-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="37246-109">Því fær hann rununúmerið.</span><span class="sxs-lookup"><span data-stu-id="37246-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="37246-110">Vegna merkingar erfa sölupöntunarfærslurnar rununúmerið.</span><span class="sxs-lookup"><span data-stu-id="37246-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="37246-111">Hægt er að endurstilla víddina þegar tilkynningin sem lokið er bókfærð.</span><span class="sxs-lookup"><span data-stu-id="37246-111">The dimension can be reset when the reporting as finished is posted.</span></span>
