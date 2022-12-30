---
title: Stjórnunaryfirlit gæða og ósamkvæmni
description: Þessi grein kynnir stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management og útskýrir hvernig þeir geta hjálpað til við að bæta gæði afurða í aðfangakeðjunni.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 510dee78f6fed02e6511aedad00fcb1b15195470
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907494"
---
# <a name="quality-and-nonconformance-management-overview"></a>Stjórnunaryfirlit gæða og ósamkvæmni

[!include [banner](../includes/banner.md)]

Þessi grein kynnir stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management og útskýrir hvernig þeir geta hjálpað til við að bæta gæði afurða í aðfangakeðjunni.

Gæðaeftirlit felur í sér prófun á vörum og umsjón með ósamkvæmu efni. Gæðastjórnunarferli hjálp að tryggja mikinn vörugæði í birgðakeðjunni. Þessar ferli hjálpa einnig að besta birgðakeðjuferli og auka ánægju viðskiptavina. Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra. Hægt er að tengja niðurstöður greiningar við leiðréttingarverkefni. Kerfið getur raðað verkefni til að leiðrétta vandamál og því að koma í veg endurtekningar af þeim vandamálum í framtíðinni. Gæðastjórnun leyfir þér einnig að rekja vandamál (þ.m.t innri vandamál) eftir gerð vandamáls, og leyfir þér að bera kennsl lausnir sem annaðhvort til skamms tíma eða lengri tíma. Upplýsingar um afkastavísi (KPI) veita innsýn í vandamál með ósamkvæmi sem hafa áður komið upp og þeirra lausna sem voru notuð til að leiðrétta þau. Hægt er að nota söguleg gögn hjálpa til að fara yfir skilvirkni fyrri gæðaráðstafana og til að ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.

Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra. Þar sem greiningargerðir eru tengdar leiðréttingaskýrslum getur Supply Chain Management raðað verki til að leiðrétta vandamál og komið í veg fyrir þau verði endurtekin.

Auk virkni fyrir stjórnun ósamkvæmni inniheldur gæðastjórnun virkni til að rekja úthreyfingar eftir gerð vanda (jafnvel þegar um er að ræða innri vandamál) og til að auðkenna lausnir sem skammtíma- eða langtímalausnir. Upplýsingar um afkastavísi (KPI) veita innsýn í sögulegan feril fyrri vandamála með ósamkvæmi og þeirra lausna sem voru notuð til að leiðrétta þau. Hægt er að nota söguleg gögn til að fara yfir skilvirkni fyrri gæðaráðstafana og ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.

Þegar gæðatenging er sett upp getur Supply Chain Management myndað gæðapantanir fyrir ýmis viðskiptaferli, tilvik og skilyrði. Gæðatengingin getur náð yfir ákveðna vöru, einstökan vöruflokk eða allar vörur.

## <a name="examples-of-the-use-of-quality-management"></a>Dæmi um notkun á gæðastjórnun

Gæðastjórnun er sveigjanleg og hægt er að innleiða hana á mismunandi vegu til að uppfylla kröfur um tiltekið stig í aðgerðum framboðskeðju. Eftirfarandi dæmi sýna hugsanlega notkun á þessum eiginleikum:

- Hefja ferli gæðaeftirlits sjálfvirkt, byggt á fyrirfram skilgreindum skilyrðum (t.d. við vöruhússkráningu innkaupapöntunar frá tilteknum lánardrottni).
- Læsa birgðum við skoðun til að koma í veg fyrir að ósamþykktar birgðir séu notaðar (alger stöðvun á pöntunarmagni innkaup).
- Vörusýnishorn eru notuð sem hluti af gæðatengingu til að skilgreina magn gildandi efnislegra birgða sem verður að skoða. Sýnatökur geta verið byggðar á föstu magni, prósentu eða heillri númeraplötu.
- Stofna gæðapantanir fyrir hluta móttöku. Til að búa til gæðapöntun sem byggir á magninu sem er efnislega tekið frá fyrir pöntun, þarf að velja gátreitinn **Fyrir hvert uppfært magn** á síðunni **Sýnataka vöru**.
- Stofna prófunargerðir sem innihalda lágmark, hámark og markprófunargildi og framkvæma eigindlega-samanborið við-eigindlega prófun sem hefur fyrirfram skilgreindar niðurstöður villuleitar.
- Tilgreina viðunandi gæðastig (AQL) til að stjórna vikmörkum gæðaráðstafana.
- Tilgreina tilföng sem skoðunaraðgerð krefst, eins og prófunarsvæði og prófunartæki.

> [!NOTE]
> Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferla_ eykur möguleika gæðastjórnunar. Ef þú ert að nota þennan eiginleika skaltu skoða [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md) fyrir dæmi sem sýnir hvernig gæðastjórnun virkar þegar hún er virkjuð.

## <a name="controlling-the-quality-management-process"></a>Stjórna Gæðastjórnunarferli

Hér eru nokkrar aðferðir til að stjórna gæðastjórnunarferli:

- Stofna gæðapantanir sem byggja á kveikjupunktum, eins og "við móttöku afurða" fyrir aðgerðum á innleið eða "þegar afurð er sótt" fyrir aðgerðir á útleið.
- Skrá niður niðurstöður prófana, og ákvarða hvort að niðurstöðurnar uppfylla fyrirframákveðnum próunarskilyrði, og viðunandi gæðastig.
- Nota skjalastjórnun fyrir nákvæmar lýsingar afurðar og notandatengdum athugasemdir sem hluti af skráningu við skoðunarferli.
- Viðhalda ósamkvæmum afurðum og setja þessar afurðir í samhengi við viðbótar ósamkvæmiupplýsingar til að rekja upprunalegu orsök vandamáls.
- Skrá Kostnaður við stjórnun ósamkvæmni. Kostnaðurinn innifelur vörurnar, (eins og varahluti) og mismunandi gjöld, og vinnustundir á vinnuskýrslu sem krafist er til að leiðrétta ósamkvæmninni.
- Áætlua villuleiðréttingarferli með því að nota leiðréttingarmeðhöndlun sem er tengd gæðapantanir.

[![Gæðastjórnunarferli.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Afurðaprófanir og gæðapantanir

Vöruprófun kallast venjulega gæðaeftirlit og notar gæðapantana . Með því að nota virkni gæðaeftirlits er hægt að gera eftirfarandi:

- Skilgreina prófanir sem þarf að framkvæma fyrir efni. Þessar prófanir innihalda gæðaforskriftir, viðeigandi prófverkfæri, skjöl sem lýsa prófi, úrtaksáætlun, og gæðastig.
- Stofna gæðapöntun sem tilgreinir þær prófanir sem þarf að gera fyrir tiltekna pöntun (til dæmis innkaupa- eða framleiðslupöntun) eða tiltekið birgðamagn. Gæðapöntun má stofna handvirkt eða gæðapöntun sjálfvirkt samkvæmt gæðareglum.
- Skilgreina gæðareglur sem tengjast tengdu innkaupum, biðgeymslu, framleiðslupöntunum eða sölupöntunum í hverju viðskiptaferli, fyrir sjálfvirka myndun gæðapöntunar sem tilgreinir kröfur fyrir prófun á magni á inn- eða útleið.
- Skrá niðurstöður prófana í gæðapöntun, bera niðurstöðurnar saman við viðunandi gæðastig og prenta greiningarskírteini sem sýnir niðurstöður prófunarinnar.

## <a name="nonconformance"></a>Ósamkvæmni

Ósamkvæmni lýsir vöru með gæðavandamál. Ósamkvæmniferli gerir notendum kleift að stofna ósamkvæmnipöntun sem lýsir magni ósamkvæms efnis með uppruna vandans, gerð vandans og útskýringum. Hægt er að skilgreina flokkun á gerðum vanda fyrirfram fyrir greiningu á ósamkvæmu efni auðveldari. Einnig er hægt að prenta ósamkvæmnimerki og ósamkvæmniskýrslu til að veita leiðbeiningar um niðurskipan fyrir ósamkvæmu efni. Til dæmis, gætu merki og skýrslu gefið til kynna **ónýtanlegt** eða **Takmarkaðar notkun**.

Í eftirfarandi töflu er listi yfir sex sjálfgefnar gerðir ósamkvæmni og lýsir upplýsingar sem verður að vera skráð fyrir hverja tegund.

| Gerð ósamkvæmni | Upprunaupplýsingar |
|---|---|
| Viðskiptavinur | Lykilnúmer viðskiptavinar, sölupöntunarnúmer eða lotunúmer sölupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni sölupöntunarsendingu eða ábendingu viðskiptavinar um gæði vöru. |
| Þjónustubeiðni | Lykilnúmer viðskiptavinar, sölupöntunarnúmer eða lotunúmer sölupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni sölupöntunarsendingu eða kvörtun viðskiptavinar um gæði vöru. |
| Lánardrottinn | Lykilnúmer viðskiptavinar, innkaupapöntunarnúmer eða lotunúmer innkaupapöntunarfærslu. Til dæmis gæti ósamkvæmni átt við um móttöku innkaupapöntunar eða áhyggna lánardrottins varðandi hlut sem hann veitir. |
| Framleiðsla | Framleiðslupöntunarnúmer eða lotunúmer framleiðslupöntunarfærslu. Til dæmis gæti ósamkvæmni tengst tiltekinni runu sem var framleidd. |
| Innra | Gæðapöntunarnúmer eða lotunúmer gæðapöntunarfærslu. Til dæmis gæti ósamkvæmni tengst prófunum sem eru framkvæmd sem hluti af gæðapöntun eða áhyggjum starfsmanns um gæði vöru. |
| Framleiðsla aukaafurðar | Ósamkvæmni aukaafurðar framleiðslupöntunar sem er tengd framleiðslupöntun runu. |

Ósamkvæmni er tengd við gerð vandamáls. Gerðir vandamála eru skilgreindar í á **gerðir Vandamála** síðuna þar sem tilgreint er hvaða gerðir vandamála getur verið tengt við hverja gerð ósamkvæmni. Til dæmis gætu gerðir vandamála fyrir ósamkvæmni fyrir gerina **þjónustubeiðna** endurspeglað flokkun fyrir kvartanir viðskiptavina, en hinsvegar gerðir ósamkvæmni fyrir gerina **innra** gætu staðið fyrir flokkun á gallakóðum.

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

## <a name="additional-resources"></a>Frekari upplýsingar

- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Stöðvun í birgðum](inventory-blocking.md)
- [Biðgeymslupantanir](quarantine-orders.md)
- [Kanna vörugæði](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
