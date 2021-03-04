---
title: Yfirlit yfir skráningu tíma og mætingu
description: Starfsmaður sem sinnir tímaskráningu getur fært inn mismunandi gerðir tímaskráningar, til dæmis innstimplun, útstimplun, skráningu óbeinna aðgerða og fjarvistarskráningu. Þetta efnisatriði lýsir skráningum, útreikningi þeirra, samþykki og notkun verkflæðis til að bæta skipulag og sjálfvirku samþykki ferlisins að samþykkja vinnuskýrslur.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr, JmgRegistrationSetup, JmgStampTrans, JmgStampJournalTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6fa5715a04aa8077651f5c6e29e6bca83d763c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430378"
---
# <a name="time-and-attendance-registration-overview"></a>Yfirlit yfir skráningu tíma og mætingu

[!include [banner](../includes/banner.md)]

Starfsmaður sem sinnir tímaskráningu getur fært inn mismunandi gerðir tímaskráningar, til dæmis innstimplun, útstimplun, skráningu óbeinna aðgerða og fjarvistarskráningu. Þetta efnisatriði lýsir skráningum, útreikningi þeirra, samþykki og notkun verkflæðis til að bæta skipulag og sjálfvirku samþykki ferlisins að samþykkja vinnuskýrslur. 

<a name="registrations"></a>Skráningar
-------------

Í fyrirtækjum sem nota Tíma og viðveru þurfa starfsmenn að skrá tíma sem°þeir eru í vinnu°auk°viðveru. Starfsmenn í sumum fyrirtækjum þurfa jafnvel aðeins að skrá sig þegar þeir stimpla sig inn og út. Í öðrum fyrirtækjum kunna starfsmenn einnig að þurfa að skrá tímanotkun í raunverulega verkþætti sem þeir framkvæma ásamt pásum sem teknar eru. Tími og viðvera er ætlað fyrir:
-   Starfsmenn sem eiga að skrá tíma og viðveru með reglulegu millibili, til dæmis daglega, vikulega eða hálfsmánaðarlega.
-   Yfirmenn, stjórnendur og launafulltrúa sem reikna, samþykkja og flytja starfsmannaskráningar til frekari vinnslu.

| **Ábending**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ef Tími og viðvera er keyrð með Framkvæmdarferli framleiðslu, munu allar skráningar á verkum, verkþáttum, óbeinum verkþáttum, fjarvistarkóðum og yfirvinnu og sveigjanlegum tíma verða skráð og eru notaðir til að reikna út laun°í báðum kerfum. |

## <a name="time-registrations-workers"></a>Starfsmenn í tímaskráningu
Til að hægt sé að skrá tíma og fjarvistir, verður að setja starfsmenn upp sem starfsmenn í tímaskráningu í fyrirtækinu sem þeir starfa í.

Eftir uppsetningu, geta starfsmenn fært inn ólíkar gerðir skráninga.

-   Innstimplun- og útstimplun þegar komið er til eða farið frá vinnu.
-   Tíma- og notkun á vörum í framleiðsluvinnslu.
-   Tími á vél í vinnslusal, ef vél hefur verið skilgreind sem tilfang.

| **Ábending**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hægt er að úthluta starfsmanni sjálfkrafa tímaskráningu sem gerðar eru á tiltekinni vél í vinnslusal, ef starfsmaðurinn velur að vinna sem aðstoðarmaður á vél þegar hann eða hún°hefur framleiðsluvinnslu. |

-   Tímaskráningar á verk og verkþætti.
-   Skrá verkgjöld og vörunotkun með þóknanabækur viðeigandi verk og verkbækur vöru.
-   Áætlaðar fjarvistir.
-   Fjarvistir þegar mætt er seint til vinnu eða vinna yfirgefin fyrr en áætlað.
-   Vinnuhlé, skráð handvirkt eða sjálfkrafa reiknuð út af kerfinu.
-   Óbeinir verkþættir, sem eru óframleiðnir verkþættir sem starfsmaður gæti tekið þátt í í vinnudeginum. Dæmi um þessar aðgerðir eru fundir eða°hreinsun á vinnusvæði.
-   Yfirvinna, sem°hægt er að skrá annaðhvort sem aukavinnu, með sveigjanlegan vinnutíma eða yfirvinnu.

## <a name="adding-clock-out-registrations"></a>Bæta við útstimplun sem vantar
Ef starfsmaður gleymir að stimpla út í lok vinnudags, er hægt að bæta við skráningu sem vantar með því að keyra runuvinnslu. Kerfið mun bera saman innstimplun og útstimplun tíma samkvæmt tengdum forstillingum starfsmanns og setja sjálfvirkt inn í útstimplun sem vantar til að jafna lokatíma forstillingar. Bæði innstimplunar og útstimplunar skráningar eru nauðsynlegar fyrir síðari útreikning og samþykkt tímaskráningar áður en hægt er að flytja þær í launavinnslu.

## <a name="calculating-registrations"></a>Reikna skráningar
Þegar skráningu starfsmanns er úthlutað á flokk útreiknings sem vanalega tengist ákveðnu teymi, vakt eða vinnuflokki. Stjórnandi hópsins eða yfirmaður staðfestir yfirleitt skráningar eftir starfsmenn og er því einnig ábyrgur fyrir að keyra útreikning fyrir viðkomandi reikniflokka daglega. Sem hluti af útreikningi geta stjórnandi hópsins eða yfirmaður:
-   Leiðrétt ranga skráningu. Til dæmis er hægt að breyta skiptikóða°og°leiðrétta svörun á framleiðsluvinnslu.
-   Bætt við skráningu sem vantar. Til dæmis er hægt að stofna útstimplanir og stofna fjarvistafærslur.
-   Eyða rangri skráningu.

Þar sem skráður tími verður að passa við forstillingu vinnutíma starfsmanns fyrir útreikning á skráningum, verður að hnekkja forstillingu vinnutíma fyrir hvaða starfsmann sem hefur undantekningu á stöðluðum vinnutíma. Í því tilfelli þar sem forstilling starfsmanns er dagvakt, og starfsmaður hefur samþykkt að vinna næturvakt með engin yfirvinnulaun, verður stjórnandi hópsins eða yfirmaður að hnekkja sjálfgefinni forstillingu starfsmanns til að reikna út vinnutíma á stöðluðum næturtaxta og ekki sem yfirvinnu. Við útreikning birtist einnig villa ef fjarvistarskráningu vantar. Það°verður að bæta henni við áður en hægt er að ljúka útreikningnum.

## <a name="approving-registrations"></a>Samþykkja skráningar
Rétt eins og reikniflokki er úthlutað á starfsmann með tímaskráningu verður að úthluta samþykkisflokk einnig. Flokkurinn er yfirleitt sértækur fyrir teymi, vakt eða vinnuflokk. Samþykkja tímaskráningar sem reiknaður var rétt – þetta þýðir að gera útreikning án villna – áður en hægt er að mynda laun sem svo er hægt að flytja í launakerfi. Yfirmaður launa mun venjulega samþykkja skráningar og fyrir samþykkt getur hann:
-   Hnekkt launasamningum einstakra starfsmanna.
-   Bætt við handvirkum kaupaukum.
-   Fært inn viðbótarupplýsingar um fjarvistarskráningar.

| **Ábending**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ef yfirvinna hefur verið reiknuð fyrir einstaka starfsmenn er hægt að úthluta yfirvinnunni á einstakar vinnslur yfir daginn. Þetta á við ef vinnslukostnaður er reiknaður út frá launum starfsmanna. |

## <a name="approving-registrations-using-workflow"></a>Samþykkja skráningar með því að nota verkflæði
Hægt er að setja upp verkflæði samþykktarferli sem samþykkir sjálfkrafa skráningar sem samræmast reglum um verkflæði, og skilur aðeins eftir frávik til að meðhöndla handvirkt. Ef verkflæðissamþykki er virkjað, mun yfirmaður hópsins eða yfirmaður senda reiknaðar skráningar til samþykkis. Vinnuflæði stofnar viðeigandi samþykki og verkefni og°úthlutar þeim síðan til viðeigandi notenda og hlutverka eins og skilgreint er í vinnuflæðinu. Tvö verkflæðissamþykki eru fyrir tíma og viðveru.

| Verkflæði                                  | Tilgangur                                                                                                   | Skráningargerð                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ráðstafa dagasamtölu tíma og viðveru            | Verkflæði staðfestir skráningu gagnvart, t.d. væntanlegum fjölda vinnustunda yfir daginn. |                                                                                                                                                                                                                                                       |
| Skráning aðgerðatíma og viðveru í færslubók. | Verkflæði staðfestir hverja gerð skráningar fyrir dagsetningu skráningar.                           | Tími og mæting • innstimplun • útstimplun • Fjarvistir • Hlé • Skiptkóði • Verk • verkþáttar • Framleiðsluvinnsla óbeins verkþáttar • Biðröð fyrir • Uppsetning • Ferli • Skörun • Flutningur • Biðröð eftir • Ræsa aðstoð • Stöðva aðstoð |



## <a name="transferring-approved-registrations"></a>Flutningur skráðra samþykkta
Eftir að skráningar eru samþykktar er hægt að færa þær í°reglubundnar launavinnslur. Flutt skráning er bókuð á verkþátt eða starf sem hún tengist, til dæmis, framleiðslupöntun eða verki. Launafærslur eru myndaðar fyrir hvern starfsmann samkvæmt skráningunni.  

## <a name="reversing-transferred-registrations"></a>Bakfæra flutta skráningu.
Hægt er að gera verkið að bakfæra færslur – afturkalla þær – þar til flutningur launa fyrir launatímabilið er keyrður. Þetta þýðir að launagögn hafi verið flutt í ytri skrá. Við bakfærslu eru allar skráningar teknar til baka og færslur sem bókaðar hafa verið á tilteknar framleiðslupantanir eða verk eru mótfærðar og þannig núllaðar út.

| **Ábending**                                                 |
|----------------------------------------------------------|
| Hægt er að flytja ytri skrá inn í launakerfið. |

## <a name="registrations-in-electronic-timecards"></a>Skráningar rafræns stimpilkorts.
Starfsmönnum með verkefni sem krefjast ekki tafarlausra viðbragða, svo sem við vinnslur, en sem°vinna við verkþætti, getur notið góðs af því að nota rafræna stimpilkortið. Rafræn stimpilkort bjóða sveigjanleika til að færa inn skráningar hvenær sem er og á bestan hátt fyrir viðskiptaáætlun°þína– daglega, vikulega eða þegar starfsmaður er aftur kominn til vinnu eftir að hafa verið frá. Til að nota rafræn stimpilkort fyrir þessa starfsmenn, verður að tilgreina, Nota stimpilkort,°í upplýsingar starfsmanna. Rafræn stimpilkost gefa starfsmanninum tækifæri til að skrá:

-   Dagsetning
-   Skráningargerð
-   Vinnslutilvísun, svo sem verk, framleiðslupöntun eða óbeinan verkþátt
-   Vinnslukenni
-   Tímanotkun
-   Þóknun fyrir verk
-   Verkatriði






[!INCLUDE[footer-include](../../includes/footer-banner.md)]