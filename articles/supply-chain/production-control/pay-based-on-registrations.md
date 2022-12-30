---
title: Laun byggð á skráningum
description: Þessi grein útskýrir hvernig laun eru reiknuð út frá starfsmannaskráningum.
author: johanhoffmann
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 729e2f6c7c2dac598154b342244ab3d8eccaf4d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844381"
---
# <a name="pay-based-on-registrations"></a>Laun byggð á skráningum

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir ítarlega hvernig laun eru reiknuð út frá starfsmannaskráningum. Það felur í sér dæmi sem sýna hvernig hinar ýmsu samsetningar á möguleikum uppsetningar sem eru tiltækar fyrir útreikninginn hafa áhrif á niðurstöðuna. Hér eru nokkur af þeim sviðum sem verður farið yfir:

- Sveigjanlegur tími
- Yfirvinna
- Hlé
- Skiptikóðar
- Launaliðir
- Launasamningar
- Færibreytuútreikningar tíma og viðveru
- Fjarvist

## <a name="the-use-of-flex-time"></a>Notkun sveigjanlegs tíma

Tímabil sveigjanlegs tíma eru sett upp í tímaforstillingum sem notaðar eru í Tími og viðvera. Það eru til tvær sveigjanlegar forstillingargerðir: **Sveigjanlegur+** og **Sveigjanlegur-**. Þegar starfsmaður skráir tíma á tímabilinu Sveigjanlegur+, er staða sveigjanlegs tíma starfsmanns aukin um klukkustundirnar sem var unnið. Starfsmaður fær enga uppbót fyrir klukkustundirnar sem unnið var á tímabilinu Sveigjanlegur+. Hins vegar getur starfsmaður tekið frí á meðan á tímabilinu Sveigjanlegur- stendur og fengið það bætt með klukkustundunum sem eru á sveigjanleikastöðu hans. Þess vegna lítur kerfið á frítíma á sveigjanlegum tímabilum sem fjarvist.

## <a name="scenarios-based-on-flex-periods"></a>Tilfelli byggð á sveigjanlegum tímabilum

Tilfellin tvö sem fylgja eru byggð á sveigjanlegri forstillingu sem táknar vinnudag. Í báðum tilfellum eru laun reiknuð samkvæmt sveigjanlega tímabilinu þar sem starfsmaður stimplar sig inn og út.

### <a name="flex-profile-for-one-workday"></a>Sveigjanleg forstilling fyrir einn vinnudag

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Tilfelli 1: Starfsmaður stimplar sig inn á Sveiganlegt+ tímabilinu og stimplar sig út á Sveigjanlegt- tímabilinu.

Skráning starfsmannsins fyrir daginn lítur svona út.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 06:30 | 06:30 |
| Framleiðsluverk            | 06:30 | 14:45 |
| Stimpla út                 | 14:45 | 14:45 |

Skráningar starfsmannsins fyrir daginn eru reiknaðar og færðar til greiðslu á síðunni **Samþykkja** (**Tími og viðvera** &gt; **Yfirfara og samþykkja** &gt; **Samþykkja**). Eftir að skráningar hafi verið reiknaðar út er hægt að skoða niðurstöðu útreiknings á flipanum **Tímar**. 

Til að skilja þetta tilfelli, sjá eftirfarandi reiti.

| Sveigjanlegur + | Sveigjanlegur - | Tími | Launatími |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Útreikningur á Sveigjanlegum+

Samkvæmt forstillingu sveigjanlegs er tíminn á milli kl. 06:00 og 07:00 tímabilið Sveigjanlegur+. Ef starfskraftur stimplar sig þannig inn klukkan 06:30, fær hann 0,5 klst. Þessum tímafjölda er bætt við sveigjanlegan reikning starfsmannsins.

#### <a name="calculation-of-flex-"></a>Útreikningur á Sveigjanlegum-

Samkvæmt forstillingu sveigjanlegs byrjar tímabilið Sveigjanlegur- kl. 02:30 og endar klukkan 03:30. Þannig að ef starfsmaðurinn stimplar sig út klukkan 02:45 þá eru 45 mínúturnar (0,75 klst.) sem eftir eru á tímabilinu Sveigjanlegur- skráðar sem launatími og sami tímafjöldi er dreginn frá sveigjanlegum reikningi starfsmannsins. 45 mínúturnar eru innifaldar í launatíma vegna þess að starfsmaðurinn fær greidd laun fyrir 45 mínúturnar sem eftir eru á tímabilinu Sveigjanlegur-. Ef starfsmaður er fjarverandi á tímabilinu Sveigjanlegur- verða þessar 45 mínútur dregnar frá sveigjanlegum reikningi hans.

#### <a name="calculation-of-time"></a>Útreikningur á tíma

Tími er reiknaður sem tíminn á milli inn- og útstimplunar, það er 06:30 til 14:45 sem jafngildir 8,25 klst.

#### <a name="calculation-of-pay-time"></a>Útreikningur á launatíma

Launatími er sá tími sem starfsmaður fær greidd laun fyrir. Í þessu tilfelli er starfsmaðurinn í vinnu í 8,25 klst. (**Tími**). Hins vegar er **Launatími** reiknaður út sem 8,50 klst. vegna þess að starfsmaður fær greidd laun á tímabilinu Sveigjanlegur- eftir að hann stimplar sig út. Launatíminn jafngildir áætluðum vinnutíma vegna þess að tíma Sveigjanlegs+ er bætt við sveigjanlegan reikning starfsmanns, en ekki við launatímann. Launatíminn bætir upp fjarvistartíminn á tímabilinu Sveigjanlegur- og er dreginn frá sveigjanlegum reikningi starfsmannsins.

| Tími              | Skráningargerð | Launatími (klst.)      |
|-------------------|-------------------|-----------------------|
| 06:30 - 07:00 | Sveigjanlegt+             | 0                     |
| 07:00 – 14:45 | Staðaltími     | 7,75                  |
| 14:45 – 15:30 | Sveigjanlegt-             | 0,75 (fjarvistatímabil) |
|                   | Alls             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Tilfelli 2: Starfsmaður vinnur yfir allt tímabilið Sveigjanlegur- og vinnur einnig yfirvinnu

Skráningar starfsmannsins fyrir daginn líta svona út.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 06:30 | 06:30 |
| Framleiðsluverk            | 06:30 | 17:00 |
| Stimpla út                 | 17:00 | 17:00 |

Eftir að búið er að reikna út færslubókarskráningu á síðunni **Samþykkt** er hægt að skoða niðurstöðu útreiknings á flipanum **Tímar**. Til að skilja þetta tilfelli, sjá eftirfarandi reiti.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími | Yfirvinnutími |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 1.50         |

#### <a name="calculation-of-flex"></a>Útreikningur á Sveigjanlegum+

Samkvæmt forstillingu sveigjanlegs er tíminn á milli kl. 06:00 og 07:00 tímabilið Sveigjanlegur+. Ef starfskraftur stimplar sig þannig inn klukkan 06:30, fær hann 0,5 klst. af Sveigjanlegum+ tíma inn á sveigjanleikastöðu sína.

#### <a name="calculation-of-flex-"></a>Útreikningur á Sveigjanlegum-

Sveigjanlegur- er ekki reiknaður vegna þess að starfsmaðurinn vinnur á tímabilinu Sveigjanlegur-. Sveigjanlegur- er reiknaður aðeins ef starfsmaður er fjarverandi á tímabilinu Sveigjanlegur-. Frá sjónarhorni greiðslu, ef starfsmaður vinnur á tímabilinu Sveigjanlegur- fær launataxta sem er skilgreindur fyrir staðaltíma. Ef starfsmaðurinn er fjarverandi á tímabilinu Sveigjanlegur- eru 45 mínúturnar dregnar frá sveigjanlegum reikningi hans.

#### <a name="calculation-of-time"></a>Útreikningur á tíma

Tími er reiknaður sem tíminn á milli innstimplunar klukkan 06:30 og útsimplunar klukkan 05:00, eða 10,50 klst.

#### <a name="calculation-of-pay-time"></a>Útreikningur á launatíma

Í þessu tilfelli vinnur starfsmaðurinn 10,50 klst. (**Tími**). Hins vegar er **Launatími** reiknaður sem 10,00 klst. vegna þess að starfsmaðurinn fær ekki greidd laun á tímabilinu Sveigjanlegur+.

#### <a name="calculation-of-pay-overtime"></a>Útreikningur yfirvinnulauna

| Tími               | Skráningargerð | Launatími (klst.) |
|--------------------|-------------------|------------------|
| 06:30 - 07:00  | Sveigjanlegt+             | 0                |
| 07:00 – 14:30  | Staðaltími     | 7,50             |
| 14:30 – 15:30  | Sveigjanlegt-             | 1,00             |
| 15:30 – 17:00 | Yfirvinna          | 1.50             |
|                    | Alls             | 10,00            |

### <a name="generation-of-pay-items"></a>Myndun launaliða

Starfsmannaskráning fyrir daginn er hægt að flytja frá síðunni **Samþykkja**. Á meðan á flutningsferlinu stendur eru launaliðir og fluttar skráningar myndaðar. Launaliðir tákna skiptingu launatíma í staðaltíma, yfirvinnu, launað hlé og svo framvegis.

Til að opna lista yfir launaliði skal velja **Tími og viðvera** &gt; **Yfirfara og samþykkja** &gt; **Samþykkja**. Veldu síðan **Fyrirspurn** &gt; **Fluttar skráningar**.

Launaliðir eru grundvöllur launa starfsmanns. Hægt er að mynda skrá sem inniheldur upplýsingar úr launaliðum og flytja þessa skrá inn í launakerfi.

Sem hluti af flutningsferlinu er tími og kostnaður við framleiðslu- og verkþætti fluttur til framleiðslu- og verkbóka til að gera grein fyrir eyðslu tíma og kostnaðar. Fluttar skráningar eru grundvöllur tíma og kostnaðarverðs á klukkustund fyrir framleiðslupantanir og verk. Þú getur opnað fluttar skráningar með því að nota valmyndina **Fyrirspurn** á síðunni **Samþykkja**.

Til dæmis í tilfelli 2 eru eftirfarandi launaliðir myndaðir.

| Launagerð     | Launagerð | Launaeiningar | Taxti  | Heildarkostnaður |
|---------------|----------|-----------|-------|------------|
| Staðaltími | 1201     | 10,0      | 10    | 100        |
| Yfirvinna      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Alls | 107,50     |

Launaliður fyrir staðaltíma hefur launaeiningu upp á 10 klukkustundir sem nær yfir staðaltíma, Sveigjanlegan- tíma og yfirvinnu. Staðaltími, Sveigjanlegur- tími og yfirvinna eru sameinuð í einn launalið vegna þess að allar gerðirnar eru reiknaðar sem staðaltími, byggt á sjálfgefnum stillingum á færibreytu á síðunni **Færibreytur útreiknings** (**Tími og viðvera** &gt; **Uppsetning** &gt; **Færubreytur útreiknings**). Yfirvinna er reiknuð ofan á staðaltíma með því að nota viðbótartaxta upp á 5.

Ef þú vilt greina almennilega á milli staðaltíma og yfirvinnu þannig að launaliðir fyrir launagerðir ná aðeins til raunverulegs tíma sem fer í staðaltíma og yfirvinnu skal reikna launaeiningar fyrir staðaltíma sem 8,50 og reikna skal launaeiningar yfirvinnu sem 1,50.

Til að grunnstilla kerfið til að greina almennilega á milli staðaltíma og yfirvinnu, verður þú að útiloka yfirvinnu frá staðaltíma. Þú verður einnig að breyta uppsetningu launagerðar fyrir yfirvinnu svo að launataxti yfirvinnu nái yfir alla greiðslur fyrir klukkustundirnar sem var eytt í yfirvinnu.

### <a name="exclude-overtime-from-the-standard-time"></a>Útiloka yfirvinnu frá staðaltíma

Á síðunni **Færibreytur útreikninga** skal velja **Yfirvinna** sem gerð lýsingar fyrir forstillingu og stilla valkostinn **Launatími** á **Nei** eins og sýnt er hér.

| Skráð lýsing | Gerð lýsingar fyrir forstillingu | Útreikningur   | Stilling | Greiddur         | Stilling |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Vinnutími       | Yfirvinna                   | Staðaltími | Já | Launatími     | Nei  |
|                    |                            | Launatími      | Já | Yfirvinnutími | Já |

Eftir að þú hefur stillt færibreytur útreiknings myndast eftirfarandi launaliðir.

| Launagerð     | Launagerð | Launaeiningar | Taxti  | Heildarkostnaður |
|---------------|----------|-----------|-------|------------|
| Staðaltími | 1201     | 8,50      | 10    | 85,0       |
| Yfirvinna      | 1301     | 1.50      | sept    | 22,50      |
|               |          |           | Alls | 107,50     |

> [!NOTE]
> Færibreytur útreiknings eru með ráðlagða staðalstillingu. Almennt ættir þú að sýna varkárni þegar þú breytir þessum færibreytum. Til að endurheimta ráðlagðar staðalstillingar á síðunni **Færibreytur útreiknings** skal velja **Endurheimta gildi**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Leyfa frávik frá forstillingum staðallauna

Á síðunni **Forstillingar** (**Tími og viðvera** &gt; **Uppsetning** &gt; **Tímaforstillingar** &gt; **Forstillingar**) getur þú sett upp forstillingagerðir sem innihalda skiptikóða og hlé.

### <a name="switch-codes"></a>Skiptikóðar

Þú getur notað skiptikóða til að leyfa starfsmönnum að víkja frá forstillingargerð þeirra með því að breyta mismunandi gerðum forstillinga. Til dæmis getur þú leyft starfsmanni að skipta úr Sveigjanlegum+ tíma í yfirvinnu. Starfsmaður getur bætt við skiptikóða við skráningu eða þú getur úthlutað því verki að bæta skiptikóða við samþykktaraðila skráningarinnar.

Áður en hægt er að nota skiptikóða verður þú að skilgreina hann sem tegund af óbeinum verkþætti. Þú verður síðan að bæta skiptikóðanum við tímaforstillinguna fyrir tímabilið þar sem þú vilt leyfa breytingu á gerð forstillingar. Til dæmis, fylgdu þessum skrefum til stofna skiptikóða sem gerir kleift að breyta tímabilinu Sveigjanlegur+ frá 06:00 til 07:00 í yfirvinnu.

1. Stofnaðu skiptikóða sem heitir **OTBCI (Breyta sveigjanlegum í yfirvinnu fyrir innstimplun)**. Veldu **Tími og viðvera** &gt; **Stjórna óbeinum verkþáttum** &gt; **Óbeinir verkþættir**.
2. Í dálknum **Skiptikóði** skal bæta OTBCI við línu Sveigjanlegs+ í sömu tímaforstillingu.
3. Í dálknum **Aukalegt** skal bæta við forstillingargerðinni **Yfirvinna**.

Íhugaðu eftirfarandi forstillingu sveigjanlegs sem táknar vinnudag.

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

Hér eru skráningar starfsmanns fyrir daginn.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 06:30 | 06:30 |
| Framleiðsluverk            | 06:30 | 14:45 |
| Stimpla út                 | 17:00 | 17:00 |

Eftirfarandi launaliðir myndast eftir flutninginn.

| Launagerð     | Launagerð | Launaeiningar | Taxti  | Heildarkostnaður |
|---------------|----------|-----------|-------|------------|
| Staðaltími | 1201     | 8,50      | 10    | 85,0       |
| Yfirvinna      | 1305     | 1.50      | sept    | 22,50      |
|               |          |           | Alls | 107,50     |

Á síðunni **Samþykkja** skaltu afturkalla flutninginn og nota síðan valmyndina **Skiptikóði** til að nota skiptikóðann **OTBCI**. Þegar þú flytur skráningarnar í annað skipti myndast eftirfarandi launaliðir.

| Launagerð     | Launagerð | Launaeiningar | Taxti  | Heildarkostnaður |
|---------------|----------|-----------|-------|------------|
| Staðaltími | 1201     | 8,50      | 10    | 80,0       |
| Yfirvinna      | 1305     | 2.00      | sept    | 30,0       |
|               |          |           | Alls | 107,50     |

> [!NOTE]
> Þegar þú notar skiptikóðann eykst yfirvinna um 0,5 klst., frá 1,50 til 2,00. 0,5 klukkustundirnar er umbreytingin á Sveigjanlegum+ tíma sem er skráður, frá 6:30 til 07:00 í yfirvinnu.

### <a name="breaks"></a>Hlé

Hlé frá vinnu hefur áhrif á launaútreikning starfsmanns. Hlé eru skilgreind sem gerð af óbeinum verkþætti. Hægt er að skilgreina þau sem annaðhvort **Launað** til að hlénu verði bætt við laun starfsmannsins eða **Ólaunað** til að koma í veg fyrir að hlénu verði bætt við laun starfsmannsins. Einnig er hægt að skilgreina hlé sem annaðhvort **Áætlað** eða **Skráð**.

#### <a name="planned-breaks"></a>Áætlað hlé

Ef fyrirtæki hefur fast hlé, svo sem fastan hádegismat, getur hléið verið fyrirframskilgreint í tímaforstillingunni. Í þessu tilviki þarf starfsmaðurinn ekki að skrá hlé á síðum verkspjalds. Í staðinn er sjálfkrafa gert grein fyrir hléinu þegar skráningar starfsmanns eru reiknaðar út á síðunni **Samþykkja**.

#### <a name="registered-breaks"></a>Skráð hlé

Ef fyrirtæki notar ekki áætluð hlé, geta starfsmenn skráð hlé meðan á vinnudegi stendur. Hægt er að nota skráð hlé, til dæmis, ef starfsmaður vinnur á móti forstillingu sveigjanlegs tíma sem hefur enga skilgreinda innstimplunar- og útstimplunartíma. Skráð hlé eru tegund af óbeinum verkþætti. Starfsmaður skráir hlé á afgreiðslusíðunni **Verkspjald** eða á tækjasíðunni **Verkspjald**. Á báðum þessum síðum getur notandinn valið gerð af hléi úr lista af fyrirframskilgreindum verkþáttarhléum.

#### <a name="paid-and-unpaid-breaks"></a>Launuð og ólaunuð hlé

Verkþátt hlés er hægt að setja upp sem **Launað** eða **Ólaunað**. Launað hlé er innifalið í útreikningi á launatíma og kerfið notar launagerðina sem skilgreind er í launasamningi fyrir skráningargerðina **Hlé**.

### <a name="example-of-a-planned-break"></a>Dæmi um áætlað hlé

Íhugaðu eftirfarandi forstillingu tíma sem inniheldur ólaunað hádegisverðarhlé.

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 12:00 | Mánudagur  |
| Hlé         | 12:00 | 12:30 | Mánudagur  |
| Staðaltími | 12:30 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

Hér eru skráningar starfsmanns fyrir daginn.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 06:30 | 06:30 |
| Framleiðsluverk            | 06:30 | 14:45 |
| Stimpla út                 | 17:00 | 17:00 |

Eftir að búið er að reikna út færslubókarskráningu á síðunni **Samþykkt** er hægt að skoða niðurstöðu útreiknings á flipanum **Tímar**. Til að skilja þetta tilfelli, sjá eftirfarandi reiti.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími | Ógreiddur hlétími | Yfirvinnutími |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Kerfið reiknaði 0,5 klukkustundir af ógreiddum hlétíma og þessi tími er ekki hluti af launatíma.

### <a name="example-of-a-registered-break"></a>Dæmi um skráð hlé

Íhugaðu eftirfarandi forstillingu tíma sem inniheldur ekki áætluð hlé.

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

Hér eru skráningar starfsmanns fyrir daginn.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      |
|---------------------------|----------|----------|
| Innstimplun                  | 06:30 | 06:30 |
| Framleiðsluverk            | 06:30 | 17:00 |
| Hlé                     | 12:03 | 12:32 |
| Stimpla út                 | 17:00 | 17:00 |

Þegar skráningar eru reiknaðar er tíminn verkþáttanna reiknaður út.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      | Tími  |
|---------------------------|----------|----------|-------|
| Innstimplun                  | 06:30 | 06:30 |       |
| Framleiðsluverk            | 06:30 | 17:00 | 10,00 |
| Hlé                     | 12:03 | 12:32 | 0,50  |
| Stimpla út                 | 17:00 | 17:00 |       |

> [!NOTE]
> Hlétími gengur samhliða tíma verkþáttar (framleiðsluverki í þessu dæmi). Þessi leið er alltaf notuð fyrir hlétíma. Þegar skráningar eru reiknaðar er hlétíminn dreginn frá tíma verkþáttar. Í þessu tilviki tekur framleiðsluverkið 10,50 klst., en tíminn er reiknaður sem 10 vegna þess að 0,5 klst. af hlétíma eru dregnar frá tíma verkþáttar.

Eftir að búið er að reikna út færslubókarskráningu á síðunni **Samþykkt** er hægt að skoða niðurstöðu útreiknings á flipanum **Tímar**. Til að skilja þetta tilfelli, sjá eftirfarandi reiti.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími | Ógreiddur hlétími | Yfirvinnutími |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Ef áætlað hlé hefði verið launað í stað ólaunað myndi niðurstöður útreiknings líta svona út.

| Sveigjanlegur + | Sveigjanlegur - | Tími  | Launatími | Greiddur hlétími | Yfirvinnutími |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Launaliðir og launað hlé

Þegar þú flytur skráningar á síðunni **Samþykkja** eru launaliðir myndaðir. Aðskilinn launaliður er myndaður fyrir launuð hlé.

Launataxtinn fyrir launað hlé er ákvarðaður af launagerðinni sem sett er upp í launasamningum fyrir hléið. Í stað þess að nota launagerð getur þú sett upp kostnaðarverð fyrir hverja klukkustund í hléi fyrir skilgreint dagsetningabil.

Íhugaðu eftirfarandi tímaforstillingu.

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

Hér eru skráningar starfsmanns fyrir daginn.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      | Tími |
|---------------------------|----------|----------|------|
| Innstimplun                  | 07:00 | 07:00 |      |
| Framleiðsluverk            | 07:00 | 15:00 | 7.5  |
| Hlé (greitt)              | 12:00 | 12:30 | 0,5  |
| Stimpla út                 | 15:00 | 15:00 |      |

Í þessu dæmi er launagerðin fyrir staðaltíma stilltur á **1201** og launataxtinn **10** er settur upp í launasamningi. Launað hlé hefur launagerðina **1301** og launataxtann **8**. Þegar skráningar eru fluttar eru eftirfarandi launaliðir myndaðir.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 7,50      | 10   |
| Sveigjanlegt-         | 1201     | 0,50      | 10   |
| Hlé (greitt)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Hvernig kostnaði á launuðu hléi er úthlutað til verka og framleiðslupantana

Hægt er að setja upp kostnað á klukkustund fyrir verkþætti og framleiðsluverk þannig að hann sé ákvarðaður annaðhvort af launataxta sem er reiknaður í „Tími og viðvera“ eða af kostnaðartegundum sem eru skilgreindar fyrir verkþætti.

Til að setja upp kostnaðartegundina skaltu velja **Framleiðslustýring** &gt; **Uppsetning** &gt; **Framkvæmd framleiðslu** &gt; **Sjálfgildi framleiðslupöntunar** og stilla reitinn **Kostnaðartegund** á **Já** eða **Nei**.

- **Nei** - Kostnaður er reiknaður út frá launatöxtum sem eru skilgreindir fyrir Skráningargerðir tíma og viðveru.
- **Já** - Kostnaður er reiknaður út frá kostnaðartegundum fyrir framleiðslu og verkþætti.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Kostnaðarútreikningur byggður á launatöxtum sem reiknaðir eru í „Tími og viðvera“

Eftirfarandi dæmi sýnir hvernig kostnaður á klukkustund er reiknaður þegar kostnaður er settur upp þannig að hann sé reiknaður út frá launatöxtum.

Taxti tímakaups sem notaður er fyrir framleiðslupantanir og verk er reiknaður á meðan á flutningsferlinu stendur. Til að skoða taxta tímakaups fyrir hvern verkþátt skal opna síðuna **Samþykkja** í „Tími og viðvera“ og velja síðan **Fyrirspurn** &gt; **Fluttar skráningar**. Þú getur fundið taxta kostnaðar á klukkustund fyrir hverja skráningu á flipanum **Kostnaðarverð**.

Íhugaðu eftirfarandi skráningar sem nota sömu tímaforstillingu og í fyrra dæmi.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      | Tími |
|---------------------------|----------|----------|------|
| Innstimplun                  | 07:00 | 07:00 |      |
| Ferli (Pöntun: 4711)     | 07:00 | 11:00 | 4    |
| Ferli (Pöntun: 4712)     | 11:00 | 15:00 | 3,50 |
| Hlé (greitt)              | 12:00 | 12:30 | 0,50 |
| Stimpla út                 | 15:00 | 15:00 |      |

Eftir að skráningar eru fluttar eru eftirfarandi fluttar skráningar búnar til.

| Skráningargerð     | Tími | Kostnaðarverð á klukkustund |
|-----------------------|------|---------------------|
| Innstimplun              | 0,00 | 0,00                |
| Ferli (Pöntun: 4711) | 4,00 | 10,00               |
| Ferli (Pöntun: 4712) | 3,50 | 11,14               |
| Hlé (greitt)          | 0,50 | 0,00                |
| Stimpla út             | 0,00 | 0,00                |

Útreikningur kostnaðarverðs á klukkustund fyrir launað hlé fer eftir stillingu á beinum launakostnaði. Veldu **Tími og viðvera** &gt; **Uppsetning** &gt; **Færibreytur tíma og viðveru**. Á flipanum **Kostnaðarverð**, undir **Beinn launakostnaður**, í reitnum **Staðaltími** getur þú valið **Já**, **Nei** eða **Úthlutun**.

- **Já** - Þetta gildi er notað fyrir dæmið hér að ofan. Kostnaðinum er úthlutað til framleiðslu eða verkþáttar sem keyrir samhliða verkþætti launaðs hlés. Í dæminu er þessi verkþáttur framleiðsluverkið fyrir pöntun 4712. Eins og þú sérð er kostnaðarverð á klukkustund fyrir launað hlé 0 (núll) og því er úthlutað á starfið sem keyrir samhliða hlénu.

    Launaða hléið er 0,5 klukkustundir og launataxtinn er 8. Þess vegna er heildarkostnaður fyrir launað hlé 4. Heildarkostnaðinum er síðan úthlutað á 3,5 klukkustunda langt vinnsluverk. Þess vegna leggur launað hlé 1,14 á klukkustund af mörkum til kostnaðar (4 ÷ 3,5 = 1,14).

- **Úthlutun** - Launuðu hléi er dreift jafnt á verkin sem eru skráð fyrir daginn. Ef þetta gildi er notað fyrir dæmið hér að ofan eru eftirfarandi fluttar skráningar búnar til.

    | Skráningargerð     | Tími | Kostnaðarverð á klukkustund |
    |-----------------------|------|---------------------|
    | Innstimplun              | 0,00 | 0,00                |
    | Ferli (Pöntun: 4711) | 4,00 | 10,53               |
    | Ferli (Pöntun: 4712) | 3,50 | 10,53               |
    | Hlé (greitt)          | 0,50 | 0,00                |
    | Stimpla út             | 0,00 | 0,00                |

    Heildarvinnslutími fyrir framleiðsluverkin tvö er 7,5 klst. og heildarkostnaður við launað hlé er 4. Því er kostnaður við hléið reiknaður sem 0,53 (= 4 ÷ 7,5).

- **Nei** - Kostnaður við launað hlé eykur ekki kostnað á klukkutíma fyrir vinnsluverkþætti.

    | Skráningargerð     | Tími | Kostnaðarverð á klukkustund |
    |-----------------------|------|---------------------|
    | Innstimplun              | 0,00 | 0,00                |
    | Ferli (Pöntun: 4711) | 4,00 | 10,00               |
    | Ferli (Pöntun: 4712) | 3,50 | 10,00               |
    | Hlé (greitt)          | 0,50 | 0,00                |
    | Stimpla út             | 0,00 | 0,00                |

## <a name="absence"></a>Fjarvist

Fjarvistarkóði er notaður til að skrá fjarvistartímabil starfsmanns. Eins og hlé og skiptikóðar er fjarvistarkóði gerð af óbeinum verkþætti. Fjarvistartími getur verið annaðhvort áætlaður eða skráður og fjarvist getur verið annaðhvort leyfileg eða óleyfileg. Dæmi um leyfilega fjarvist á t.d. við um læknaheimsókn, námskeið eða kviðdómsskyldu. Óleyfileg fjarvist er fjarvist án góðrar ástæðu, svo sem þegar starfsmaður mætir of seint til vinnu. Venjulega felur leyfileg fjarvist ekki í sér frádrátt á launum starfsmanns, á meðan óleyfileg fjarvist felur í sér frádrátt.

### <a name="planned-absence"></a>Áætlaðar fjarvistir

Þú getur búið til áætlaða fjarvist á síðunni **Búa til áætlaða fjarvist** (**Tími og viðvera** &gt; **Búa til áætlaða fjarvist**). Þar er áætluð fjarvist skráð sem fjarvistarverk fyrir tiltekinn dag og tíma.

Verkið byggist á fyrirspurn. Þess vegna getur þú búið til áætlaða fjarvist fyrir marga starfsmenn, t.d. starfsmenn sem tilheyra sama reikniflokknum. Ef áætluð fjarvist er fyrir einn starfsmann getur skráningin verið slegin inn annaðhvort á síðunni **Viðvera** eða á síðunni **Tímaskráning starfsmanna**.

- Til að slá inn fjarvistarskráningu á síðunni **Viðvera** skaltu velja **Tími og viðvera** &gt; **Fyrirspurnir og skýrslur** &gt; **Viðvera** &gt; **Viðvera** og velja síðan **Fjarvistaskráning**.
- Til að slá inn fjarvistarskráningu á síðunni *<strong><em>Tímaskráning starfskrafta</em></strong>* skal velja <strong>Tími og viðvera</strong> &gt; <strong>Uppsetning</strong> &gt; <strong>Tímaskráning starfskrafta</strong> og síðan á flipanum <strong>Tími</strong>, undir <strong>Tímaúthlutun</strong> skal velja <strong>Fjarvistaskráningar</strong>.

Þú getur notað skýrsluna **Áætlaðar fjarvistir** til að sjá yfirlit yfir áætlaðar fjarvistir starfsmanna. Til að opna þessa skýrslu skal velja **Tími og viðvera** &gt; **Fyrirspurnir og skýrslur** &gt; **Fjarvistaskýrslur** &gt; **Áætlaðar fjarvistir**.

### <a name="registered-absence"></a>Skráð fjarvist

Almennt eru starfsmenn taldir fjarverandi ef þeir eru ekki í vinnu fyrir hvaða tíma sem er á milli áætlaðs innstimplunar- og útstimplunartíma. Ef starfsmenn stimpla sig inn seinna en áætlað er eða ef þeir stimpla sig út fyrr en áætlað er, eru þeir beðnir um að velja fjarvistarkóða til að gefa upp ástæðu fyrir fjarverunni. Hægt er að setja upp fjarvistarkóða þannig að hann eigi við um skráningu. Einungis verður hægt að velja úr viðeigandi kóðum á listanum.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Sýnishorn byggð á ýmsum samsetningum vinnutímaskráninga

Eftirfarandi sýnishorn sýna launaliði og færslur til samþykktar sem eru búnar til fyrir starfsmenn miðað við skráningar þeirra. Öll sýnishornin byggjast á eftirfarandi tímaforstillingu.

| Gerð forstillingar  | Ræsa    | Ljúk.      | Dagur     |
|---------------|----------|----------|---------|
| Yfirvinna     | 00:00 | 06:00 | Mánudagur  |
| Sveigjanlegt+         | 06:00 | 07:00 | Mánudagur  |
| Innstimplun      | 07:00 | 07:00 | Mánudagur  |
| Staðaltími | 07:00 | 14:30 | Mánudagur  |
| Sveigjanlegt-         | 14:30 | 15:30 | Mánudagur  |
| Stimpla út     | 15:30 | 15:30 | Mánudagur  |
| Yfirvinna     | 15:30 | 06:00 | Þriðjudagur |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Sýnishorn 1: Starfsmaður stimplar sig inn seinna en samkvæmt áætlun

Starfsmaðurinn stimplar sig inn kl. 08:30. Vegna þess að áætlaður innstimplunartími hans er 07:00, hefur hann mætt 1,50 klukkustund of seint í vinnuna. Vegna þess að 1,50 klukkustundin er talinn fjarvistartími er starfsmaður beðinn um að velja fjarvistarkóða. Starfsmaður fer úr vinnu kl. 15:30, sem er áætlaður útstimplunartími. Þegar skráningar starfsmanns eru reiknaðar og samþykktar, birtist fjarvistaskráningin, ásamt fjarvistarkóða sem starfsmaðurinn hefur valið, við innstimplun fyrir tímann á milli kl. 07:00 og 08:30.

Í tímaforstillingu er hægt að skilgreina **Innstimplun** þannig að það sé svigrúm þegar starfsmenn mæta of seint til vinnu. Til dæmis, ef þú setur upp svigrúm upp á 5, þá er starfsmaður aðeins beðinn um að fjarvistarkóða ef hann stimplar sig inn seinna en kl. 07:05.

Í þessu tilviki, vegna þess að starfsmaðurinn hefur ekki góða ástæðu til að mæta of seint í vinnu, velur hann fjarvistarkóða sem er skilgreindur fyrir óleyfilega fjarvist. Fjarvistarkóði er álitinn eiga við um óleyfilega fjarvist ef stillingin fyrir yfirvinnufrádrátt er virk fyrir fjarvistarflokkinn sem fjarvistarkóðinn tilheyrir. Til að stilla stillinguna skal velja **Tími og viðvera** &gt; **Uppsetning** &gt; **Flokkur** &gt; **Fjarvistarflokkur** og velja síðan gátreitinn **Frádráttur yfirvinnu**.

Hér er sýnt hvernig skráningar starfsmanns fyrir daginn birtast á síðunni **Samþykkja** eftir útreikning.

| Gerð færslubókarskráningar         | Ræsa    | Ljúk.      | Tími |
|-----------------------------------|----------|----------|------|
| Fjarvist (óleyfileg - seinn til vinnu) | 07:00 | 08:30 | 1.5  |
| Innstimplun                          | 08:30 | 08:30 |      |
| Framleiðsluverk                    | 07:30 | 15:30 | 7.0  |
| Stimpla út                         | 15:30 | 15:30 |      |

Hér er launaliðurinn sem fylgir eftir að skráningar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 7,00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Sýnishorn 2: Starfsmaðurinn stimplar sig út fyrir áætlaðan útstimplunartíma á meðan á staðaltíma stendur

Starfsmaðurinn stimplar sig inn klukkan kl. 07:00 og stimplar sig snemma út klukkan kl. 13:00. Vegna þess að kl. 13:00 er á undan áætlaðri útstimplun kl. 15:30, og kl 13:00 er innan staðaltímabils, er starfsmaður beðinn um að velja fjarvistarkóða. Starfsmaðurinn velur fjarvistarkóða fyrir læknisheimsókn sem er skilgreint sem leyfileg fjarvist. Launataxtinn fyrir leyfilega fjarvist er skilgreindur í launasamningum fyrir skráningargerðina **Fjarvist** (**Tími og viðvera** &gt; **Uppsetning** &gt; **Laun** &gt; **Launasamningar**).

Hér er sýnt hvernig skráningar starfsmanns fyrir daginn birtast á síðunni **Samþykkja** eftir útreikning.

| Gerð færslubókarskráningar              | Ræsa    | Ljúk.      | Tími |
|----------------------------------------|----------|----------|------|
| Innstimplun                               | 07:00 | 07:00 |      |
| Framleiðsluverk                         | 07:00 | 13:00 | 4,0  |
| Stimpla út                              | 13:00 | 13:00 |      |
| Fjarvist (leyfileg - læknaheimsókn) | 13:00 | 15:30 | 3.5  |

Hér er launaliðurinn sem fylgir eftir að skráningar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Sýnishorn 3: Starfsmaðurinn stimplar sig út á undan áætluðum útstimplunartíma á meðan á tímabili Sveigjanlegs- stendur

Starfsmaðurinn stimplar sig inn kl. 07:00 og stimplar sig út kl. 14:15, sem er innan tímabils Sveigjanlegs-. Ekki er litið á tímann á milli raunverulegs útstimplunartíma og áætlaðs útstimplunartíma sem fjarvist og starfsmaðurinn er ekki beðinn um að velja fjarvistarkóða. Upphæðin er dregin frá sveigjanlegum reikningi starfsmanns og hann fær greidd laun það sem eftir lifir af tímabili Sveigjanlegs-, frá 14:15 til 15:30.

Hér er sýnt hvernig skráningar starfsmanns fyrir daginn birtast á síðunni **Samþykkja** eftir útreikning.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      | Tími |
|---------------------------|----------|----------|------|
| Innstimplun                  | 07:00 | 07:00 |      |
| Framleiðsluverk            | 07:00 | 14:15 | 7,25 |
| Stimpla út                 | 14:15 | 14:15 |      |

Hér er launaliðurinn sem fylgir eftir að skráningar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Sýnishorn 4: Starfsmaðurinn stimplar sig seint inn og stimplar sig út eftir áætlaðan útstimplunartíma á yfirvinnutímabili

Starfsmaðurinn stimplar sig seint inn kl. 09:30 og síðan, til að bæta upp fyrir seina mætingu, vinnur yfirvinnu og stimplar sig út kl. 17:00. Vegna þess að starfsmaðurinn kom seint og bætti það upp með því að vinna lengur, vill fyrirtækið ekki veita starfsmanninum yfirvinnulaun fyrir vinnustundirnar sem hann starfaði milli áætlaðs útstimplunartíma kl. 15:30 og raunverulegs útstimplunartíma kl. 17:00, jafnvel þó að þetta tímabil sé skilgreint sem yfirvinna í tímaforstillingu.

Til að takast á þetta er hægt að setja upp fjarvistarkóðann til að draga frá yfirvinnutímanum með þeim vinnustundum sem fóru í óleyfilega fjarvist starfsmanns á sama degi. Veldu **Tími og viðvera** &gt; **Uppsetning** &gt; **Flokkar** &gt; **Fjarvistaflokkar** og veldu gátreitinn **Frádráttur yfirvinnu** til að draga frá yfirvinnu sem nemur vinnustundum af óleyfilegri fjarvist.

Hér er sýnt hvernig skráningar starfsmanns fyrir daginn birtast á síðunni **Samþykkja** eftir útreikning.

| Gerð færslubókarskráningar         | Ræsa    | Ljúk.      | Tími |
|-----------------------------------|----------|----------|------|
| Fjarvist (óleyfileg - seinn til vinnu) | 07:00 | 09:30 | 1.5  |
| Innstimplun                          | 09:30 | 09:30 |      |
| Framleiðsluverk                    | 09:30 | 17:00 | 7.5  |
| Stimpla út                         | 17:30 | 17:30 |      |

Ef gátreiturinn **Frádráttur yfirvinnu** er valinn fyrir valdan fjarvistarkóða, er dregið frá yfirvinnulaunum sem nemur vinnustundunum sem starfsmaður var með í óleyfilegri fjarvist. Í þessu tilviki eru eftirfarandi launaliðir myndaðar eftir að skráningarnar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 9,00      | 10   |
| Yfirvinna      | 1301     | 0,5       | sept   |

Hér eru 1,5 klukkustundir af óleyfilegri fjarvist, frá kl. 07:00 til 09:30, dregnar frá 2,0 klukkustundir af yfirvinnu, frá 15:30 til 17:30. Niðurstaðan af skráningunni er 1,5 klukkustund af staðaltíma og 0,5 klukkustundir af yfirvinnu.

Hins vegar, ef gátreiturinn **Frádráttur yfirvinnu** er hreinsaður fyrir valdan fjarvistarkóða, eru yfirvinnulaunin veitt starfsmanninum, jafnvel þótt hann hafi mætt seint og verið með óleyfilega fjarvist. Í þessu tilviki eru eftirfarandi launaliðir myndaðar eftir að skráningarnar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 7,50      | 10   |
| Yfirvinna      | 1301     | 2,0       | sept   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Sýnishorn 5: Starfsmaðurinn stimplar sig út á undan áætluðum útstimplunartíma og getur umbreytt fjarvistartímabilinu yfir í tímabil Sveigjanlegs

Eftirfarandi dæmi sýnir hvernig hægt er að draga af sveigjanlegum reikningi starfsmanns með því að umbreyta fjarvistartímabilinu í tímabil Sveigjanlegs-.

Starfsmaðurinn stimplar sig inn kl. 07:00 og stimplar sig út kl. 13:00. Starfsmaðurinn er með samkomulag um að hann geti farið heim yfir helgina ef hann dregur þessa tíma af sveigjanlega reikningnum sínum. Þegar starfsmaður stimplar sig út kl. 13:00 er hann beðin um að velja fjarvistarkóða vegna þess að tímabil fjarvistar sem eftir er af þeim hluta vinnudagsins sem verður fyrir áhrifum er ekki innan áætlaðs tímabils Sveigjanlegs-. Til að umbreyta það sem eftir er af vinnudeginum í sveigjanlegan-, getur starfsmaður valið fjarvistarkóða sem er settur upp til að draga frá sveigjanlegum reikningi hans.

Til að minnka stöðuna á sveigjanlegum vinnustundum fyrir starfsmenn sem skrá fjarvist á vinnudegi skal velja **Tími og viðvera** &gt; **Uppsetning** &gt; **Flokkar** &gt; **Fjarvistarflokkar** og velja gátreitinn **Minnka sveigjanlegan**.

Hér er sýnt hvernig skráningar starfsmanns fyrir daginn birtast á síðunni **Samþykkja** á undan útreikningi.

| Gerð færslubókarskráningar | Ræsa    | Ljúk.      | Tími |
|---------------------------|----------|----------|------|
| Innstimplun                  | 07:00 | 07:00 |      |
| Framleiðsluverk            | 07:00 | 13:00 | 6,0  |
| Stimpla út                 | 13:00 | 13:00 |      |

Ef starfsmaður velur fjarvistarkóða fyrir óleyfilega fjarvist, þá er sýnt hér hvernig launaliðurinn sem fylgir kemur til með að líta út eftir að skráningin er flutt.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 6,00      | 10   |

Ef starfsmaður velur fjarvistarkóða fyrir leyfilega fjarvist, og fjarvistarkóðinn er settur upp til að draga af sveigjanlegum reikningi hennar, þá er sýnt hér hvernig launaliðirnar sem fylgja koma til með að líta út eftir að skráningar eru fluttar.

| Launagerð     | Launagerð | Launaeiningar | Taxti |
|---------------|----------|-----------|------|
| Staðaltími | 1201     | 8,50      | 10   |

Í þessu tilviki er dregið af sveigjanlegri stöðu starfsmanns sem nemur vinnustundunum á milli raunverulegs útstimplunartíma og áætlaðs útstimplunartíma (það er 2,5 klst. frá 13:00 til 15:30).

> [!NOTE]
> Við mælum ekki með því að þú veljir báða gátreitina **Draga af sveigjanlegum** og **Draga af yfirvinnu** fyrir fjarvistarkóða, vegna þess að þessi uppsetning mun draga óleyfilegar vinnustundir frá yfirvinnustundum starfsmanns og draga samtímis af sveigjanlegum reikningi starfsmanns.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Sýnishorn 6: Það er engar áætlaðar fjarvistir og engin viðvera starfsmanns fyrir daginn

Hafi starfsmaður mætir ekki til vinnu á vinnudegi og engin áætluð fjarvist er fyrir starfsmanninn þann dag er sjálfgefinn fjarvistarkóði notaður við útreikning á skráningum starfsmanns. Til að skilgreina sjálfgefna fjarvistarkóða skal velja **Tími og viðvera** &gt; **Færibreytur tíma og viðveru**. Þú getur síðan valið fjarvistarkóða í eftirfarandi reitum:

- Færa sjálfkrafa inn Sveigjanlegan-
- Færa fjarvistir sjálfkrafa inn

Þegar daglegar skráningar eru reiknaðar fyrir starfsmann sem er með sveigjanlegar vinnustundir virkar, er fjarvistarkóðinn sem er tilgreindur í reitnum **Færa Sveigjanlegan- sjálfkrafa inn** notaður sem sjálfgefinn fjarvistarkóði. Ef starfsmaður er ekki með sveigjanlegar vinnustundir virkar, er fjarvistarkóðinn sem er tilgreindur í reitnum **Færa fjarvistir sjálfkrafa inn** notaður. Ef fyrirtæki hefur samsetningu af starfsmönnum sem eru með sveigjanlegar vinnustundir virkar og starfsmönnum sem eru ekki með sveigjanlegar vinnustundir virkar þarf að setja upp báðar færibreyturnar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]