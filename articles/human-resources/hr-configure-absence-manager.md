---
title: Skilgreina hlutverk fjarvistastjórnanda
description: Þessi grein útskýrir hvernig á að setja upp fjarvistarstjórahlutverkið fyrir stjórnun orlofs starfsmanna.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b752b722bf63958fc35b10a4612f7f02e2e8e717
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337324"
---
# <a name="configure-the-absence-manager-role"></a>Skilgreina hlutverk fjarvistastjórnanda


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í sumum fyrirtækjum er ekki víst að stjórnendur hafi umsjón með leyfum fyrir teymið þeirra. Þess í stað gæti fjarvistastjórnandi séð um þetta ferli fyrir teymismeðlimi í mörgum deildum og teymum. Fjarvistastjórnendur hafa eftirfarandi möguleika fyrir leyfisstjórnun:

- Yfirfara og samþykkja frí á grundvelli annars stigveldis.
- Skoða stöðu teymismeðlima.
- Skoða fjarvistadagatalið.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

1. Á vinnusvæðinu **Kerfisstjórnun** skal velja **Eiginleikastjórnun**.
2. Í flipanum **Eiginleikastjórnun** skal virkja eiginleikann **Fjarvistarstjóri stjórnar leyfi**.

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

1. Í **Kerfisstjórnun** vinnusvæði, veldu **Tenglar**.
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

Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns**, í flipanum **Stjórnun leyfa**, sjást fjarvistaupplýsingar starfsmanna sem er úthlutað til fjarvistastjóra í leyfisstigveldinu. Það eru nokkrir valkostir í boði fyrir fjarverustjórann: 
 - Farðu yfir frítímabeiðnir.</br>
 - Senda inn beiðni um frí fyrir hönd starfsmanns.</br>
 - Skoðaðu alla starfsmenn sem honum er úthlutað sem hluti af frítímastigveldinu.</br>
 - Skoða dagatal fjarvistarstjóra.</br>

Á vinnusvæðinu **Stjórnun leyfis** eru tveir flipar:
 - **Beiðni um frí**: Þessi flipi mun sýna allar beiðnir um frí í biðstöðu sem fjarvistastjórnandi getur samþykkt. Fjarvistastjórnandinn getur valið margar færslur og gert aðgerðir á þeim öllum samtímis. Ef leyfisyfirlit milli fyrirtækja er virkjað mun þessi listi sýna frítímabeiðnir í biðstöðu í öllum lögaðilum sem hann hefur aðgang að. Annars sýnir hann frítímabeiðnir í biðstöðu fyrir þann lögaðila sem er valinn. </br>
 - **Allir starfsmenn**: Þessi flipi mun skrá alla starfsmenn sem fjarvistastjórnandanum er úthlutað í leyfisstigveldinu. Hægt er að velja um nokkra valkosti fyrir hvern starfsmann:
    - **Beiðni um frí** - Sendu inn nýja beiðni um frí fyrir valinn starfsmann.</br>
    - **Frí** – Skoðaðu stöður, samþykkt frí og beiðnir um frí fyrir valdan starfsmann.</br>

## <a name="approve-time-off-requests"></a>Samþykkja beiðnir um frí

Fjarvistastjórar geta samþykkt eða hafnað beiðnum um frí fyrir starfsmenn. 

> [!IMPORTANT]
> Áður en fjarvistarstjórar geta samþykkt eða hafnað óskum um frí verður að stilla verkflæði leyfisbeiðna til að úthluta þeim vinnuliðum leyfisbeiðni til skoðunar.
>
> 1. Á síðunni **Verkflæði fyrir mannauð** skal velja eða búa til verkflæði leyfisbeiðni.
> 2. Veldu valkostinn **Tengja stigveldi** og síðan í reitnum **Heiti stigveldis** skal velja **Leyfi**.
> 3. Uppfærðu verkflæðið í hönnuði verkflæðis. Undir **Úthlutunargerð** skal velja valkostinn **Stigveldi** og síðan í flipanum **Stigveldisval** skal velja **Skilgreinanlegt stigveldi**.
>
> Frekari upplýsingar um hvernig á að búa til verkflæði leyfisbeiðni er að finna í [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md).

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna** skal velja flipann **Stjórnun leyfa**.
2. Í flipanum **Beiðni um frí** skal velja frítímabeiðnirnar þar sem á að framkvæma aðgerð. Hægt er að velja margar skrár í þessum lista.
3. Notaðu aðgerðahnappana efst í hnitanetinu til að samþykkja, hafna eða úthluta frítímabeiðninni. 

Einnig getur notandinn notað reitinn **Beiðnir um frí** vinstra megin til að fara í listann yfir vinnuliði allra frítímabeiðna. 

## <a name="view-time-off-in-the-calendar"></a>Skoða frí í dagatalinu

Notendur í hlutverki fjarvistarstjóra geta skoðað frítímabeiðnir í dagatalinu sínu. Fylgdu þessum skrefum til að fá aðgang að leyfisdagatalinu.

> [!IMPORTANT]
> Kerfisstjóri verður að skilgreina valkosti yfirlits fyrir dagatal fjarvistarstjóra. Á síðunni **Færibreytur leyfis og fjarvista**, í flipanum **Dagatal**, eru valkostir um að fela eða sýna fæðingardaga, fjarvistir án leyfis, fjarvistarleyfi og leyfisbeiðnir í biðstöðu. Einnig er sá möguleiki fyrir hendi að sía valkost dagatalsyfirlitsins eftir gerð starfsmanns.

1. Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Stjórnun leyfis** og síðan **Dagatal fjarvistarstjóra**.
2. Í reitinn **Dagsetning** skal færa inn æskilegar dagsetningar.
3. Uppfærðu skoðunarvalkostina eftir þörfum.

Dagatal fjarvistarstjóra sýnir allar færslur fyrir starfsmenn sem heyra undir fjarvistastjórann í leyfisstigveldinu.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md)
- [Skoða dagatöl hóps og fyrirtækis](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
