---
title: "Verðherming"
description: "Þessi grein gefur upplýsingar um verðhermingu fyrir tilboð. Verðherming hjálpar til við að meta áhrif frádráttar á söluverð í framtíðinni í tilboðsferlinu, áður en staðfest er sérstakt verð."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53809f5fe68efd6334f362a517faa81bdf1abb18
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="price-simulation"></a>Verðherming

[!include[banner](../includes/banner.md)]


Þessi grein gefur upplýsingar um verðhermingu fyrir tilboð. Verðherming hjálpar til við að meta áhrif frádráttar á söluverð í framtíðinni í tilboðsferlinu, áður en staðfest er sérstakt verð.

Verðherming fyrir tilboð sýnir nýja heildarupphæð, á grundvelli tillögu um nýtt verð. Verðherming getur einnig sýna nýja upphæð fyrir tiltekna línu sem er stofnuð í fyrirliggjandi tilboði. Hægt er að færa inn verðhermingu og nota síðar. Að öðrum kosti, er Hægt að nota upprunalegt tilboð án verðhermingar og gera frekari breytingar á meðan söluferlið stendur yfir með viðskiptavininum.  

Verðherming breyta ekki verðið í tilboðið. Ef verðhermun er beitt á allt tilboðið, er hún meðhöndluð sem sérstakur afsláttur í tilboðshausnum. Ef verðhermun er beitt á tiltekna vöru, er hún meðhöndluð sem sérstakur afsláttur í tilboðslínunum. Einingarsöluverð á tilboðslínunni sem er stofnuð breytist ekki þegar verðherming er notuð. Þess í stað er notuð afsláttarprósenta sem samsvarar verðlækkuninni í tilboðslínunni. Þegar verðhermingin er notuð, er einingarsöluverð og afsláttarprósentan flutt í tilboðslínuna eða tilboðshausinn.  

**Athugasemd** Þegar verðherming er framkvæmd er eingöngu gildandi sölugjaldmiðill notaður til þess að stofna herminguna. Hinsvegar, Þegar samtölur tilboða eru skoðaðar sjást hins vegar samsetning sölugjaldmiðils og fyrirtækisgjaldmiðils.  

Fylgivörur sem bætt er við tilboðslínur gæti sett af stað línuafsláttar eða samvalsafsláttar. Þær gætu einnig virkja heildarafslátt sem breyta framlegð og framlegðarstigi tilboðslínanna tilboðslína og alls afsláttarins.  

Hægt er að keyra margar verðhermingar til þess að rekja áhrif verðleiðréttinga á tilboðsmarkið. Keyrsla verðherminganna gerir mögulegt að leiðrétta heildarverð tilboðs, eða verð á einni línu eða tilteknum línum í tilboðinu, og síðan beita þeirri verðhermingu sem líklegust er til þess að hjálpa þér að ná sölunni.  

Hægt er að setja upp viðvörun þegar tilboð er stofnað. Hér eru nokkrar aðferðir sem viðvaranir eru notaðar við:

-   Þeir geta halda þér upplýstum um stöðu tilboða innan fyrirtækisins.
-   Til þess að setja af stað yfirferð á tilteknu tilboði, eða upplýsa þig um hvenær farið hefur verið yfir hámarksafsláttarmörk.

## <a name="price-simulation-and-discounts"></a>Verðlíking og afslættir
Til að tryggja að afslættir og verð séu rétt reiknuð þarf að sýna varkárni þegar keyrð er verðherming á tilboðum með afslætti. Þar sem farið er með allar verðhermingar sem sérstakan afslátt á virku tilboðslínunni eða öllu tilboðinu, verður að rekja mismuninn á afsláttunum.

### <a name="types-of-discounts-in-trade-agreements"></a>Gerð afsláttar í viðskiptasamningum

Viðskiptasamningar í Microsoft Dynamics 365 for Operations geta haft fjórar gerðir verðafsláttar. Hægt er að setja þessa afslætti upp fyrir mismunandi vörur, viðskiptavini eða verðflokka og hægt er að takmarka þá við dagsetningar. Til að forðast vitlausa útreikninga þarf að íhuga viðskiptasamninga þegar verðherming er keyrð. Hér eru Fjórar afsláttargerðir í viðskiptasamningum:

-   **Söluverð** - Hægt er að tilgreina aðskilin söluverð fyrir tilteknar vörur. Þegar tilboðslínur eru stofnaðar leitar forritið að réttu söluverði fyrir vöru og flytur það í tilboðslínur. Þess vegna hefur viðskiptasamningur með þessi gerð afsláttar ekki áhrif á verðhermingu. Söluverð sem er notað í tilboðslínunni endurspeglar viðskiptasamning.
-   **Línuafsláttur** – Sérstakan afslátt eru tilgreindar fyrir vörur eftir magni sem er pantað. Línuupphæðir eru yfirleitt lækkaðar af línuafsláttur áður en verðherming er keyrð. Þess vegna hefur viðskiptasamningur með þessi gerð afsláttar áhrif á verðhermingu.
-   **Samvalsafsláttur** - Ef sameinaður fjöldi fer yfir þau mörk sem þú hefur tilgreint, virkja fyrirfram tilgreindar samsetningar pantaðra vara afslátt á alla pöntunina. Línuupphæðir eru yfirleitt lækkaðar af línuafsláttur áður en verðherming er keyrð. Þess vegna hefur viðskiptasamningur með þessi gerð afsláttar áhrif á verðhermingu.
-   **Heildarafsláttur** - Ef sameinaður upphæð fer yfir þau mörk sem þú hefur tilgreint, virkja fyrirfram tilgreindar pantaðar vörur afslátt á alla pöntunina. Heildarafslátturinn er myndaður af tilboðslínunum. Hins vegar þar heildarafsláttur er notaður á samtölu tilboðs sem afsláttur, lækkar það heildarupphæð tilboðs. Þess vegna hefur viðskiptasamningur með þessi gerð afsláttar áhrif á verðhermingu.

### <a name="quotation-lines-and-trade-agreements"></a>Tilboðslínur og viðskiptasamningar

Þegar þú stofna eða leiðrétta tilboðslínu eru línuafslættir reiknaðir sjálfkrafa. Viðeigandi söluverð finnst fyrir vöru, byggt á viðskiptasamningsins.

## <a name="price-simulation-examples"></a>Dæmi um verðlíkingu
Eftirfarandi dæmi nota verðhermi fyrir tilboðshausa og vörur með eina línu.

### <a name="price-simulation-for-quotation-headers"></a>Verðhermir tilboðshausa

Notandi gerir tilboð sem er með eftirfarandi línum:

-   10 einingar af vöru BR-12 (kostnaðarverð á hverja einingu USD 9,52 og söluverð á hverja einingu USD 15,32).
-   12 einingar af vöru BR-14 (kostnaðarverð á hverja einingu USD 7,48 og söluverð á hverja einingu USD 13,75).

Eftirfarandi tafla sýnir tilboðslínurnar.

|                            | Útreikningur                          | Niðurstaða   |
|----------------------------|--------------------------------------|----------|
| Sölumagn             | 10 einingar + 12 einingar                  | 22 einingar |
| Sölugildi í Bandaríkjadölum         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kostnaðargildi í Bandaríkjadölum          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Framlegð í Bandaríkjadölum | 318,20 – 184,96                      | 133,24   |
| Framlegðarhlutfall         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87%   |

Verðhermir er keyrður og þú notar 15 prósent heildarafsláttur fyrir allt tilboðið eða tilboðshausinn. Eftirfarandi tafla sýnir nýju heildartölur tilboðsins eftir að verðherming er keyrð.

|                                                      | Útreikningur                               | Niðurstaða   |
|------------------------------------------------------|-------------------------------------------|----------|
| Sölumagn                                       | 10 einingar + 12 einingar                       | 22 einingar |
| Gamalt sölugildi í Bandaríkjadölum                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Gamalt kostnaðargildi í Bandaríkjadölum                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Gömul framlegð í Bandaríkjadölum                       | 318,20 – 184,96                           | 133,24   |
| Gamalt framlegðarhlutfall                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87%   |
| Verðherming uppá 15% heildarafslátt í Bandaríkjadölum | (15 × 318.2) ÷ 100                        | 47,73    |
| Nýtt sölugildi í Bandaríkjadölum                               | 318,20 – 47,73                            | 270,47   |
| Ný framlegð í Bandaríkjadölum                       | 270,47 – 184,96                           | 85,51    |
| Nýtt framlegðarhlutfall                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61%   |

### <a name="price-simulation-for-single-line-items"></a>Verðhermir fyrir vörur í einni línu

Notandi gerir tilboð sem er með eftirfarandi línum:

-   10 einingar af vöru BR-12 (kostnaðarverð á hverja einingu USD 9,52 og söluverð á hverja einingu USD 15,32).
-   12 einingar af vöru BR-14 (kostnaðarverð á hverja einingu USD 7,48 og söluverð á hverja einingu USD 13,75).

Eftirfarandi tafla sýnir tilboðslínurnar.

|                                      | Útreikningur                          | Niðurstaða   |
|--------------------------------------|--------------------------------------|----------|
| Sölumagn                       | 10 einingar + 12 einingar                  | 22 einingar |
| Söluvirði í USD fyrir BR-12         | 10 × 15,32                           | 153,20   |
| Söluvirði í USD fyrir BR-14         | 12 × 13,75                           | 165,00   |
| Kostnaðarvirði í USD fyrir BR-12          | 10 × 9,52                            | 95,20    |
| Kostnaðarvirði í USD fyrir BR-14          | 12 × 7,48                            | 89,76    |
| Framlegð í USD fyrir BR-12 | 153,20-95,20                       | 58,00    |
| Framlegð í USD fyrir BR-14 | 165,00-89,76                       | 75,24    |
| Hlutfall framlegðar í USD fyrir BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Hlutfall framlegðar í USD fyrir BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Heildarsölugildi í Bandaríkjadölum             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Heildarkostnaðarvirði í USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Heildarframlegð í Bandaríkjadölum     | 318,20 – 184,96                      | 133,24   |
| Heildarframlegðarhlutfall             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87%   |

Verðhermir er keyrður og notaður er 10 prósent heildarafsláttur á BR-12 einingar. Eftirfarandi tafla sýnir nýju heildartölur tilboðsins eftir að verðherming er keyrð fyrir staka línuatriðið.

|                                                   | Útreikningur                             | Niðurstaða   |
|---------------------------------------------------|-----------------------------------------|----------|
| Sölumagn                                    | 10 einingar + 12 einingar                     | 22 einingar |
| Gamalt sölugildi í Bandaríkjadölum fyrir BR-12                  | 10 × 15,32                              | 153,20   |
| Verðhermun uppá 10% afsláttur fyrir BR-12 | (10 × 153.2) ÷ 100                      | 15,32    |
| Nýtt sölugildi í Bandaríkjadölum fyrir BR-12                  | (10 × 15.32) – 15.32                    | 137,88   |
| Söluvirði í USD fyrir BR-14                      | 12 × 13,75                              | 165,00   |
| Kostnaðarvirði í USD fyrir BR-12                       | 10 × 9,52                               | 95,20    |
| Kostnaðarvirði í USD fyrir BR-14                       | 12 × 7,48                               | 89,76    |
| Ný framlegð í Bandaríkjadölum fyrir BR-12          | 137,88-95,20                          | 42,68    |
| Framlegð í USD fyrir BR-14              | 165,00-89,76                          | 75,24    |
| Nýtt framlegðarhlutfall í Bandaríkjadölum fyrir BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Hlutfall framlegðar í USD fyrir BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Nýtt heildarsölugildi í Bandaríkjadölum                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Heildarkostnaðarvirði í USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Ný heildarframlegð í Bandaríkjadölum              | 302,88 – 184,96                         | 117,92   |
| Nýtt heildarframlegðarstig                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93%   |

Verðhermirinn hefur eingöngu áhrif á línuna þar sem hann er notaður á og dregur úr samtölu þeirrar línu.




