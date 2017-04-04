---
title: "Setja upp sjálfgefna debet tilskipun SEPA"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Setja upp sjálfgefna debet tilskipun SEPA



SEPA-beingreiðsla (Single Euro Payment Area )  gerir kleift að safna fjármagn frá bankareikningi viðskiptavinar hjá lánardrottni svo lengi sem undirrituð umboðið hefur verið veitt af viðskiptavini í lánardrottins. Viðskiptavinurinn skrifar umboð sem heimilar lánardrottins til að innheimta greiðslu og veitir banka viðskiptavinar fyrirmæli um að greiða innheimtuna. Í þessu efnisatriði er raðað til að birta ferli til að setja upp SEPA-umboð fyrir beint debet.

## <a name="prerequisites"></a>Forkröfur
Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

| Tegund       | Skilyrði                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/svæði | Aðalaðsetur fyrir lögaðilann verður að vera í eftirfarandi löndum/svæðum: |

1. Setja upp númeraröð fyrir Hverja umboð fyrir beint debet verður að hafa einkvæm númer umboð fyrir beint debet. Nota skal síðuna **  númeraraðir** til að stofna númeraröð fyrir umboð fyrir beingreiðslu. Þú munt nota þetta kenni til að úthluta númeraröð á umboð fyrir beingreiðslu í á    **færibreytur viðskiptakrafna** síða.

2. Setja upp færibreytur viðskiptavina fyrir umboð fyrir beint debet Notkun á **Færibreytur viðskiptakrafna** síðu til að setja upp færibreytur fyrir umboð fyrir beint debet. Til að setja upp færibreytur sem á við **beingreiðsla** breytt sjálfgefnar færibreytur sem krafist er. Síðan skal á **Númeraraðir** flipanum, uppfæra á **umboð Beingreiðslukenni** með númeraröð sem er sett upp fyrr.

3. Setja upp greiðsluhátt fyrir beint debet krefst verður að setja upp greiðsluhátt fyrir umboð fyrir beint debet. Nota þennan greiðsluhátt til að spyrjast fyrir um reikninga til að mynda beingreiðslur fyrir. Nota skal **Greiðslumáti ** síða til að setja upp greiðslumáta. Til að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu, verður að fylgja þessum viðbótarskref fyrir greiðslumáta:

-   Í **reitnum greiðslugerð** skal velja **rafræn greiðsla**
-   Valfrjálst: Ef búist er við hverja viðskiptavinum að hafa margar krefst, í því **Tímabil** svæðinu, veljið **Reiknings**. Er aðskilin greiðsla stofnuð fyrir hvern reikning og hverrar greiðslu verður að nota umboðið sem tilgreindur er fyrir reikninginn.
-   Velja skal **  krefjast umboðs ** valkost til að búa til greiðslur með umboð fyrir beingreiðslu. **Krefjast umboðs** valkosturinn er tiltækur aðeins ef þú velur **Rafræna greiðslu** í á **greiðslugerð** svæði.

Sjá Einnig [yfirlit fyrir Beint debet](sepa-direct-debit-overview.md) 

