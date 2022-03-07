---
title: Ekki er kveikt á stillingunni Bóka á gjaldalykil í fjárhag
description: Þetta vandamál á sér stað þegar innkaupapöntun er reikningsfærð, ef valkosturinn „Bóka á gjaldalykil í fjárhag“ er stilltur á já í flipanum „Reikningur“ á síðunni „Færibreytur viðskiptaskulda“
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
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476680"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Ekki er kveikt á stillingunni Bóka á gjaldalykil í fjárhag

## <a name="symptoms"></a>Einkenni

Þetta vandamál á sér stað þegar innkaupapöntun er reikningsfærð, ef valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**.

## <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
1. Í flipanum **Reikningur** skal stilla valkostinn **Bóka á gjaldalykil í fjárhag** á *Já*.
1. Opnið **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**.
1. Í flipanum **Innkaupapöntun** skal ganga úr skugga um að öllum línum hafi verið eytt í útgjöldum innkaupa fyrir afurðina.
1. Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Stofna innkaupapöntun. Í reitnum **Lánardrottnalykill** skal velja *1001 Acme Skrifstofuvörur*.
1. Bætið við innpöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *D0011 Leysiprentari*
    - **Svæði:** *1*
    - **Vöruhús:** *11*
    - **Magn:** *4*

1. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerð**, skal velja **Staðfesta**.
1. Á aðgerðasvæðinu, í flipanum **Móttaka**, í flokknum **Mynda**, skal velja **Innhreyfingarskjal afurðar**.
1. Í svargluggannn **Bókun innhreyfingarskjals afurða**, í reitinn **Innhreyfingarskjal**, skal færa inn handahófskennt númer og velja síðan **Í lagi**.
1. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
1. Í reitinn **Númer** skal færa inn handahófskennt númer sem reikningsnúmerið.
1. Uppfærið samsvörunarstöðuna og bókið.
1. Takið eftir því að nú kemur upp eftirfarandi villa þegar reikningur er búinn til úr innkaupapöntun: „Númer lykils fyrir færslugerðin Útgjöld innkaupa fyrir afurð er ekki til.“

## <a name="resolution"></a>Lausn

Þetta fer eftir færibreytustillingunum fyrir reikninga og reikningaflokka. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Bókhald fyrir Útgjöld innkaupa og Afbrigði birgða](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
