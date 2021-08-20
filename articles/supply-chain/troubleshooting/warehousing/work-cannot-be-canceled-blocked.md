---
title: Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð
description: Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722200"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Ekki er hægt að hætta við vinnu vegna þess að hún er lokuð

Villukóði: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Ekki er hægt að hætta við vinnu %1 vegna þess að ástæða af gerðinni %2 hefur lokað á hana. Opna verður vinnuna áður en hægt er að hætta við hana.

## <a name="cause"></a>Orsök

Verkið er lokað og ekki er hægt að hætta við.

Á síðunni **Vinna**, á flipanum **Almennt**, er valkosturinn **Lokað** stilltur á *Já*. Þessi stilling gefur til kynna að vinnan sé lokuð. Flipinn **Ástæður lokunar** sýnir ástæðu þess að lokað var á vinnuna.

## <a name="resolution"></a>Upplausn

Til að opna fyrir vinnuna skal velja flipann **Lokunarástæður** og fylgja svo einu af eftirfarandi skrefum:

- Ef reiturinn **Ástæða fyrir vinnulokun** er stilltur á *Óskilgreind ástæða*: Á aðgerðasvæðinu, í flipanum **Vinna**, í flokknum **Vinna**, skal velja **Opna fyrir verk**.
- Ef reiturinn **Ástæða fyrir vinnulokun** er stilltur á *Bylgjuvinnsla*: Á aðgerðasvæðinu, í flipanum **Tengdar upplýsingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgja**. Á síðunni **Bylgjur**, á aðgerðasvæðinu, á flipanum **Bylgja** í **Bylgja** hópnum skal síðan velja **Hreinsa bylgjugögn**.

## <a name="workaround"></a>Hjáleið

Ef fyrri skrefin leystu ekki úr vandanum er hægt að hætta við verkið með því að fylgja þessum skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).
