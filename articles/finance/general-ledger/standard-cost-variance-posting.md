---
title: Bókun hefðbundins kostnaðarfráviks
description: Þetta efnisatriði veitir upplýsingar um uppsetningu bókunarsniða fyrir staðlaða kostnað.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804641"
---
# <a name="standard-cost-variance-posting"></a>Bókun hefðbundins kostnaðarfráviks

Þegar þú notar staðalkostnað fyrir eina eða fleiri vörur í fyrirtækinu þínu verður þú að stilla [forsendur staðalkostnaðar](/supply-chain/cost-management/prerequisites-standard-costs.md). Þetta efnisatriði útskýrir bókunarlyklana sem eru nauðsynlegir fyrir skref 3 í forsendunum, "Úthluta fjárhagslyklum á vörubókanir sem tengjast stöðluðum kostnaðarfrávikum."

Mismunandi gerðir af frávikum geta komið fram fyrir innkaup og framleiðslupantanir. Fyrir dæmi um framleiðslufrávik, sjá [Algengar uppsprettur framleiðslufrávika](/supply-chain/cost-management/common-sources-of-production-variances.md). Verðfrávik innkaupapöntunar eiga sér stað þegar þú notar staðalkostnað fyrir keypta vöru og það er munur á staðalkostnaði vörunnar og reikningsfærðu upphæðinni á innkaupapöntuninni.

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið

Eftirfarandi tafla sýnir dæmi um sjálfgefnar færslugerðir. Það inniheldur sýnishorn af aðalreikningum og lýsingum.

- "Debet/kredit?" Dálkurinn sýnir hvort viðskiptin eru venjulega debet eða kredit. Í sumum tilfellum getur færslan bókað annað hvort skuldfærslur eða inneignir.
- Dálkurinn „Jöfnunarreikningur“ gefur til kynna að bókunartegundin sé jöfnunarreikningur. Með öðrum orðum, upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslunnar. "P" táknar líkamlega bókun og "F" táknar fjárhagslega bókun.
- Dálkurinn „Fylgjast með“ gefur til kynna hvort aðalreikningur bókunartegundarinnar sé venjulega sá sami og aðalreikningur annarrar bókunartegundar. Nánar tiltekið gefur það til kynna færslugerðina sem venjulega er notuð.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga í töflunni eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Frávik innkaupaverðs | 510310 | Frávik innkaupaverðs | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar frávik er á milli innkaupaverðs og staðalkostnaðar á innkaupapöntun. |
| Endurmat birgðakostnaðar | 510330 | Endurmat birgðakostnaðar | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar ný kostnaðarútgáfa er virkjuð fyrir staðlaðan kostnaðarlið til að endurmeta á lager. |
| Frávik kostnaðarbreytinga | 510320 | Frávik kostnaðarbreytinga | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar munur er á staðalkostnaði milli vefsvæða, eða þegar vöru er skilað og það er breyting á milli upphaflegs staðalkostnaðar og núverandi staðalkostnaðar fyrir vöru. |
| Framleiðsla lotustærðarfrávika | 510370 | Framleiðsla lotustærðarfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar munur er á útreikningsgrunni efnisskrár (BOM) og raunverulegu magni fyrir útreikning framleiðslupöntunarkostnaðar. |
| Frávik framleiðsluverða | 510340 | Frávik framleiðsluverða | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar verðmunur er á áætluðum kostnaði og raunkostnaði fyrir framleiðslupöntun. |
| Framleiðsla magnfrávika | 510350 | Framleiðsla magnfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar það er magnmunur á áætluðum kostnaði og raunkostnaði fyrir framleiðslupöntun. |
| Framleiðsla staðgengilsfrávika | 510360 | Framleiðsla staðgengilsfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar það er óvænt notkun á framleiðslupöntun. |
| Sléttunarfrávik | 618160 | Sléttunarmismunur | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar það er námundunarmunur þegar framleiðslukostnaður er reiknaður út frá staðalkostnaði. |
