---
title: Færibreytuuppsetning kreditstjórnunar
description: Þetta efni lýsir valkostunum sem þú getur notað til að stilla lánastjórnun til að uppfylla kröfur fyrirtækisins.
author: mikefalkner
manager: AnnBe
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c4930d346ddc4679e6a3196c5f35adb598ed38c1
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651906"
---
# <a name="credit-management-parameters-setup"></a>Færibreytuuppsetning kreditstjórnunar

[!include [banner](../includes/banner.md)]

Þetta efni lýsir valkostunum sem þú getur notað til að stilla lánastjórnun til að uppfylla kröfur fyrirtækisins. Til að nota aðgerðir fyrir kreditstjórnun skaltu setja upp færibreyturnar á síðunni **Færibreytur skulda og innheimtu** (**Skuldir og innheimta \> Uppsetning \> Færibreytur skulda og innheimtu**).

## <a name="credit-parameters"></a>Kreditfæribreytur

Það eru fjórir flýtiflipar í hlutanum **Kredit** þar sem hægt er að breyta færibreytum sem stjórna kreditstjórnun: **Lán í biðstöðu**, **Gátstaður lánastýringar**, **Talnagögn lánastýringar** og **Lánamörk**. Eftirfarandi hlutar lýsa stillingum sem eru fáanlegar á hverjum flýtiflipa.

### <a name="credit-holds"></a>Lán í biðstöðu

- Stillið valkostinn **Leyfa breytingu á virði sölupantana þegar biðstaða pöntunar er losuð** á **Nei** til að krefjast þess að bókunarreglur verði aftur athugaðar ef gildi sölupöntunar (heildarverðs) hefur hækkað frá því að sölupöntunin var losuð úr biðlistanum. .
- Í reitnum **Ástæður niðurfelldra pantana** velurðu losunarástæðuna sem verður sjálfkrafa notuð þegar sölupöntun sem var í lánastýringarbið er felld niður.
- Stilltu valkostinn **Athuga lánamörk viðskiptavinahópa** á **Já** til að athuga lánamörk viðskiptavinahóps þegar viðskiptavinurinn í sölupöntun tilheyrir lánshópi viðskiptavina. Lánamörk hópsins verða athuguð og síðan, ef það er nægjanlegt, verður lánsfjárhæðin fyrir viðskiptavininn athuguð.
- Stilltu valkostinn **Athuga lánamörk þegar greiðsluskilmálar eru hækkaðir** á **Já** til að kanna röðun á greiðsluskilmálum til að ákvarða hvort greiðsluskilmálar í sölupöntuninni eru frábrugðnir sjálfgefnum greiðsluskilmálum fyrir viðskiptavininn. Ef nýju greiðsluskilmálarnir eru hærri en upphaflegir greiðsluskilmálar, þá er pöntunin sett á kreditstjórnunarbið.
- Stilltu valkostinn **Athuga lánamörk þegar uppgjörsafsláttur er hækkaður** á **Já** til að kanna röðun á uppgjörsafslætti til að ákvarða hvort staðgreiðsluafsláttur í sölupöntuninni eru frábrugðinn sjálfgefnum staðgreiðsluafslætti fyrir viðskiptavininn. Ef nýi staðgreiðsluafslátturinn er hærri en upphaflegur staðgreiðsluafsláttur, þá er pöntunin sett á kreditstjórnunarbið.
- Í reitnum **Ástæða fyrir losun á breyttum pöntunum** velurðu losunarástæðuna sem verður sjálfkrafa notuð þegar breyttar pantanir eru sjálfkrafa gefnar út úr lánastýringarstjórninni.
- Stilltu valkostinn **Hunsa útrunna lokunarreglu lánamarka þegar gildistími er auður** á **Já** til að stjórna hegðun reglunnar **Lánamark rann út**. Stilltu valkostinn á **Nei** til að loka fyrir pöntun þegar gildistími er auður.
- Í vöruhúsastjórnun er hægt að búa til farm við sölupöntunarfærslu. Stilltu valkostinn **Fjarlægja læstar farmlínur** á **Nei** til að láta sölupöntunarlínur vera á farminum þegar sölupöntun er í kreditbið. Ekki er hægt að vinna með álagið meðan sölupöntunin er í bið. Stilltu valkostinn á **Já** til að fjarlægja sölupantanalínur úr farminum þegar sölupöntun er í kreditbið. Síðan er hægt að vinna úr álaginu.
- Sölupöntunum er hægt að losa sjálfkrafa við yfirferð lánamála. Í reitnum **Ástæða til að losa sjálfkrafa** velurðu losunarástæðuna sem verður sjálfkrafa notuð þegar sölupantanir eru losaðar sjálfkrafa.
- Sölupöntunum er hægt að losa sjálfkrafa við yfirferð lánamála. Í reitnum **Sjálfvirk losun** velurðu **Án bókunar** til að losa bið á pöntun. Þú verður að keyra handvirkt ferlið sem setur pöntunina í bið. Veldu **Með bókun** til að bóka pöntunina með því að nota sama bókunarferli og var keyrt þegar sölupöntunin var sett í bið.

### <a name="credit-management-checkpoint"></a>Gátstaður lánastýringar

Þú getur stillt tímasetningu sem er notuð til að athuga sölupantanir vegna lánamála. Flýtiflipinn **Greiðslumark lánamála** auðkennir bókunarferli skjala sem fela í sér vinnslu á lánastjórnunarreglum. Þú getur einnig athugað lánsreglurnar á meðan þú annaðhvort birtir bókun bráðabirgðareiknings eða fulla bókun sölupöntunarinnar. Veldu gátreitina til að skilgreina bókunarferla sem ættu að setja pöntun í bið ef vandamál er að finna eftir að reglur um útlán á lánamálum eru unnar.

Þú getur einnig skilgreint fjölda biðdaga áður en lánsreglurnar eru athugaðar aftur. Þó að þú getir tilgreint að kreditstýringarreglurnar séu merktar við bókunina verða reglurnar ekki skoðaðar í tiltekinn fjölda biðdaga. Til dæmis staðfestir þú sölupöntun á fyrsta degi og þú tilgreinir tvo biðdaga fyrir staðfestingarskrefið. Í þessu tilfelli verða lánareglur ekki merktar við næsta póstskref (til dæmis að búa til pakkningaseðil eða reikning á pöntuninni) fyrr en á 4. degi. Á eða eftir dag 4 verða reglurnar athugaðar aftur þegar bókun á sér stað og fjölda biðdaga verður breytt í gildi sem er tilgreint fyrir næsta gátstað fyrir bókun.

Ef þú tilgreinir ekki fjölda biðdaga verður kreditreglurnar athugaðar við hvert bókunarskref sem er sett upp til að keyra reglur um lánamál. Ef þú sleppir sölupöntuninni án þess að pósta og keyrir aftur sama pöntunarvinnsluskref, verður kreditreglurnar athugaðar aftur. Til dæmis er pöntun sett í bið eftir staðfestingu og þú sleppir henni annaðhvort með eða án bókunar. Í þessu tilfelli verður pöntunin sett í bið aftur ef þú staðfestir hana aftur. Notaðu biðdaga ef pöntunin ætti að fara yfir í næsta vinnsluskref án þess að fara aftur í bið.

Þú getur ekki tilgreint biðdaga fyrir suma gátstaði bókunar en ekki fyrir aðra. Þú verður að setja upp alla gátstaði bókunar þannig að þeir hafi biðdaga, eða þú verður að setja þá alla upp svo þeir eigi ekki biðdaga.

- Veldu gátreitinn **Bókun** til að keyra reglurnar um lánastjórnun þegar gátreitur bókunar sem er sýndur á línunni er keyrður. Ef þú velur ekki gátreitinn verða reglurnar aðeins merktar einu sinni á öllu bókunarferlinu.
- Ef þú velur gátreitinn **Bókun** tilgreinirðu fjölda biðdaga sem ættu að líða áður en lokunarreglurnar eru merktar aftur. Þú getur ekki bætt við biðdögum ef gátreiturinn **Bókun** er hreinsaður.
- Veldu gátreitinn **Bráðabirgðareikningur** til að keyra reglurnar um lánastjórnun þegar gátreitur bráðabirgðareiknings sem er sýndur á línunni er keyrður. Í flestum tilvikum er reiturinn **Bókun** er stillt á **Nei** í glugganum sem birtist þegar sölupöntun er bókuð.
- Ef þú velur gátreitinn **Bókun** tilgreinirðu fjölda biðdaga sem ættu að líða áður en lokunarreglurnar eru merktar aftur. Þú getur ekki bætt við biðdögum ef gátreiturinn **Bókun** er hreinsaður.

### <a name="credit-management-statistics"></a>Talnagögn lánastýringar

Nokkrar tölfræði um lánastjórnun er að finna í upplýsingareitnum **Tölfræði um stjórnun lána viðskiptavina** á síðunni **Viðskiptavinur**. Þú verður að tilgreina nokkur gildi sem þarf til að reikna út þessa tölfræði. Sláðu inn fjölda mánaða sem er notaður til að reikna eftirfarandi gildi í upplýsingareitnum **Tölfræði um stjórnun lána viðskiptavina**:

1. Dagar útistandandi sölu 1
2. Dagar útistandandi sölu 2
3. Meðaljöfnuður 1
4. Meðaljöfnuður 2
5. Meðalkreditmörk %
6. Meðaláhætta %

### <a name="credit-limits"></a>Lánamörk

- Í lánastjórnun er lánsheimild viðskiptavinarins sýnd í gjaldmiðli viðskiptavinarins. Þú verður að skilgreina gerð gengis fyrir lánamörk í gjaldmiðli viðskiptavinarins. Í reitnum **Gerð lánsfjárhámarks** velurðu þá gerð gengis sem ætti að nota til að umbreyta aðal lánsfjárhámarki í lánamörk viðskiptavinarins.
- Stilltu valkostinn **Leyfa handvirka klippingu á lánamörkum** á **Nei** til að koma í veg fyrir að notendur geti breytt kreditmörkum á síðunni **Viðskiptavinur**. Ef þessi valkostur er stilltur á **Nei** er aðeins hægt að gera breytingar á lánamörkum viðskiptavinar með því að birta leiðréttingarfærslur lánamarka.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Númeraraðir og samnýttar færibreytur númeraraða

Auðkenni dagbókar er krafist til að vinna úr leiðréttingum á lánamörkum. Þú verður að bæta við leiðréttingarnúmeri fyrir lánsfjárhæð sem ætti að nota til að búa til dagbókarauðkenni.
