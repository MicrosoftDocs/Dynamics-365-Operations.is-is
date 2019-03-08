---
title: Sjálfgefnar pöntunarstillingar fyrir víddir og afurðarafbrigði
description: Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b7c36553c9ad5bf4b061285d617be85ce77d0fcd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "326378"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Sjálfgefnar pöntunarstillingar fyrir víddir og afurðarafbrigði

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Sjálfgefið pöntunarstillingar í Microsoft Dynamics 365 for Finance and Operations skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Sjálfgefnar pöntunarstillingar eru notaðar þegar innkaupapantanir, sölupantanir, flutningspantanir, birgðabókum eru stofnaðar, og við aðaláætlanagerð til að mynda áætluð pöntun. Sjálfgefnar pöntunarstillingar geta verið tengdar ákveðnum vörum, svæðum, afurðarafbrigðum, eða afurðarvíddum.

Þú getur skilgreinir sjálfgefnar pöntunarstillingar á **Sjálfgefnar pöntunarstillingar** síðu. Til að opna þessa síðu farið í **Vöruupplýsingastjórnun** &gt; **Afurðir** &gt; **Losaðar afurðir** &gt; **Velja losaða afurð** &gt; á **Áætlun** eða **Stjórna birgðum** Aðgerðarrúða &gt; **Pöntunarstillingar** &gt; **Sjálfgefnar pöntunarstillingar**.

## <a name="default-order-settings"></a>Sjálfgefnar pöntunarstillingar
Það eru þrjár gerðir af sjálfgefnum pantanastillingum fyrir innkaup, sölu og birgðir. Sjálfgefnar pantanastillingar fyrir innkaup eru notaðar þegar stofnaðar eru:

-   Innkaupapöntunarlínur
-   Innkaupasamningslínur
-   Línur í beiðni um tilboð
-   Innkaupabeiðnilínur
-   Áfyllingarlínur vörusendingar
-   Innkaupatillögur

Sjálfgefnar pantanastillingar fyrir sölu eru notaðar þegar stofnaðar eru:

-   Sölupöntunarlínur
-   Sölusamningslínur
-   Sölutilboðslínur
-   Skilapantanalínur og skiptilínur vöru.
-   Eftirspurnarspárlínur

Sjálfgefnar sölupantanastillingar eiga einnig við þegar stofnaðar eru:

-   Vöruþarfir verks
-   Þjónustupöntun vöruþarfar

Sjálfgefnar pantanastillingar fyrir birgðir eru notaðar þegar stofnaðar eru:

-   Birgðabækur
-   Flutningspantanir
-   Flutningstillögur

Sjálfgefnar birgðapantanastillingar eiga einnig við þegar stofnaðar eru:

-   Biðgeymslupantanir
-   Gæðapantanir
-   Framleiðslupantanir
-   Uppskriftarlínur
-   Framleiðslutillögur

## <a name="full-definition-of-a-released-product"></a>Full skilgreining á útgefin afurð
Þegar færsla er stofnuð, þarf að tilgreina fulla skilgreiningu á losaðri afurð á línuna Finance and Operations reynir að auðkenna sjálfgefnar pantanastillingar. Full skilgreining fyrir útgefna afurð þýðir að vörunúmer og allar virkar afurðarvíddir, eins og afbrigði, stærð, stíl og lit, eru tilgreind í færslunni. Til dæmis, ef innkaupapöntunarlínu fyrir útgefin afurðarafbrigði eru stofnaðar handvirkt þarf að tilgreina allt nauðsynlegt afurðarvíddum áður en svæði, vöruhúsi, magn og afhendingartíma birtist sjálfkrafa í pöntunarlínu. 

Ekki allar sjálfgefnar færibreytur pöntunarstillinga eru notaðar stofnaðar eru pöntunar- eða færslubókarlínur. Magn og afhendingartími birtast aðeins sjálfgefið þegar við á. Til dæmis, þegar verið er að telja færslubókarlínu, birtist aðeins svæðið og vöruhús sjálfkrafa þegar línan er stofnuð. Augljóslega fer ekki fram nein sjálfgefið magn eða athuganir á mörgum eða lágmarki þegar verið er að stofna línuna eða bóka færslubókina. 

Kerfið reynir alltaf að finna sjálfgefið svæði og vöruhús þegar pöntunina eða færslubókarlínan er stofnuð. Svæðinu er ekki alltaf birt sjálfgefið úr pöntunarstillingum. T.d. þegar sölupöntun eða innkaupapöntun eru stofnaðar, er svæðið úr haus sjálfkrafa notað í pöntunarlínum. Þegar uppskriftarlína er stofnuð, er svæði úr haus Uppskriftar notaður. Þegar svæði er ákvarðað, verður það notað til að finna hvers kyns pöntunarstillingar sem tengjast tilteknu svæði sem má þá nota sem sjálfgefið fyrir vöruhúsið. 

Sjálfgefin pöntunargerð, innkaup og afhendingartíma í birgðir má hnekkja með þekjureglur vörunnar á **Vöruþekja** síðu. Þó svo sjálfgefnar pantanastillingar gefa ekki kost á því að greina á milli afhendingartíma framleiðslu og flutnings, þá leyfa þekjureglur vörunnar það. Hins vegar, uppsetningu vöruþekju verður aðeins notað af MRP (áætlanagerð í framleiðsluaðföngum) þegar stofnaðar eru framleiðslutillaga og flutningstillaga og er ekki notað þegar framleiðslupantanir eða flutningspantanir eru stofnaðar handvirkt. 

## <a name="default-order-settings-rules"></a>Reglur fyrir sjálfgefnar pöntunarstillingar
Hægt er að skilgreina almennar sjálfgefnar pantanastillingar og fjölda reglna fyrir sjálfgefna pöntunarstillingar sem eiga aðeins við sérstakar aðstæður, til dæmis svæði eða ákveðna afurðarvídd eða samsetningu afurðarvídda. Ekki er hægt að skilgreina pöntunarstillingar fyrir tiltekna vöruhúsi.

### <a name="rank-in-default-order-settings"></a>Forgangsröðun fyrir sjálfgefnar pöntunarstillingar

Sjálfgefnu pöntunarstillingar hafa forgangsröðun. Því hærra vægi í forgangsröðun, því mikilvægari er reglan, sem þýðir það mun hafa hærri forgang og notaðar á undan öðrum reglum með lægra vægi. Almenn sjálfgefnar pantanastillingar hafa vægi núll, sem ekki er hægt að breyta. Aðeins getur verið ein færsla með vægið núll. Reglur geta haft sama vægi, svo lengi sem víddirnar sem þær eiga við eru mismunandi. Þetta er gagnlegt til að sníða til pöntunarstillingar fyrir tiltekin svæði. Þegar ný sjálfgefin pöntunarstillingum er stofnuð erfast gildi fyrir gildi pantana, stöðvunarflagga, o. s. frv. úr reglu með vægi núll, en geta ekki verið hnekkt.

### <a name="default-order-settings-for-released-products"></a>Sjálfgefnar pöntunarstillingar fyrir útgefnar afurðir

Fyrir einkvæmrar útgefnar afurðir, er hægt að skilgreina almennar pöntunarstillingar eða pöntunarstillingar tiltekinna svæða. Almenn pöntunarstillingar hafa alltaf vægi núll. Ef sett er upp nýjar pöntunarstillingar fyrir sala, innkaup og birgðir á sama tíma, er mælt með því að nota **Upplýsingayfirlit** á í síðunni **Sjálfgefnar pöntunarstillingar**. Til að skipta yfir í upplýsingayfirlit, er farið í **Valkosti** Aðgerðarúðu &gt; **Valkostir síðu** &gt; **Breyta yfirliti** &gt; **Upplýsingayfirlit**.

### <a name="site-specific-order-settings"></a>Pöntunarstillingar tengdar svæði

Til að stofna pöntunarstillingar fyrir tiltekin svæði, smelltu á **Nýtt**. Í **Upplýsingayfirlit**, fylla út svæði í á **Stillingum fyrir** &gt; **Svæði** svæðinu. Í á **hnitanetsyfirlit**, fyllið út í svæðinu á **Svæði** dálkinn. Nýja reglu fær sjálfkrafa nýtt vægi, hærra en núll. Hægt er að stofna eins mörg reglur fyrir tiltekin svæði eftir þörfum og úthluta sama vægi fyrir reglur tiltekinna svæða, og sníða þær þannig að allar séu þær jafngildar. 

Ef þú ert í **Upplýsingayfirlit**, er ekki hægt að fá yfirlit yfir reglur sem eru stofnaðar fyrir vöruna. Víxla á **Sýna/Fela lista** hnappinn til að sjá yfirlit yfir upplýsingar. Þegar pöntunarlína af einhverri gerð er stofnuð og hún er ekki með neitt svæði úthlutað, leitar Finance and Operations að reglu sem ekki hefur tilgreint svæði. Þetta gæti auðveldað ákvörðun á sjálfgefið svæði á pöntunarlínu. Þetta svæði er síðan notaður til að leita að reglu fyrir tiltekin svæði, þar sem sjálfgefið vöruhús hefur hugsanlega verið stillt. Vöruhús er notaður í pöntunarlínuna.

### <a name="specific-order-settings-for-product-dimension"></a>Tilteknar Pöntunarstillingar fyrir afurðarvídd

Hægt er að tilgreina sjálfgefnar pantanastillingar sem eiga við allar virkar afurðarvídd eða alla virka samsetningu afurðavídda. Sé svæði afurðarvíddar tómt, þá gildir sú regla um öll gildi afurðarvíddarinnar. 

Íhugið eftirfarandi dæmi um vöru:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Afurðarheiti**                                    | Ljósnemi                    |
| **Vörunúmer**                                     | XW56                                    |
| **Skilgreining** (notað til að sníða til gerð ljóss) | C1 Sýnilegt rautt ljós, C2 innrautt ljós |
| **Stíll** (notað til að sníða til endurskoðun verkfræðinga)  | R1, R2, R3                              |

Í þessu dæmi, gerum ráð fyrir að afurðar er keypt og ekki framleidd. Gerið einnig ráð fyrir að skilgreiningu C1 er oftar notuð, svo hún hefur styttri afhendingartíma. 

Stofna eftirfarandi sjálfgefnar pantanastillingar til að sníða til líkanið í þessum aðstæðum.

| Vægi | Svæði | Grunnstilling | Stíll | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Já                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Þegar innkaupapöntunarlínu eða áætluð innkaupapöntun er stofnuð fyrir XW56, Skilgreiningu C1, óháð endurskoðun eða svæði sem línan er staðsett hjá, mun afhendingartími teljast vera 2. Gera ráð fyrir að allar endurskoðanir utan R3 er stöðvuð.

Hægt er að stofna eftirfarandi sjálfgefnar reglur pöntunarstillingar.

| Vægi | Svæði | Grunnstilling | Stíll | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Já                                  |                    | Já                | Já                               | Já             |
| 20   |      |               | R1    | Já                                  |                    | Já                | Já                               | Já             |
| 10   |      | C1            |       | Já                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Reglurnar tvær til að stöðva gömlu endurskoðanirnar hafa sama vægi, sem þýðir að þær eru jafn mikilvægar. Báðar hafa hærra vægi en reglnar fyrir forstillingu C1, sem þýðir að þær hafa forgang yfir reglu fyrir skilgreiningu C1. 

Þetta dæmi útskýrir þörf fyrir vægi. Ef innkaupapöntun er búin til fyrir skilgreiningu C1 og endurskoðun R2, þá yrðu reglurnar tvær sem skilgreindar eru fyrir R2 og C1 tvíræðrar, ef vægi vantar. Til að leysa úr tvíræðni, leitar Finance and Operations í reglunum í lækkandi röð vægis og notar fyrstu viðeigandi regluna. Í Gildandi dæmi þegar innkaupalína er stofnuð fyrir skilgreiningu C1 og endurskoðun R2, fær notandinn viðvörunarskilaboð um að varan er í bið og að þetta sé vegna gildis endurskoðunar. Ef regla fyrir skilgreiningu væri með hærra vægi en reglan fyrir endurskoðunina, þá hefði tekist að stofna innkaupapöntunarlínu skilgreiningar C1 og endurskoðunar R2 og ekkert skilaboð 'vara í biðstöðu' myndi hafa birst fyrir notanda. 

Íhugið eftirfarandi reglur fyrir sjálfgefnar pöntunarstillingar.

| Vægi | Svæði | Grunnstilling | Stíll | Sjálfgefið svæði | Sjálfgefið vöruhús | Innkaup - Hnekkja sjálfgefinni geymsluvídd | Innkaupavöruhús |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Já                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Kerfið ber saman reglupörin tvisvar til að ákvarða svæði og vöruhús. Þegar innkaupapöntunarlína er stofnuð fyrir skilgreiningu C1, stíl R2, er svæði ákvarðað samkvæmt reglu með vægi 10. Síðan leitar kerfið að regla fyrir svæði 2 til að ákvarða vöruhúss. Regla 20 finnst og þar sem hún er með hærra vægi, verður vöruhúss á innkaupapöntunarlína 22, og ekki 21. 

Sem almenn viðmið, sértækar reglur og reglur fyrir víddir sem eru mikilvægari en aðrar víddir fá hærra vægi, á meðan almennari reglur fá lægra vægi. 

Regla með núll vægi er öryggisnet. Sé ekki svörun frá öðrum reglum, eru notaðar sjálfgefnar pöntunarstillingar úr núll reglunni. 

Þar sem númer vægis er svo mikilvægt, eru aðgerðir á aðgerðarúða **Sjálfgefnar pöntunarstillingar** til að færa reglu upp eða niður og að endurnúmera reglur, svo þær séu alltaf með gildisaukningu 10. 

Reglur sem eru stofnaðar fyrir útgefnar afurðir geta verið margar. Svo hægt sé að ná átta sig betur á hvað hver regla er að hnekkja og til hvers það þarf, mælum við með að nota **hnitanetsyfirlit** á **Sjálfgefnar pöntunarstillingar** síðuna. Hægt að virkja hnitanetsyfirlit með því að fara á **Valkostir** Aðgerðarrúðu &gt; **Valkostir síðu** &gt; **Breyta yfirliti** &gt; **hnitanetsyfirlit**. Fjöldi dálka í hnitanetinu gætu mjög umfangsmikill, sérstaklega fyrir flipa fyrir sölu og birgða. Til að takmarka fjölda dálka í hnitanetinu, er hægt að fela flokkar dálka eða birta með því að nota hnappana á **Sjálfgefnar pöntunarstillingar** &gt; **birting Dálka** valmynd.

### <a name="specific-order-settings-for-released-product-variant"></a>Tilteknar pöntunarstillingar fyrir útgefin afurðarafbrigði

Ef reglukerfið fyrir sjálfgefnar pöntunarstillingar er of óþjált, þá er kostur á að skilgreina einfaldlega sjálfgefnar pöntunarstillingar fyrir hvert afurðarafbrigði. Eftirfarandi dæmi sýnir hvernig þetta mun líta út fyrir afurðina og tilvikum sem lýst er hér fyrir ofan.

| Vægi | Svæði | Grunnstilling | Stíll | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Já                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Já                                  | 5                  | Já                | Já                               | Já             |
| 10   |      | C2            | R1    | Já                                  | 5                  | Já                | Já                               | Já             |
| 10   |      | C1            | R3    | Já                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Já                                  | 2                  | Já                | Já                               | Já             |
| 10   |      | C1            | R1    | Já                                  | 2                  | Já                | Já                               | Já             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Vægi í þessu tilfelli er ekki mikilvægt í raun, þannig að hægt er að velja að fela það. Þessa lausn leiðir mögulega til vandamáls varðandi viðhalds. Hins vegar er gott að viltu íhuga að nota uppsetningu þú ert að íhuga að samþætta við Product Lifecycle Management (PLM)-kerfi.



