---
title: Innkaupasamningar
description: Þessi grein gefur upplýsingar um innkaupasamninga. Innkaupasamningur er samningur sem skuldbindur stofnun til að kaupa tiltekið magn eða upphæð með því að nota margar innkaupapantanir á tilteknum tíma. Í skiptum fyrir þessa skuldbindingu fær kaupanda sérstakt verð og afslættir.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4911bd891c081892e52bda4bcc87984b3fb189b2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570491"
---
# <a name="purchase-agreements"></a>Innkaupasamningar

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um innkaupasamninga. Innkaupasamningur er samningur sem skuldbindur stofnun til að kaupa tiltekið magn eða upphæð með því að nota margar innkaupapantanir á tilteknum tíma. Í skiptum fyrir þessa skuldbindingu fær kaupanda sérstakt verð og afslættir. 

Innkaupasamningurinn getur átt við tiltekið magn af afurð, ákveðna gjaldmiðilsupphæð af afurð, eða ákveðna gjaldmiðilsupphæð af afurðunum í innkaupategund. Verð og afslættir af innkaupasamningur hunsa verð og afslætti sem eru tilgreindar í hvaða viðskiptasamninga sem ríkir.  

Á **innkaupasamnings** síðunni er hægt að stofna, beita og fylgja eftir innkaupasamningum sem eru til á milli fyrirtækisins þíns og lánardrottnanna. Þegar búið er að stofna innkaupasamning er hægt að panta beitn af því. Sérhver innkaupasamningur hefur gildistíma sem er skilgreint af þeim aðila sem býr til innkaupasamninginn. Afhendingardagur innkaupa verður að vera innan gildisdagsetninga gildistímans.  

Þegar búið er að stofna innkaupasamning þarf að virkja hann áður en hann tekur gildi. Til að virkja innkaupasamning; Stilla valkost **Merkja samning sem gildan** á **Já**. 

Til að koma í veg fyrir að innkaupasamningur þinn sé notaður og staðfestur skaltu merkja stöðu samningsins sem **Lokað**. Þú getur samt uppfært stöðuna í **Virkt** hvenær sem er eftir þessi breyting er gerð.

## <a name="responsible-workers-on-purchase-agreements"></a>Ábyrgir starfsmenn vegna innkaupasamninga

Þú getur borið kennsl á aðalábyrgðan starfskraft og annan ábyrgðan starfskraft í flokkun innkaupasamningsins. Þessi gildi efast með innkaupasamningi sem af því leiðir. Þú þarft ekki að bæta ábyrgum starfskröftum við innkaupasamninginn og þeim er hægt að breyta beint hverju sinni í innkaupasamningnum sjálfum. Þú getur ekki tilgreint annan ábyrgðan starfskraft án aðalábyrgs starfskrafts, jafnvel þó að þú sért ekki með annan ábyrgðan starfskraft. Þú getur ekki tilgreint sama starfskraft sem bæði aðal- og annan ábyrgan starfskraft.

> [!IMPORTANT]
> Áður en hægt er að nota eiginleika ábyrgðaraðila verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:
> 
> - **Eining:** *Innkaup og uppruni*
> - **Heiti eiginleika:** *Ábyrgðaraðili innkaupasamnings*

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
Í sumum aðstæðum þar sem innkaupapantanir eru stofnaðar óbeint er hægt að stjórna því hvort Supply Chain Management eigi að leita sjálfvirkt að innkaupasamningum sem við eiga. Til dæmis gæti þetta verið gert þegar sjálfkrafa eru staðfestar innkaupatillögur eða stofnun innkaupapantana sem eru byggðar á sölupöntunum.

## <a name="matching-policy-on-purchase-agreements"></a>Jöfnunarregla varðandi kaupsamninga
Þú getur skilgreint línujöfnunarreglu í hausnum á kaupsamningnum. Þessi lína jöfnunarreglu mun virða línujöfnunarreglu viðskiptakrafna þegar reiturinn **Leyfa að jöfnunarreglu sé hnekkt** á síðunni **Færibreytur viðskiptaskulda** (á flýtiflipanum **Samsvörun verðs og magns**) er stillt á **Hærri en regla fyrirtækis**. Skjöl sem vísa til innkaupasamningsins munu nota línujöfnunarregluna sem er skilgreind í haus innkaupasamnings nema annað sé skilgreint á samsvarandi vöru, vöru og lánardrottni eða innkaupastefnu flokks.

## <a name="purchase-agreements-and-intercompany-trade"></a>Innkaupasamningar og samstæðuviðskipti.
Hægt er að stofna vensl viðskiptasamninga samstæðunnar milli lánardrottnalykla og lykla viðskiptavinar sem eru í mismunandi lögaðila. Þegar sölupöntun eða innkaupapöntun er stofnuð fyrir einn aðilanna er pöntunarkeðja innan samstæðunnar stofnuð. Í pöntunarkeðjunni er sölupöntun og innkaupapöntun stofnuð í viðeigandi lögaðila.  

Hægt er að stofna innkaupasamning eða sölusamning fyrir einn viðskiptafélaga samstæðunnar. Síðan er hægt að mynda samsvarandi sölusamning eða innkaupasamning fyrir hinn aðilann innian samstæðunnar í hinum lögaðilanum.  

Ef þú stofnar innkaupapöntun innan samstæðu sem notar samstæðusölupöntun í einum lögaðila notar samsvarandi innkaupapöntun innan samstæðu samsvarandi sölusamning í hinum lögaðilanum. Uppfylling samkomulags sölusamning og uppfylling innkaupasamninga eru samstilltar, rétt eins og samstæðusölupöntun og samstæðuinnkaupapöntun eru samstilltar.

## <a name="financial-dimensions-on-purchase-agreements"></a>Fjárhagsvíddir á innkaupasamningum
Hægt er að afrita fjárhagsvíddir á skjalahausa eða á einstaka línur í innkaupasamningi. Ef þú breytir víddum í haus þjónustusamnings eða samningslínu hefur breytingin ekki áhrif á neinar losaðar pantanir, en hún kemur fram á öllum nýjum pöntunum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stofna innkaupasamning](tasks/create-purchase-agreement.md)
- [Nota innkaupasamning þegar innkaupapöntun er stofnuð](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]