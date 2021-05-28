---
title: Reiturinn „Síðasti prófunardagur“ uppfærist ekki þegar margar gæðapantanir eru stofnaðar
description: Reiturinn „Síðasti prófunardagur“ uppfærist ekki þegar stofnaðar eru margar gæðapantanir.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026620"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="c09f6-103">Reiturinn „Síðasti prófunardagur“ uppfærist ekki þegar margar gæðapantanir eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="c09f6-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="c09f6-104">KB númer: 4612803</span><span class="sxs-lookup"><span data-stu-id="c09f6-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="c09f6-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="c09f6-105">Symptoms</span></span>

<span data-ttu-id="c09f6-106">Reiturinn **Síðasti prófunardagur** uppfærist ekki þegar stofnaðar eru margar gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="c09f6-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="c09f6-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="c09f6-107">Resolution</span></span>

<span data-ttu-id="c09f6-108">Kerfið hagar sér eins og það er hannað.</span><span class="sxs-lookup"><span data-stu-id="c09f6-108">The system is behaving as designed.</span></span> <span data-ttu-id="c09f6-109">Síðasta prófaða dagsetningin tengist ekki gæðapöntunum.</span><span class="sxs-lookup"><span data-stu-id="c09f6-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="c09f6-110">Hún geymir dagsetninguna þegar lokavörurnar voru fyrst keyptar eða framleiddar.</span><span class="sxs-lookup"><span data-stu-id="c09f6-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="c09f6-111">Þessi dagsetning er notuð til að reikna út ráðlagðan endingartíma.</span><span class="sxs-lookup"><span data-stu-id="c09f6-111">This date is used to calculate the shelf life advice date.</span></span>
