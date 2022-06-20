---
title: Skoða áætlunarsögu og skipulagsskrár
description: Þessi grein útskýrir hvernig á að skoða feril áætlanagerðarverka sem eru ræst af aðgerðinni áætlanagerð fínstillingu.
author: t-benebo
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b2c9257fc67a06b57418b2f5b035b2b540131405
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863941"
---
# <a name="view-plan-history-and-planning-logs"></a>Skoða áætlunarsögu og skipulagsskrár

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að skoða feril áætlanagerðaverka sem eru ræst af virkni skipulagsfínstillingar í Microsoft Dynamics 365 Supply Chain Management.

Til að skoða sögu fyrir áætlun, opnaðu áætlunina með því að fara til **Aðaláætlunargerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir** og velja **Saga**. Í sögunni eru allar vinnslur fyrir valda áætlun. Listinn nær yfir loknar og virkar vinnslur.

Kerfið geymir að hámarki 60 söguskrár í hverju aðalskipulagi og eyðir færslum eldri en 30 daga. Í hvert skipti sem þú keyrir nýjan aðalskipulagsútreikning bætir kerfið við nýrri söguskrá og hreinsar síðan upp elstu færslurnar eftir þörfum.

Auk þess að sjá upphafstíma og stöðu á vinnslum geturðu skoðað kladda fyrir tiltekna vinnslu. Í kladdanum eru viðbótarupplýsingar og viðvaranir. Ekki eru allar vinnslur með kladda. Til að skoða kladda fyrir vinnslu velurðu **Kladdi**. Kladdafærslur eru aðeins geymdar í 30 daga frá deginum sem verkið klárast og er eytt sjálfkrafa eftir það.

Ef valkosturinn **Runuvinnsla** í flýtiflipanum **Keyra í bakgrunni** var virkjaður þegar vinnsla aðaláætlanagerðar var sett upp, sýnir kladdi runuvinnslu frekari upplýsingar um viðvaranir og villur sem komu upp í keyrslu aðaláætlanagerðar. Til dæmis eru villur sjálfvirkrar staðfestingar aðeins fangaðar í runuvinnslukladdanum. Þær eru ekki sýndar í klöddum á síðunni **Ferill**.

Til að skoða villur sjálfvirkrar staðfestingar og aðrar viðvaranir eða villur sem komu upp í keyrslu aðaláætlanagerðar skal fylgja þessum skrefum.

1. Farðu í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur**.
1. Finndu og veldu færsluna sem stendur fyrir keyrslu aðaláætlanagerðar sem þú hefur áhuga á. (Til dæmis gæti gildi reitsins **Lýsing vinnslu** byrjað á *Aðaláætlanagerð*.)
1. Fylgdu einu af þessum skrefum, eftir því hvort þú ert að nota *endurbætta skjámynd* eða *eldri (óendurbætta) skjámynd* fyrir síðuna **Runuvinnslur**:

    - Ef þú ert að nota endurbættu skjámyndina: Veldu **Runuvinnsluferil** á aðgerðasvæðinu. Því næst, á síðunni **Runuvinnsluferill**, skal velja **Kladdi** á aðgerðasvæðinu.
    - Ef þú notar eldri skjámynd: Á aðgerðasvæðinu, í flipanum **Runuvinnsla**, skal nota **Kladdi**.

1. Veldu **Upplýsingar um skilaboð** til að opna gluggann **Upplýsingar um skilaboð** þar sem þú getur skoðað allar viðvaranir og villur sem voru fangaðar í vinnslunni.

## <a name="related-resources"></a>Tengd tilföng

- [Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)
- [Hafist handa með fínstillingu áætlanagerðar](get-started.md)
- [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)
- [Nota síur á áætlun](plan-filters.md)
- [Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
