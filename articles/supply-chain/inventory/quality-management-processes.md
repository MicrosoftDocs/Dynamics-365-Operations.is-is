---
title: Gæðastjórnunarferli
description: Þessi grein gefur upplýsingar gæðastjórnunarferli fyrir ósamkvæmar afurðir. Það lýsir því hvernig hægt er að nota aðgerðir gæðaeftirlits, hvernig skuli skilgreina og vinna með ósamkvæmni og hvernig skuli meðhöndla leiðréttingar.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ab3b886b9d5237e96e193d7369c6060f19516e5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214068"
---
# <a name="quality-management-processes"></a>Gæðastjórnunarferli

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar gæðastjórnunarferli fyrir ósamkvæmar afurðir. Það lýsir því hvernig hægt er að nota aðgerðir gæðaeftirlits, hvernig skuli skilgreina og vinna með ósamkvæmni og hvernig skuli meðhöndla leiðréttingar.

Gæðaeftirlit felur í sér prófun á vörum og umsjón með ósamkvæmu efni. Gæðastjórnunarferli hjálp að tryggja mikinn vörugæði í birgðakeðjunni. Þessar ferli hjálpa einnig að besta birgðakeðjuferli og auka ánægju viðskiptavina. Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra. Hægt er að tengja niðurstöður greiningar við leiðréttingarverkefni. Kerfið getur raðað verkefni til að leiðrétta vandamál og því að koma í veg endurtekningar af þeim vandamálum í framtíðinni. Gæðastjórnun leyfir þér einnig að rekja vandamál (þ.m.t innri vandamál) eftir gerð vandamáls, og leyfir þér að bera kennsl lausnir sem annaðhvort til skamms tíma eða lengri tíma. Upplýsingar um afkastavísi (KPI) veita innsýn í vandamál með ósamkvæmi sem hafa áður komið upp og þeirra lausna sem voru notuð til að leiðrétta þau. Hægt er að nota söguleg gögn hjálpa til að fara yfir skilvirkni fyrri gæðaráðstafana og til að ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.

## <a name="controlling-the-quality-management-process"></a>Stjórna Gæðastjórnunarferli
Hér eru nokkrar aðferðir til að stjórna gæðastjórnunarferli:

-   Stofna gæðapantanir sem byggja á kveikjupunktum, eins og "við móttöku afurða" fyrir aðgerðum á innleið eða "þegar afurð er sótt" fyrir aðgerðir á útleið.
-   Skrá niður niðurstöður prófana, og ákvarða hvort að niðurstöðurnar uppfylla fyrirframákveðnum próunarskilyrði, og viðunandi gæðastig.
-   Nota skjalastjórnun fyrir nákvæmar lýsingar afurðar og notandatengdum athugasemdir sem hluti af skráningu við skoðunarferli.
-   Viðhalda ósamkvæmu afurðir og setja þessar afurðir í samhengi við viðbótar ósamkvæmiupplýsingar til að rekja upprunalegu orsök vandamáls.
-   Skrá Kostnaður við stjórnun ósamkvæmni. Kostnaðurinn innifelur vörurnar, (eins og varahluti ) og mismunandi gjöld, og vinnustundir á vinnuskýrslu sem krafist er til að leiðrétta ósamkvæmninni.
-   Áætlua villuleiðréttingarferli með því að nota leiðréttingarmeðhöndlun sem er tengd gæðapantanir.

[![Gæðastjórnunarferli](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Afurðaprófanir og gæðapantanir
Vöruprófun kallast venjulega gæðaeftirlit og notar gæðapantana . Með því að nota virkni gæðaeftirlits er hægt að gera eftirfarandi:

-   Skilgreina prófanir sem þarf að framkvæma fyrir efni. Þessar prófanir innihalda gæðaforskriftir, viðeigandi prófverkfæri, skjöl sem lýsa prófi, úrtaksáætlun, og viðunandi gæðastig (AQL).
-   Stofna gæðapöntun sem tilgreinir þær prófanir sem þarf að gera fyrir tiltekna pöntun (til dæmis innkaupa- eða framleiðslupöntun) eða tiltekið birgðamagn. Gæðapöntun má stofna handvirkt eða mynda sjálfvirkt samkvæmt gæðareglum.
-   Skilgreina gæðareglur sem tengjast tengdu innkaupum, biðgeymslu, framleiðslupöntunum eða sölupöntunum í hverju viðskiptaferli, fyrir sjálfvirka myndun gæðapöntunar sem tilgreinir kröfur fyrir prófun á magni á inn- eða útleið.
-   Skrá niðurstöður prófana í gæðapöntun, bera niðurstöðurnar saman við viðunandi gæðastig og prenta greiningarskírteini sem sýnir niðurstöður prófunarinnar.

## <a name="nonconformance"></a>Ósamkvæmni
Ósamkvæmni lýsir vöru með gæðavandamál. Ósamkvæmniferli gerir notendum kleift að stofna ósamkvæmnipöntun sem lýsir magni ósamkvæms efnis með uppruna vandans, gerð vandans og útskýringum. Hægt er að skilgreina flokkun á gerðum vanda fyrirfram fyrir greiningu á ósamkvæmu efni auðveldari. Einnig er hægt að prenta ósamkvæmnimerki og ósamkvæmniskýrslu til að veita leiðbeiningar um niðurskipan fyrir ósamkvæmu efni. Til dæmis, gætu merki og skýrslu gefið til kynna **ónýtanlegt** eða **Takmarkaðar notkun**.

Í eftirfarandi töflu er listi yfir sex sjálfgefnar gerðir ósamkvæmni og lýsir upplýsingar sem verður að vera skráð fyrir hverja tegund.

| Gerð ósamkvæmni   | Upprunaupplýsingar                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viðskiptavinur              | Lykilnúmer viðskiptavinar, sölupöntunarnúmer eða lotunúmer sölupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni sölupöntunarsendingu eða ábendingu viðskiptavinar um gæði vöru.       |
| Þjónustubeiðni       | Lykilnúmer viðskiptavinar, sölupöntunarnúmer eða lotunúmer sölupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni sölupöntunarsendingu eða kvörtun viðskiptavinar um gæði vöru.     |
| Lánardrottinn                | Lykilnúmer viðskiptavinar, innkaupapöntunarnúmer eða lotunúmer innkaupapöntunarfærslu. Til dæmis gæti ósamkvæmni átt við um móttöku innkaupapöntunar eða áhyggna lánardrottins varðandi hlut sem hann veitir. |
| Framleiðsla            | Framleiðslupöntunarnúmer eða lotunúmer framleiðslupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni runu sem var framleidd.                                                                      |
| Innra              | Gæðapöntunarnúmer eða lotunúmer gæðapöntunarfærslu. Til dæmis gæti ósamkvæmni tengst prófunum sem eru framkvæmd sem hluti af gæðapöntun eða áhyggjum starfsmanns um gæði vöru.     |
| Framleiðsla aukaafurðar | Ósamkvæmni aukaafurðar framleiðslupöntunar sem er tengd framleiðslupöntun runu.                                                                                                                                                    |

Ósamkvæmni er tengd við gerð vandamáls. Gerðir vandamála eru skilgreindar í á **gerðir Vandamála** síðuna þar sem tilgreint er hvaða gerðir vandamála getur verið tengt við hverja gerð ósamkvæmni. Til dæmis gætu gerðir vandamála fyrir ósamkvæmni fyrir gerðina **Þjónustubeiðni** endurspeglað flokkun fyrir kvartanir viðskiptavina, en hinsvegar gerðir ósamkvæmni fyrir gerðina **Innra** gætu staðið fyrir flokkun á gallakóðum.

Þegar stofnuð er ný ósamkvæmni, þú Velja gerð ósamkvæmni og gerð vandamáls. Upphafleg samþykktarstaðan er **Nýtt**, sem stendur fyrir beiðni um aðgerðina. Næsta skref er að breyta samþykktarstöðu í **samþykkt** eða **hafnað** til að gefa til kynna hvort bregðast eigi við ósamkvæmninni eða ekki. Einnig er hægt að loka ósamkvæmni (með því að velja sérstakur gátreitur ) til að gefa til kynna að búið sé að ljúka henni eða opna ósamkvæmni aftur til að gefa til kynna að þörf sé á frekari athugun.

Hægt að færa inn athugasemdir fyrir ósamkvæmni með því að tengja skjal. Er góð hugmynd að skilgreina einkvæma skjalgerð fyrir ósamkvæmni með því að nota í **Skjalagerð** síðu. Síðan er hægt að nota í **skýrsluuppsetningu** síðu til að skilgreina hvort athugasemdir fyrir þessa skjalagerð ætti að prenta á ósamkvæmnimerki og ósamkvæmniskýrslu. Hægt er að nota ósamkvæmniskýrslu og -merki til að auðvelda efnisráðstöfun. Hægt er að mynda skýrslur og merki með byggt á valskilyrðum, sem eru tengd ósamkvæmni. Meðal skilyrðanna eru númer ósamkvæmni, vöru, viðskiptavini, lánardrottna og stöðu.

Ósamkvæmniskýrslan birtir við númer ósamkvæmni, vöru og gerð vandamáls. Eftir uppsetningarreglu skýrslu, getur skýrslan einnig birt tengdar athugasemdir um ósamkvæmni. Ósamkvæmnimerkið birtir álíka upplýsingar, og innifela einnig biðgeymslusvæðið og -gerðina (til dæmis **takmarkaða notkun** eða **ónothæft**) sem er úthlutuð ósamkvæmninni til að stýra ráðstöfun gallaða efnisins.

## <a name="approved-nonconformance"></a>Samþykkt ósamkvæmni
Hægt er að velja að skilgreina eina eða fleiri tengdar aðgerðir fyrir samþykkta ósamkvæmni. Tengd aðgerð lýsir verkinu sem ætti að framkvæma og inniheldur lista yfir aðgerðir gæðapöntun sem hefur verið skilgreind og lýsandi texti um ástæðuna fyrir verkinu. Eftir að aðgerð er skilgreind er hægt að velja að skilgreina mismunandi gjöldin, vörurnar og vinnustundir vinnuskýrslunnar sem þarf til að framkvæma verkið. Útreiknaði kostnaðurinn er sýndur fyrir tengdu aðgerðina og útreiknaði heildarkostnaðurinn er sýndur fyrir ósamræmið. Útreiknaður kostnaður og undirliggjandi upplýsingarnar (um vörur, vinnustundir og ýmis gjöld) eru tilvísunarupplýsingar, sem eru aðeins notaðar í gæðastjórnun.

Hægt er að velja að stofna gæðapöntun úr ósamkvæmni með því að gera fyrst fyrirspurn fyrir gæðapantanir, og svo með því að stofna nýja gæðapöntun. Til dæmis gæti gæðapöntun gefið til kynna þörf á að prófa (eða endurprófa) gallaða efnið. Nýlega stofnaða gæðapöntunin birtir tengslin við uppruna ósamkvæmni.

Hægt er að velja að tengja eitt ósamræmi við annað eða stofna nýtt ósamræmi úr ósamræmi sem er til fyrir. Til dæmis gætu tengslin endurspeglað innri tengsl á milli gæðavandamála.

## <a name="correction-handling"></a>Leiðréttingarmeðhöndlun
**Leiðréttingar** síðu gerir kleift að búa til lista yfir ósamkvæmi sem þarf að leiðrétta . Hver leiðréttingarvara er tengd gerð greiningar sem orsakaði að vandamál fundust. Síðan **Leiðréttingar** inniheldur einnig upplýsingar um hver skuli framkvæma leiðréttingaraðgerðar og hvenær. Hægt er að lýsa vandamálinu í nákvæmni og leiðréttingaraðgerðina sem krafist er með því að tengja skjal við leiðréttinguna. Eftir að búið er að taka á ósamkvæmi eða leiðrétta , er leiðréttingarvöru "lokað" með því að velja á **Lokið** valkost. Einnig er hægt að tilgreina að lausnina var skammtímalausn.

Góð hugmynd er að skilgreina einkvæma skjalgerð fyrir ósamkvæmni með því að nota síðuna **Skjalagerð**. Síðan er hægt að nota síðuna **Skýrsluuppsetning** síðu til að skilgreina hvort athugasemdir fyrir þessa skjalagerð ætti að prenta á leiðréttingarskýrslu. Prentuð leiðréttingingarskýrsla birtir upplýsingar um ósamkvæmnina og tengdar athugasemdir um ósamkvæmni. Skýrslan inniheldur einnig leiðréttingarupplýsingar, eins og gerð greiningar og tengdar athugasemdir um leiðréttingar.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Gæðastjórnunaryfirlit](enable-quality-management.md)

[Stjórnun ósamkvæmi](enable-nonconformance-management.md)

[Birgðalæsing](inventory-blocking.md)

[Biðgeymslupantanir](quarantine-orders.md)

[Setja upp gæðapantanir](tasks/set-up-quality-orders.md)

[Skoða gæði vara](tasks/inspect-quality-goods.md)
