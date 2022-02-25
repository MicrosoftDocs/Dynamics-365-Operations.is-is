---
title: Sjálfgefnar pöntunarstillingar fyrir víddir og afurðarafbrigði
description: Sjálfgefið pöntunarstillingar skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað.
author: johanhoffmann
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: dca0aba081321dff5ae061ebe4bddcae0e42bc54
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102764"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Sjálfgefnar pöntunarstillingar fyrir víddir og afurðarafbrigði

[!include [banner](../includes/banner.md)]

Sjálfgefið pöntunarstillingar í Dynamics 365 Supply Chain Management skilgreina svæði og vöruhús þar sem afurðir verða upprunnin frá eða geymdar, í lágmarks, hámarks, margar og staðlaðs magns sem verða notuð fyrir viðskipti eða birgðastjórnun, afhendingartíma, stöðvunarflagg, og aðferðina pöntun lofað. Sjálfgefnar pöntunarstillingar eru notaðar þegar innkaupapantanir, sölupantanir, flutningspantanir, birgðabókum eru stofnaðar, og við aðaláætlanagerð til að mynda áætluð pöntun. Sjálfgefnar pöntunarstillingar geta verið tengdar ákveðnum vörum, svæðum, afurðarafbrigðum, eða afurðarvíddum.

Til að skilgreina sjálfgefnar pöntunarstillingar fyrir afurð skal fylgja þessum skrefum.

1. Farðu í **Afurðaupplýsingastjórnun** &gt; **Afurðir** &gt; **Losaðar afurðir**.
1. Veljið viðeigandi afurð í hnitanetinu.
1. Í aðgerðasvæðinu skal fylgja einu af þessum skrefum til að opna síðuna **Sjálfgefnar pöntunarstillingar** fyrir valda afurð:

    - Í flipanum **Áætlun**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**.
    - Í flipanum **Stjórna birgðum**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**.

1. Skilgreinið stillingarnar eins og lýst er í þessu efnisatriði.

## <a name="default-order-settings"></a>Sjálfgefnar pöntunarstillingar

Það eru þrjár gerðir af sjálfgefnum pantanastillingum fyrir innkaup, sölu og birgðir. Sjálfgefnar pantanastillingar fyrir innkaup eru notaðar þegar stofnaðar eru:

- Innkaupapöntunarlínur
- Innkaupasamningslínur
- Línur í beiðni um tilboð
- Innkaupabeiðnilínur
- Áfyllingarlínur vörusendingar (að hluta til stutt, sjá athugasemd)
- Innkaupatillögur

> [!NOTE]
> Fyrir áfyllingarpöntunarlínur vörusendingar eru aðeins stillingar úr **Innkaupapöntun** flýtiflipa **Sjálfgefnar pöntunarstillingar** sem gilda **Sjálfgefið svæði** reitur, **Sjálfgefið vöruhús** svæði, og **Stöðva** gátreitur.

Sjálfgefnar pantanastillingar fyrir sölu eru notaðar þegar stofnaðar eru:

- Sölupöntunarlínur
- Sölusamningslínur
- Sölutilboðslínur
- Skilapantanalínur og skiptilínur vöru.
- Eftirspurnarspárlínur

Sjálfgefnar sölupantanastillingar eiga einnig við þegar stofnaðar eru:

- Vöruþarfir verks
- Þjónustupöntun vöruþarfar

Sjálfgefnar pantanastillingar fyrir birgðir eru notaðar þegar stofnaðar eru:

- Birgðabækur
- Flutningspantanir
- Flutningstillögur

Sjálfgefnar birgðapantanastillingar eiga einnig við þegar stofnaðar eru:

- Biðgeymslupantanir
- Gæðapantanir
- Framleiðslupantanir
- Uppskriftarlínur
- Framleiðslutillögur

## <a name="full-definition-of-a-released-product"></a>Full skilgreining á útgefin afurð

Þegar færsla er búin til þarf að tilgreina fulla skilgreiningu á útgefinni afurð í línunni, þannig að Supply Chain Management geti reynt að bera kennsl á sjálfgefnar pöntunarstillingar. Í fullu skilgreiningunni fyrir útgefna afurð er vörunúmerið og allar virku afurðarvíddirnar, eins og skilgreining, stærð, stíll, útgáfa og litur, tilgreint í færslunni. Til dæmis, ef innkaupapöntunarlínu fyrir útgefin afurðarafbrigði eru stofnaðar handvirkt þarf að tilgreina allt nauðsynlegt afurðarvíddum áður en svæði, vöruhúsi, magn og afhendingartíma birtist sjálfkrafa í pöntunarlínu. 

Ekki allar sjálfgefnar færibreytur pöntunarstillinga eru notaðar stofnaðar eru pöntunar- eða færslubókarlínur. Magn og afhendingartími birtast aðeins sjálfgefið þegar við á. Til dæmis, þegar verið er að telja færslubókarlínu, birtist aðeins svæðið og vöruhús sjálfkrafa þegar línan er stofnuð. Þess vegna er ekkert sjálfgefið magn eða gerðar athuganir á margs konar magni eða lágmarksmagni þegar lína er búin til eða færslubók bókuð. 

Kerfið reynir alltaf að finna sjálfgefið svæði og vöruhús þegar pöntunina eða færslubókarlínan er stofnuð. Svæðinu er ekki alltaf birt sjálfgefið úr pöntunarstillingum. T.d. þegar sölupöntun eða innkaupapöntun eru stofnaðar, er svæðið úr haus sjálfkrafa notað í pöntunarlínum. Þegar uppskriftarlína er stofnuð, er svæði úr haus Uppskriftar notaður. Þegar svæðið er ákvarðað, verður það notað til að finna hvers kyns pöntunarstillingar sem tengjast tilteknu svæði sem má þá nota sem sjálfgefið fyrir vöruhúsið. 

Sjálfgefin pöntunargerð, innkaup og afhendingartíma í birgðir má hnekkja með þekjureglur vörunnar á **Vöruþekja** síðu. Þó svo sjálfgefnar pantanastillingar gefa ekki kost á því að greina á milli afhendingartíma framleiðslu og flutnings, þá leyfa þekjureglur vörunnar það. Hins vegar, uppsetning vöruþekju verður aðeins notað af aðaláætlanagerð (MRP) þegar stofnaðar eru framleiðslutillögur og flutningstillögur og á ekki við þegar framleiðslu- og flutningspantanir eru stofnaðar handvirkt. 

## <a name="default-order-settings-rules"></a>Reglur fyrir sjálfgefnar pöntunarstillingar

Hægt er að skilgreina almennar sjálfgefnar pantanastillingar og fjölda reglna fyrir sjálfgefna pöntunarstillingar sem eiga aðeins við sérstakar aðstæður, til dæmis svæði eða ákveðna afurðarvídd eða samsetningu afurðarvídda. Ekki er hægt að skilgreina pöntunarstillingar fyrir tiltekið vöruhús.

### <a name="rank-in-default-order-settings"></a>Forgangsröðun fyrir sjálfgefnar pöntunarstillingar

Sjálfgefnu pöntunarstillingar hafa forgangsröðun. Því hærra vægi í forgangsröðun, því mikilvægari er reglan, sem þýðir það mun hafa hærri forgang og notaðar á undan öðrum reglum með lægra vægi. Almenn sjálfgefnar pantanastillingar hafa vægi núll, sem ekki er hægt að breyta. Aðeins getur verið ein færsla með vægið núll. Reglur geta haft sama vægi, svo lengi sem víddirnar sem þær eiga við eru mismunandi. Þetta er gagnlegt til að sníða pöntunarstillingar fyrir tiltekin svæði. Þegar ný sjálfgefin pöntunarstillingum er stofnuð erfast gildi fyrir gildi pantana, stöðvunarflagga, o. s. frv. úr reglu með vægi núll, en geta ekki verið hnekkt.

### <a name="default-order-settings-for-released-products"></a>Sjálfgefnar pöntunarstillingar fyrir útgefnar afurðir

Fyrir einkvæmar útgefnar afurðir er hægt að skilgreina almennar pöntunarstillingar eða pöntunarstillingar fyrir tiltekin svæði. Almenn pöntunarstillingar hafa alltaf vægi núll. Ef sett er upp nýjar pöntunarstillingar fyrir sala, innkaup og birgðir á sama tíma, er mælt með því að nota **Upplýsingayfirlit** á síðunni **Sjálfgefnar pöntunarstillingar**. Til að skipta yfir í upplýsingayfirlitið skal fara í **Valkostir** &gt; **Valkostir síðu** &gt; **Breyta yfirliti** &gt; **Upplýsingayfirlit**.

### <a name="site-specific-order-settings"></a>Pöntunarstillingar tengdar svæði

Til að búa til pöntunarstillingar fyrir tiltekið svæði skal velja **Nýjar**. Í **Upplýsingayfirlit** skal fara í svæðið í reitnum **Svæði** í hlutanum **Stillingar eiga við um**. Í **Yfirlit hnitanets** skal fara í svæðið í dálknum **Svæði**. Nýju reglunni er sjálfkrafa úthlutað nýju vægi sem er hærra en 0 (núll). Hægt er að búa til eins margar svæðismiðaðar reglur og þörf er á. Til að gefa til kynna að þeir séu jafn mikilvægar er hægt að úthluta sama vægi á allar svæðismiðaðar reglur.

Ef þú ert í **Upplýsingayfirlit**, er ekki hægt að fá yfirlit yfir reglur sem eru stofnaðar fyrir vöruna. Nota skal hnappinn **Sýna/fela lista** til að sjá yfirlit upplýsinga. Þegar pöntunarlína af einhverri gerð er stofnuð og hún er ekki með neitt svæði úthlutað, leitar Supply Chain Management að reglu sem ekki hefur tilgreint svæði. Þetta auðveldar að ákvarða sjálfgefið svæði í pöntunarlínunni. Þetta svæði er síðan notað til að leita að reglu fyrir tiltekið svæði, þar sem sjálfgefið vöruhús hefur hugsanlega verið stillt. Vöruhús er notaður í pöntunarlínuna.

### <a name="specific-order-settings-for-product-dimension"></a>Tilteknar Pöntunarstillingar fyrir afurðarvídd

Hægt er að tilgreina sjálfgefnar pantanastillingar sem eiga við allar virkar afurðarvídd eða alla virka samsetningu afurðavídda. Sé reitur afurðarvíddar er tómur, gildir sú regla um öll gildi afurðarvíddarinnar. 

Íhugið eftirfarandi dæmi um vöru:

| vara                                                | Virði                                   |
|-----------------------------------------------------|-----------------------------------------|
| **Afurðarnafn**                                    | Ljósnemi                    |
| **Vörunúmer**                                     | XW56                                    |
| **Skilgreining** (notað til að sníða til gerð ljóss) | C1 Sýnilegt rautt ljós, C2 innrautt ljós |
| **Útgáfa** | V1, V2, V3                              |

Í þessu dæmi, gerum ráð fyrir að afurðar er keypt og ekki framleidd. Gerið einnig ráð fyrir að skilgreiningu C1 er oftar notuð, svo hún hefur styttri afhendingartíma. 

Stofna eftirfarandi sjálfgefnar pantanastillingar til að sníða til líkanið í þessum aðstæðum.

| Vægi | Svæði | Grunnstilling | Útgáfa | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Já                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Þegar innkaupapöntunarlínu eða innkaupatillaga er stofnuð fyrir vöru XW56, skilgreiningu C1, óháð útgáfu eða svæði þar sem línan er sett, mun afhendingartími teljast vera 2. Gera ráð fyrir að allar útgáfur utan V3 séu hættar.

Hægt er að stofna eftirfarandi sjálfgefnar reglur pöntunarstillingar.

| Vægi | Svæði | Grunnstilling | Útgáfa | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Já                                  |                    | Já                | Já                               | Já             |
| 20   |      |               | V1    | Já                                  |                    | Já                | Já                               | Já             |
| 10   |      | C1            |       | Já                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Reglurnar tvær til að stöðva gömlu útgáfurnar hafa sama vægi. Þess vegna eru þær jafn mikilvægar. Úr því að báðar þessar reglur eru með meira vægi en regla skilgreiningar C1, hafa þær forgang yfir reglu fyrir skilgreiningu C1. 

Þetta dæmi útskýrir þörf fyrir vægi. Ef vægið er ekki notað þegar innkaupapöntun er stofnuð fyrir skilgreiningu C1 og útgáfu V2, eru reglurnar tvær sem skilgreindar eru fyrir V2 og C1 tvíræðar. Til að leysa úr tvíræðni, leitar Supply Chain Management í reglunum í lækkandi röð vægis og notar fyrstu viðeigandi regluna. Í núverandi dæmi, þegar innkaupapöntunarlína er stofnuð fyrir skilgreiningu C1 og útgáfu V2, fær notandinn viðvörunarboð um að varan sé í bið og að það sé vegna útgáfugildsins. Ef reglan fyrir skilgreininguna hefði meira vægi en reglan fyrir útgáfuna, væri innkaupapöntunarlína stofnuð fyrir skilgreiningu C1 og útgáfu V2 og notandinn fengi ekki skilaboðin „vara í bið“. 

Íhugið eftirfarandi reglur fyrir sjálfgefnar pöntunarstillingar.

| Vægi | Svæði | Grunnstilling | Útgáfa | Sjálfgefið svæði | Sjálfgefið vöruhús | Innkaup - Hnekkja sjálfgefinni geymsluvídd | Innkaupavöruhús |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Já                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Kerfið ber saman reglupörin tvisvar til að ákvarða svæði og vöruhús. Þegar innkaupapöntunarlína er stofnuð fyrir skilgreiningu C1, útgáfu V2, er svæðið ákvarðað samkvæmt reglu með vægi 10. Kerfið leitar þá að reglu fyrir svæði 2 til að ákvarða vöruhús. Regla 20 finnst og þar sem hún er með hærra vægi, verður vöruhúss á innkaupapöntunarlína 22, og ekki 21.

Sem almenn viðmið, sértækar reglur og reglur fyrir víddir sem eru mikilvægari en aðrar víddir fá hærra vægi, á meðan almennari reglur fá lægra vægi. 

Regla með núll vægi er öryggisnet. Sé ekki svörun frá öðrum reglum, eru notaðar sjálfgefnar pöntunarstillingar úr núll reglunni. 

Þar sem númer vægis er svo mikilvægt, eru aðgerðir á aðgerðarúða **Sjálfgefnar pöntunarstillingar** til að færa reglu upp eða niður og að endurnúmera reglur, svo þær séu alltaf með gildisaukningu 10. 

Reglur sem eru stofnaðar fyrir útgefnar afurðir geta verið margar. Til að öðlast betri skilning á því hvað hver regla er að hnekkja og af hverju það er nauðsynlegt, mælum við með að nota **Töfluyfirlit** á síðunni **Sjálfgefnar pöntunarstillingar**. Hægt að virkja töfluyfirlitið með því að fara í **Valkostir** &gt; **Valkostir síðu** &gt; **Breyta yfirliti** &gt; **Töfluyfirlit**. Fjöldi dálka í hnitanetinu gætu mjög umfangsmikill, sérstaklega fyrir flipa fyrir sölu og birgða. Til að takmarka fjölda dálka í hnitanetinu, er hægt að fela flokkar dálka eða birta með því að nota hnappana á **Sjálfgefnar pöntunarstillingar** &gt; **birting Dálka** valmynd.

### <a name="specific-order-settings-for-released-product-variant"></a>Tilteknar pöntunarstillingar fyrir útgefin afurðarafbrigði

Ef reglukerfið fyrir sjálfgefnar pöntunarstillingar er of óþjált, þá er hægt að velja um að skilgreina sjálfgefnar pöntunarstillingar fyrir hvert afurðarafbrigði. Eftirfarandi dæmi sýnir hvernig þetta mun líta út fyrir afurðina og tilvikum sem lýst er hér fyrir ofan.

| Vægi | Svæði | Grunnstilling | Útgáfa | Innkaup - Hnekkja sjálfgefnum stillingum | Afhendingartími innkaupa | Innkaup - stöðvuð | Sala - Hnekkja sjálfgefnum stillingum | Sölur - Stöðvað |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Já                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Já                                  | 5                  | Já                | Já                               | Já             |
| 10   |      | C2            | V1    | Já                                  | 5                  | Já                | Já                               | Já             |
| 10   |      | C1            | V3    | Já                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Já                                  | 2                  | Já                | Já                               | Já             |
| 10   |      | C1            | V1    | Já                                  | 2                  | Já                | Já                               | Já             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Vægi í þessu tilfelli er ekki mikilvægt í raun, þannig að hægt er að velja að fela það. Þessa lausn leiðir mögulega til vandamáls varðandi viðhalds. Hins vegar er gott að viltu íhuga að nota uppsetningu þú ert að íhuga að samþætta við Product Lifecycle Management (PLM)-kerfi.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Nota ítarlega eða staðlaða staðfestingu á sjálfgefnu pöntunarmagni

Hægt er að velja hversu ítarlegt kerfið á að vera þegar það staðfestir magn sem fært er inn í **Sjálfgefnar pöntunarstillingar** fyrir afurð. Þegar þessi nýi ítarlegi valkostur er notaður, verður **Staðlað magn í pöntun** alltaf að vera margfeldi af tiltekna gildinu **Margfeldi** fyrir innkaupapantanir, birgðir og sölupantanir. Ef ítarleg staðfesting er notuð, verður ekki hægt að vista sjálfgefnar pöntunarstillingar sem uppfylla ekki þessa kröfu (og villa birtist í skilaboðastikunni). 

Ítarleg staðfesting nær yfir gildi **Staðlaðs magn í pöntun** sem tiltekið er í flýtiflipunum **Innkaupapöntun**, **Birgðir** og **Sölupöntun** á síðunni **Sjálfgefnar pöntunarstillingar**. Hver flýtiflipi er með eigin stillingu á **Margfeldi**, sem er notað til að staðfesta gildið **Staðlað magn í pöntun** sem tiltgreint er fyrir þann flýtiflipa.

### <a name="turn-the-strict-validation-option-on-or-off"></a>Kveiktu eða slökktu á stranga staðfestingarvalkostinum

Til að nota stranga staðfestingu, *Strangt löggilding á sjálfgefnu pöntunarmagni* kveikt verður á eiginleikanum fyrir kerfið þitt. Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geturðu kveikt eða slökkt á þessari virkni með því að fara á [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og að leita að *Strangt löggilding á sjálfgefnu pöntunarmagni* eiginleiki.

### <a name="set-the-validation-option"></a>Stilla valkost staðfestingar

Til að stilla staðfestingarvalkostinn:

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Færibreytur afurðaupplýsingastjórnunar**.
1. Í flipanum **Almennt** skal stilla **Staðfesting á sjálfgefnu pöntunarmagni** á eitt af eftirfarandi gildum:
    - **Ítarlegt** - Veljið þennan valkost til að tryggja að öll gildin fyrir **Staðlað magn í pöntun** verði margfeldi af gildinu **Margfeldi** fyrir hvern flýtiflipa (**Innkaupapöntun**, **Birgðir** og **Sölupöntun**).
    - **Staðlað** - Veljið þennan valkost til að nota staðlaða staðfestingu (sem virkar á sama hátt og þegar þessi eiginleiki er ekki virkur).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]