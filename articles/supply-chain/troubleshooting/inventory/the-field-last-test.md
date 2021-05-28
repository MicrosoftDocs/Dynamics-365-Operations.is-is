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
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Reiturinn „Síðasti prófunardagur“ uppfærist ekki þegar margar gæðapantanir eru stofnaðar

KB númer: 4612803

## <a name="symptoms"></a>Einkenni

Reiturinn **Síðasti prófunardagur** uppfærist ekki þegar stofnaðar eru margar gæðapantanir.

## <a name="resolution"></a>Upplausn

Kerfið hagar sér eins og það er hannað. Síðasta prófaða dagsetningin tengist ekki gæðapöntunum. Hún geymir dagsetninguna þegar lokavörurnar voru fyrst keyptar eða framleiddar. Þessi dagsetning er notuð til að reikna út ráðlagðan endingartíma.
