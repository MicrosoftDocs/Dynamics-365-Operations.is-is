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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714211"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Að afturkalla skýrslu sem er lokið býr til óvænta opna færslu

KB númer: 4612469

## <a name="symptoms"></a>Einkenni

Ef þú bakfærir skýrslu sem lokið sem er með merkingu býrð kerfið til opna færslu þar sem bakfærða magnið hefur sömu birgðastærðir og bakfærða færslan.

## <a name="resolution"></a>Upplausn

Þegar skýrsla er bakfærð, er birgðavíddin ræstu úr framleiðslubókinni. Því fær hann rununúmerið. Vegna merkingar erfa sölupöntunarfærslurnar rununúmerið.

Hægt er að endurstilla víddina þegar tilkynningin sem lokið er bókfærð.
