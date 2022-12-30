---
title: Áætlanagerð með neikvæðu magni á lager
description: Þessi grein útskýrir hvernig neikvæðar birgðir eru meðhöndlaðar.
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
ms.openlocfilehash: b4fc8b37fd800e3b4652513f150f9806bf1d5d67
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741123"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Áætlanagerð með neikvæðu magni á lager

[!include [banner](../../includes/banner.md)]

Ef kerfið sýnir neikvætt samanlagt birgðamagn, meðhöndlar áætlunarvélin magnið sem 0 (núll) til að koma í veg fyrir offramboð. Svona virkar þessi virkni:

1. Aðalskipulag safnar saman magni í byrgðum á lægsta stigi þekju. (Til dæmis, ef *staðsetning* er ekki þekjuvídd, tekur fínstilling áætlanagerðar saman magn á lager á stigi *vöruhússins*.)
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

Ef þú breytir birgðum meðan efnislegar frátekningar eru til geturðu búið til aðstæður þar sem pöntun er efnislega frátekin í neikvæðri birgðastöðu. Í þessu tilviki, vegna þess að bókun er til staðar, þarftu að hafa birgðir til að standa undir fráteknu magni. Þar af leiðandi er áfylling nauðsynleg þannig að kerfið muni annaðhvort stofna áætlaða pöntun til að fylla á magnið sem ekki var hægt að ná yfir með fyrirliggjandi lagerbirgðum eða ná yfir það með fyrirliggjandi pöntun fyrir vöruna.

Eftirfarandi dæmi lýsir þessum aðstæðum.

### <a name="example"></a>Dæmi

Kerfið er stillt með eftirfarandi hætti:

- Vara *FG* er til og er með *10* stk. í lagerbirgðum.
- Afurðarafbrigðið býður upp á neikvæða efnislega birgðastöðu.
- Sölupöntun er til fyrir magn upp á *10* stk. vöru *FG*.
- Sölupöntunarmagnið er tekið frá úr fyrirliggjandi birgðum.

Þú stillir síðan magn vörunnar *FG* þannig að lagerbirgðirnar verði 5. Þar sem vörur í birgðum eru 5 er sölupöntunarmagnið nú frátekið miðað við magn sem er ekki tiltækt á vörum (það væri svipað ef vörubirgðir væru 0, í þeim tilvikum væri sölupöntunin frátekin miðað við neikvæðar birgðir). Ef þú keyrir aðaláætlanagerð núna verður áætluð pöntun upp á 5 í magni fyrir *FG* stofnuð til að anna sölupöntuninni því að aðaláætlanagerð mun alltaf nota fyrirliggjandi eftirspurn eða stofna áætlaða pöntun til að anna efnislegri frátekningu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
