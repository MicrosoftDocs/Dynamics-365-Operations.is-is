---
title: Innkaupapantanir endurspegla ekki tungumálastillingar lögaðilans
description: Afurðarheitið á innkaupapöntun er sýnt á tungumáli kerfisins í staðinn fyrir tungumálið sem er stillt fyrir lögaðilann þar sem innkaupapöntunin var búin til
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476649"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Innkaupapantanir endurspegla ekki tungumálastillingar lögaðilans


## <a name="symptoms"></a>Einkenni

Afurðarheitið á innkaupapöntun er sýnt á tungumáli kerfisins í staðinn fyrir tungumálið sem er stillt fyrir lögaðilann þar sem innkaupapöntunin var búin til.

## <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Stillið kerfistungumálið á *EN-US* (bandaríska ensku).
1. Gangið úr skugga um að það sé til afurð þar sem tungumálin *EN-US* og *DE* (þýska) eru notuð fyrir þýðingar á afurðarheiti.
1. Breytið tungumáli fyrir lögaðila í *DE*.
1. Í lögaðilanum þar sem *DE* er stillt sem tungumál skal stofna innkaupapöntun sem inniheldur afurðina.
1. Takið eftir því að afurðarheitið er enn sýnt á bandarískri ensku (kerfistungumálinu).

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Í innkaupapöntunum er afurðin alltaf sýnd á tungumáli kerfisins. Tungumál innkaupapantana er notað þegar staðfestingarbók er stofnuð.
