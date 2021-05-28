---
title: Rununúmer er hreinsað við val á nýju lotukenni
description: Þegar vallína dagbókar er skoðuð er gildið í svæðinu Lotunúmer hreinsað ef nýtt gildi er valið í svæðinu Lotunúmer.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026594"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="59853-103">Rununúmer er hreinsað við val á nýju lotukenni</span><span class="sxs-lookup"><span data-stu-id="59853-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="59853-104">KB númer: 4613107</span><span class="sxs-lookup"><span data-stu-id="59853-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="59853-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="59853-105">Symptoms</span></span>

<span data-ttu-id="59853-106">Þegar vallína dagbókar er skoðuð er gildið í svæðinu **Lotunúmer** hreinsað ef nýtt gildi er valið í svæðinu **Lotunúmer**.</span><span class="sxs-lookup"><span data-stu-id="59853-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="59853-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="59853-107">Resolution</span></span>

<span data-ttu-id="59853-108">Kerfið hagar sér eins og það er hannað.</span><span class="sxs-lookup"><span data-stu-id="59853-108">The system is behaving as designed.</span></span> <span data-ttu-id="59853-109">Ef auðkenni lotukennis er breytt breytist samhengi hlutarins.</span><span class="sxs-lookup"><span data-stu-id="59853-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="59853-110">Því er rununúmerið endurstillt.</span><span class="sxs-lookup"><span data-stu-id="59853-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="59853-111">Til að tengja lotunúmerið við lotukenni verður fyrst að stilla lotukennið.</span><span class="sxs-lookup"><span data-stu-id="59853-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
