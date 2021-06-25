---
title: Ekki er hægt að minnka magn þegar hætt er við sölupöntun
description: Ekki er hægt að minnka magn þegar hætt er við sölupöntun.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230837"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Ekki er hægt að minnka magn þegar hætt er við sölupöntun

Villukóði SYS138831

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Ekki er hægt að draga úr magninu. Fjöldi birgðafærslna í pöntun er of lítill vegna þess að úttakspöntun eða framleiðslupöntun vísar í magnið eða hluta þess, eða vegna þess framleiðslupöntun er merkt á móti öðrum færslum.

## <a name="cause"></a>Orsök

Ef vinna tengist sölupöntun er ekki hægt að hætta við sölupöntunina fyrr en hætt er við vinnu og hún bakfærð. Þessi krafa gildir jafnvel þótt vinnan sem tengist sölupöntuninni sé lokuð.

## <a name="resolution"></a>Lausn

Til að leysa þetta vandamál skal ljúka eftirfarandi verkum:

1. Hætta við opin verk.
1. Eyðið farminum.
1. Minnka tiltekið magn.

### <a name="cancel-open-work"></a>Hætta við opin verk

Til að hætta við opið verk skal fylgja þessum skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

### <a name="delete-the-load"></a>Eyðið farminum

Til að eyða hleðslu skal fylgja eftirfarandi skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Viðeigandi sölupöntun er opnuð.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Vöruhús \> Upplýsingar um verk**.
1. Á síðunni **Vinna**, á aðgerðasvæðinu, í flipanum **Verk**, í flokknum **Verk**, skal velja **Hætta við verk**.
1. Staðfestið að reiturinn **Staða verks** sé stilltur á *Hætt við*.
1. Lokaðu síðunni **Vinna**.
1. Á síðunni upplýsingar um sölupöntun, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Vöruhús \> Upplýsingar hleðslu**.
1. Á aðgerðasvæðinu skal velja **Eyða**.
1. Veljið **Já** til að staðfesta að ætlunin sé að eyða hleðslunni.
1. Loka síðunni **Hleðsla**.

### <a name="reduce-the-picked-quantity"></a>Minnka tiltekið magn

Eftir að hætt hefur verið við alla vinnu skal fylgja þessum skrefum til að draga úr tiltektarmagninu.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Viðeigandi sölupöntun er opnuð.
1. Í flipanum **Sölupöntunarlínur** skal velja **Uppfæra línu \> Tiltekt** úr tækjastikunni.
1. Á síðunni **Tiltekt** í hlutanum **Færslur** er valin sú lína þar sem reiturinn **Staða máls** er stilltur á *Tekið til*.
1. Í hlutanum **Færslur** skal velja **Bæta við tiltektarlínu** úr tækjastikunni.
1. Í hlutanum **Tiltektarlínur** skal velja **Staðfesta tiltekt á öllu** úr tækjastikunni.
1. Lokið síðunni **Tiltekt**.
1. Á upplýsingasíðu sölupöntunar, á aðgerðasvæðinu, í flipanum **Sölupöntun**, í hópnum **Vinna með**, skal velja **Hætta við**.
1. Veljið **Já** til að staðfesta að hætta skuli við sölupöntunina.
