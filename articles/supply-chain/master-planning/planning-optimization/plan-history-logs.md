---
title: Skoða áætlunarsögu og skipulagsskrár
description: Þetta efni útskýrir hvernig á að skoða sögu áætlunarvinnsla sem fara af stað vegna virkni fínstillingar áætlunargerðar.
author: ChristianRytt
ms.date: 10/30/2019
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 93e8f933524b34116987c9e0d91d226e21d98f4d
ms.sourcegitcommit: 5c9a5bfef507ed36f0f849ab56fa0aa8abb78d54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/20/2021
ms.locfileid: "6646488"
---
# <a name="view-plan-history-and-planning-logs"></a>Skoða áætlunarsögu og skipulagsskrár

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að skoða sögu áætlunarvinnsla sem fara af stað vegna virkni fínstillingar áætlunargerðar í Microsoft Dynamics 365 Supply Chain Management.

Til að skoða sögu fyrir áætlun, opnaðu áætlunina með því að fara til **Aðaláætlunargerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir** og velja **Saga**. Í sögunni eru allar vinnslur fyrir valda áætlun. Listinn nær yfir loknar og virkar vinnslur.

Verkferillinn fyrir keyrslur aðaláætlanagerðar á fínstillingu skipulagningar geymir að hámarki 60 færslur fyrir hverja aðaláætlun. Í hvert sinn sem nýr útreikningur aðaláætlanagerð verður elstu ferilfærslu áætlunarinnar eytt.

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
