---
title: Bókun hefðbundins kostnaðarfráviks
description: Þessi grein veitir upplýsingar um að setja upp færslusnið fyrir staðlaða kostnaðarkostnað.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894878"
---
# <a name="standard-cost-variance-posting"></a>Bókun hefðbundins kostnaðarfráviks

Þegar þú notar staðalkostnað fyrir eina eða fleiri vörur í fyrirtækinu þínu verður þú að stilla [forsendur staðalkostnaðar](/supply-chain/cost-management/prerequisites-standard-costs.md). Þessi grein útskýrir bókunarlyklana sem eru nauðsynlegir fyrir skref 3 í forsendunum, "Úthluta fjárhagslyklum á vörubókanir sem tengjast stöðluðum kostnaðarfrávikum."

Mismunandi gerðir af frávikum geta komið fram fyrir innkaup og framleiðslupantanir. Fyrir dæmi um framleiðslufrávik, sjá [Algengar uppsprettur framleiðslufrávika](/supply-chain/cost-management/common-sources-of-production-variances.md). Verðfrávik innkaupapöntunar eiga sér stað þegar þú notar staðalkostnað fyrir keypta vöru og það er munur á staðalkostnaði vörunnar og reikningsfærðu upphæðinni á innkaupapöntuninni.

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið

Eftirfarandi tafla sýnir dæmi um sjálfgefnar færslugerðir. Það inniheldur sýnishorn af aðalreikningum og lýsingum.

- "Debet/kredit?" Dálkurinn sýnir hvort viðskiptin eru venjulega debet eða kredit. Í sumum tilfellum getur færslan bókað annað hvort skuldfærslur eða inneignir.
- Dálkurinn „Jöfnunarreikningur“ gefur til kynna að bókunartegundin sé jöfnunarreikningur. Með öðrum orðum, upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslunnar. "P" táknar líkamlega bókun og "F" táknar fjárhagslega bókun.
- Dálkurinn „Fylgjast með“ gefur til kynna hvort aðalreikningur bókunartegundarinnar sé venjulega sá sami og aðalreikningur annarrar bókunartegundar. Nánar tiltekið gefur það til kynna færslugerðina sem venjulega er notuð.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga í töflunni eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir fyrirtækisþarfir þínar.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Frávik innkaupaverðs | 510310 | Frávik innkaupaverðs | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar frávik er á milli innkaupaverðs og staðalkostnaðar á innkaupapöntun. |
| Endurmat birgðakostnaðar | 510330 | Endurmat birgðakostnaðar | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar ný kostnaðarútgáfa er virkjuð fyrir staðlaðan kostnaðarlið til að endurmeta á lager. |
| Frávik kostnaðarbreytinga | 510320 | Frávik kostnaðarbreytinga | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar munur er á staðalkostnaði milli vefsvæða, eða þegar vöru er skilað og það er breyting á milli upphaflegs staðalkostnaðar og núverandi staðalkostnaðar fyrir vöru. |
| Framleiðsla lotustærðarfrávika | 510370 | Framleiðsla lotustærðarfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar munur er á útreikningsgrunni efnisskrár (BOM) og raunverulegu magni fyrir útreikning framleiðslupöntunarkostnaðar. |
| Frávik framleiðsluverða | 510340 | Frávik framleiðsluverða | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar verðmunur er á áætluðum kostnaði og raunkostnaði fyrir framleiðslupöntun. |
| Framleiðsla magnfrávika | 510350 | Framleiðsla magnfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar það er magnmunur á áætluðum kostnaði og raunkostnaði fyrir framleiðslupöntun. |
| Framleiðsla staðgengilsfrávika | 510360 | Framleiðsla staðgengilsfrávika | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar það er óvænt notkun á framleiðslupöntun. |
| Sléttunarfrávik | 618160 | Sléttunarmismunur | Kostnaður | Annað hvort | Nr. | F | Á ekki við | Þessi reikningur er notaður þegar námundunarmunur er þegar framleiðslukostnaður er reiknaður út frá staðalkostnaði. |
