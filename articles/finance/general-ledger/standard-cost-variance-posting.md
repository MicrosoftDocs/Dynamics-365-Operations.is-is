---
title: Bókun á stöðluðu kostnaðarfráviki
description: Þessi grein veitir upplýsingar um uppsetningu á bókunarsniðum fyrir staðalkostnað.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894878"
---
# <a name="standard-cost-variance-posting"></a>Bókun á stöðluðu kostnaðarfráviki

Þegar staðalkostnaður er notaður fyrir eina eða fleiri afurðir í fyrirtækinu þarf að skilgreina [skilyrði fyrir staðalkostnað](/supply-chain/cost-management/prerequisites-standard-costs.md). Þessi grein útskýrir bókunarlyklana sem þarf fyrir skref 3 fyrir skilyrði, „Úthluta fjárhagslyklum á vörubókanir sem tengjast frávikum staðalkostnaðar.“

Mismunandi tegundir frávika geta átt sér stað fyrir innkaup og framleiðslupantanir. Dæmi um framleiðslufrávik er að finna í [Algengar ástæður framleiðslufrávika](/supply-chain/cost-management/common-sources-of-production-variances.md). Verðfrávik innkaupapöntunar gerast þegar staðalkostnaður er notaður fyrir keypta vöru og munur er á milli staðalkostnaði afurðar og reikningsfærðrar upphæðar í innkaupapöntuninni.

## <a name="sample-posting-profile-configuration"></a>Skilgreining prófunarbókunarreglu

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir. Þar er að finna sýnishorn af aðallyklum og lýsingar.

- „Debet/kredit?“ dálkur segir til um hvort færslan sé yfirleitt debet eða kredit. Í sumum tilvikum getur færslan bókað annaðhvort debet eða kredit.
- Dálkurinn „Millireikningur“ gefur til kynna að bókunargerðin sé millireikningur. Þ.e. upphæðin sem er bókuð á þennan lykil er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslu. „P“ stendur fyrir bókun og „F“ stendur fyrir fjárhagslega bókun.
- Dálkurinn „Fylgja“ gefur til kynna hvort aðallykillinn fyrir bókunargerðina sé yfirleitt sá sami og aðallykillinn fyrir aðra bókunargerð. Nánar tiltekið gefur hann til kynna bókunargerðina sem yfirleitt er notuð.

> [!NOTE]
> Aðallyklarnir og heiti aðallykla í töflunni eru tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Frávik innkaupaverðs | 510310 | Frávik innkaupaverðs | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi lykill er notaður þegar frávik er á milli innkaupsverðs og staðalkostnaðar og innkaupapöntunar. |
| Endurmat birgðakostnaðar | 510330 | Endurmat birgðakostnaðar | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar ný kostnaðarútgáfa er virkjuð fyrir staðlaðan kostnaðarlið til að endurmeta vörubirgðirnar. |
| Frávik kostnaðarbreytinga | 510320 | Frávik kostnaðarbreytinga | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi lykill er notaður þegar mismunur er á staðalkostnaði milli svæða eða þegar vöru er skilað og breyting er á upprunalegum staðalkostnaði og núverandi staðalkostnaði fyrir vöru. |
| Framleiðsla lotustærðarfrávika | 510370 | Framleiðsla lotustærðarfrávika | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi lykill er notaður þegar munur er á milli útreikningsgrunns uppskriftir og raunverulegu magni fyrir kostnaðarútreikning framleiðslupöntunar. |
| Frávik framleiðsluverða | 510340 | Frávik framleiðsluverða | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar verðmunur er á áætluðum kostnaði og raunverulegum kostnaði fyrir framleiðslupöntun. |
| Framleiðsla magnfrávika | 510350 | Framleiðsla magnfrávika | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar magnmunur er á áætluðum kostnaði og raunkostnaði við framleiðslupöntun. |
| Framleiðsla staðgengilsfrávika | 510360 | Framleiðsla staðgengilsfrávika | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar óvænt neysla á sér stað á framleiðslupöntun. |
| Sléttunarfrávik | 618160 | Sléttunarmismunur | Kostnaður | Annaðhvort | Nr. | F | Á ekki við | Þessi lykill er notaður þegar sléttunarmunur er til staðar þegar framleiðslukostnaður er reiknaður út frá staðalkostnaði. |
