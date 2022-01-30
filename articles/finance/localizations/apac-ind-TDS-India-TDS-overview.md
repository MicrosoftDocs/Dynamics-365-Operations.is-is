---
title: Yfirlit yfir frádreginn skatt á upprunastað (TDS) fyrir Indland
description: Þetta efnisatriði veitir ítarlegar upplýsingar um frádreginn skatt á upprunastað (TDS) fyrir Indland. TDS-fylgiskjölin ná yfir virknina í þessum möguleika.
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d33faaff8be4821005b8772875eb91f0afe26cb0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983904"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Yfirlit yfir frádreginn skatt á upprunastað (TDS) fyrir Indland

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir ítarlegar upplýsingar um frádreginn skatt á upprunastað (TDS) fyrir Indland.

TDS-fylgiskjölin ná yfir virknina í þessum möguleika. Það útskýrir einnig hvernig á að gera grunnuppsetningu fyrir TDS, reikna út TDS í færslum, ljúka uppgjörsferli TDS, skrá vottorðanúmer TDS og mynda TDS-fyrirspurnir, TDS-uppgjör og TDS-vottorð. Fylgiskjölin innihalda eftirfarandi efnisatriði:

- [Grunnuppsetning TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Virkni formúluhönnuðar og vikmarka fyrir TDS-útreikning](apac-ind-TDS-Formula-designer.md)
- [Útreikningur TDS á reikningum, greiðslum, eigin víxlum og færslum milli fyrirtækja](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Reglubundið TDS-uppgjörsferli og uppgjör TDS-upphæða til TDS-lánardrottnayfirvalda](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [Skráning og uppfærsla á númerum og dagsetningum TDS-vottorða](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Kynning á TDS

Samkvæmt lögum um tekjuskatt, 1961, er tekjuskattur dreginn frá uppruna af viðtakanda þjónustunnar þegar fyrirframgreiðsla er innt af hendi eða við bókhaldsvinnu kreditfærslu, hvort sem kemur á undan. Sá sem greiðir þarf að draga skattupphæðina frá og greiða þjónustuaðilanum aðeins nettóstöðu vegna þjónustunnar. TDS er notað í þjónustum sem yfirvöld tilgreina og skatturinn er dreginn frá með því að nota taxtana sem yfirvöld gefa upp fyrir tímabil. Frádráttarhlutfallið byggir á stöðu þess sem tekur við greiðslunni eða veitir þjónustuna. Stöður eru **Einstaklingur**, **Óskipt hindúafjölskylda** (**HUF**), **Fyrirtæki**, **Firma**, **Samtök einstaklinga** (**AOP**), **Hópur einstaklinga** (**BOI**) og **Staðaryfirvöld**.

Eftirfarandi hlutar telja upp þá þjónustu sem TDS er notað fyrir eins og tilgreint af yfirvöldum á Indlandi.

**Íbúar**

- Tekjur af launum (skv. lið 192)
- Tekjur af vöxtum verðbréfa (skv. lið 193)
- Tekjur af arði (skv. lið 194)
- Tekjur af vöxtum (skv. lið 194A)
- Tekjur af happdrætti (skv. lið 194B)
- Að vinna úr kappreiðum o.fl. (undir kafla 194BB)
- Verktakar og undirverktakar (skv. lið 194C)
- Tryggingarþóknun (skv. lið 194D)
- Tekjur af innborgun vegna séreignasparnaðar (skv. lið 194EE)
- Tekjur af verðbréfasjóði eða UTI (skv. lið 194F)
- Þóknun, umbun, verðlaun o.s.frv. af sölu eða happdrætti (skv. lið 194G)
- Greiðsla þóknunar eða miðlunar (skv. lið 194H)
- Leiga (skv. lið 194I)
- Fagleg þjónusta (skv. lið 194J)
- Tekjur af einingum (skv. lið 194K)
- Greiðsla þóknunar við kaup á tiltekinni fasteign (skv. lið 194LA)

**Ekki ríkisborgari**

- Greiðslur til erlends íþróttafólks eða erlends íþróttasambands (skv. lið 194E)
- Aðrar fjárhæðir (skv. lið 195)
- Tekjur vegna eininga erlendra aðila (skv. lið 196A)

    - Tekjur af skuldabréfum eða hlutabréfum í erlendum gjaldmiðli í indversku fyrirtæki (skv. lið 196C)
    - Tekjur erlendra fagfjárfesta af verðbréfum (skv. lið 196D)
    - Laun og allar aðrar jákvæðar tekjur undir hvaða tekjuhóp sem er (liður 192)
    - Vextir af verðbréfum (liður 193)
    - Vextir aðrir en vextir af verðbréfum (liður 194A)
    - Greiðslur til verktaka og undirverktaka (liður 194C)
    - Vinningar úr happdrætti eða krossgátum (liður 194B)
    - Vinningar úr kappreiðum (kafli 194BB)
    - Tryggingaþóknun sem nær yfir allar greiðslur fyrir öflun tryggingastarfsemi (liður 194D)
    - Allir aðrir vextir en vextir af verðbréfum sem greiðast til erlendra aðila sem ekki eru fyrirtæki eða til erlends fyrirtækis (liður 195)
    - Greiðsla til erlends íþróttamanns, þ.m.t. íþróttasambands eða stofnunar. Ef um erlendan íþróttamann er að ræða, greiðslur í sambandi við auglýsingar ásamt greinum um leiki/íþróttir á Indlandi í fréttablöðum, tímaritum o.þ.h. er innifalið (liður 194E)
    - Greiðsla vegna innstæðna samkvæmt NSS \[National Saving Scheme\] (liður 194EE)
    - Greiðsla vegna endurkaupa á einingum með verðbréfasjóði eða UTI (liður 194F)
    - Greiðsla fyrir þóknun eða miðlun (liður 194H)
    - Greiðsla leigu (liður 194I)
    - Greiðsla þóknana vegna faglegrar eða tæknilegrar þjónustu (liður 194J)
    - Þóknun til kaupmanna, dreifingaraðila, kaupenda og seljenda happdrættismiða, þ.m.t. endurgjald eða verðlaun fyrir slíka miða (liður 194G)
    - Tekjur af einingum sem keyptar eru í erlendum gjaldmiðli eða langtíma verðmætisaukning sem stafar af flutningi slíkra eininga sem keyptar eru í erlendum gjaldmiðli (liður 196B)
    - Greiðsla allra tekna til erlendra aðila vegna vaxta eða arðs af skuldabréfum og hlutabréfum (liður 196C)

TDS er reiknað vegna kaupa, sölu, söluskila, kreditnóta, eignakaupa, fyrirframgreiðslna, eigin víxla, vinnuskatts og færslna milli fyrirtækja.

> [!NOTE]
> Í núverandi skattaumhverfi Indlands er TDS ekki reiknað fyrir sölufærslur. Kerfið inniheldur hins vegar ákvæði um að reikna út TDS sem er endurheimtanlegt í sölufærslum, þá sérstaklega fyrir færslur milli fyrirtækja.

Útreikningur á TDS tekur alltaf mið af mörkum og undantekningarmörkum sem eru skilgreind fyrir TDS-hlutann.

Reglubundið uppgjörsferli TDS þarf að keyra og TDS-greiðslur þarf að gera upp hjá TDS-lánardrottnayfirvöldum.

Hægt er að skrá og uppfæra númer og dagsetningar vottorða fyrir TDS-vottorð sem eru móttekin frá lánardrottnum eða viðskiptavinum. Auk þess er hægt að mynda eyðublað 26Q og 27Q vegna ársfjórðungslegs uppgjörs og eyðublað 16A vegna vottorðs fyrir TDS í Finance.

## <a name="setting-up-and-working-with-tds"></a>Setja upp og vinna með TDS

Hér er yfirlit yfir ferlið við að setja upp og að vinna með TDS:

1. **TDS uppsetning:**

    - Uppsetning á færibreytum

        - Í færibreytum fjárhags skal virkja færibreytur sem tengjast TDS.
        - Í færibreytum fjárhags skal setja upp númeraraðir fyrir greiðslur staðgreiðsluskatts.
        - Setjið upp færibreytur í viðskiptaskuldum og viðskiptakröfum.

    - Grunnuppsetning:

        - Setjið upp TDS-skráningarnúmer fyrir fyrirtæki, viðskiptavini og lánardrottna.
        - Setjið upp flokka TDS-hluta.
        - Setjið upp TDS-hluta, hengið flokka TDS-hluta við þá og skilgreinið mörkin og undantekningarmörkin fyrir þá.
        - Setjið upp TDS-yfirvöld.
        - Setjið upp TDS-uppgjörstímabil.
        - Setjið upp skattkóða TDS og hengið TDS-hluta við þá.
        - Setjið upp skattflokka TDS og hengið skattkóða TDS við þá.
        - Í formúluhönnuðinum skal skilgreina formúlu til að reikna út TDS fyrir TDS-flokk.
        - Skráið vottorðanúmer TDS-skattaívilnunar.

    - Uppsetning fjárhagslykla og fyrirtækis:

        - Setjið upp fjárhagslykla viðskiptaskulda og viðskiptakrafa TDS.
        - Setjið upp lykilnúmer skattafrádrátts og skattinnheimtu (TAN) og flokk frádráttargerðar fyrir fyrirtækið.

    - Önnur uppsetning:

        - Setjið upp greiðsluáætlun sem inniheldur TDS-úthlutun.
        - Setjið upp gerð greiðsluþóknunar fyrir greiðslur til TDS-yfirvalda.
        - Setjið upp upplýsingar um TDS-flokka, varanleg lykilnúmer (PAN) og TAN fyrir lánardrottna og viðskiptavini.

2. **Útreikningur TDS í færslum:**

    - Reikningar og greiðslur
    - Eigin víxlar
    - Fyrirframgreiðslur
    - Fyrirframgreiðslur

3. **TDS-uppgjör:**

    - Reglubundið uppgjörsferli TDS
    - Uppgjör á TDS-greiðslum til lánardrottnayfirvalda TDS og myndun TDS-greiðslukvittunar

4. **Fyrirspurnir, uppgjör og vottorð vegna TDS:**

    - Skráið og uppfærið númer og dagsetningar TDS-vottorða.
    - Búið til TDS-fyrirspurn og bókið TDS-fyrirspurn.
    - Búið til TDS-eyðublað 27A, 26Q og 27Q og rafræn ársfjórðungsleg uppgjör TDS.
    - Búið til eyðublað 16A vegna TDS-vottorðs.
