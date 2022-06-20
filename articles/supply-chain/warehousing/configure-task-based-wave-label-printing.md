---
title: Tímasetja prentun bylgjumerkis í bylgju
description: Þessi grein lýsir því hvernig á að setja upp og nota virknina fyrir verkefnabundna bylgjumerkisprentun.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889458"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Tímasetja prentun bylgjumerkis í bylgju

[!include [banner](../../includes/banner.md)]

Notið eiginleikann *Prentun á verktengdu bylgjumerki* sem hluta af bylgjuferlinu til að auka skilvirkni og til að kerfið stofni bylgjumerki og vinnu í aðskildum verkum.

Aðferðin við að stilla prentun bylgjumerkis er flókin og reiðir sig á nákvæmum stillingum og aðalgögnum. Það er ekki óalgengt að færslumyndun bylgjumerkja mistakist og þegar það gerist verður allri bylgjuvinnslunni snúið við. Eiginleikinn *Prentun á verktengdu bylgjumerki* hjálpar þér til að losna undan því að endurstofna vinnu og vinnulínur í hvert skipti sem bylgjumerki er prentað á rangan hátt.

Þegar eiginleikinn *Prentun á verkefnaháðu bylgjumerki* er notaður stofnar kerfið fyrst vinnu og vinnulínur. Það býr síðan til og prentar bylgjumerki. Að lokum, ef bylgjumerkin eru búin á réttan hátt, losar það vinnuna og bylgjuna fyrir tiltekt.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Kveikja á eiginleika fyrir prentun á verkefnaháðu bylgjumerki í eiginleikastjórnun

Til að nota eiginleikana sem lýst er í þessari grein verður að kveikja á þeim fyrir kerfið þitt. Notið vinnusvæði [Eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikunum í eftirfarandi röð:

1. *Prentun bylgjumerkis* – Þennan eiginleika þarf til að virkja aðferð bylgjuvinnslunnar fyrir prentun bylgjumerkis.
1. *Vinnulokun fyrir allt fyrirtækið* – Þennan eiginleika þarf fyrir bæði handvirka og sjálfvirka skilgreiningu á tímasettri vinnustofnun. (Frá og með Supply Chain Management útgáfu 10.0.21 er þessi eiginleiki nauðsynlegur, þannig að það er sjálfgefið kveikt á honum og ekki er hægt að slökkva á honum aftur.)
1. *Prentun á verkefnaháðu bylgjumerki* – Þennan eiginleika þarf til að skipta niður prentun bylgjumerkis til að dreifa álaginu.

## <a name="manually-enable-the-new-wave-step-method"></a>Virkja nýja aðferð bylgjuskrefs handvirkt

Fyrst þarf að stofna nýja aðferð bylgjuskrefs og virkja hana fyrir samhliða, ósamstillta verkvinnslu.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Veldu **Endurgera aðferð** á aðgerðasvæðinu. Takið eftir að *waveLabelPrinting* er bætt við lista yfir aðferðir bylgjuvinnslu sem hægt er að nota í bylgjusniðmátum sendingar.
1. Veljið færsluna þar sem reiturinn **Heiti aðferðar** er stilltur á *waveLabelPrinting* og veljið síðan á aðgerðasvæðinu **Skilgreining verks**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Vöruhús** – Veljið vöruhúsið sem nota á til að tímasetja vinnslu á stofnun vinnu. (Ef notuð eru sýnigögn til prófunar er hægt að velja vöruhús *24*.)
    - **Hámarksfjöldi runuverka** - Tilgreinið hámarksfjölda runuverka. Í flestum tilvikum ætti gildið að vera frá *8* til *16*. Hins vegar er mælt með því að þú prófir þig áfram til að finna kjörstillinguna fyrir þínar aðstæður.
    - **Runuflokkur bylgjuvinnslu** – Veljið sérstakan runuflokk bylgjuvinnslu til að fínstilla vinnslu runubiðraðar.

Nú er hægt að uppfæra fyrirliggjandi bylgjusniðmát þannig að það noti bylgjuvinnsluaðferðina *Prentun bylgjumerkis*. Einnig er hægt að stofna nýtt bylgjusniðmát sem notar hana.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í listaglugganum skal velja bylgjusniðmát sem á að uppfæra. (Ef notuð eru sýnigögn til prófunar er hægt að velja vöruhús *24 Sjálfgefin sending*.)
1. Í flýtiflipanum **Aðferðir**, í dálknum **Aðferðir sem eftir standa**, skal velja línuna þar sem reiturinn **Heiti** er stilltur á *waveLabelPrinting*.
1. Veljið **bæta við** (hægri örvarhnappur) til að færa valda línu í dálkinn **Valdar aðferðir**.
1. Í reitinn **Kóði bylgjuskrefs** skal færa inn kóða bylgjuskrefs sem verður notaður til að tengja bylgjusniðmátið við sniðmát bylgjumerkis.

## <a name="set-wave-task-processing-threshold-data"></a>Stilla þröskuldsgögn fyrir úrvinnslu bylgjuverks

Fyrsta skipti sem bylgjuvinnsla keyrir með því að nota verktengda vinnslu býr kerfið til þröskuldsgögn sjálfgefins bylgjuverks. Þessi gögn eru notuð til að stjórna því hvort bylgjuvinnsla muni keyra ósamstillt og vera byggð á verki þannig að hún geti unnið úr og búið til bylgjumerki samhliða.

Sjálfgefin gögn nota upphaflega þröskuldsgildið *1* fyrir lágmarksfjölda vinnukenna (`MinimumWorkThresholdForLabelPrinting`). Þar af leiðandi, þegar kerfið vinnur úr bylgju sem er með meira en eitt vinnukenni, notar það verktengda vinnslu bylgjumerkja í aðskildri færslu. Hægt er að setja inn eða uppfæra þessi gögn í `WHSWaveTaskProcessingThresholdParameters` töflunni í prófunarumhverfunum. Til að breyta þessari stillingu í vinnsluumhverfi þarf að hafa samband við notendaþjónustu Microsoft til að óska eftir uppfærslunni.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Breytingar á rökum bylgjuvinnslunnar þegar verktengd prentun bylgjumerkis er notuð

Ef vinnsla bylgjumerkis fer yfir vinnsluþröskuld bylgjuverks verður verktengd vinnsla sett í gang. Í næstu bylgjuvinnslu sem passar við bylgjusniðmátið mun prentun bylgjumerkis keyra í sjálfstæðri færslu *ttsbegin*/*ttscommit* strax eftir stofnun vinnu. Ef vinnulosun (afblokkun) er skilgreind í bylgjusniðmátinu til að keyra sjálfkrafa gerist hún aðeins eftir að prentferli bylgjumerkis hefur heppnast.

Ef myndun bylgjumerkis tekst ekki (til dæmis ef umbreyting á vinnumagni í magn bylgjumerkis mistekst og skilar villu) er það aðeins viðeigandi færsla sem mistekst. Vinnan sem var stofnuð áður helst áfram fryst. Til að leiðrétta villur og prenta bylgjumerkin skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið viðeigandi bylgju í hnitanetinu.
1. Á aðgerðasvæðinu, í flipanum **Bylgja**, í flokknum **Prenta**, skal velja **Bylgjumerki**.
1. Fylgið leiðbeiningunum á skjánum til að senda merki til prentunar.
1. Á aðgerðasvæðinu, í flipanum **Bylgja**, í hópnum **Bylgja**, skal velja **Losa** til að losa vinnuna handvirkt fyrir valda bylgju.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Prentun bylgjumerkis](configure-wave-label-printing.md)
- [Áætla stofnun vinnu í bylgju](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
