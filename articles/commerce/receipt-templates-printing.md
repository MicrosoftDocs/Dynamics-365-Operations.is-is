---
title: Setja upp og hanna kvittunarsnið
description: Þessi grein lýsir því hvernig á að breyti útliti skjámynda til að stjórna því hvernig kvittanir, reikningar og önnur skjöl eru prentuð. Dynamics 365 Commerce inniheldur útlitshönnuður skjámyndar sem gerir notendum kleift að búa til og breyta útliti ýmissa skjámynda á auðveldan hátt.
author: BrianShook
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dac0ad75ff35367b5d6ac84c75c68e22e2cb0cb1
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779402"
---
# <a name="set-up-and-design-receipt-formats"></a>Setja upp og hanna kvittunarsnið

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að breyti útliti skjámynda til að stjórna því hvernig kvittanir, reikningar og önnur skjöl eru prentuð. Útlitshönnuður skjámyndar í Dynamics 365 Commerce gerir kleift að búa til og breyta útliti ýmissa skjámynda á auðveldan hátt.

> [!IMPORTANT]
> Setja verður upp sniðsútlit skjámyndar og kvittunarforstillingar til að prenta móttökur og önnur skjöl úr Retail Modern POS og sölukerfi í skýinu. Hægt er að hafa mörg útlit skjámynda í kvittunarforstillingu. Síðan geturðu úthlutað kvittunarforstillingu á prentara með því að breyta vélbúnaðarreglu.

## <a name="set-up-a-receipt-format"></a>Setja upp snið kvittunar

1. Smellið á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Sölustaður** &gt; **Snið kvittunar**.
2. Á síðunni **snið kvittunar** skal smella á **nýtt** til að stofna nýtt útlit skjámyndar eða velja núverandi snið skjámyndar.
3. Á svæðinu **snið kvittunar** skal færa inn kennimerki fyrir útlit skjámyndarinnar og velja síðan gerð kvittunarinnar sem þetta útlit er notað fyrir. Einnig er hægt að færa inn lýsingu og stutt heiti fyrir kvittunina í svæðið **Titill**.
4. Á við **Almennt** flýtiflipa, velja valkost til að skilgreina prenthegðun

    - **Alltaf prenta** – kvittun er sjálfkrafa prentuð, eins og við á.
    - **Ekki prenta** - kvittunin er ekki prentuð.
    - **Kvaðning notanda** – notandinn er beðinn um að prenta kvittunina.
    - **Eftir þörfum** – Þessi valkostur er einungis notaður fyrir kvittanir gjafakorts. Þegar þessi valkostur er valinn getur notandi prentað kvittun fyrir gjöf úr á **Breytingu** síðuna, ef þörf er á kvittun fyrir gjöf.

## <a name="print-images"></a>Prenta myndir

Kvittanahönnuðurinn inniheldur **Lógó** breytu. Þú getur notað þessa breytu til að tilgreina mynd sem á að prenta á kvittanir. Myndir sem prentaðar eru á kvittanir með því að nota **Lógó** breytuna ættu að vera með einlita skráargerðir (.bmp). Ef punktamynd er tilgreind í hönnuði kvittunar en er ekki prentuð þegar kvittun er sent til prentarans gæti orsökin verið eitt af eftirfarandi vandamálum:

- Skráin er of stór eða pixlastærðir myndarinnar eru ekki samhæfðar við prentarann. Í þessu tilviki skaltu reyna að minnka upplausn eða víddir myndskrárinnar.
- Sumt OLE (Object Linking and Embedding) fyrir prentararekla sölustaðar innleiða ekki aðferðina **PrintMemoryBitmap** sem vélbúnaðarstöðvar nota til að prenta myndir af lógóum. Í þessu tilviki skaltu reyna að bæta eftirfarandi flaggi við skrána **HardwareStation.Extension.config** í þinni eigin eða samnýttri vélbúnaðarstöð:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>Hanna kvittunarsnið

Nota skal útlitshönnuð skjámyndarinnar til að búa til útlit skjámyndarinnar á myndrænan hátt. **sniðhönnuður Kvittunar** síðu hefur þrjá hluta: **Haus**, **Línur**, og **Síðufót**. Sumar gerðir skjámyndsútlita nota atriði úr öllum þremur hlutum, en aðrar gerðir nota atriði úr einum eða tveimur hlutum. Til að skoða einingarnar sem eru tiltækar fyrir hvern hluta, skal smella á viðeigandi hnapp á yfirlitssvæðinu vinstra megin á síðunni.

1. Smellið á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Sölustaður** &gt; **Snið kvittunar**.
2. Á **kvittunarsnið** síðunni, veljið útlit skjámyndar og smella síðan á **Hönnuður**.
3. Smellið á **Keyra** til að byrja að setja upp hýsil Commerce-hönnuðar.
4. Á Tilkynningarslá sem mun birtast neðst í Internet Explorer glugganum, smellið á **Opna** til að byrja að setja upp eins-smells hönnuð. (Tilkynningaslá gæti birst annars staðar í öðrum vöfrum). Framvinduvísir sýnir framvindu uppsetningarferlis.
5. Eftir að uppsetningu er lokið skal færa inn Commerce notandanafn og aðgangsorð, og smellið svo á **Innskráningu** til að hefja hönnuðurinn.
6. Eftir að skilríkin þín eru villuleitaðar og hönnuður hefst er hægt að byrja að hanna kvittunarsnið eða breyta fyrirliggjandi snið.
7. Til að stofna einingar skjámyndarinnar skal velja **Haus**, **Línur** eða **síðufótur** hlutann og draga síðan einingu úr hlutanum yfir í vinnusvæðið. Flestar einingar innihalda breytur sem eru sjálfkrafa fylltar út með gögnum úr gagnagrunninum. Aðrar einingar, svo sem **Texti**, gera kleift að prenta sérsniðinn texta á kvittunina.

    > [!NOTE]
    > Hægt er að tilgreina hvað hver hluti skal taka margar línur með því að velja fjölda þeirra í horninu neðst til hægri í hlutanum. Til að auðvelda breytingar í hluta, aukið hæð hlutans með því að draga stærðarstikuna neðst í hlutanum. Hæð hlutans á vinnusvæðinu hefur ekki áhrif á fjölda línanna á raunverulegu kvittuninni.

8. Þegar einingar hafa verið dregnar yfir á vinnusvæðið, skal stilla eiginleika fyrir þann hluta á svæðinu **Upplýsingar um hlut** neðst á skjámyndinni. Færa skal inn eitt eða fleiri af eftirfarandi stillingum:

    - **Jafna** – Stilla skal samhæfingu svæðisins annað hvort í **Vinstri** eða **Hægri**.
    - **Fyllistafur** – Tilgreinið hvíta-bils stafinn. Að sjálfgefnu, er að autt bil notað en hægt er að færa inn hvaða staf sem er.
    - **Forskeyti** – Slá skal inn gildið sem birtist í upphafi svæðisins. Þessi stilling gildir aðeins fyrir **Línur** hlutann í útlitinu.
    - **Stafir** – Tilgreinið fjölda stafa í sem svæðið má innihalda ef einingin inniheldur breytu. Ef textinn á svæðinu er lengri en fjöldi stafanna sem tilgreindir eru, er textinn styttur til þess að hann passi á svæðið.
    - **Breyta** – Þessi gátreitur er valinn sjálfkrafa ef einingin inniheldur breytu og ekki er hægt að sérsníða.
    - **Leturgerð** – Stilltu leturgerðina annaðhvort á **Venjulegt** eða **Feitletrað**. Feitletraðir bókstafir taka tvöfalt meira pláss en venjulegir stafir. Þess vegna gæti verið að sumir stafir eru styttir.
    - **Leturgerð** – Stilltu leturstærðina annaðhvort á **Venjulegt** eða **Stórt**. Stórir bókstafir eru tvisvar sinnum hærri en venjulegir stafir. Þess vegna getur texti skarast á kvittun ef stórir stafir eru notaðir.
    - **Eyða** – Smellið á þennan hnapp til að fjarlægja valinn hluta úr útliti skjámyndar.

## <a name="assign-receipt-profiles"></a>Úthluta kvittunarforstillingar

Kvittunarforstillingar eru tengdar beint í prentara með vélbúnaðarreglu.

1. Opna vélbúnaðarreglu með því að smella á **Retail og Commerce** &gt; **Uppsetningu rásar** &gt; **Uppsetning smásölustaðar** &gt; **POS forstillingar** &gt; **Vélbúnaðarreglu**.
2. Velja prentara, og síðan, í því **forstillingu Kvittunar** skal úthluta kvittunarforstillingu sem nota á afgreiðslukassanum.

> [!NOTE]
> Ef tveir prentarar eru notaðir, er hægt að nota einn prentara til að prenta staðlaða 40 dálka thermal-kvittanir. Önnur prentara er yfirleitt notað til að prenta kvittun af heilsíðugerð, sem krefjast frekari upplýsingar. Þessar gerðir kvittana innifela pöntun viðskiptavinar og reikningum viðskiptavina.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
