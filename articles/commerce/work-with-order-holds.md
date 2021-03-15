---
title: Skilgreina og vinna með símaverspantanir í bið
description: Þetta efnisatriði lýsir því hvernig á að vinna með biðstöðu pantana með því að nota Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 55b794029ec765162ccfca1f39f3816c6772273d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000435"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Skilgreina og vinna með símaverspantanir í bið

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum fyrir pantanir í bið sem Dynamics 365 Commerce er með fyrir símaverspantanir.

## <a name="configuring-call-center-order-holds"></a>Grunnstilling símaverspantanir í bið

Til að hægt sé að nota eiginleikum fyrir símaverspantanir í bið þarf fyrst að skilgreina biðkóða. Til að búa til sett af notendaskilgreindum biðkóðum, byggða á kröfur fyrirtækis þíns, skaltu fara í **Sala og markaðssetning** \> **Uppsetning** \> **Sölupantanir** \> **Biðkóðar pöntunar**. Þú getur valið að merkja einn af biðkóðunum sem sjálfgefinn biðkóðann með því að stilla **Sjálfgefið fyrir sölupöntun** valkostinn á **Já** fyrir hann. Þessi biðkóði verður notaður hvenær sem sölupöntun er sett í bið. Ef sölupöntun hefur frátekið birgðir, og frátekningarnar verður að fjarlægja sjálfkrafa ef pöntunin er sett í bið af sérstakri ástæðu, þá skal stilla **Fjarlægja birgðafrátekningar** valkostinn á **Já** fyrir ástæðukóðana.

Til að tilgreina gerð athugasemdar sem verður sótt þegar notendur sem setja á sölupöntun í bið færa inn valfrjálst athugasemdir, skal fara í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakrafna**, og þá, á **Söluuppsetning** flýtiflipanum, á **Almennt** flipanum, skal stilla **Gerð athugasemdar** reitinn. Notaðu **Staða sölupöntunar í bið** reitinn til að skilgreina lit sem verður notuð til að auðkenna sölupantanir sem eru í bið þegar þau eru skoðuð á **Notendaþjónusta** síðu.

Til að búa til valfrjálst sett af ástæðubiðkóðum skaltu fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Upplýsingakóðar**. Þessir upplýsingakóðar geta verið notaðir sem auka ástæðukóðar til að skilgreina aðal biðkóðann frekar. Veldu **Nýr** til að búa til ástæðukóðasett og veldu síðan **Undirkóðar** til að skilgreina lista yfir viðbótarástæður. Til að tengja einhverja upplýsingakóða sem þú skilgreinir við símaversrásina skaltu fara í **Retail og Commerce** \> **Rásir** \> **Símaver** \> **Allar símstöðvar**. Á **Almennt** flýtiflipanum skaltu stilla **Biðkóði** reitinn.

## <a name="putting-orders-on-hold"></a>Setja pantanir í bið

Pantanir sem notendur símavers búa til í bakvinnslu Commerce forritsins er hægt að setja handvirkt eða sjálfkrafa í bið við sérstökum aðstæðum.

Við pöntunarfærslu, en áður en pöntun er send inn og staðfest, gætu notendur símavers viljað handvirkt leggja pöntun í bið til að koma í veg fyrir að henni verði sleppt í vörugeymsluna til frekari vinnslu. Til dæmis gæti viðskiptavinurinn sem leggur inn pöntunina ekki verið tilbúinn til að skuldbinda sig henni eða mikilvæg gögn sem þarf til að vinna úr pöntuninni gætu vantað.

Á pöntunarfærsla síðunni, símaver notandinn getur sett pöntun í bið með því að nota **Pantanir í bið** valkost á **Sölupöntun** flipanum á pöntunarfærsla valmyndinni. Að öðrum kosti getur notandinn valið **Í bið** valmyndaratriði á **Sölupöntunarsamantekt** síðunni sem birtist þegar hann eða hún velur **Ljúka** á sölupöntun símavers.

Í báðum tilvikum opnast **Pantanir í bið** síðan. Notandinn getur síðan valið **Nýr** til að búa til bið fyrir pöntunina. Í reitnum **Biðkóði**, skal notandinn velja þann kóða sem best lýsir ástæðu fyrir bið. Í **Ástæðukóði** reitinn, notandinn getur mögulega valið viðbótarkóða til að veita annað stigs lýsingu á biðinni.

Á **Athugasemdir** flýtiflipi, í **Bið athugasemdir** reitnum, getur notandinn slegið inn viðbótar athugasemdir, óháð formi, til að gefa frekari samhengi eða upplýsingar um biðina. Þessar athugasemdir geta hjálpað öðrum notendum sem yfirfara eða vinna með pöntunina í bið síðar.

Eftir að biðupplýsingarnar eru færðar inn og vistaðar getur notandinn lokað **Pantanir í bið** síðunni. Notandinn er síðan færður aftur inn á síðu sölupöntunarfærslu. Ef ekki er þörf á frekari aðgerðum á sölupöntuninni, getur notandinn lokað síðu sölupöntunarfærslu.

Ef kveikt er á **Virkja lok pöntunar** flaggi á símaversrásinni, þarf ekki að virkja greiðslu fyrir pöntun sem er sett í bið. Hins vegar fyrir sölupöntun sem ekki er settir í bið, geta notendur ekki yfirgefið síðu sölupöntunarfærslu fyrr en greiðsla er virkjuð. Auðvitað verður greiðslu krafist áður en losað er um biðstöðu pöntunarinnar.

Þar að auki geta notendur símavers sett pöntun, sem eru grunsamlegar af einhverjum ástæðum, handvirkt í bið sökum svika. Pantanir geta einnig verið settar í bið sjálfkrafa þegar upp kemur samsvörun við virk svikaviðmið og reglur. Nánari upplýsingar um þessa tegund af biðstöðu pöntunar er að finna í [Uppsetning svikatilkynninga](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts) svikatilkynninga.

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Skoða og stjórna pöntunum sem eru í bið

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Skoða biðupplýsingar um eina sölupöntun

Á **Notendaþjónusta** síðunni getur notendur sjónrænt þekkt pantanir sem eru í bið vegna þess að pöntunarlínurnar eru auðkenndar í tiltekinni lit. Þessi litur er skilgreindur af **Staða sölupöntunar í bið** reitnum á **Færibreytur viðskiptakrafna** síðunni.

> [!NOTE]
> Ef línan er valin á síðunni er auðkenningarliturinn ekki sýnilegur.

Notendur geta einnig skoðað nákvæmar upplýsingar um stöðu sölupöntunar til að vita hvort pöntunin sé í bið. Nákvæmar upplýsingar um stöðu er hægt að nálgast úr **Allar sölupantanir** eða **Notendaþjónusta** síðunni. Ef pöntun er í bið er **Ekki setja í vinnslu** fáninn stilltur fyrir það, og **Ítarleg stöðu** reiturinn sýnir stöðu annað hvort **Í bið** eða **Í bið sökum svika**, allt eftir atburðarásinni.

Til að skoða upplýsingar um einstaka pöntun í bið, notandi getur opnað ítarlegt yfirlit yfir **Pöntun í bið** síðunni úr **Notendaþjónusta** síðunni, með því að nota **Valkostir** valmyndina fyrir pöntunina sem er valin. Notendur geta einnig farið í þetta yfirlit frá **Allar sölupantanir** síðunni með því að velja **Pantanir í bið** valmyndaratriði á **Sölupöntun** flipanum.

### <a name="viewing-all-orders-that-are-on-hold"></a>Skoða allar pantanir sem eru í bið

Til að skoða allar pantanir sem hafa verið settar á handvirkt eða sjálfvirkan bið skaltu fara á **Retail og Commerce** \> **Viðskiptavinir** \> **Pantanir í bið**.

**Pantanir í bið** vinnusvæðið er með lista yfir allar pantanir sem eru í bið vegna handvirkra biðaðgerða eða biðaðgerða sem tengjast svikum. Með því að nýta sér staðlaða afmörkunar- og flokkunarvalkostina á síðunni geta notendur búið til yfirlit sem gera þeim kleift að vinna með eða stjórna tilteknum biðkóðum sem þeir bera ábyrgð á að yfirfara. **Pantanir í bið** vinnusvæði sýnir einnig fjölda daga sem pöntun hefur verið í bið. Þessar upplýsingar geta hjálpað notendum að forgangsraða biðröðinni.

Til að fá nánari yfirlit yfir þær pantanir sem eru í bið, geta notendur smellt á **Pöntun í bið** í valmyndinni. Þetta yfirlit veitir upplýsingar um viðskiptavininn, einhverjar athugasemdir sem hafa verið gerðar varðandi pöntunina, viðskiptavininn eða biðaðgerðinni. Yfirlitið veitir einnig upplýsingar um ástæðuna fyrir sjálfvirkan bið, ef pöntunin var sett í bið vegna samsvörunar við reglu um svik.

Frá bæði listayfirlitinu og ítarlegu yfirliti af **Pantanir í bið** síðunni geta notendur skoðað eða breytt viðbótarupplýsingum sem tengjast pöntunum, svo sem greiðslur, samtölur og athugasemdir.

Valkostirnir á flipanum **Athugun á bið** gætu verið gagnlegir ef margar notendur í fyrirtækinu þínu vinna í biðröðinni á sama tíma. Með því að velja **Athugun** valkostur, notendur geta gefið til kynna að þeir eru að vinna að endurskoða og rannsaka pöntunina í bið. Þannig eyða aðrir notendur ekki tíma með því að reyna að gera sama vinnuna. Frá ítarlega yfirlitinu á **Pantanir í bið** síðunni geta notendur skoðað upplýsingar um dag- og tímasetningu athugunar, og um notandann sem athugaði biðskrána.

Eftir að búið er að athuga biðskrá, getur aðeins notandinn sem athugaði skrána hreinsað athugunina. Þessi takmörkun er ætlað að koma í veg fyrir að notendur taki skrár sem aðrir notendur eru að vinna með. Til að sleppa pöntun til baka í biðröð þannig að aðrir notendur geti unnið með það, velur notandi sem athugaði skrána valkostinn **Hreinsa athugun**.

> [!NOTE]
> Ekki er losað um bið þegar athugunin er hreinsuð.

Í sumum tilfellum, svo sem þegar notandi er veikur eða hefur yfirgefið fyrirtækið, gæti það þurft að færa skrár sem eru athugaðar af honum yfir til annars notanda. Stjórnandi getur endurúthlutað skrám með því að nota **Hnekkja athugun** valkostinn.

## <a name="releasing-orders-that-are-on-hold"></a>Losa pantanir sem eru í bið

Í bæði listayfirliti og ítarlegt yfirliti **Pantanir í bið** síðunnar, inniheldur **Hreinsa bið** flipann valkostina sem eru notaðir til að losa pöntun í bið. Notaðu valkostinn **Hreinsa biðstöður** til að losa pöntun frá völdum biðkóðanum.

Símaverspantanir krefjast greiðslu. Því er ekki hægt að hreinsa bið að fullu ef greiðsla hefur ekki verið virkjuð fyrir pöntunina. Á **Færibreytur símavers** síðunni, á **Biðstöður** flipanum, vertu viss um að **Senda inn þegar hreinsað** breytu sé virkur. Þessi stilling hjálpar til við að tryggja að hreinsað pöntun í bið fer í gegnum réttan innsendingargrunn fyrir pöntun til að sannprófa og heimila greiðslur. Ef greiðslur vantar fær notandinn villuboð og biðkóðinn er ekki hreinsaður.

Ef **Senda inn þegar hreinsað** færibreytan hefur ekki verið stillt, ættu notendur að velja **Hreinsa og senda inn** valkostinn á **Hreinsa bið** valmyndina til að hjálpa til við að tryggja að pöntunin fer í gegnum allar nauðsynlegar greiðslusannprófanir. Ef innsending pöntunar mistekst þegar kveikt er á **Virkja lok pöntunar** flagginu á símaversrásinni, þá er pöntunin sleppt úr biðstöðu, en **Ekki setja í ferli** flaggið er áfram stilltur. Þess vegna er pöntunin ekki gefin út til vörugeymsluna fyrr en réttar greiðslur hafa verið virkjaðar og sannprófaðar.

Ef notendur vilja hreinsa bið en gera frekari breytingar á pöntuninni áður en hún er gefin út til frekari vinnslu, geta þeir valið **Hreinsa og breyta** valkostinum. Þessi valkostur fjarlægir biðkóðann og opnar upplýsingar um sölupöntun þannig að notendur geta gert frekari breytingar á pöntuninni. Notendur geta einnig virkjað greiðslu og sent sölupöntunina gegnum sannprófunargrunn fyrir greiðslur þegar kveikt er á **Virkja lok pöntunar** flagginu á símaversrásinni.

## <a name="reporting-options"></a>Valkostir tilkynninga

Fara í **Retail og Commerce** \> **Fyrirspurnir og skýrslur** \> **Símaversskýrslur** \> **Pantanir í bið skýrslur** til að keyra skýrslu um pantanir í bið eftir tímabili, biðkóða eða öðrum tengdum viðmiðunum.


[!INCLUDE[footer-include](../includes/footer-banner.md)]