---
title: Magn er ekki gilt þegar pantanir á innleið eru skráðar
description: 'Ef magnið sem er úthlutað fyrir númeraplötu er meira en magnið sem þarf að taka á móti færðu villuna: „Magnið er ekki gilt.“'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476700"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Magn númeraplötu er ekki gilt þegar pantanir á innleið eru skráðar

## <a name="symptoms"></a>Einkenni

Þegar pantanir á innleið eru skráðar gætir þú fengið eftirfarandi villuboð:

> Magnið er ekki gilt.

Ef reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda* fyrir valmyndaratriði fartækis sem er notað til að skrá pantanir á innleið, kemur upp þessi villa og ekki verður hægt að ljúka skráningunni.

## <a name="cause"></a>Orsök

Þegar *Skilgreint af notanda* er notað sem regla um flokkun númeraplötu, skiptir kerfið væntanlegum birgðum niður á aðskildar númeraplötur eins og röðunarflokkur einingar gefur til kynna. Ef runu- og raðnúmer eru notuð til að rekja vöruna sem tekið er á móti þarf að tilgreina magn hverrar runu eða raðnúmers fyrir hverja númeraplötu sem er skráð. Ef magnið sem er tilgreint fyrir númeraplötu er umfram magnið sem þarf enn að taka á móti fyrir núverandi víddir, koma upp þessi villuboð.

## <a name="resolution"></a>Lausn

Þegar vara er skráð með því að nota valmyndaratriði fartækis þar sem reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda*, gæti kerfið gert kröfu um að númeraplötunúmer, rununúmer eða raðnúmer verði staðfest eða slegin inn.

Á staðfestingarsíðu númeraplötu sýnir kerfið magnið sem er úthlutað fyrir núverandi númeraplötu. Á staðfestingarsíðum rununúmers og raðnúmers sýnir kerfið magnið sem þarf enn að taka á móti á núverandi númeraplötu. Þar verður einnig reitur þar sem hægt er að slá inn magnið til að skrá fyrir þá samsetningu af númeraplötu og runu- eða raðnúmeri. Í þessu tilfelli skal ganga úr skugga um magnið sem verið er að skrá fyrir númeraplötuna fari ekki umfram magnið sem þarf enn að taka á móti.

Ef verið er að búa til of margar númeraplötur við skráningu á pöntun á innleið verður hægt að breyta gildinu í reitnum **Regla um flokkun númeraplötu** í *Flokkun númeraplötu*, hægt verður að úthluta nýjum röðunarflokki einingar á vöruna eða hægt verður að gera valkostinn **Flokkun númeraplötu** fyrir röðunarflokk einingar óvirkan.
