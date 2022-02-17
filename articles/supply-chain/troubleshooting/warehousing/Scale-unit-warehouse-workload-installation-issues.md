---
title: Vinnsluvandamál eiga sér stað eftir að vinnuálag mælieiningar vöruhúss er sett upp
description: Þetta efnisatriði lýsir vandamálum sem geta komið upp fljótlega eftir að vinnuálag vöruhúss mælieininga er sett upp og gefur ráð til að laga þau.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071778"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Vinnsluvandamál eiga sér stað eftir að vinnuálag mælieiningar vöruhúss er sett upp

Þetta efnisatriði lýsir vandamálum sem geta komið upp fljótlega eftir að vinnuálag vöruhúss mælieininga er sett upp og gefur ráð til að laga þau.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Mál 1: Villa eftir að hleðsla er losuð af vinnubekk fyrir áætlanagerð

### <a name="symptoms-of-issue-1"></a>Einkenni vandamála 1

Þegar þú losar álag frá **Hleðsluskipulag vinnubekkur** eða **Áætlunarbekkur á útleið** síðu færðu villuboð sem hefur eftirfarandi form:

> Undantekning kom upp við bókun farmsins %1, ekki var hægt að losa farminn.
> 
> UPPFÆRÐU WHSSHIPMENTTAFLUSETT...
> 
> Ekki er hægt að breyta færslu í Sendingar (WHSShipmentTable). Sendingarauðkenni: ...

Hér er raunverulegt dæmi sem inniheldur sýnishornsgögn:

> Undantekning náðist þegar hleðslan USMF-000033 var birt, ekki var hægt að losa hleðsluna.
Fundur 5133 (stjórnandi)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? HVAR ((RECID=?) OG (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 fyrir SQL Server][SQL Server]Scale Unit @@ reyndi að uppfæra færslur í eigu Scale Unit @A.  
> Object Server Azure:
>
> Ekki er hægt að breyta færslu í Sendingar (WHSShipmentTable). Sendingarauðkenni: USMF-000031, USMF-000033. SQL gagnagrunnur hefur tilkynnt um villu.

### <a name="cause-of-issue-1"></a>Orsök máls 1

Þetta vandamál getur komið upp ef eftirfarandi samsetning skilyrða er fyrir hendi þegar þú setur upp vinnuálag vöruhúss mælieininga:

- Kerfið inniheldur óútgefið hleðslu þar sem margar línur eru tengdar mismunandi pöntunum og sumar hleðslulínur eru ekki tengdar sendingu.
- Kerfið er sett upp til að nota sendingarsamstæðu.

Í dreifðri blandaðri staðfræðiuppfærslu er hver hleðslu- og sendingarskrá merkt sem í eigu ákveðinnar mælikvarðaeiningar eða miðstöðvar. Þegar þú losar álag frá **Hleðsluskipulag vinnubekkur** síðu breytir kerfið úthlutað eignarhaldi. Hins vegar, vegna áður skráðra aðstæðna, gæti kerfið ekki leyst úr eignarhaldi gagna. Þess vegna tekst það ekki að losa álagið á vöruhúsið.

### <a name="resolution-of-issue-1"></a>Úrlausn 1. máls

Skiptu hleðslunni í tvær smærri hleðslur áður en þú sleppir því í vöruhúsið.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>2. mál: Villa á meðan bylgja er unnin á mælikvarðaeiningu

### <a name="symptoms-of-issue-2"></a>Einkenni vandamála 2

Þegar þú ert að vinna úr bylgju á kvarðaeiningu færðu villuboð sem hefur eftirfarandi form:

> Þú getur ekki breytt hleðslulínu með RecId =%1, hlaða id=%2 þar sem það er enn í eigu fyrirtækjamiðstöðvarinnar. Gakktu úr skugga um að samsvarandi hleðsla á útleið hafi verið losuð á mælikvarðaeiningu og þar með búið til vöruhúsapöntunarlínur.

Hér er raunverulegt dæmi sem inniheldur sýnishornsgögn:

> Upplýsingaskrá fyrir starf Keyra Wave USMF-000000012 (9223377668365210)  
> Upplýsingaskrá fyrir verkefni Keyra Wave USMF-000000012 (9223377668370462)  
> Þú getur ekki breytt hleðslulínu með RecId = 68719478242, load id= USMF-000034 þar sem hún er enn í eigu fyrirtækjamiðstöðvarinnar. Gakktu úr skugga um að samsvarandi hleðsla á útleið hafi verið losuð á mælikvarðaeiningu og þar með búið til vöruhúsapöntunarlínur.

### <a name="cause-of-issue-2"></a>Orsök máls 2

Í dreifðri blönduð staðfræðiuppfærslu er eignarhaldi á hleðslu- og sendingargögnum úthlutað til ákveðinnar mælikvarðaeiningu eða miðstöð. Sem hluti af veifandi úrvinnslu er gert ráð fyrir að eignarhald á gögnunum verði úthlutað til mælieiningu.

Þegar þú setur upp vinnuálag á mælieiningu vöruhúss, ef opin sending er tengd hleðslu og bylgju, getur kerfið ekki stjórnað eignarhaldi gagna. Þess vegna mistekst bylgjuvinnslan á mælikvarðaeiningunni.

### <a name="resolution-of-issue-2"></a>Úrlausn 2. máls

Losaðu farminn í vöruhúsið frá miðstöðinni.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Lestu vandamál með því að skoða eignarhald og áfangastað færslu

Í dreifðri blendingur svæðisfræði dreifing, eru margar tegundir af færslum merktar sem í eigu ákveðinnar mælikvarðaeiningu eða miðstöð. Eftir að skipt hefur verið yfir í dreifða blendinga svæðisfræði og/eða sett upp nýtt mælieininga vöruhús vinnuálag, úthlutar kerfið eignarhaldi á hverja viðeigandi færslu. Þetta ferli getur stundum valdið villum eða óvæntum niðurstöðum. Þess vegna geta upplýsingar um eignarhald og flutningsáfangastað færslu hjálpað þér að leysa vandamál sem koma upp eftir að þú gerir þessar tegundir breytinga.

Fylgdu þessum skrefum til að skoða eignarhald og flutningsáfangastað færslu.

1. Opnaðu viðkomandi skrá.
1. Á aðgerðarrúðunni, á **Valmöguleikar** flipa, í **Skrá upplýsingar** hópur, veldu **Sýna alla reiti**.
1. Síðan sem birtist sýnir gildi fyrir alla reiti sem eru tiltækir fyrir valda færslu. Skoðaðu eftirfarandi reiti:

    - **SYSSCALEUNITID** – Þessi reitur sýnir núverandi eiganda færslunnar.
    - **SYSTARGETSCALEUNITID** – Þessi reitur sýnir mælieiningakenni miðstöðvarinnar eða mælieiningarinnar sem færslan verður flutt yfir á þegar núverandi eigandi hefur lokið vinnu við hana. Gildi þessa reits er notað af runuverkum sem stjórna þessari tegund ferlis. Þó að þessi reitur sé ekki beintengdur eignarhaldi gæti eignarhald breyst þegar skráningin er flutt. Í sumum tilfellum verður þessi reitur auður.
