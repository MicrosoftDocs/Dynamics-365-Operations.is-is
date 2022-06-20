---
title: Búa til hópdagatal
description: Skoða og stofna hópsdagatöl í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6dffcb265030922e5134cfab1310027be43d87ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904160"
---
# <a name="view-team-and-company-calendars"></a>Skoða dagatöl hóps og fyrirtækis

>[!Important]
>Virknin sem getið er um í þessari grein er eins og er í boði fyrir viðskiptavini á sjálfstætt Dynamics 365 Human Resources. Sum eða öll virknin verður í boði sem hluti af síðari útgáfu í tölvukerfi Finance eftir útgáfu 10.0.26 af Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hægt er að skoða dagbækur hóps og fyrirtækis í Dynamics 365 Human Resources. Dagatöl hópa sýnir aðeins beinar skýrslur eins og skilgreint er í línustigveldinu.

## <a name="view-your-team-calendar-as-an-employee"></a>Skoðaðu dagatal hópsins sem starfsmaður

- Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Fjarvistadagatal teymis** undir **Samantekt**.

## <a name="view-your-team-calendar-as-a-manager"></a>Skoðaðu dagatal hópsins sem stjórnandi

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna** velurðu **Hópurinn minn**.

2. Veljið **Leyfi og fjarvistir** og veljið síðan **Skoða fjarvistadagatal stjórnanda**.

Stjórnendur geta einnig nálgast dagatal hópsins úr **Beiðnir um frí í bið vegna hóps míns**, **Samþykkt frí**, og **Beiðnir um frí**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Skoða dagatal fjarvistarstjóra sem fjarvistarstjóri

> [!NOTE]
> Til að skoða dagatal fjarvistarstjóra þarf fyrst að kveikja á eiginleikanum **(Forskoðun) Fjarvistarstjóri stjórnar fríi** í eiginleikastjórnun. Frekari upplýsingar um hvernig á að kveikja á forútgáfueiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

Notendur í hlutverki fjarvistarstjóra geta skoðað frítímabeiðnir í dagatalinu sínu. Fylgdu þessum skrefum til að fá aðgang að leyfisdagatalinu.

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Stjórnun leyfis** og síðan **Dagatal fjarvistarstjóra**.

2. Í reitinn **Dagsetning** skal færa inn æskilegar dagsetningar.

3. Uppfærðu skoðunarvalkostina eftir þörfum.

Dagatal fjarvistarstjóra sýnir allar færslur fyrir starfsmenn sem heyra undir fjarvistastjórann í leyfisstigveldinu.

## <a name="view-a-company-calendar"></a>Skoða dagatal fyrirtækisins

Starfsmenn með hlutverk í mannauði geta skoðað dagatöl fyrirtækisins. Dagatöl fyrirtækisins sýna alla starfsmenn. Sjálfgefið er að dagatalið sýnir dagsetningu í dag auk 28 daga, en þú getur breytt tímabilinu. Þú getur líka síað dagatalið eftir **Nafn**, **Starfsmannanúmer** og **Gerð leyfis**.

1. Í **Leyfi og fjarvera** vinnusvæði, veldu **Tenglar**.

2. Veldu **Orlof og fjarvistardagatal**.

Hlutverk Human resources geta einnig farið í dagatal fyrirtækisins úr **Beiðnir um leyfi og fjarvistir**, **Samþykkt frí** og **Beiðnir um frí**. 

Dagatöl innihalda nú viðbótarsíur og valmöguleika. Í öllum dagatölum eru skoðunarmöguleikar fyrir:

- Samþykktar beiðnir
- Beiðnir sem bíða
- Starfsfólk með leyfisbeiðnir
- Starfsmenn án leyfisbeiðna
- Afmæli starfsmanna
- Fríbeiðnir 
- Beiðnir um fjarvistarleyfi

Dagatalsstillingar á síðunni **Færibreytur leyfis og fjarvista** ákvarðar tiltæka valkosti yfirlits.

Einnig er hægt að sía dagatöl eftir stjórnanda eða deild. Aðalstöðuverk ákvarðar hvaða starfsmenn birtast þegar þessar síur eru stilltar. 

> [!IMPORTANT]
> Þú getur kveikt á eiginleikanum **Leyfisyfirlit á milli fyrirtækja** í eiginleikastjórnun. Þú verður þá að virkja eiginleikann á síðunni **Samnýttar færibreytur fyrir mannauð** til að sýna síu lögaðilans í dagatölum. Frekari upplýsingar eru í [Grunnstilla færibreytur leyfis og fjarvista](hr-leave-and-absence-parameters.md).
> 
> Hægt er að sía dagatalið eftir lögaðila. Til að skoða alla starfsmenn, óháð lögaðila, skal hreinsa síureitinn og velja síðan **Enter**. 

Fyrir upplýsingar um stillingar dagatals, sjá [Skilgreina færibreytur dagatals](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
