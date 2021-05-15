---
title: Áfram er lokað á vinnu
description: Áfram er lokað á vinnu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924131"
---
# <a name="work-remains-blocked"></a>Áfram er lokað á vinnu

Villukóði: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Vinna %1 er áfram útilokuð vegna þess að tengd bylgja %2 er með stöðuna %3.

## <a name="cause"></a>Orsök

Vinnan er í bylgjuvinnslu og ekki er hægt að opna hana, eins og tilgreint er með einu af eftirfarandi skilyrðum:

- Á flipanum **Ástæður lokana** er reiturinn **Ástæða fyrir vinnulokun** fyrir eina eða fleiri línur stilltur á *Bylgjuvinnsla*.
- Þegar þú velur **Bylgja** í flokknum **Tengdar upplýsingar** á flipanum **Tengdar upplýsingar** í aðgerðasvæðinu er **Staða bylgju** stillt á *Vinnsla*.

## <a name="resolution"></a>Upplausn

Á aðgerðasvæðinu, í flipanum **Tengdar upplýsingar**, í flokknum **Tengdar upplýsingar**, skal velja **Bylgja**. Á síðunni **Bylgjur**, á aðgerðasvæðinu, á flipanum **Bylgja** í **Bylgja** hópnum skal síðan velja **Hreinsa bylgjugögn**.

## <a name="workaround"></a>Hjáleið

Ef fyrri skrefin leystu ekki úr vandanum er hægt að hætta við verkið með því að fylgja þessum skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).
