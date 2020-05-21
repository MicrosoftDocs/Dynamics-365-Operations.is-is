---
title: Áætlunargerð með neikvætt lagermagn
description: Þetta efni útskýrir hvernig neikvæður lager er meðhöndlaður þegar þú notar fínstillingu áætlunargerðar.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323509"
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

## <a name="related-resources"></a>Tengd tilföng

[Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)
