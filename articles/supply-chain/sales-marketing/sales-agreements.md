---
title: "Sölusamningar"
description: "Í þessu efnisatriði er að finna upplýsingar um sölusamninga. Sölusamning er samningur sem bindur viðskiptavin til að kaupa vörur í ákveðnu magni eða ákveðna upphæð yfir tíma í skiptum fyrir for sérstakt verð og afslætti."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21e9c53f39b0f4def0052bf7f04c77279bfc610b
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="sales-agreements"></a>Sölusamningar

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er að finna upplýsingar um sölusamninga. Sölusamning er samningur sem bindur viðskiptavin til að kaupa vörur í ákveðnu magni eða ákveðna upphæð yfir tíma í skiptum fyrir for sérstakt verð og afslætti.

Sölusamning er samningur sem bindur viðskiptavin til að kaupa vöru í ákveðnu magni eða ákveðna upphæð yfir tíma í skiptum fyrir for sérstakt verð og sérstaka afslætti, og aðra sérstaka skilmála, eins og greiðslu og afhendingarskilmálar. Verð og afslættir af sölusamnings hunsa verð og afslætti sem eru tilgreindar í hvaða viðskiptasamninga sem ríkir.  

Gildistíma sölusamningslínunni er skilgreint með **upphafsdagsetningu** og  **Lokadagsetningu** svæði í samningi. Sölupöntun viðskiptavinar uppfyllir skilyrði fyrir samningsskilmála ef umbeðin sendingardagsetning pöntunarinnar er innan gildistíma. Allar sölupöntunarlínur sem eru tengdar við sölusamning stuðlar að uppfyllingu þess sölusamnings.  

Hægt er að stofna sölupöntun beint úr sölusamning með því að nota í **Úttektarpöntun** aðgerð. Einnig er hægt að velja virkan sölusamnings þegar verið er að taka pantanirnar (sjá í "Nota sölusamningar í pöntunarferlið" hluta í þessari grein).  

**Athugið** Í eldri útgáfum voru sölusamningar nefndir standandi sölupantanir.

## <a name="commitment-types"></a>Ráðstöfunargerðir
Hver lína í sölusamningi lýsir skuldbindingu um að selja eitthvað. Almennt séð, eru tvær tegundir af ráðstöfun:

-   **Virðisráðstöfun** – Viðskiptamaðurinn samþykkir að kaupa afurð fyrir tiltekna upphæð.
-   **Magnráðstöfun** – Viðskiptamaðurinn samþykkir að kaupa tiltekið magn afurðar.

Þar að auki geta samningur skuldbundið viðskiptavin til að kaupa tilteknar afurðir í vörutegund. Með því að sameina þessar tvo þætti (virði miðað við magn) og tiltekinn afurðir samanborið við afurðaflokka, fáum við fjórar gerðir ráðstöfunar:

-   **ráðstöfun afurðarmagns**– viðskiptavinurinn fellst á að kaupa ákveðið magn afurða. Línur sem nota þessa gerð ráðstöfunar eru skilgreindar eftir vörunúmeri, og magni og einingu sem samið var um. **Upphæð** svæði ekki tiltækt.
-   **Virðisráðstöfun afurðar** – Viðskiptamaðurinn samþykkir að kaupa tiltekna afurð fyrir tiltekna upphæð. Línur sem nota þessa gerð ráðstöfunar eru skilgreindar eftir vörunúmeri, og upphæði sem samið var um. **Magn** og **Einingu** svæði ekki eru tiltæk.
-   **Virðisráðstöfun afurðategundar** – Viðskiptamaðurinn samþykkir að kaupa afurð úr tiltekinni söluflokkur fyrir tiltekna upphæð. Línur sem nota þessa gerð ráðstöfunar eru skilgreindar eftir söluflokki í stigveldi sölutegunda og upphæð. **Magn** og **Einingu** svæði ekki eru tiltæk.
-   **Virðisráðstöfun** – Viðskiptamaðurinn samþykkir að hvaða afurð eða afurðir sem er í hvaða innkaupategund sem er fyrir tiltekna upphæð. **Magn** og **Einingu** svæði ekki eru tiltæk.

Línur í sama sölusamnings getur haft mismunandi gerðir af ráðstafanir.

## <a name="pricing-terms-for-sales-agreements"></a>Verðskilmálar fyrir innkaupasamninga
Verðskilmálra geta verið mismunandi, allt eftir skuldbindingu. Á sölupöntun sem er tengd við sölusamningur, , verðskilmálar úr þeim sölusamningur hnekkja alla aðra verðskilmálar sem eiga við á grundvelli viðskiptasamningar. Eftirfarandi tafla lýsir verðtengdum reitum sem hafa árhfia á ráðstöfunargerð. Já gefur til kynna að hægt er að uppfæra reit á pöntunarlínu.

| Ráðstöfunargerð                   | Einingarverð | Einingarverð | Afsláttarprósenta | Upphæð staðgreiðsluafsláttar |
|-----------------------------------|------------|------------|------------------|----------------------|
| Ráðstafað afurðarmagn       | Já        | Já        | Já              | Já                  |
| Ráðstöfunarvirði afurðar          |            |            | Já              |                      |
| Ráðstöfunarvirði vörutegundar |            |            | Já              |                      |
| Ráðstöfunarvirði                  |            |            | Já              |                      |

## <a name="policies-for-sales-agreements"></a>Reglur fyrir sölusamninga
Eftirfarandi stefnur hafa áhrif á það hvernig tengsl er milli skuldbindingar sölusamnings og samsvarandi sölupöntunarlínur virka:

-   **Hámark er tryggt** - Heildarmagn eða upphæð fyrir allar pöntunarlínur geta ekki verið meiri en magnið eða upphæðin sem er tilgreind á viðkomandi skuldbindingu.
-   **Verð og afsláttur eru föst** – Verðið á pöntunarlínu og verðið á tengdu skuldbindingu getur ekki verið mismuanndi. Ef verðið er breytt á pöntunarlínu rofnar tengiliinn við skuldbindinguna. Ef tengillinn er rofinn úthlutar pöntunarlínan ekki til uppfyllingar skuldbindingarinnar.
-   **Lágmarks losunarupphæð** Og **hámarks losunarupphæð** – Ef upphæð er tilgreind birtast skilaboð ef einhver breyting er gerð á pöntunarlínu sem veldur því að pöntunarlínan verði frábrugðin tengdu skuldbindingunni.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Útreikningur uppfyllingar fyrir sölusamninga
**Uppfyllingar** flipi á **Línuupplýsingar** flýtiflipa á síðunni **sölusamningar** sýnir magn uppfyllingar og upphæðir.  

Í því **uppfyllingar**  svæði, er hægt að skoða samtals magn og upphæðir fyrir allar pöntunarlínur sem eru tengdar við tilgreinda sölusamninga. Einnig er hægt að skoða eftirstandandi upphæð eða magn sem þarf til að uppfylla ráðstöfun.  

Í því **samningur**  svæði, er hægt að skoða magn og upphæðir fyrir úr tilgreinda sölusamninga. Þessi magn og upphæðir eru samtals magn og upphæðir sem voru staðfest.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Staðfestinga- og útgáfusögu fyrir sölusamninga
Þegar sölusamningur er staðfestur er núverandi útgáfa sölusamnings vistuð í sögutöflu. Ef sölusamningur er breytt hægt að staðfesta hann aftur til að geyma aðra útgáfu af sölusamningur í sögu.  

Ef sölusamningur er ekki staðfest enn hægt að nota hann til að stofna sölupöntun. Hins vegar eru söguupplýsingar sölusamnings ekki vistuð.  

Hægt er að forskoða eða prenta allar endurskoðanir af staðfestingunum. Svo er hægt að deila endurskoðunum til viðskiptavinar til að fá samþykki.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Jafna sölusamninga í pöntunarferli
Ef ekki er að losa sölupantanir beint fyrir sölusamninga, hægt samt að tengja sölusamning við pöntun við ferli pöntunarfærsla. Þegar verið er að stofna nýja sölupöntun og velja sölusamning, eru skilmálar þess samnings, eins og greiðsluskilmálar, afhendingarskilmálar, og afhendingaraðsetur, eru jafnaðar í pöntunarhaus, og tengingu milli samning og pöntunin er stofnuð. Síðan, pöntunarlínum, er hægt að velja afurðir og tegundirnar sem eru tilgreindar í sölusamningnum, verðin og afslættirnir eru afritaðir úr þeim samningi. Í sömu sölupöntun geta verið báðar línur sem eru ekki tengdar við sölusamning og línur sem hafa ráðstöfun fyrir sölusamning.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Breyta sölupantanir sem eru tengdar við sölusamninga
Ef hefur verið stofnað (losað) sölupöntun gagnvart sölusamning, sum svæði í sölupöntunarlínum er hægt að breyta eingöngu ef þú fjarlægir hlekkinn í tengdar sölusamningslínur. Eftirfarandi tafla sýnir sumum þessara reita.

| Reitur                                                             | Lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umbeðin sendingardagsetning                                               | Ef þú breytir umbeðin sendingardagsetning til dagsetning sem er fyrri en gildi **Gildisdagsetningar** á sölusamningslína, verður þú fjarlægja hlekkinn í sölusamningslína áður en þú getur vistað breytt sendingardagsetning. Ef þú breytir umbeðin sendingardagsetning til dagsetning sem er seinni en gildi **lokadagsetningar** á sölusamningslína, verður þú fjarlægja hlekkinn í sölusamningslína áður en þú getur vistað breytt sendingardagsetning. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet amount | Ef þú breyta gildinu í einhverju af þessum svæðum, og ef **Verð og afsláttur er föst** gátreiturinn er valinn á tengda sölusamningslínu, biður skilaboðagluggi um að vista breytingarnar. Smellið á **Já** til að fjarlægja hlekkinn í sölusamningslínuna og endurreikna verð. Smellið á **Nei** til að fjarlægja hlekkinn í sölusamningslínuna án þess að endurreikna verð.                                                                   |
| Nettóupphæð                                                        | Ef tilgreina á upphæð sem er hærri en upphæðin sem er tilgreint á sölusamningslína þar sem **Hámark er tryggt** gátreiturinn er valinn, biður skilaboðagluggi um að vista breyttar upphæð. Smellið á **Já** til að fjarlægja hlekkinn í sölusamningslínuna og endurreikna verð. Smellið á **Nei** til að fjarlægja hlekkinn í sölusamningslínuna án þess að endurreikna verð.                                                                 |
| Magn                                                          | Ef tilgreina á magn sem er hærri en magnið sem er tilgreint á sölusamningslína þar sem **Hámark er tryggt** gátreiturinn er valinn, biður skilaboðagluggi um að vista breyttar magn. Smellið á **Já** til að fjarlægja hlekkinn í sölusamningslínuna og endurreikna verð. Smellið á **Nei** til að fjarlægja hlekkinn í sölusamningslínuna án þess að endurreikna verð.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Skila vöru sem var pöntuð úr sölusamningi
Þegar viðskiptamaður skilar afurð sem hefur verið pöntuð úr sölusamningi, getur Microsoft Dynamics 365 for Finance and Operations fundið og uppfært sjálfkrafa tengda ráðstöfun sölusamnings til að endurspegla breytingar á magni eða upphæð. Með því að stofna vöruskilapöntun byggða á upprunalegu sölupöntuninni sem er tengd við sölusamning,staðfestir þú tengsl milli sölusamnings, ráðstöfunar sölusamnings, sölusamningslína og reiknings vöruskilapöntunar.  

Ef ekki á að draga frá skilavörumagnið úr ráðstöfun sölusamnings er hægt að nota stýringuna **fjarlægja hlekk** í síðunni **skilapöntun** til að fjarlægja tengingu milli skilapöntunar og ráðstöfunar sölusamnings . Ef þú þarft að endurstofna tengil síðar, er smellt á **stofna tengil**.  

**Athugasemd** Vöruskilapöntun getur aðeins tengst einum sölusamningi. Ef viðskiptamaðurinn skilar fleiri en einni afurð sem hefur verið pöntuð frá fleiri en einum sölusamningi þarf að stofna nýja skilapöntun fyrir hverja afurð og búa til tengingu í samsvarandi sölusamning.

## <a name="automatic-search-for-sales-agreements"></a>Sjálfvirk samningsleit sölusamninga
Í sumum aðstæðum þar sem sölupantanir eru stofnaðar óbeint, eins og þegar sölupantanir innan samstæðu eða kreditnótu er stofnað, er hægt að stjórna því hvort Microsoft Dynamics 365 for Finance and Operations leitar sjálfvirkt að viðeigandi sölusamninga.

## <a name="financial-dimensions-on-sales-agreements"></a>Fjárhagsvíddir í sölusamningum
Hægt er að afrita fjárhagsvíddir í annað hvort skjalhausa eða í einstakar línur sölusamnings. Hægt er að breyta víddum á samningshaus eða samningslínu hvenær sem er. Í þessu tilfelli eru víddir svo sjálfkrafa afritaðar í útgáfuhaus eða losunarlínu úttektarpöntunar.




