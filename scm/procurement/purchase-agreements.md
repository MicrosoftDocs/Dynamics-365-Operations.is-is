---
title: Innkaupasamningar
description: "Þessi grein gefur upplýsingar um innkaupasamninga. Innkaupasamningur er samningur sem skuldbindur stofnun til að kaupa tiltekið magn eða upphæð með því að nota margar innkaupapantanir á tilteknum tíma. Í skiptum fyrir þessa skuldbindingu fær kaupanda sérstakt verð og afslættir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e7412eb1be4b1f5431fc0dd07aa2f778f461a74b
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="purchase-agreements"></a>Innkaupasamningar

[!include[banner](../includes/banner.md)]


Þessi grein gefur upplýsingar um innkaupasamninga. Innkaupasamningur er samningur sem skuldbindur stofnun til að kaupa tiltekið magn eða upphæð með því að nota margar innkaupapantanir á tilteknum tíma. Í skiptum fyrir þessa skuldbindingu fær kaupanda sérstakt verð og afslættir. 

Innkaupasamningurinn getur átt við tiltekið magn af afurð, ákveðna gjaldmiðilsupphæð af afurð, eða ákveðna gjaldmiðilsupphæð af afurðunum í innkaupategund. Verð og afslættir af innkaupasamningur hunsa verð og afslætti sem eru tilgreindar í hvaða viðskiptasamninga sem ríkir.  

Á **innkaupasamnings** síðunni er hægt að stofna, beita og fylgja eftir innkaupasamningum sem eru til á milli fyrirtækisins þíns og lánardrottnanna. Þegar búið er að stofna innkaupasamning er hægt að panta beitn af því. Sérhver innkaupasamningur hefur gildistíma sem er skilgreint af þeim aðila sem býr til innkaupasamninginn. Afhendingardagur innkaupa verður að vera innan gildisdagsetninga gildistímans.  

Þegar búið er að stofna innkaupasamning þarf að virkja hann áður en hann tekur gildi. Til að virkja innkaupasamning; Stilla valkost **Merkja samning sem gildan** á **Já**.

## <a name="commitment-types"></a>Ráðstöfunargerðir
Hver lína í innkaupasamningi er skuldbinding til að kaupa eitthvað. Þú getur notað línur frá mörgum innkaupapöntununum til að uppfylla skuldbindingar. Til eru fjórar tegundir skuldbindinga:

-   **Skuldbinding um magn afurða** – Þú kaupir ákveðið magn af afurð.
-   **Skuldbinding um gildi afurða** – Þú kaupir ákveðna gjaldmiðilsupphæð af vöru.
-   **Skuldbinding um ráðstöfunarvirði vörutegundar** - Þú kaupir ákveðna gjaldmiðilsupphæð af innkaupategund. Fjárhæð getur verið fyrir vörulistaatriði eða vöru sem er ekki á vörulista..
-   **Skuldbinding um virði** – Þú kaupir ákveðna gjaldmiðilsupphæð af hvaða vöru sem er eða í hvaða innkaupategund.

## <a name="pricing-terms-for-purchase-agreements"></a>Verðskilmálar fyrir innkaupasamning
Verðskilmálra geta verið mismunandi, allt eftir skuldbindingu. Verðskilmálar fyrir innkaupasamning geta hnekkt öðrum verðskilmálum sem eru settir upp fyrir viðskiptasamninga. Eftirfarandi tafla lýsir verðtengdum reitum sem hafa árhfia á ráðstöfunargerð. Reitir sem innihalda **Já** er hægt að uppfæra á pöntunarlínu.

| Ráðstöfunargerð                   | Einingarverð | Einingarverð | Afsláttarprósenta | Upphæð staðgreiðsluafsláttar |
|-----------------------------------|------------|------------|------------------|----------------------|
| Ráðstafað afurðarmagn       | Já        | Já        | Já              | Já                  |
| Ráðstöfunarvirði afurðar          |            |            | Já              |                      |
| Ráðstöfunarvirði vörutegundar |            |            | Já              |                      |
| Ráðstöfunarvirði                  |            |            | Já              |                      |

## <a name="policies-for-purchase-agreements"></a>Stefnfur fyrir innkaupasamninga
Eftirfarandi stefnur hafa áhrif á það hvernig tengslin er milli skuldbindingar innkaupasamnings og samsvarandi innkaupapöntunarlína:

-   **Hámark er tryggt** - Heildarmagn eða upphæð fyrir allar pöntunarlínur geta ekki verið meiri en magnið eða upphæðin sem er tilgreind á viðkomandi skuldbindingu.
-   **Verð og afsláttur eru föst** – Verðið á pöntunarlínu og verðið á tengdri skuldbindingu verður að vera það sama. Ef verðið er breytt á pöntunarlínu rofnar tengiliinn við skuldbindinguna. Ef tengillinn er rofinn úthlutar pöntunarlínan ekki til uppfyllingar skuldbindingarinnar.
-   **Lágmarks losunarupphæð og hámarks losunarupphæð** – Ef upphæð er tilgreind birtast skilaboð ef einhver breyting er gerð á pöntunarlínu sem veldur því að pöntunarlínan verði frábrugðin tengdu skuldbindingunni.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Útreikningur uppfyllingar fyrir innkaupasamninga
Uppfyllingarmagn og -upphæðir koma fram í **Uppfyllingar** flipanum á **Línuupplýsingar** flýtiflipanum°á síðunni **Innkaupasamningar**.  

**Uppfyllingar** svæðið sýnir eftirstandandi upphæð eða magn sem er áskilið til að uppfylla skuldbindinguna.  

Svæðið **Samkomulag** sýnir heildarmagn eða heildarupphæð sem sölusamningslína er gild fyrir.  

Þú getur nálgast innkaupapöntunarlínur og reikningslínur sem hafa áhrif á uppfyllingarútreikninga með því að velja aðgerðina **Tengdar upplýsingar** í línum eða á haus innkaupasamnings.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Staðfestingar og útgáfusögu fyrir innkaupasamninga
Þegar innkaupasamningur er staðfestur er núverandi útgáfa innkaupasamningsins vistuð í sögutöflu. Ef innkaupasamnings er breytt hægt að staðfesta hann aftur til að geyma aðra útgáfu af innkaupasamnings í sögu. Ef innkaupasamningur er ekki staðfestur er enn hægt að nota hann til að stofna innkaupapantanir. Hins vegar eru söguupplýsingar innkaupasamnings ekki vistuð. Hægt er að forskoða eða prenta allar útgáfur samningsins. Svo er hægt að deila endurskoðunum til lánardrottins til að fá samþykki.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Jafna innkaupasamninga í pöntunarferli
Þegar innkaupapöntun er stofnuð er hægt að nota innkaupasamning við hana. Upplýsingar úr skilmálum samningsins, t.d. greiðsluskilmálar, afhendingarskilmálar, og afhendingaraðsetur, eru síðan afritaðar á haus innkaupapöntunarinnar. Ef innkaupapöntunin inniheldur eina eða fleiri línur fyrir afurð eða flokka sem samkomulagið nær yfir, er verð og afsláttur úr innkaupasamningnum notað fyrir þær línur. Upphæð eða magn í pöntunarlínunni hefur áhrif á uppfyllingu samningsins í innkaupapöntuninni. Sama innkaupapöntunin getur bæði haft línur sem eru ekki tengdar við sölusamning og línur sem hafa samning fyrir innkaupapöntun.  

Þú getur aðeins valið innkaupasamning þegar þú stofnar innkaupapöntunarlínu. Ekki er hægt að velja innkaupasamning eftir að°innkaupapöntunin hefur°verið stofnuð.  
Í sumum aðstæðum þar sem innkaupapantanir eru stofnaðar óbeint er hægt að stjórna því hvort Finance and Operations eigi að leita sjálfvirkt að innkaupasamningum sem við eiga. Til dæmis gæti þetta verið gert þegar sjálfkrafa eru staðfestar innkaupatillögur eða stofnun innkaupapantana sem eru byggðar á sölupöntunum.

## <a name="purchase-agreements-and-intercompany-trade"></a>Innkaupasamningar og samstæðuviðskipti.
Hægt er að stofna vensl viðskiptasamninga samstæðunnar milli lánardrottnalykla og lykla viðskiptavinar sem eru í mismunandi lögaðila. Þegar sölupöntun eða innkaupapöntun er stofnuð fyrir einn aðilanna er pöntunarkeðja innan samstæðunnar stofnuð. Í pöntunarkeðjunni er sölupöntun og innkaupapöntun stofnuð í viðeigandi lögaðila.  

Hægt er að stofna innkaupasamning eða sölusamning fyrir einn viðskiptafélaga samstæðunnar. Síðan er hægt að mynda samsvarandi sölusamning eða innkaupasamning fyrir hinn aðilann innian samstæðunnar í hinum lögaðilanum.  

Ef þú stofnar innkaupapöntun innan samstæðu sem notar samstæðusölupöntun í einum lögaðila notar samsvarandi innkaupapöntun innan samstæðu samsvarandi sölusamning í hinum lögaðilanum. Uppfylling samkomulags sölusamning og uppfylling innkaupasamninga eru samstilltar, rétt eins og samstæðusölupöntun og samstæðuinnkaupapöntun eru samstilltar.

## <a name="financial-dimensions-on-purchase-agreements"></a>Fjárhagsvíddir á innkaupasamningum
Hægt er að afrita fjárhagsvíddir á skjalahausa eða á einstaka línur í innkaupasamningi. Ef þú breytir víddum í haus þjónustusamnings eða samningslínu hefur breytingin ekki áhrif á neinar losaðar pantanir, en hún kemur fram á öllum nýjum pöntunum.

<a name="see-also"></a>Sjá einnig
--------

[Stofna innkaupasamning (verkleiðbeiningar)](/dynamics365/unified-operations/supply-chain/procurement/tasks/create-purchase-agreement)

[Stofna úttektarpöntun innkaupa úr innkaupasamningi (verkleiðbeiningar)](/dynamics365/unified-operations/supply-chain/procurement/tasks/create-purchase-release-order-purchase-agreement)




