---
title: Lagerbirgðir eru ekki taldar með fyrir runu fyrir ofan vörur
description: Sum hólfasniðmát taka ekki tillit til fyrirliggjandi lagerbirgða fyrir runu fyrir ofan vörur. Runu- eða raðnúmer þarf að tilgreina í eftirspurnarpöntuninni.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476660"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Hólfasniðmát taka ekki tillit til lagerbirgða fyrir runu fyrir ofan vörur

## <a name="symptoms"></a>Einkenni

Hólfasniðmát sem eru með hólfaskilyrðið *Íhuga magn í birgðum* taka ekki til greina núverandi lagerbirgðir fyrir *runu fyrir ofan* vörur. Þau taka þær aðeins til greina ef rununúmerið er tilgreint í sölupöntunarlínunni.

En þegar notuð er *runa fyrir ofan* vörur verða núverandi lagerbirgðir teknar til greina eins og vænta má.

Frekari upplýsingar er að finna í [Hólfaskipting vöruhúss](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Lausn

Hægt er að skilgreina haus hólfasniðmáts fyrir eftirspurnarleiðina *Pantað*, *Frátekið* eða *Losað*. Fyrir eftirspurnarleiðina *Pantað* eiga sömu kröfur um frátekningastigveldi við og gilda um frátekningu eða losun í vöruhúsaferli. Þar af leiðandi, fyrir vörur sem eru með *runa fyrir ofan* og *raðnúmer fyrir neðan* frátekningastigveldi, þarf að tilgreina runu eða raðnúmer í eftirspurnarpöntuninni (sölu eða flutning).

Annars er hægt að nota eftirspurnarleiðina *Frátekið* til að velja runu eða raðnúmer áður en eftirspurn eftir hólfaskiptingu í vöruhúsi er búin til.
