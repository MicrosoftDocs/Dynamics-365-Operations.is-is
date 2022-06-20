---
title: Áætlanagerð með neikvæðu magni á lager
description: Þessi grein útskýrir hvernig neikvæð viðvörun er meðhöndluð þegar þú notar hagræðingu áætlanagerðar.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04006bb12142be69c84bc8085dd82fc99280e90b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856136"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Áætlunargerð með neikvætt lagermagn

[!include [banner](../../includes/banner.md)]

Ef kerfið sýnir neikvætt samanlagt birgðamagn, meðhöndlar áætlunarvélin magnið sem 0 (núll) til að koma í veg fyrir offramboð. Svona virkar þessi virkni:

1. Fínstilling áætlunargerðar safnar saman lagermagninu á lægsta stigi þekjuvídda. (Til dæmis ef *staðsetning* er ekki þekjuvídd safnar fínstilling áætlanagerðar saman lagermagni á stigi *vöruhúss*.)
1. Ef samanlagt lagermagn á lægsta stigi þekjuvídda er neikvætt, gerir kerfið ráð fyrir að lagermagnið sé í raun 0 (núll).

> [!IMPORTANT]
> Áætlunarkerfið getur aðeins verið eins nákvæmt og inntaksgögnin. Ef inntaksgögnin eru ónákvæm, munu neikvæðar lagerfærslur gefa til kynna að birgðagögnin í Microsoft Dynamics 365 Supply Chain Management eru ekki samstillt við hinn raunverulega heim. Þess vegna verður niðurstaða áætlunargerðar gölluð. Til að fá nákvæma niðurstöðu áætlanagerðar ættir þú að lágmarka fjölda skráa sem sýna neikvætt lagermagn.

## <a name="example-1"></a>Dæmi 1

Vöruhús 13 er stillt á eftirfarandi hátt:

- **Þekjukóði:** Lágm./Hám.
- **Lágmark:** 15 stykki (stk.)
- **Hámark:** 25 stk.

Lægsta stig umfjöllunar er *vöruhús* og eftirfarandi lagermagn er skráð á stig *staðsetningar*:

- **Vefsvæði 1, vöruhús 13, staðsetning 1:** 20 stk.
- **Vefsvæði 1, vöruhús 13, staðsetning 2:** &minus;8 stk.

Þess vegna er samanlagt magn á hendi fyrir vöruhús 13 12 stk. (= 20 stk. &minus; 8 stk.).

Í þessu tilfelli notar áætlunarvélin samanlagt lagermagn 12 stk. fyrir vöruhús 13.

Niðurstaðan er áætluð röð 13 stk. (= 25 stk. &minus; 12 stk.) til að fylla á vöruhús 13 frá 12 stk. í 25 stk.

## <a name="example-2"></a>Dæmi 2

Vöruhús 13 er stillt á eftirfarandi hátt:

- **Þekjukóði:** Lágm./Hám.
- **Lágmark:** 15 stk.
- **Hámark:** 25 stk.

Lægsta stig umfjöllunar er *vöruhús* og eftirfarandi lagermagn er skráð á stig *staðsetningar*:

- **Vefsvæði 1, vöruhús 13, staðsetning 1:** 4 stk.
- **Vefsvæði 1, vöruhús 13, staðsetning 2:** &minus;8 stk.

Þess vegna er samanlagt magn á hendi fyrir vöruhús 13 &minus;4 stk. (= 4 stk. &minus; 8 stk.). Með öðrum orðum, minna en 0 (núll).

Í þessu tilfelli gerir áætlunarvélin ráð fyrir að lagermagn fyrir vöruhús 13 sé 0 stk. í staðinn fyrir &minus;4 stk.

Niðurstaðan er áætluð röð 25 stk. (= 25 stk. &minus; 0 stk.) til að fylla á vöruhús 13 frá 0 stk. í 25 stk.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Skipulagning þegar gerð er frátekning á neikvæðum lagerbirgðum

Ef þú breytir birgðum meðan efnislegar frátekningar eru til geturðu búið til aðstæður þar sem pöntun er efnislega frátekin í neikvæðri birgðastöðu. Í þessu tilviki, vegna þess að efnisleg frátekt er til staðar, þarftu að hafa framboð til að standa undir fráteknu magni. Þess vegna er áfyllingar krafist, þannig að kerfið mun annaðhvort búa til áætlaða pöntun til að fylla á magnið sem ekki var hægt að dekka af fyrirliggjandi lagerbirgðum eða hylja það með fyrirliggjandi pöntun fyrir vöruna.

Eftirfarandi dæmi lýsir þessum aðstæðum.

### <a name="example"></a>Dæmi

Kerfið er stillt með eftirfarandi hætti:

- Vara *FG* er til og er með *10* stk. í lagerbirgðum.
- Afurðarafbrigðið býður upp á neikvæða efnislega birgðastöðu.
- Sölupöntun er til fyrir magn upp á *10* stk. vöru *FG*.
- Sölupöntunarmagnið er tekið frá úr fyrirliggjandi birgðum.

Þú stillir síðan magn vörunnar *FG* þannig að birgðastaðan verður 5. Vegna þess að birgðastaða vörunnar er 5, er sölupöntunarmagnið nú frátekið á móti magni sem er ekki tiltækt á lager (það væri svipað ef á lager væri 0, í því tilviki væri sölupöntunin frátekin gegn neikvæðum birgðum ). Ef þú keyrir aðalskipulagningu núna, áætlað pöntun magn 5 fyrir *FG* verður stofnað til að útvega sölupöntunina, vegna þess að áætlanagerð fínstilling mun alltaf nota núverandi framboð eða búa til nýja áætlaða pöntun til að útvega efnislega frátekninguna.

## <a name="related-resources"></a>Tengd tilföng

- [Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)
- [Hafist handa með fínstillingu áætlanagerðar](get-started.md)
- [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)
- [Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)
- [Hætta við áætlunarvinnslu](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
