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

[!include[banner](../includes/banner.md)]




SEPA-beingreiðsla (Single Euro Payment Area )  gerir kleift að safna fjármagn frá bankareikningi viðskiptavinar hjá lánardrottni svo lengi sem undirrituð umboðið hefur verið veitt af viðskiptavini í lánardrottins. Viðskiptavinurinn skrifar umboð sem heimilar lánardrottins til að innheimta greiðslu og veitir banka viðskiptavinar fyrirmæli um að greiða innheimtuna. Þessu efnissviði er raðað þannig að það sýnir ferli fyrir uppsetningu SEPA-umboð fyrir beingreiðslu.

## <a name="prerequisites"></a>Forkröfur
Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

| Tegund       | Skilyrði                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/svæði | Aðalaðsetur fyrir lögaðilann verður að vera í eftirfarandi löndum/svæðum: |

1. Setja upp númeraröð fyrir umboð fyrir beint debet Hvert umboð fyrir beint debet verður að hafa einkvæmt númer. Nota skal síðuna **  númeraraðir** til að stofna númeraröð fyrir umboð fyrir beingreiðslu. Þú munt nota þetta kenni til að úthluta númeraröð á umboð fyrir beingreiðslu í á    **færibreytur viðskiptakrafna** síða.

2. Setja upp færibreytur viðskiptavina fyrir umboð fyrir beint debet Nota skal síðuna **Færibreytur viðskiptakrafna** til að setja upp færibreytur fyrir umboð fyrir beingreiðslu. Til að setja upp færibreytur á **beingreiðsla** flipa skal breyta sjálfgefnum færibreytum eins og krafist er. Síðan skal á **Númeraraðir** flipanum uppfæra **Kenni umboðs fyrir beint debet** svæði með númeraröð sem var sett upp áður.

3. Til að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu verður þú að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu. Nota þennan greiðsluhátt til að spyrjast fyrir um reikninga til að mynda beingreiðslur fyrir. Nota skal **Greiðslumáti ** síða til að setja upp greiðslumáta. Til að setja upp greiðsluhátt fyrir umboð fyrir beingreiðslu, verður að fylgja þessum viðbótarskref fyrir greiðslumáta:

-   Í **reitnum greiðslugerð** skal velja **rafræn greiðsla**
-   Valfrjálst: Ef þú átt von á að hver viðskiptavinur þinn hafi mörg umboð, í reitnum **Tímabil** skaltu velja **Reikningur**. Aðskild greiðsla verður stofnuð fyrir hvern reikning og hver greiðsla notar umboð sem er tilgreind fyrir reikninginn.
-   Velja skal **  krefjast umboðs ** valkost til að búa til greiðslur með umboð fyrir beingreiðslu. **Krefjast umboðs** valkosturinn er tiltækur aðeins ef þú velur **Rafræna greiðslu** í á **greiðslugerð** svæði.

Sjá einnig [Yfirlit yfir beint debet](sepa-direct-debit-overview.md) 



