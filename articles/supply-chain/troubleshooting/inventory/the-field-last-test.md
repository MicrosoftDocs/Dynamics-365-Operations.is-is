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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742029"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Reiturinn „Síðasti prófunardagur“ uppfærist ekki þegar margar gæðapantanir eru stofnaðar

KB númer: 4612803

## <a name="symptoms"></a>Einkenni

Reiturinn **Síðasti prófunardagur** uppfærist ekki þegar stofnaðar eru margar gæðapantanir.

## <a name="resolution"></a>Upplausn

Kerfið hagar sér eins og það er hannað. Síðasta prófaða dagsetningin tengist ekki gæðapöntunum. Hún geymir dagsetninguna þegar lokavörurnar voru fyrst keyptar eða framleiddar. Þessi dagsetning er notuð til að reikna út ráðlagðan endingartíma.
