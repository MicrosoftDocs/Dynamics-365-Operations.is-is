---
title: Skoða áætlunarsögu og skipulagsskrár
description: Í þessari grein er sagt frá því hvernig skoða má sögu áætlunarverka.
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
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740932"
---
# <a name="view-plan-history-and-planning-logs"></a>Skoða áætlunarsögu og skipulagsskrár

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að skoða sögu áætlunarverka í Microsoft Dynamics 365 Supply Chain Management.

Til að skoða sögu fyrir áætlun, opnaðu áætlunina með því að fara til **Aðaláætlunargerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir** og velja **Saga**. Í sögunni eru allar vinnslur fyrir valda áætlun. Listinn nær yfir loknar og virkar vinnslur.

Kerfið heldur að hámarki 60 ferilfærslur samkvæmt aðalskipulagi og eyðir skrám sem eru eldri en 30 daga. Í hvert sinn sem nýtt aðalskipulag er keyrt bætir kerfið við nýrri ferilskrá og hreinsar síðan upp elstu skrárnar eftir þörfum.

Auk þess að sjá upphafstíma og stöðu á vinnslum geturðu skoðað kladda fyrir tiltekna vinnslu. Í kladdanum eru viðbótarupplýsingar og viðvaranir. Ekki eru allar vinnslur með kladda. Til að skoða kladda fyrir vinnslu velurðu **Kladdi**. Kladdafærslur eru aðeins geymdar í 30 daga frá deginum sem verkið klárast og er eytt sjálfkrafa eftir það.

Ef valkosturinn **Runuvinnsla** í flýtiflipanum **Keyra í bakgrunni** var virkjaður þegar vinnsla aðaláætlanagerðar var sett upp, sýnir kladdi runuvinnslu frekari upplýsingar um viðvaranir og villur sem komu upp í keyrslu aðaláætlanagerðar. Til dæmis eru villur sjálfvirkrar staðfestingar aðeins fangaðar í runuvinnslukladdanum. Þær eru ekki sýndar í klöddum á síðunni **Ferill**.

Til að skoða villur sjálfvirkrar staðfestingar og aðrar viðvaranir eða villur sem komu upp í keyrslu aðaláætlanagerðar skal fylgja þessum skrefum.

1. Farðu í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur**.
1. Finndu og veldu færsluna sem stendur fyrir keyrslu aðaláætlanagerðar sem þú hefur áhuga á. (Til dæmis gæti gildi reitsins **Lýsing vinnslu** byrjað á *Aðaláætlanagerð*.)
1. Fylgdu einu af þessum skrefum, eftir því hvort þú ert að nota *endurbætta skjámynd* eða *eldri (óendurbætta) skjámynd* fyrir síðuna **Runuvinnslur**:

    - Ef þú ert að nota endurbættu skjámyndina: Veldu **Runuvinnsluferil** á aðgerðasvæðinu. Því næst, á síðunni **Runuvinnsluferill**, skal velja **Kladdi** á aðgerðasvæðinu.
    - Ef þú notar eldri skjámynd: Á aðgerðasvæðinu, í flipanum **Runuvinnsla**, skal nota **Kladdi**.

1. Veldu **Upplýsingar um skilaboð** til að opna gluggann **Upplýsingar um skilaboð** þar sem þú getur skoðað allar viðvaranir og villur sem voru fangaðar í vinnslunni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
