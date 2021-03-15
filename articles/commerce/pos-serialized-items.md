---
title: Vinna með raðaðar vörur á sölustaðnum
description: Í þessu efnisatriði er útskýrt hvernig á að stjórna röðuðum vörum í forriti sölustaðar.
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0431ffa45eceac5c12d8ed991b00730c50ca62f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972556"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Vinna með raðaðar vörur á sölustaðnum

[!include [banner](includes/banner.md)]

Margir smásalar selja vörur sem krefjast raðstjórnunar. Þessar vörur eru nefndar *raðaðar vörur*. Sumir smásalar gætu viljað viðhalda raðnúmerum í verslun eða vöruhúsabirgðum til rakningar. Aðrir smásalar gætu viljað sækja raðnúmer í söluferlinu vegna þjónustu og ábyrgðar. Í þessu efnisatriði er útskýrt hvernig þú getur stjórnað röðuðum vörum í Microsoft Dynamics 365 Commerce forriti sölustaðar.

## <a name="serial-number-configurations"></a>Skilgreiningar raðnúmers

Vara er talin röðuð vöru ef henni hefur verið úthlutað rakningarvíddarflokki sem er settur upp til að heimila raðnúmer. Í höfuðstöðvum Commerce, á síðunni **Rakningarvíddarflokkar**, skal velja valkostinn **Virkt** til að leyfa raðnúmer fyrir birgðaferli, eða velja **Virkt í söluferli** valkostinn til að leyfa raðnúmer fyrir söluferli.

Í flýtiflipanum **Rakningarvíddir**, skal kveikja á færibreytunni **Auð innhreyfing heimil** til að leyfa valkvæman innslátt raðnúmers við birgðamóttöku raðaðra vara. Ef slökkt er á þessari færibreytu þarf að slá inn raðnúmer. Á sama hátt stjórnar færibreytan **Auð úthreyfing heimil** því hvort raðnúmer er nauðsynlegt á meðan verið er að senda birgðir.

> [!NOTE]
> Til að nota **Birgðir á innleið** og **Birgðir á útleið** aðgerðir í sölustað til að skrá eða staðfesta raðnúmer gegn raðaðri vöru, verður þú að stilla vöruna þannig að henni sé úthlutað rakningarvíddarflokki sem eru uppsettur þannig að hann leyfi raðnúmer fyrir valkostinn **Virkt** og ekki valkostinn **Virkt í söluferli**.

## <a name="serial-number-management-page"></a>Stjórnunarsíða raðnúmers

Í **Birgðir á innleið** og **Birgðir á útleið** aðgerðir í sölustað, ef varan sem verið er að taka á móti, senda eða velja er vara með raðnúmer inniheldur **Upplýsingasvæðið** valkostinn **Stjórna raðnúmeri** sem tengist **Stjórnunarsíða raðnúmers** þar sem þú getur skráð eða staðfest raðnúmer fyrir vöruna. Að öðrum kosti er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort með því að velja **Raðnúmer** aðgerðina í forritastiku fyrir yfirlit pöntunarupplýsinga eða með því að velja **Stjórna raðnúmeri** valkostinn í svarglugganum sem birtist þér í móttöku- eða sendingarferlinu. 

Síðan **Stjórnun raðnúmers** sýnir allar opnar línur raðnúmers sem bíða skráningu eða staðfestingar. Það kunna að vera tveir flipar á þessari síðu: einn fyrir núverandi vöru og annar fyrir allar raðaðar vörur í pöntuninni.

Reiturinn **Staða** á síðunni **Stjórnun raðnúmers** veitir upplýsingar um núverandi stöðuna á hverju raðnúmeri fyrir sig í:

- **Ekki skráð** - Ekki hefur verið útvegað raðnúmeri eða forskráð raðnúmer hefur ekki verið staðfest (í móttökuferli).
- **Skráning** – Raðnúmerið hefur verið skráð og vistað staðbundið í gagnagrunnsrás verslunarinnar eða forskráð raðnúmer hefur verið staðfest. Aðeins raðnúmer með stöðuna **Skráning** verða send til höfuðstöðva Commerce þegar móttöku eða uppfyllingu lýkur.

## <a name="receive-serialized-items"></a>Móttaka á röðuðum vörum

Aðgerðin **Birgðir á innleið** í sölustað gerir notendum kleift að framkvæma eftirfarandi verk fyrir raðaðar vörur:

- Skrá raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun.
- Staðfesta forskráð raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun eða flutningspöntun.

### <a name="register-serial-numbers-against-serialized-items"></a>Skrá raðnúmer á móti röðuðum vörum

Fyrir innkaupapöntun birtist svargluggi með **Stjórna raðnúmeri** valkostinum meðan á móttökuferlinu stendur fyrir raðaða vöru. Hægt er að velja þann valkost til að opna síðuna **Stjórnun raðnúmers** og hefja skráningu raðnúmera. Einnig er hægt að sleppa þessu skrefi í móttökuferlinu og gefa upp innsláttinn seinna, áður en móttakan er bókuð.

Sjálfgefið er að flipinn fyrir núverandi vöru er sýndur. Allar raðnúmeralínur eru með autt raðnúmer og stöðuna **Ekki skráð**. Hægt er að gefa strikamerkjum raðnúmer eða velja **Raðnúmer** í forritastikunni til að halda áfram að slá inn raðnúmer. Raðnúmerin sem slegin eru inn birtast í listanum og staða þeirra breytist í **Skráir**. Hámarksfjöldi raðnúmera sem hægt er að skrá í listanum samsvarar móttökumagninu. Ef mistök eru gerð er hægt að velja **Breyta** eða **Hreinsa** á svæðinu **Upplýsingar** til að gera breytingar á raðnúmerunum sem voru slegin inn.

Einnig er hægt að skrá raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að skráð raðnúmer fyrir af listanum.

### <a name="validate-serial-numbers-on-serialized-items"></a>Villuleita raðnúmer á númeruðum atriðum

Fyrir flutningspöntun verður að forskrá raðnúmer á röðuðum vörur fyrir hlutann sem er á útleið í sendingarferlinu. Fyrir innkaupapöntun gæti birginn útvegað upplýsingar um raðnúmer í gegnum ítarlega sendingartilkynningu og hægt er að forskrá númerin á vörunum sem verða send. Í báðum tilvikum eru raðnúmerin þekkt á undan móttökunni. Þess vegna þarf í hluta innleiðar aðeins að staðfesta að tekið hafi verið á móti því sem átti að taka á móti.

Til að staðfesta raðnúmer er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort í móttökuferlinu eða hvenær sem er áður en móttakan er bókuð. Fyrir hverja raðaða vöru sem er með forskráð raðnúmer eru öll raðnúmerin sjálfkrafa stillt á upphafsstöðuna **Ekki skráð** á þessari síðu. Til að staðfesta raðnúmer er hægt að skanna eða slá þau inn. Þar sem raðnúmer er slegin inn staðfestir forritið hvort þau samsvari forskráðum raðnúmerum. Ef þau stemma er stöðu þeirra breytt í **Skráir**. Annars færðu villuboð. Einnig er hægt að velja raðnúmer beint og velja svo valkostinn **Staðfesta raðnúmer** á **Upplýsingasvæði** til að merkja á fljótlegan hátt raðnúmerið sem staðfest. Hámarksfjöldi raðnúmera sem hægt er að staðfesta í listanum samsvarar móttökumagninu.

Einnig er hægt að staðfesta raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að staðfesta raðnúmer fyrir af listanum.

## <a name="ship-serialized-items"></a>Senda raðaðar vörur

Hægt er að nota **Birgðir á útleið** aðgerð í sölustað til að skrá raðnúmer á móti vörum með raðnúmerum þegar þær eru fluttar úr núverandi verslun í gegnum flutningspöntun.

### <a name="register-serial-numbers-against-serialized-items"></a>Skrá raðnúmer á móti röðuðum vörum

Fyrir flutningspöntun birtist svargluggi með **Stjórna raðnúmeri** valkostinum meðan á sendingarferlinu stendur fyrir raðaða vöru. Hægt er að velja valkostinn til að opna síðuna **Stjórnun raðnúmers** og hefja skráningu raðnúmera. Einnig er hægt að sleppa þessu skrefi í sendingarferlinu og gefa upp innsláttinn seinna, áður en sendingin er bókuð.

Sjálfgefið er að flipinn fyrir núverandi vöru er sýndur. Allar raðnúmeralínur eru með autt raðnúmer og stöðuna **Ekki skráð**. Hægt er að gefa strikamerkjum raðnúmer eða velja **Raðnúmer** í forritastikunni til að halda áfram að slá inn raðnúmer. Raðnúmerin sem slegin eru inn birtast í listanum og staða þeirra breytist í **Skráir**. Hámarksfjöldi raðnúmera sem hægt er að skrá í listanum samsvarar sendingarmagninu. Ef mistök eru gerð er hægt að velja **Breyta** eða **Hreinsa** á svæðinu **Upplýsingar** til að gera breytingar á raðnúmerunum sem voru slegin inn.

Einnig er hægt að skrá raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að skráð raðnúmer fyrir af listanum.

Einnig er hægt að virkja staðfestingu tiltækis raðnúmers við skráningu raðnúmers geng flutningspöntun á útleið. Með þessari staðfestingu, ef reynt er að senda raðnúmer sem er ekki í boði í birgðum sendingar birtast villuboð og gefa verður upp annað númer.

Til að virkja slíka staðfestingu þarf að áætla eftirfarandi verk til að keyra á endurteknum grunni:

- **Retail og Commerce** > **Upplýsingatækni Retail og Commerce** > **Vörur og birgðir** > **Afurðaframboð með rakningarvíddum**
- **Retail og Commerce** > **Dreifingaráætlanir** > **1130** (**Afurðarframboð**)

## <a name="sell-serialized-items-in-pos"></a>Selja raðaðar vörur á sölustað

Á meðan forrit sölustaðar hefur alltaf stutt sölu á röðuðum vörum, í Commerce útgáfu 10.0.17 og nýrri, geta fyrirtæki virkjað aðgerð sem bætir viðskiptagrunninn sem ræsist þegar afurðir eru seldar sem eru stilltar á rakningu raðnúmers.

Þegar eiginleikinn **Bætt prófun raðnúmers þegar pantanir eru sóttar og uppfylltar á sölustað** er virkjaður eru eftirfarandi afurðarafbrigði metin þegar raðaðar afurðir eru seldar á sölustað:

- Uppsetningin **Gerð raðar** fyrir afurð (**virk** eða **virk í sölu**).
- Stillingarnar **Auð úthreyfing heimil** fyrir afurðina.
- Stillingin **Efnislega neikvæð birgðastaða** fyrir afurðina og/eða vöruhús sölu.

### <a name="active-serial-configurations"></a>Skilgreiningar virkrar röðunar

Þegar vörur eru seldar á sölustað sem er skilgreindur með rakningarvídd raðnúmers sem **Virka**, kveikir sölustaður á prófunarreglu sem kemur í veg fyrir að notendur ljúki sölu á raðaðri vöru með raðnúmeri sem finnst ekki í núverandi birgðum söluvöruhúss. Tvær undantekningar eru á þessari prófunarreglu:

- Ef varan er einnig skilgreind með **Auð úthreyfing heimil** virkt geta notendur sleppt innslætti raðnúmers og selt vöruna án raðnúmers.
- Ef varan og/eða söluvöruhúsið er skilgreint með **Efnislega neikvæð birgðastaða** virkt samþykkir forritið og selur raðnúmer sem ekki er hægt að staðfesta að sé í birgðum í vöruhúsinu sem það er selt úr. Þessi skilgreining leyfir að birgðafærslan fyrir þessa tilteknu vöru/raðnúmer verði neikvæð og kerfið leyfir þar af leiðandi sölu á óþekktum raðnúmerum.

> [!IMPORTANT]
> Til að tryggja að forrit sölustaðar geti staðfest almennilega hvort raðnúmerin sem verið er að selja fyrir vörur með **Virka** raðnúmeragerð séu í birgðum í söluvöruhúsi, þurfa fyrirtæki að keyra verkið **Afurðaframboð með rakningarvíddum** í Commerce Headquarters og tilheyrandi **1130** dreifingarverk afurðaframboðs í gegnum Commerce Headquarters með reglulegu millibili. Þegar nýjar raðaðar birgðir eru mótteknar inn í söluvöruhús, til þess að sölustaður geti staðfest birgðaframboð raðnúmer sem eru seld, verður yfirnotandi birgða að uppfæra reglulega gagnagrunnsrásins með nýjustu gögnum um birgðaframboð. Verkið **Afurðaframboð með rakningarvíddum** tekur skyndimynd af yfirbirgðum, þ.m.t. raðnúmerum, fyrir öll vöruhús fyrirtækis. Dreifingarvinnslan **1130** tekur þessa skyndimynd af birgðum og deilir henni með öllum skilgreindum gagnagrunnsrásum.

### <a name="active-in-sales-process-serial-configurations"></a>Skilgreiningar virkrar röðunar í söluferli

Vörur sem eru skilgreindar með röðunarvíddum sem **Virkar í söluferli** fara ekki í gegnum neinar prófunarreglur á birgðum þar sem þessi skilgreining gerir í skyn að þessi raðnúmer birgða séu ekki forskráð í birgðir og raðnúmerin eru aðeins sótt þegar sala á sér stað.  

Ef **Auð úthreyfing heimil** er einnig skilgreind fyrir skilgreindar vörur í **Virkt í söluferli**, er hægt að sleppa innslætti númers. Ef **Auð úthreyfing heimil** er ekki skilgreind krefst forritið þess að notandinn slái inn raðnúmer jafnvel þótt það verði ekki sannprófað gagnvart tiltækum birgðum.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Nota raðnúmer þegar færslur sölustaðar eru búnar til

Forriti sölustaðar biður notendur strax um að sækja raðnúmer þegar röðuðu vara er seld, en forritið leyfir notendum að sleppa innslætti raðnúmera upp að ákveðnu marki í söluferlinu. Þegar notandinn byrjar að sækja greiðslu gerir forritið kröfu um innslátt raðnúmers fyrir allar vörur sem ekki eru skilgreindar til að vera uppfylltar í gegnum sendingar eða afhendingar í framtíðinni. Allar raðaðar vörur sem eru skilgreindar fyrir staðgreiðslu eða taka með krefjast þess að notandinn sæki raðnúmerið (eða samþykki að skilja það eftir autt ef vöruafbrigðið leyfir það) áður en hann lýkur sölunni.

Fyrir raðaðar vörur sem seldur eru fyrir sótt eða sent í framtíðinni, geta notendur sölustaðar sleppt innslætti raðnúmersins og samt lokið við stofnun viðskiptavinapöntunar.   

> [!NOTE]
> Þegar raðaðar afurðir eru seldar eða uppfylltar í gegnum forrit sölustaðar er magn upp á „1“ sett inn fyrir raðaðar vörur í sölufærslunni. Þetta er vegna þess hvernig upplýsingar um raðnúmer eru raktar í sölulínunni. Þegar færsla er seld eða uppfyllt fyrir margar raðaðar vörur í gegnum sölustað verður hver sölulína aðeins skilgreind með magninu „1“. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Nota raðnúmer við uppfyllingu eða tiltekt pöntunar viðskiptavinar

Þegar pöntunarlínur viðskiptavina eru uppfylltar fyrir raðaðar afurðir með aðgerðinni **Uppfylling pöntunar** á sölustað, þá krefst sölustaður að raðnúmerið sé sótt á undan lokauppfyllingu. Ef raðnúmer var þar af leiðandi ekki gefið upp þegar pöntun var upphaflega sótt, þarf að sækja það í tiltektar-, pökkunar- eða sendingarferlum á sölustað. Prófun er gerð í hverju skrefi og notandinn verður aðeins spurður um gögn raðnúmersins, hvort það vanti eða er ekki lengur gilt. Til dæmis ef notandi sleppir tiltektar- eða pökkunarskrefunum og setur strax af stað sendingu, og raðnúmer hefur ekki verið skráð fyrir línuna, mun sölustaður krefjast þess að raðnúmerið verði slegið inn áður en lokið verður við lokaskref reiknings. Þegar framfylgja á að raðnúmerið verði sótt í aðgerðum pöntunaruppfyllingar á sölustað, eiga allar reglur sem minnst var á áður í þessu efnisatriði enn við. Aðeins raðaðar vörur sem eru skilgreindar sem **Virkar** fara í gegnum prófun á raðnúmeri birgða. Vörur sem eru skilgreindar sem **Virkar í söluferli** verða ekki staðfestar. Ef **Efnislega neikvæð birgðastaða** er leyfð fyrir **Virkar** afurðir, verður hvaða raðnúmer sem er samþykkt, óháð birgðaframboði. Fyrir bæði vörur sem eru **Virkar** og **Virkar í söluferli**, ef **Auð úthreyfing heimil** er skilgreind, getur notandi skilið raðnúmer eftir auð ef þess er óskað í tiltektar-, pökkunar- og sendingarskrefum.

Prófanir á raðnúmerum munu einnig eiga sér stað þegar notandi framkvæmir aðgerðir fyrir sótt í pöntunum viðskiptavina á sölustað. Forrit sölustaðar leyfir ekki að sótt verði klárað á raðaðri afurð nema hún standist prófanir eins og hefur verið minnst á hér áður. Prófanir byggjast alltaf á rakningarvídd afurðarinnar og skilgreiningum söluvöruhúss. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Birgðaaðgerð á innleið á sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Birgðaaðgerð á útleið á sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]