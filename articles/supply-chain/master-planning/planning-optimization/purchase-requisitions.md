---
title: Innkaupabeiðnir
description: Þetta efnisatriði lýsir því hvernig innkaupabeiðnir eru studdar í fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1d6fd4be0ee1913264c4a565234cfdf711365792
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570865"
---
# <a name="purchase-requisitions"></a>Innkaupabeiðnir

[!include [banner](../../includes/banner.md)]

Aðaláætlanagerð getur fyllt á samþykktar innkaupabeiðnir. Til að ná yfir innkaupabeiðnir þurfa notendur þar af leiðandi ekki að nota verkflæði til að stofna innkaupapantanir. Þess í stað er getur aðaláætlanagerð dekkað innkaupabeiðnir. Vegna þessarar virkni getur innkaupabeiðni framleitt innkaupapöntun, flutningspöntun eða framleiðslupöntun, allt eftir gildinu fyrir **Gerð áætlaðrar pöntunar** sem er stillt fyrir tengda afurðina.

## <a name="enable-master-plans-to-include-requisitions"></a>Virkja aðaláætlanir til að hafa með beiðnir

Til að hafa með beiðnir við þekjuútreikning fyrir aðaláætlun skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.
1. Stofnið eða veljið aðaláætlun.
1. Í flýtiflipanum **Almennt** skal stilla valkostinn **Hafa með beiðnir** á *Já*.
1. Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að hafa með beiðnir.

## <a name="approved-requisitions-time-fence"></a>Samþykkt tímamörk beiðna (dagar)

*Tímamörk samþykktra beiðna* ákveða hversu langt aftur (í dögum) aðaláætlun mun hafa með eftirspurn frá samþykktum áfyllingarbeiðnum. Hægt er að stilla tímamörk samþykktra beiðna á bæði þekjuflokksstigi og aðaláætlunarstigi.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Stilla tímamörk samþykktra beiðna fyrir þekjuflokk

1. Fara skal í **Aðaláætlanagerð** \> **Uppsetning** \> **Þekja** \> **Þekjuflokkar**.
1. Stofnið eða veljið þekjuflokk.
1. Í flýtiflipanum **Annað** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.
1. Endurtakið skref 2 og 3 fyrir hvern þekjuflokk til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Stilla tímamörk samþykktra beiðna fyrir einstaka þekjuflokka

Þegar stillt eru tímamörk samþykktra beiðna fyrir staka aðaláætlun mun stillingin hnekkja stillingu tímamarka fyrir alla þekjuflokka sem eiga við.

1. Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.
1. Stofnið eða veljið aðaláætlun.
1. Í flýtiflipanum **Tímamörk í dögum** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.
1. Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.

> [!IMPORTANT]
> **Væntanlegt:** Tímamörk samþykktra beiðna eru ekki enn studd fyrir fínstillingu skipulagningar. Þar til þau eru studd verða öll gildin hunsuð sem færð eru inn í reitinn **Tímamörk samþykktra beiðna (dagar)**.

## <a name="independent-supply-regardless-of-coverage-code"></a>Sjálfstætt framboð, óháð þekjukóða

Innkaupabeiðnir eru alltaf dekkaðar af sjálfstæðum áætluðum pöntunum burtséð frá því hver þekjukóðinn er. Þessi hegðun tryggir skýran rekjanleika og verkflæði á milli innkaupabeiðna og áfyllingarpantana.

### <a name="example-1"></a>Dæmi 1

Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:

- Birgðamagn á lager = 10.
- Lágmarksmagn birgða = 15.
- Hámarksmagn birgða = 20.
- Innkaupabeiðni fyrir eitt stykki er til. Hún er með umbeðna dagsetningu fyrir daginn í dag.

Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: eina fyrir 10 stykki til að fylla á birgðir upp í hámarksmagn og eina fyrir eitt stykki til að fylla á innkaupabeiðnina.

### <a name="example-2"></a>Dæmi 2

Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:

- Birgðamagn á lager = 17.
- Lágmarksmagn birgða = 15.
- Hámarksmagn birgða = 20.
- Innkaupabeiðni fyrir eitt stykki er til. Hún er með umbeðna dagsetningu fyrir daginn í dag.

Þegar aðaláætlanagerð er keyrð er ein áætluð pöntun fyrir eitt stykki stofnuð til að fylla á innkaupabeiðnina.

### <a name="example-3"></a>Dæmi 3

Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem *Tímabil* og lengd tímabils upp á sjö daga. Hún er með eftirfarandi stöður á birgðum, sölupöntun og beiðni:

- Birgðamagn á lager = 0.
- Sölupöntun fyrir fimm stykki er til. Hún er með væntanlega sendingardagsetningu fyrir daginn í dag plús einn dagur.
- Innkaupabeiðni fyrir þrjú stykki er til. Hún er með umbeðna dagsetningu fyrir daginn í dag plús þrír dagar.

Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: ein fyrir þrjú stykki til að fylla á innkaupabeiðnina og eina fyrir fimm stykki til að fylla á eftirspurn sölupöntunar.

> [!NOTE]
> Þegar áætluð pöntun sem er fest við innkaupabeiðni er staðfest heldur áætlunarvélin þarfarakningunni á innkaupabeiðninni. Ef kemur í ljós síðar að það vanti magn í staðfestu pöntunina sem þarf til að fylla á innkaupabeiðnina mun kerfið stofna nýja áætlaða pöntun sem nemur mismuninum.

Frekari upplýsingar um innkaupabeiðnir er að finna í [Yfirlit innkaupabeiðna](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]