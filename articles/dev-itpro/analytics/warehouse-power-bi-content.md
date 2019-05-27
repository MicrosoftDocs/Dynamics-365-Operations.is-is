---
title: Afköst vöruhúss Power BI efni
description: Þetta efnisatriði lýsir því sem er innifalið í afköstum vöruhúss Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.
author: Mirzaab
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 99966a67fa1fd91fc54e7100f8e2e41b87f6a406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551137"
---
# <a name="warehouse-performance-power-bi-content"></a>Afköst vöruhúss Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Afköst vöruhúss** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Afköst vöruhúss** Power BI-efnið var stofnað til að hjálpa vöruhúsa- og verkstjórum að fylgjast með því sem kemur inn, fer út sem og mælikvörðum birgða. Notast er við vöruhúsakerfi, vörur og önnur færslugögn úr kerfinu þínu, og birtir bæði uppsöfnuð afköst vöruhúss og sundurliðun lánardrottna, vöruflokka og vörur, og svæði og vöruhús.

Vöruhúsastjórnendur geta notað **Afköst vöruhúss** Power BI-efnið til að mæla eftirfarandi þrjú svæði:

- **Afköst á innleið** – Mælir það hversu vel lánardrottinn framkvæmir gagnvart kröfum viðskiptavina (með öðrum orðum afhendingarafköst) og mælir frágangsafköst svo að hægt sé auðkenna vandamál sem snerta starfskrafta eða vörur yfir tímabil. Það er mikilvægt að vitað hvort lánardrottnar afhendi á réttum tíma, snemma eða seint, þannig að hægt sé að ákvarða hvernig frammistaða þeirra hefur áhrif á frágangsafköst. Lánardrottinn sem afhendir utan þeirra dagsetninga sem voru ákveðnar getur sett pressu á vöruhúsið vegna óvæntrar vinnu, og getur aukið meðaltíma frágangs.
- **Sendingarframmistaða** – Mælir hvort vöruhúsið sendir að fullu og tímanlega til viðskiptavina (með öðrum orðum mæling á sendingum og afhendingu), þannig að hægt er að auðkenna vandamál sem snerta vörur, svæði eða vöruhús eða tiltekna viðskiptavini. Ef verið er að senda seint á tiltekin svæði eða bæja gæti þurft að veita flutningi eða reikningastjórnun meiri athygli.
- **Nákvæmni staðsetningarbirgða** – Nákvæmni birgða er mikilvægt fyrir viðskiptagreind innri vöruhús (BI). Það er mjög mikilvægt að ákvarðað sé hversu nákvæmlega talning er almennt. Þó er einnig er mikilvægt að ákvarða hvernig nákvæmlega vörur eru geymdar á réttum stöðum, og að misræmisgögn séu auðkenn þannig að hægt sé að finna betri stöður fyrir vörur eða hefja allsherjartalningu á tilteknum vörum. (Eins og er, er nýja talningarvirknin afhent sem bráðabót.) Ef verið er að nota þetta Power BI-efni til að ákvarða nákvæmni lagerbirgða eftir staðsetningu, er einnig hægt að greina þjófnaði í verslunum. Einnig er hægt að ákvarða hvort staðsetningar hafa lagermagn sem er frábrugðið ERP (Enterprise Recource Planning). Staðsetningarnar gætu verið of stórar eða ómögulegt að telja. Einnig kunna sumar efnislegar staðsetningu að vera rangar, þannig að erfitt sé að hafa eina gerð vöru samstillta við gögn á lager.

## <a name="accessing-the-power-bi-content-pack"></a>Farið í Power BI efnispakkann
**Afköst vöruhúss** Power BI-efni er sýnt á síðunni **Afköst vöruhúss** (**Vöruhúsastjórnun** \> **Fyrirspurnir og skýrslur** \> **Greining á afköstum vöruhúss** \> **Afköst vöruhúss**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI efni
**Afköst vöruhúss** Power BI-efni inniheldur skýrslu. Skýrslan samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í **Afköst vöruhúss** Power BI-efni .

| Skýrslusíða                 | Gröf                                   | lýsing |
|-----------------------------|------------------------------------------|-------------|
| Afköst á innleið         | Samtala frágangs                          | Fjöldi frágangslína sem eru unnar á tilteknum tíma. |
| Afköst á innleið         | Meðaltími frágangs                    | Meðaltími í klukkustundum, fyrir allar frágangslínur innkaupapöntunar sem eru unnar úr skráning vara þar til síðasti frágangur fer fram. |
| Afköst á innleið         | Móttekið fyrir tímann                           | Fjöldi innkaupapöntunarlínur sem eru mótteknar snemma. |
| Afköst á innleið         | Móttekin á réttum tíma                         | Fjöldi innkaupapöntunarlínur sem eru mótteknar á réttum tíma. |
| Afköst á innleið         | Móttekið seint                            | Fjöldi innkaupapöntunarlínur sem eru mótteknar of seint. |
| Afköst á innleið         | Á réttum tíma frá lánardrottni                        | Prósenta innkaupapöntunarlína sem eru mótteknar frá lánardrottni eða lánardrottnaflokki snemma, tímanlega og of seint. |
| Afköst á innleið         | Meðaltal frágangs frá dokku til birgða (klukkustundir) | Meðaltal frágangs frá dokku til birgða í klukkustundum yfir tíma. |
| Afköst á innleið         | Meðaltal frágangs eftir starfskrafti               | Meðaltími, í klukkustundum sem starfskraftur hefur notað í frágang innkaupapöntunarlína. |
| Afköst á innleið         | Meðaltími í klukkustundum eftir lánardrottnum          | Meðaltími frágangs í klukkustundum eftir lánardrottni eða lánardrottnaflokki. |
| Afköst á innleið         | Meðaltími frágangs í klukkustundum eftir vöru         | Meðaltími frágangs í klukkustundum eftir vöru eða vöruflokki. |
| Nákvæmni staðsetningarbirgða | Heildartalning                              | Fjöldi taldra vinnulína sem eru meðhöndlaðar fyrir tiltekið tímabil. |
| Nákvæmni staðsetningarbirgða | Misræmisgengi                         | Heildarmisræmi sem prósenta af öllum línum sem eru taldar á tilteknu tímabili. |
| Nákvæmni staðsetningarbirgða | Telja án misræmis                | Af heildarfjölda taldra vinnulína sem eru meðhöndlaðar, fjöldi lína sem eru meðhöndlaðar án misræmis. |
| Nákvæmni staðsetningarbirgða | Vörur taldar yfir tíma                  | Prósenta vara sem eru taldar með og án misræmis yfir tíma. |
| Nákvæmni staðsetningarbirgða | Vörumagn þar sem misræmi er hærra en % | Töfluyfirlit yfir taldar línur með misræmi sem fara fram úr tilgreindri prósentu. Tafla inniheldur upplýsingar um staðsetningar, vörur, meðaltal misræmis, heildartalning vinnulína sem eru taldar, fjölda talningarlínur með misræmi fyrir staðsetninguna, meðaltalsmagn sem er talið, væntanlegt heildarmagn sem verður talið og raunmagn vörunnar sem er reiknuð. |
| Nákvæmni staðsetningarbirgða | Vörutalning eftir starfskrafti                     | Talningarafköst starfskrafta. Afköst eru tilgreind sem prósenta af talningu vinnulína með og án misræmis. |
| Nákvæmni staðsetningarbirgða | Vara eftir svæði / vöruhúsi           | Talningarafköst eftir fjölda meðhöndlaðra talinna vinnulína eftir stað eða vöruhúsi með og án misræmis. |
| Nákvæmni staðsetningarbirgða | Misræmisgengi eftir vöru              | Misræmisfjöldi fyrir talningarafköst. Fjöldi er táknaður sem prósenta af meðhöndluðum talningarlínum eftir vöru eða vöruflokki. |
| Sendingarframmistaða        | Línur sendar                            | Heildarfjöldi sendingarlína sem eru sendar á tilteknum tíma. |
| Sendingarframmistaða        | Á undan áætlun                                    | Prósenta sendingarlína sem eru sendar snemma. |
| Sendingarframmistaða        | Á réttum tíma                                  | Prósenta sendingarlína sem eru sendar á tíma. |
| Sendingarframmistaða        | Á eftir áætlun                                     | Prósenta sendingarlína sem eru sendar seint. |
| Sendingarframmistaða        | Sending eftir tíma                      | Prósenta sendingarlína sem eru sendar á tíma, snemma eða seint yfir tiltekið tímabil. Leitnilína sýnir leitni fyrir línur sem eru sendar á réttum tíma. |
| Sendingarframmistaða        | Sent seint eftir borg                     | Kort yfir borgir og svæði sem verða fyrir áhrifum af seinni sendingu. |
| Sendingarframmistaða        | Sent eftir afurð                       | Prósenta sem er send snemma, á tíma, eða seint eftir vöru eða vöruflokki. |
| Sendingarframmistaða        | Sent eftir viðskiptavini                      | Prósenta sem er send snemma, á tíma, eða seint eftir viðskiptavini eða viðskiptavinaflokki. |
| Sendingarframmistaða        | Sent eftir svæði / vöruhús              | Sú prósenta sem er send snemma, á tíma, eða seint eftir svæði eða vöruhúsi. |

## <a name="understanding-the-data-model-and-calculations"></a>Að skilja gagnalíkan og útreikning
Eftirfarandi gögn eru notuð til að fylla út í skýrslusíðurnar í **Afköst vöruhúss** Power BI efni. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Eftirfarandi lykiluppsafnaðar mælingar eru notaðar sem grunnur að efninu.

| Skýrslusíða                 | Gröf                                   | Töflur                                | Lýsing útreiknings |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Afköst á innleið         | Samtala frágangs                          | WHSWorkLine                           | Fjöldi vinnulína þar sem vinnugerðin er **frágangur**. |
| Afköst á innleið         | Meðaltími frágangs                    | WHSWorkLine                           | Samtala hámarkstími vinnulína deilt með fjölda vinnulína hámarkstíma, þar sem vinnulínur hámarkstími er hámarksbil milli stofndags vinnu og lokadags. |
| Afköst á innleið         | Móttekið fyrir tímann                           | WHSWorkLine                           | Talning vinnulína þar sem stofndagur vinnu er á undan afhendingardegi sem er notaður. Ef staðfestingardagur afhendingar er ekki valinn skal nota sjálfgefinn afhendingardag. |
| Afköst á innleið         | Móttekin á réttum tíma                         | WHSWorkLine                           | Talning vinnulína þar sem stofndagur vinnu er sami og afhendingardagur sem er notaður. Ef staðfestingardagur afhendingar er ekki valinn skal nota sjálfgefinn afhendingardag. |
| Afköst á innleið         | Móttekið seint                            | WHSWorkLine                           | Talning vinnulína þar sem stofndagur vinnu er á eftir afhendingardegi sem er notaður. Ef staðfestingardagur afhendingar er ekki valinn skal nota sjálfgefinn afhendingardag. |
| Afköst á innleið         | Á réttum tíma frá lánardrottni                        | WHSWorkLine                           | Móttekið snemma, Móttekið á tíma og Móttekið seint (sjá lýsingu fyrr í þessari töflu). |
| Afköst á innleið         | Meðaltal frágangs frá dokku til birgða (klukkustundir)   | WHSWorkLine                           | Meðaltími frágangs (sjá lýsingu fyrr í þessari töflu). |
| Afköst á innleið         | Meðaltal frágangs eftir starfskrafti               | WHSWorkLine                           | Meðaltími frágangs (sjá lýsingu fyrr í þessari töflu). |
| Afköst á innleið         | Meðaltími í klukkustundum eftir lánardrottnum          | WHSWorkLine                           | Meðaltími frágangs (sjá lýsingu fyrr í þessari töflu). |
| Afköst á innleið         | Meðaltími frágangs í klukkustundum eftir vöru         | WHSWorkLine                           | Meðaltími frágangs (sjá lýsingu fyrr í þessari töflu). |
| Nákvæmni staðsetningarbirgða | Heildartalning                              | WHSWorkLineCycleCount                 | Talning þar sem algilt misræmismagn er jafnt eða meira en 0 (núll). |
| Nákvæmni staðsetningarbirgða | Misræmisgengi                         | WHSWorkLineCycleCount                 | Talning með misræmi, deilt með heildarfjölda. Talning telst með misræmi ef algilt misræmismagn er meira en 0 (núll). |
| Nákvæmni staðsetningarbirgða | Telja án misræmis                | WHSWorkLineCycleCount                 | Talning þar sem algilt misræmismagn er meira en 0 (núll). |
| Nákvæmni staðsetningarbirgða | Telja með misræmi                   | WHSWorkLineCycleCount                 | Talning þar sem algilt misræmismagn er jafnt og 0 (núll). |
| Nákvæmni staðsetningarbirgða | Vörur taldar yfir tíma                  | WHSWorkLineCycleCount                 | Talning án misræmis og talning með misræmi (Sjá lýsingu fyrr í þessari töflu.) |
| Nákvæmni staðsetningarbirgða | Vörumagn þar sem misræmi er hærra en % | WHSWorkLineCycleCount                 | Meðaltal misræmis er algilt misræmismagn deilt með væntu magni þar sem misræmismagnið er meira en 0 (núll). Meðaltal misræmismagn er meðaltal algilts misræmismagns þar sem misræmismagnið er meira en 0 (núll). Talning með misræmi, heildartalning, væntanlegt magn og talið magn þar sem heildarmagn er flokkað eftir vöru og staðsetningu (sjá lýsingu fyrr í þessari töflu). |
| Nákvæmni staðsetningarbirgða | Vörutalning eftir starfskrafti                     | WHSWorkLineCycleCount                 | Talning án misræmis og talning með misræmi (sjá lýsingu fyrr í þessari töflu). |
| Nákvæmni staðsetningarbirgða | Vara eftir svæði / vöruhúsi           | WHSWorkLineCycleCount                 | Talning án misræmis og talning með misræmi (sjá lýsingu fyrr í þessari töflu). |
| Nákvæmni staðsetningarbirgða | Misræmisgengi eftir vöru              | WHSWorkLineCycleCount                 | Misræmistíðni (sjá lýsingu fyrr í þessari töflu). |
| Sendingarframmistaða        | Línur sendar                            | SalesLine               | Talning sölulína þar sem sölulínurnar eru sendar. |
| Sendingarframmistaða        | Á undan áætlun                                    | CustPackingSlipOnTimeStatus           | Sölulínur þar sem staða sendingardagsetningar er **1 (Snemma)**. Fljótt þýðir að sendingardagsetning á fylgiseðli kemur á undan staðfestri sendingardagsetning á sölulínu. Ef staðfest sendingardagsetning er ekki valin skal nota umbeðna sendingardagsetningu. |
| Sendingarframmistaða        | Á réttum tíma                                  | CustPackingSlipOnTimeStatus           | Sölulínur þar sem staða sendingardagsetningar er **2 (Á tíma)**. Á tíma þýðir að sendingardagsetning á fylgiseðli er jöfn staðfestri sendingardagsetning á sölulínu. Ef staðfest sendingardagsetning er ekki valin skal nota umbeðna sendingardagsetningu. |
| Sendingarframmistaða        | Á eftir áætlun                                     | CustPackingSlipOnTimeStatus           | Sölulínur þar sem staða sendingardagsetningar er **3 (Seint)**. Seint þýðir að sendingardagsetning á fylgiseðli kemur á eftir staðfestri sendingardagsetning á sölulínu. Ef staðfest sendingardagsetning er ekki valin skal nota umbeðna sendingardagsetningu. |
| Sendingarframmistaða        | Sending eftir tíma                      | SalesLine CustPackingSlipOnTimeStatus | Pantanirnar sem eru sendar að fulla, þar sem allt magn sölulínu er sent, auk Snemma, Á tíma og Seint (sjá lýsingu fyrr í þessari töflu). |
| Sendingarframmistaða        | Sent seint eftir borg                     | CustPackingSlipOnTimeStatus           | Seint (sjá lýsingu fyrr í þessari töflu). |
| Sendingarframmistaða        | Sent eftir afurð                       | CustPackingSlipOnTimeStatus           | Snemma, Á tíma og Seint (sjá lýsingu fyrr í þessari töflu). |
| Sendingarframmistaða        | Sent eftir viðskiptavini                      | CustPackingSlipOnTimeStatus           | Snemma, Á tíma og Seint (sjá lýsingu fyrr í þessari töflu). |
| Sendingarframmistaða        | Sent eftir svæði / vöruhús              | CustPackingSlipOnTimeStatus           | Snemma, Á tíma og Seint (sjá lýsingu fyrr í þessari töflu). |
