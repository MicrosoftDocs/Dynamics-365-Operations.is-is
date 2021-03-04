---
title: Úthluta lífferilsstaða afurðar til útgefins afurðasniðmáts
description: Þetta ferli sýnir hvernig á að úthluta lífferilsstöðu afurðar á útgefið afurðasniðmát og afbrigði þess.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430186"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Úthluta lífferilsstaða afurðar til útgefins afurðasniðmáts

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að úthluta lífferilsstöðu afurðar á útgefið afurðasniðmát og afbrigði þess. Forkröfur: Spila þarf verkefnaleiðbeiningarnar „Búa til nýja lífferlisstöðu vöru“ fyrst til að ganga úr skugga um að a.m.k. ein lífferlisstaða afurðar sé stofuað áður en hægt er að spila þessar verkefnaleiðbeiningar.


## <a name="find-a-released-product-master"></a>Finna útgefið afurðarsniðmát
1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

> [!NOTE]
> Afurðarsniðmát er með Undirgerð afurðar afurðarsniðmát.  

## <a name="update-the-lifecycle-state"></a>Uppfæra lífferilsstöðu
1. Smellið á „Breyta“.
2. Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.
3. Smellið á „Vista“.
4. Smella á Já.

> [!NOTE]
> Ef Já er valið eru allar tengd útgefin afurðarafbrigði sem hafa sömu upphaflegu stöðu og valin útgefin afurðarsniðmát einnig uppfærð í nýja lífferlisstöðu afurðar. Ef Nei er valið halda öll afbrigði raunástandi sínu. Afbrigði sem hafa mismunandi lífferlisstöðu afurðar frá útgefnu afurðarsniðmáti eru ekki uppfærð.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Staðfestu lífferilsstöðu afurðarafbrigða
1. Smella á Útgefin afurðarafbrigði.

> [!NOTE]
> Athugið að öll afbrigði hafa erft valda lífferlisstöðu úr útgefnu afurðarsniðmáti.  

2. Í listanum skal merkja valda línu.
3. Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]