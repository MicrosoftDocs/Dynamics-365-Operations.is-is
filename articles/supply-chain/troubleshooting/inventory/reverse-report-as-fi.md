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
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Að afturkalla skýrslu sem er lokið býr til óvænta opna færslu

KB númer: 4612469

## <a name="symptoms"></a>Einkenni

Ef þú bakfærir skýrslu sem lokið sem er með merkingu býrð kerfið til opna færslu þar sem bakfærða magnið hefur sömu birgðastærðir og bakfærða færslan.

## <a name="resolution"></a>Upplausn

Þegar skýrsla er bakfærð, er birgðavíddin ræstu úr framleiðslubókinni. Því fær hann rununúmerið. Vegna merkingar erfa sölupöntunarfærslurnar rununúmerið.

Hægt er að endurstilla víddina þegar tilkynningin sem lokið er bókfærð.
