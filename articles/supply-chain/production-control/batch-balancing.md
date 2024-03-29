---
title: Röðun virkra efna í uppskrift
description: Í þessari grein er runujöfnunarferlinu lýst.
author: johanhoffmann
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 939066fbf4ab7b316283d406c321f1a7936c187f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066547"
---
# <a name="batch-balancing"></a>Röðun virkra efna í uppskrift

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig röðunarferli virkra efna í uppskrift er studd.

Fyrir frekari upplýsingar skaltu horfa á [myndband um jöfnun virkra efna í uppskrift](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Í röðunarferli virkra efna í uppskrift er magn innihaldsefna sem nota á í framleiðslurunu reiknað út frá styrk virkra efna í völdum afurðarunum.

## <a name="products-that-have-an-active-ingredient"></a>Afurðir sem eru með virkt efni

Afurð er hægt að skilgreina út frá styrkleika virka efnisins í henni. Virkt efni afurðar er mótað með því að nota afurðartengda runueigind sem hefur lágmarksgildi, hámarksgildi og markgildi.

Markgildi runueigindar sýnir áætlað hlutfall af virku efni í afurð. Lágmarks- og hámarksgildin sýna samþykkt frávik frá markgildinu. Til dæmis er hægt að nota þau sem samþykkt vikmörk fyrir runur við móttöku afurðar.

Afurð getur aðeins haft eitt virkt efni. Til að tilgreina virkt efni afurðar þarf fyrst að skilgreina afurðartengda runueigind. Þá er eigindin tengd við grunneigind afurðarinnar.

Á afurðastigi þarf einnig að tilgreina hvernig á að skrá magn virka efnisins fyrir runu af afurðinni: sem hluti af móttökuferli innkaupa eða sem hluti af gæðapöntunarferli.

Til að tengja grunneigind við afurð er krafist eftirfarandi uppsetningar:

- Afurðin verður að vera runustjórnað. Til að búa til runustjórnaða afurð þarf að úthluta afurðinni rakningarvíddarflokki sem er með virka runuvídd.

- Eigindin sem gefur til kynna magn innihaldsefna verður að vera skilgreind sem afurðartengd runueigind fyrir afurðina.

Til að fletta upp á og breyta raungildi virka innihaldsefnisins fyrir runu:
1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Rakningarvíddir \> Runur**.
1. Veljið rununúmer úr hnitanetinu.
1. Í aðgerðasvæði skal opna flipann **Skoða** og velja síðan **Runueigindir birgða**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Gerðir innihaldsefna og hvernig þær vinna saman í röðunarferli virkra efna í uppskrift

Formúlulína sem er stofnuð getur haft eina af þessum gerðum innihaldsefna:

- None
- Í gangi
- Uppbót
- Áfyllingaraðili

Það sem er eftir af þessum kafla eru gefin dæmi sem sýna hvernig hver gerð af innihaldsefni virkar. Dæmin eru byggð á eftirfarandi formúlu sem hefur heildarrunustærð upp á 100 lítra.

| Gerð innihaldsefnis | Vörunúmer | Magn formúlulínu | Eining |
|---|---|---|---|
| None | A | 20 | Lítri |
| Í gangi | V | 30 | Lítri |
| Uppbót | K | 10 | Lítri |
| Áfyllingaraðili | D | 40 | Lítri |

Eftirfarandi tafla sýnir yfirlit yfir niðurstöður hvers dæmis.

| Vörunúmer | Gerð innihaldsefnis | Áætlað magn | Jafnað magn | Virkt magn | Eining | Grunngildi |
|---|---|---|---|---|---|---|
| A | None | 20 | 20 | | Lítri | |
| V | Í gangi | 30 | 25,71 | 9,00 | Lítri | 30.00 |
| K | Uppbót | 10 | 14.72 | | Lítri | |
| D | Áfyllingaraðili | 40 | 39.57 | | Lítri | |

### <a name="active-ingredients"></a>Virk efni

Þegar afurð sem hefur grunneigind er bætt við formúlulína er það nefnt *virkt efni* formúlunnar. Runupantanir með formúlum sem innihalda virk efni geta verið notaðar í röðunarferli virkra efna í uppskrift. Fyrir hvert innihaldsefni í formúlunni áætlar röðunarferli virkra efna í uppskrift magnið sem þarf til að framleiða afurðina. Áætlaða magnið er byggt á styrk virkra efna í völdum runum.

#### <a name="active-ingredient-example"></a>Dæmi um virkt efni

Innihaldsefni B hefur grunneigind X og markgildi 30 og það er innifalið í formúlu sem þarfnast 30 lítra af innihaldsefni B fyrir hverja 100 lítra af afurðinni. Runupöntun er stofnuð sem hefur runustærð upp á 100 lítra. Runupöntunin er hafin og á meðan á röðunarferli virkra efna í uppskrift stendur velur notandinn runu af innihaldsefni B sem hefur styrkleikastig upp á 35. Vegna þess að styrkleikastigið upp á 35 er hærra en markgildið 30 er jafnaða magnið af innihaldsefni B minnkað með því að nota hlutfallið á milli styrkleikagildis og markgildis rununnar sem er margfaldað með áætluðu magni. Útreikningurinn á jafnaða magninu lítur svona út:

(30 ÷ 35) × 30 lítrar = 25,71

### <a name="none-ingredients"></a>Engin innihaldsefni

Þegar þú notar röðunarferli virkra efna í uppskrift þegar **Gerð innihaldsefnis** er *Ekkert* er áætlaða magnið og jafnaða magnið í formúlulínunni í runupöntuninni það sama.

#### <a name="none-ingredient-example"></a>Dæmi um ekkert innihaldsefni

Innihaldsefni A er úthlutað á innihaldsefni af gerðinni *Ekkert* og bætt við formúlu fyrir tilbúna afurð. Formúlan krefst 10 lítra af innihaldsefni A fyrir hverja 100 lítra af tilbúinni afurð. Þegar runupöntun krefst 200 lítra er bæði áætlað magn og jafnað magn innihaldsefnis A reiknað sem 20 lítrar.

### <a name="compensating-ingredients"></a>Jöfnunarefni

Uppbótarefni getur annað hvort dregið úr eða bætt áhrif virka efnisins í afurð. Þess vegna fer magn uppbótarefnis sem er notað eftir styrkleika afurðarinnar:

- **Andstæð áhrif** - Ef magn virka efnisins er meira en búist er við þarf að bæta við minna af uppbótarefninu.

- **Viðbótaráhrif** - Ef magn virka efnisins er minna en búist er við þarf að bæta við meira af uppbótarefninu.

Tengsl milli virks efnis og uppbótarefnis er sett upp á síðunni **Uppbótarregla**.

Fylgið eftirfarandi skrefum til að setja upp tengsl milli innihaldsefna.

1. Veljið **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.
1. Á formúlulínu, opnið formúlulínu og veljið síðan **Innihaldsefni** til að opna síðuna **Uppbótarregla**.
1. Veljið línuna sem táknar uppbótarreglu og veljið síðan virka efnið fyrir uppbót.

Í uppbótarreglunni er einnig færður inn jákvæður eða neikvæður uppbótarþáttur til að tilgreina hversu mikið á að bæta fyrir og hvort meginreglan eigi að vinna með eða á móti. Jákvæður þáttur gefur til kynna viðbótaráhrif og neikvæð þáttur gefur til kynna andstæð áhrif.

#### <a name="compensating-ingredient-example"></a>Dæmi um jöfnunarefni

Innihaldsefni B er virkt efni sem hefur grunneigind X og markgildi 30. Það er innifalið í formúlu sem krefst 30 lítra af innihaldsefni B fyrir hverja 100 lítra af afurðinni. Innihaldsefni C er uppbótarefni og magn upp á 10 er innifalið í sömu formúlunni. Uppbótarstuðullinn 1,10 er settur upp fyrir jöfnunarregluna. Því verður jöfnunarmagn uppbótarefnanna minnkað sem nemur mismuninum á milli jöfnunarmagns virka efnisins og áætlaða magnsins sem krafist er, margfaldað með 1,10.

Í dæminu fyrir *Virka* gerð innihaldsefnis var jafnað magn virka efnisins sem krafist er reiknað sem 25,71 og áætlaða magnið sem krafist er var reiknað sem 30. Í þessu tilviki verður jafnað magn uppbótarefnisins reiknað út sem hér segir:

1. Mismunurinn á áætluðu og jöfnuðu magni er ákvarðaður:  
    25,71 – 30 = -4,29

1. Niðurstaðan er margfölduð með uppbótarstuðlinum:  
    4,29 × 1,10 = -4,72

1. Áætlað uppbótarmagn er lækkað um -4,72 til að ákvarða jafnað uppbótarmagn:  
    10 – (-4,72) = 14,72

Vegna þess að 1,10 er jákvæður uppbótarstuðull, hefur þessi uppbótarregla viðbótaráhrif. Í þessu tilfelli er virka efnið með meiri styrkleika en búist var við. Því er nauðsynlegt að bæta við meiru af uppbótarefninu.

### <a name="filler-ingredients"></a>Fylliefni

*Fylliefnið* A er hlutlaust innihaldsefni sem er notað til að ná tilætluðu magni af tilbúinni afurð. Leiðréttingar á fylliefni eru reiknaðar út frá breytingum á virka efninu og uppbótarefninu miðað við staðlað magn.

#### <a name="filler-ingredient-example"></a>Dæmi um óvirkt efni

Þú hefur mótað afurð sem inniheldur innihaldsefni A, B, C og D fyrir formúlustærð upp á 100 lítra. Þú hefur reiknað út jafnað magn allra innihaldsefna, nema af gerðinni *Áfylling* sem er notuð í einni línu.
Jafnað magn fylliefnisins er reiknað sem mismunurinn á lotustærðinni 100 lítrar og summu innihaldsefna A, B og C:

100 – (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Röðunarferli virkra efna í uppskrift

Röðunarferli virkra efna í uppskrift er framkvæmt á síðunni **Röðun virkra efna í uppskrift**.
Veljið **Kostnaðarstjórnun \> Runupantanir** og þá á flipanum **Ferli** skal velja **Röðun virkra efna í uppskrift**. Röðun virkra efna í uppskrift er tiltæk fyrir runupantanir sem hafa stöðuna **Byrjað**.

Almennt er hægt að nota röðun virkra efna í uppskrift á runupantanir ef formúlan hefur a.m.k. eina formúlulínu þar sem **Gerð innihaldsefnis** er *Virk*. (Fyrir utantekningar á þessari reglu, sjáðu kaflann „Runupantanir sem ekki eiga við um runujöfnun“ seinna í þessari grein.)

Röðunarferli virkra efna í uppskrift er hægt að skipta niður í tvo undirferla:

1. Innihaldsefni jöfnunarrunu
1. Staðfesta og losa formúluna

### <a name="balance-batch-ingredients"></a>Innihaldsefni jöfnunarrunu

Í undirferli jöfnunarrunu fyrir innihaldsefni er útreikningur á magni innihaldsefna sem nota á í framleiðslurununni byggður á völdu rununum sem eru með virk efni. Að jafnaði er aðeins hægt að klára útreikninginn ef full þekja er á öllum innihaldsefnum. Þú getur ekki jafnað aðeins hluta af rununni sem runupöntunin sett upp til að framleiða.

> [!NOTE]
> Þú getur ekki vistað útreikning og síðan lokið röðunarferli virkra efna í uppskrift síðar. Ef þú lokar síðunni **Röðun virkra efna í uppskrift** þarf að endurtaka útreikninginn til að ljúka ferlinu.

### <a name="confirm-and-release-the-formula"></a>Staðfesta og losa formúluna

Eftir að magn innihaldsefnisins hefur verið reiknað, getur þú staðfest og losað formúluna. Losunarferlið er mismunandi eftir því hvort afurðirnar eru virkar fyrir vöruhúsakerfisferla (WMS):

- Ef afurð er virkjuð fyrir vöruhúsakerfi er formúlulínan losuð í vöruhúsið í samræmi við meginreglur vöruhúsakerfis. Formúlulínan er losuð í magni sem passar við jafnaða magnið og það er gefið út fyrir tilteknar runur sem eru valdir fyrir virku innihaldsefnin.

    > [!NOTE]
    > Aðeins er hægt að losa formúlulínur í vöruhús sem hluta af röðunarferli virkra efna í uppskrift. Þrátt fyrir að það séu aðrir möguleikar til að losa efni til framleiðslu í vöruhús, þá er ekki hægt að nota þessa valkosti fyrir formúlulínur.

- Ef afurð er ekki virk fyrir WMS er tiltektarlisti framleiðslu stofnaður fyrir afurðina þegar formúlan er staðfest og losuð.

Í stakri formúlu er hægt að sameina afurðir sem eru virkjaðar fyrir vöruhúsakerfisferla og afurðir sem ekki eru virkjaðar fyrir vöruhúsakerfisferlana. Þegar tvær gerðir afurða eru hluti af einni formúlu eru afurðirnar sem eru gerðar virkar fyrir WMS losaðar í vöruhús. Fyrir vörur sem eru ekki virkar fyrir WMS er búinn til vallisti þegar formúlan er staðfest og losuð.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Runupantanir sem ekki eiga við um röðun virkra efna í uppskrift

Það eru tvær undantekningar frá þeirri reglu að runupantanir eiga við fyrir röðun virkra efna í uppskrift ef formúlan hefur a.m.k. eina formúlulínu þar sem **Gerð innihaldsefnis** er *Virk*.

1. Ef formúla inniheldur virkt efni fyrir afurð sem er virkjuð fyrir vöruhúsakerfisferlana, en rununúmer er undir staðsetningu í frátekningarstigveldinu, á runupöntunin ekki við um röðun virkra efna í uppskrift.
1. Ef formúlumælieining er frábrugðin birgðamælieiningu virks innihaldsefnis, á tunupöntunin ekki við um röðun virkra efna í uppskrift.

Runupöntun sem á ekki við um röðun virkra efna í uppskrift fer í gegnum reglulega vinnuferilinn fyrir runupantanir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]