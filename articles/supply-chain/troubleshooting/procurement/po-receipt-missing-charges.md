---
title: Kvittun innkaupapöntunar inniheldur ekki öll gjöld
description: Kvittun innkaupapöntunar inniheldur ekki öll gjöld
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476618"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Kvittun innkaupapöntunar inniheldur ekki öll gjöld

## <a name="symptoms"></a>Einkenni

Þegar innkaupapöntun er móttekin eru ekki öll gjöld innifalin í kvittuninni.

### <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Á síðunni **Færibreytur innkaupa og aðfanga**, í flipanum **Afhending**, skal ganga úr skugga um valkosturinn **Mynda gjöld á innhreyfingarskjali afurða** sé stilltur á *Já*.
1. Stofna innkaupapöntun sem inniheldur gjöld.
1. Staðfesta innkaupapöntun.
1. Takið á móti innkaupapöntuninni.
1. Skoðið samtölu kvittunarinnar og berið hana saman við samtöluna sem búist var við.
1. Takið eftir að ekki öll gjöld eru tekin með í kvittun innkaupapöntunar.

## <a name="resolution"></a>Lausn

Úrlausnin fer eftir því hvernig þessi ýmsu gjöld hafa verið sett upp. Upplýsingar um hvernig á að setja upp ýmis gjöld til að uppfylla kröfur, er að finna í eftirfarandi bloggfærslu: [Bóka gjöld við móttöku afurðar](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
