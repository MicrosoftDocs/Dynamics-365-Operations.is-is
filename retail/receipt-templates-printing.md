---
title: "Sniðmát kvittana og prentun"
description: "Þessi grein lýsir því hvernig á að breyti útliti skjámynda til að stjórna því hvernig kvittanir, reikningar og önnur skjöl eru prentuð. Microsoft Dynamics 365 for Operations - Retail inniheldur útlitshönnuð skjámyndar sem hægt er að nota til að búa til og breyta útliti ýmissa skjámynda á auðveldan hátt."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Sniðmát kvittana og prentun

[!include[banner](includes/banner.md)]


Þessi grein lýsir því hvernig á að breyti útliti skjámynda til að stjórna því hvernig kvittanir, reikningar og önnur skjöl eru prentuð. Microsoft Dynamics 365 for Operations - Retail inniheldur útlitshönnuð skjámyndar sem hægt er að nota til að búa til og breyta útliti ýmissa skjámynda á auðveldan hátt.

**Mikilvægt:** verður að setja upp útlit skjámynda og forstillingar kvittana til að prenta kvittanir og önnur skjöl úr Retail Modern POS og Cloud POS (sölukerfi í skýinu). Hægt er að hafa mörg útlit skjámynda í kvittunarforstillingu. Síðan geturðu úthlutað kvittunarforstillingu á prentara með því að breyta vélbúnaðarreglu.

## <a name="set-up-a-receipt-format"></a>Setja upp snið kvittunar
1.  Smellið á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Sölustaður** &gt; **Snið kvittunar**..
2.  Á síðunni **snið kvittunar ** skal smella á  **nýtt** til að stofna nýtt útlit skjámyndar eða velja núverandi snið skjámyndar.
3.  Á svæðinu **snið kvittunar** skal færa inn kennimerki fyrir útlit skjámyndarinnar og velja síðan gerð kvittunarinnar sem þetta útlit er notað fyrir. Einnig er hægt að færa inn lýsingu og stutt heiti fyrir kvittunina í svæðið **Titill**.
4.  Á við **Almennt** flýtiflipa, velja valkost til að skilgreina prenthegðun
    -   **Alltaf prenta** – kvittun er sjálfkrafa prentuð, eins og við á.
    -   **Ekki prenta** - kvittunin er ekki prentuð.
    -   **Kvaðning notanda** – notandinn er beðinn um að prenta kvittunina.
    -   **Eftir þörfum** – Þessi valkostur er einungis notaður fyrir kvittanir gjafakorts. Þegar þessi valkostur er valinn getur notandi prentað kvittun fyrir gjöf úr á **Breytingu** síðuna, ef þörf er á kvittun fyrir gjöf.

## <a name="design-a-receipt-format"></a>Hanna kvittunarsnið
Nota skal útlitshönnuð skjámyndarinnar til að búa til útlit skjámyndarinnar á myndrænan hátt. **sniðhönnuður Kvittunar** síðu hefur þrjá hluta: **Haus**, **Línur**, og **Síðufót**. Sumar gerðir skjámyndsútlita nota atriði úr öllum þremur hlutum, en aðrar gerðir nota atriði úr einum eða tveimur hlutum. Til að skoða einingarnar sem eru tiltækar fyrir hvern hluta, skal smella á viðeigandi hnapp á yfirlitssvæðinu vinstra megin á síðunni.

1.  Smellið á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Sölustaður** &gt; **Snið kvittunar**..
2.  Á **kvittunarsnið** síðunni, veljið útlit skjámyndar og smella síðan á **Hönnuður**.
3.  Smellið á **Keyra** til að byrja að setja upp hönnuður smásöluhönnuðar.
4.  Á Tilkynningarslá sem mun birtast neðst í Internet Explorer glugganum , smellið á **Opna** til að byrja að setja upp eins-smells hönnuð. (Tilkynningaslá gæti birst annars staðar í öðrum vöfrum). Framvinduvísir sýnir framvindu uppsetningarferlis.
5.  Eftir að uppsetningu er lokið skal færa inn Dynamics 365 for Operations notandanafn og aðgangsorð, og smellið svo á **Innskráning** til að ræsa hönnuðinn.
6.  Eftir að skilríkin þín eru villuleitaðar og hönnuður hefst er hægt að byrja að hanna kvittunarsnið eða breyta fyrirliggjandi snið.
7.  Til að stofna einingar skjámyndarinnar skal velja **Haus**, **Línur** eða **síðufótur ** hlutann og draga síðan einingu úr hlutanum yfir í vinnusvæðið. Flestar einingar innihalda breytur sem eru sjálfkrafa fylltar út með gögnum úr gagnagrunninum. Aðrar einingar, svo sem **Texti**, gera kleift að prenta sérsniðinn texta á kvittunina. **Athugasemd** Hægt er að tilgreina hvað hver hluti skal taka margar línur með því að velja fjölda þeirra í horninu neðst til hægri í hlutanum. Til að auðvelda breytingar í hluta, aukið hæð hlutans með því að draga stærðarstikuna neðst í hlutanum. Hæð hlutans á vinnusvæðinu hefur ekki áhrif á fjölda línanna á raunverulegu kvittuninni.
8.  Þegar einingar hafa verið dregnar yfir á vinnusvæðið, skal stilla eiginleika fyrir þann hluta á svæðinu **Upplýsingar um hlut** neðst á skjámyndinni. Færa skal inn eitt eða fleiri af eftirfarandi stillingum:
    -   **Jafna** – Stilla skal samhæfingu svæðisins annað hvort í **Vinstri** eða **Hægri**.
    -   **Fyllistafur** – Tilgreinið hvíta-bils stafinn. Að sjálfgefnu, er að autt bil notað en hægt er að færa inn hvaða staf sem er.
    -   **Forskeyti** – Slá skal inn gildið sem birtist í upphafi svæðisins. Þessi stilling gildir aðeins fyrir **Línur ** hlutann í útlitinu.
    -   **Stafir** – Tilgreinið fjölda stafa í sem svæðið má innihalda ef einingin inniheldur breytu. Ef textinn á svæðinu er lengri en fjöldi stafanna sem tilgreindir eru, er textinn styttur til þess að hann passi á svæðið.
    -   **Breyta** – Þessi gátreitur er valinn sjálfkrafa ef einingin inniheldur breytu og ekki er hægt að sérsníða.
    -   **Leturgerð** – Stilla leturgerðina annað hvort á **Venjulegt** eða **Feitletrað**. Feitletraðir bókstafir nota tvöfalt meira pláss en venjulegir stafir nota. Þess vegna gæti verið að sumir stafir eru styttir.
    -   **Eyða** – Smellið á þennan hnapp til að fjarlægja valinn hluta úr útliti skjámyndar.

## <a name="assign-receipt-profiles"></a>Úthluta kvittunarforstillingar
Kvittunarforstillingar eru tengdar beint í prentara með vélbúnaðarreglu.

1.  Opna vélbúnaðarreglu með því að smella á **Smásala og viðskipti** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **POS forstillingar** &gt; **vélbúnaðarregla**.
2.  Velja prentara, og síðan, í því **forstillingu Kvittunar ** skal úthluta kvittunarforstillingu sem nota á afgreiðslukassanum.

**Ábending:** Ef tvær prentarar eru notaðar, er hægt að nota einn prentara til að prenta staðlaða 40 dálka thermal-kvittanir. Önnur prentara er yfirleitt notað til að prenta kvittun af heilsíðugerð, sem krefjast frekari upplýsingar. Þessar gerðir kvittana innifela pöntun viðskiptavinar og reikningum viðskiptavina.




