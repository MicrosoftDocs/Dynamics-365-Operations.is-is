---
title: Skilgreina hlutverk fjarvistastjórnanda
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp hlutverk fjarvistastjórnanda fyrir stjórnun á leyfi starfsmanns.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639607"
---
# <a name="configure-the-absence-manager-role"></a>Skilgreina hlutverk fjarvistastjórnanda

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Í sumum fyrirtækjum er ekki víst að stjórnendur hafi umsjón með leyfum fyrir teymið þeirra. Þess í stað gæti fjarvistastjórnandi séð um þetta ferli fyrir teymismeðlimi í mörgum deildum og teymum. Fjarvistastjórnendur hafa eftirfarandi möguleika fyrir leyfisstjórnun:

- Yfirfara og samþykkja frí á grundvelli annars stigveldis.
- Skoða stöðu teymismeðlima.
- Skoða fjarvistadagatalið.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

1. Á vinnusvæðinu **Kerfisstjórnun** skal velja **Eiginleikastjórnun**.

2. Í flipanum **Eiginleikastjórnun** skal virkja eiginleikann **(Forútgáfa) Fjarvistarstjóri stjórnar leyfi**.

## <a name="define-a-custom-hierarchy"></a>Skilgreina sérstillt stigveldi

Virkni fjarvistastjóra notar sérstillt stigveldi sem þarf að skilgreina.

1. Á vinnusvæðinu **Fyrirtækisstjórnun** skal velja **Stigveldisgerðir stöðu**.

2. Búðu til stigveldisgerð stöðu sem heitir **Leyfi**.

3. Á vinnusvæðinu **Leyfi og fjarvistir**, undir **Tenglar**, skal velja **Færibreytur leyfis og fjarvista**.

4. Í flipanum **Almennt**, í fellilistanum **Fjarvistarstigveldi**, skal velja stigveldisgerðina **Leyfi** sem var búin til hér á undan. Ljúka verður við þessa tengingu fjarvistarstigveldis fyrir alla lögaðila þar sem virkni fjarvistastjóra verður notuð.

Þegar stigveldisgerðin hefur verið skilgreind þarf að úthluta skýrslu stigveldisstöðu á stöðuna.

1. Á vinnusvæðinu **Fyrirtækisstjórnun** skal velja **Allar stöður**.

2. Veldu stöðuna þar sem á að bæta leyfisstigveldinu við.

3. Í flipanum **Tengsl** skal velja **Bæta við**.

4. Í reitnum **Heiti stigveldis** skal velja **Leyfi**.

5. Í reitnum **Skýrslur eftir stöðu** skal velja stöðu. Nafn starfsmanns er sjálfkrafa fyllt út eftir að staða er valin.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Úthluta notanda hlutverki fjarvistastjóra

Hlutverki fjarvistastjóra verður að vera úthlutað á starfsmenn til að gera þeim kleift að samþykkja eða hafna leyfisbeiðnum.

1. Á vinnusvæðinu **Kerfisstjóri** skal velja **Tenglar**.

2. Í hlutanum **Notendur** skal velja tengilinn **Notendur**.

3. Í listanum yfir notendur skal velja notandann sem á að fá úthlutað hlutverki fjarvistastjóra.

4. Í flipanum **Hlutverk notanda** skal velja **Úthluta hlutverkum**.

5. Í listanum skal velja hlutverkið **Fjarvistarstjóri**. Veljið síðan **Í lagi**.

    > [!IMPORTANT]
    > Ganga skal úr skugga um að starfsmannahlutverkinu hafi einnig verið úthlutað til notandans sem fær hlutverk fjarvistastjóra. Að öðrum kosti getur starfsmaðurinn ekki notað eiginleikann.

6. Eftir að þú hefur búið til leyfisstigveldið getur þú skoðað það með því að fylgja þessum skrefum:

    1. Á vinnusvæðinu **Fyrirtækisstjórnun** skal velja **Stigveldi stöðu**.
    
    2. Í reitnum **Stigveldisgerð** skal velja **Leyfi**.

## <a name="absence-manager-workspace"></a>Vinnusvæði fjarvistarstjóra

Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns**, í flipanum **Fjarvistarstjóri**, sjást fjarvistaupplýsingar starfsmanna sem er úthlutað til fjarvistastjóra í leyfisstigveldinu.

Í flipanum **Leyfi og fjarvistir** eru eftirfarandi valkostir í boði fyrir hvern starfsmann:

- **Frí** – Skoðaðu stöður, samþykkt frí og beiðnir um frí fyrir valdan starfsmann.
- **Leyfisstaða** – Skoðaðu lista yfir stöður fyrir mismunandi leyfisáætlanir fyrir valdan starfsmann.

## <a name="approve-time-off-requests"></a>Samþykkja beiðnir um frí

Fjarvistastjórar geta samþykkt eða hafnað beiðnum um frí fyrir starfsmenn. Þeir geta einnig búið til beiðnir fyrir hönd starfsmanna eftir þörfum.

> [!IMPORTANT]
> Áður en fjarvistarstjórar geta samþykkt eða hafnað óskum um frí verður að stilla verkflæði leyfisbeiðna til að úthluta þeim vinnuliðum leyfisbeiðni til skoðunar.
>
> 1. Á síðunni **Verkflæði fyrir mannauð** skal velja eða búa til verkflæði leyfisbeiðni.
> 2. Veldu valkostinn **Tengja stigveldi** og síðan í reitnum **Heiti stigveldis** skal velja **Leyfi**.
> 3. Uppfærðu verkflæðið í hönnuði verkflæðis. Undir **Úthlutunargerð** skal velja valkostinn **Stigveldi** og síðan í flipanum **Stigveldisval** skal velja **Skilgreinanlegt stigveldi**.
>
> Frekari upplýsingar um hvernig á að búa til verkflæði leyfisbeiðni er að finna í [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md).

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna** skal velja flipann **Fjarvistarstjóri**.

2. Í flipanum **Fjarvistarstjóri** skal velja viðeigandi starfsmann.

3. Veldu **Upplýsingar** og síðan **Frí**.

4. Finndu beiðni um frí og veldu valkostinn **Samþykki**. Þá er hægt að velja valkost til að samþykkja eða hætta við beiðni um frí.

Staðan **Hætta við** gefur til kynna að beiðninni hafi verið hafnað. Staðan **Lokið** gefur til kynna að beiðnin hafi verið samþykkt.

## <a name="view-time-off-in-the-calendar"></a>Skoða frí í dagatalinu

Notendur í hlutverki fjarvistarstjóra geta skoðað frítímabeiðnir í dagatalinu sínu. Fylgdu þessum skrefum til að fá aðgang að leyfisdagatalinu.

> [!IMPORTANT]
> Kerfisstjóri verður að skilgreina valkosti yfirlits fyrir dagatal fjarvistarstjóra. Á síðunni **Færibreytur leyfis og fjarvista**, í flipanum **Dagatal**, eru valkostir um að fela eða sýna fæðingardaga, fjarvistir án leyfis, fjarvistarleyfi og leyfisbeiðnir í biðstöðu. Einnig er sá möguleiki fyrir hendi að sía valkost dagatalsyfirlitsins eftir gerð starfsmanns.

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Fjarvistarstjóri** og síðan **Dagatal fjarvistarstjóra**.

2. Í reitinn **Dagsetning** skal færa inn æskilegar dagsetningar.

3. Uppfærðu skoðunarvalkostina eftir þörfum.

Dagatal fjarvistarstjóra sýnir allar færslur fyrir starfsmenn sem heyra undir fjarvistastjórann í leyfisstigveldinu.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md)
- [Skoða dagatöl hóps og fyrirtækis](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
