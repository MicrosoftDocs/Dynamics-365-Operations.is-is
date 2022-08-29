---
title: Vikmörk tafar (neikvæður dagafjöldi)
description: Þessi grein veitir upplýsingar um útreikning á vikmörkum seinka og hvernig það hefur áhrif á fyrirhugaða pöntunargerð í Hagræðingu áætlanagerðar.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: fa4d2d1506546cacf5f9a7ec936f17601c5727d2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335376"
---
# <a name="delay-tolerance-negative-days"></a>Vikmörk tafar (neikvæður dagafjöldi)

[!include [banner](../../includes/banner.md)]

Seinkunarþolsaðgerðin gerir skipulagshagræðingu kleift að huga að **Neikvæðar dagar** gildi sem er stillt fyrir þekjuhópa, vöruþekju og/eða aðaláætlanir. Hún er notuð til að víkka út tímabil vikmarka tafar sem er notað í aðaláætlanagerð. Þannig er hægt að komast hjá því að stofna nýjar framboðspantanir ef fyrirliggjandi framboð getur annað eftirspurn eftir stutta töf. Tilgangur virkninnar er að ákveða hvort skynsamlegt sé að búa til nýja framboðspöntun fyrir tiltekna eftirspurn.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Kveiktu eða slökktu á eiginleikum tafaþols

Til að gera tafaþolsvirkni aðgengilegan í kerfinu þínu skaltu fara á [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og kveiktu á eftirfarandi eiginleikum:

- *Neikvæðar dagar fyrir hagræðingu áætlanagerðar* – Þessi eiginleiki gerir stillingar fyrir neikvæða daga fyrir umfjöllunarhópa og vöruumfjöllun. Frá og með Supply Chain Management útgáfu 10.0.29 er aðgerðin skylda og ekki hægt að slökkva á honum.
- *Sjálfvirkni framboðs eftir pöntun* - Þessi eiginleiki gerir neikvæðar daga stillingar fyrir aðaláætlanir. (Nánari upplýsingar er að finna í [Sjálfvirkni framboðs eftir pöntun](../make-to-order-supply-automation.md) .)

## <a name="delay-tolerance-in-planning-optimization"></a>Vikmörk tafar í fínstillingu skipulagningar

Vikmörk tafar sýnir fjölda daga fram yfir afhendingartímann sem þú ert til í að bíða áður en þú pantar nýja áfyllingu þegar fyrirliggjandi framboð er þegar áætlað. Vikmörk tafar eru skilgreind með því að nota almanaksdaga, ekki viðskiptadaga.

Við aðaláætlanagerð, þegar kerfið reiknar út vikmörk tafar, tekur hún til greina stillinguna **Neikvæður dagafjöldi**. Þú getur stillt **Neikvæðar dagar** gildi á **Umfjöllunarhópar** síðu, the **Vöruumfjöllun** síðu, eða **Aðaláætlanir** síðu. Ef neikvæðum dögum er úthlutað á fleiri en einu stigi notar kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef neikvæðir dagar eru virkir á **Aðaláætlanir** síðu, þessi stilling hnekkir öllum öðrum neikvæðum dagastillingum þegar áætlunin keyrir.
- Ef neikvæðir dagar eru stilltir á **Vöruumfjöllun** síðu, þá hnekkir sú stilling stillingu umfjöllunarhóps.
- Neikvæðar dagar sem eru stilltir á **Umfjöllunarhópar** síðu eiga aðeins við ef neikvæðir dagar hafa ekki verið stilltir fyrir viðkomandi vöru eða áætlun.

Kerfið tengir útreikning á vikmörkum tafar við *fyrstu áfyllingardagsetninguna*, sem jafngildir deginum í dag að viðbættum afhendingartímanum. Seinkunarþolið er reiknað út með því að nota eftirfarandi formúlu, þar sem *hámark()* finnur stærra af tveimur gildum:

*hámark(Fyrsti áfyllingardagur, lokadagur eftirspurnar)* – *Lokadagur eftirspurnar* + *Neikvæður dagafjöldi*

Þessi formúla tryggir að aðaláætlanagerð búi ekki til nýjar framboðspantanir þegar næg eftirspurn er til meðan afhendingartími afurðar er í gangi.

> [!NOTE]
> Útreikningur vikmarka tafar í fínstillingu skipulagningar notar alltaf útreikning kvikra neikvæðra daga úr innbyggðu aðaláætlanagerðinni. Stillingin **Nota kvika neikvæða daga** á síðunni **Færibreytur aðaláætlanagerðar** hefur engin áhrif á þessa hegðun.

Ef fyrirliggjandi framboð felur í sér töfum á eftirspurn sem er minni en eða jafnt og reiknuð vikmörk tafar, bindur fínstilling skipulagningar fyrirliggjandi framboð við eftirspurnina. Í sumum tilfellum er betra að fresta eftirspurninni en að enda með offramboð.

Í eftirfarandi undirhlutum eru dæmi sem sýna hvernig vikmörk tafar hafa áhrif á gerð áætlaðra pantana í fínstillingu skipulagningar.

### <a name="example-1"></a>Dæmi 1

Afurð er með eftirfarandi skilgreiningu:

- **Afhendingartími:** *10*
- **Neikvæður dagafjöldi:** *2*

Eftirfarandi framboð og eftirspurn er til fyrir afurðina:

- **Eftirspurn fyrir daginn í dag:** Sölupöntun fyrir magnið 10
- **Birgðir eftir 12 daga:** Innkaupapöntun fyrir magnið 10

Núverandi framboð getur tryggt eftirspurnina innan 12 daga og það tímabil jafngildir vikmörkum tafa. Þegar aðaláætlanagerð er keyrð eru því engar áætlaðar pantanir stofnaðar.

### <a name="example-2"></a>Dæmi 2

Afurð er með eftirfarandi skilgreiningu:

- **Afhendingartími:** *10*
- **Neikvæður dagafjöldi:** *0*

Eftirfarandi framboð og eftirspurn er til fyrir afurðina:

- **Eftirspurn fyrir daginn í dag:** Sölupöntun fyrir magnið 10
- **Birgðir eftir 12 daga:** Innkaupapöntun fyrir magnið 10

Núverandi framboð getur aðeins annað eftirspurn eftir 12 daga. Hins vegar eru vikmörk tafa 10 dagar. Þegar aðaláætlanagerð er keyrð er því áætluð pöntun fyrir magnið 10 stofnuð.

### <a name="example-3"></a>Dæmi 3

Afurð er með eftirfarandi skilgreiningu:

- **Afhendingartími:** *10*
- **Neikvæður dagafjöldi:** *2*

Eftirfarandi framboð og eftirspurn er til fyrir afurðina:

- **Eftirspurn eftir 11 daga:** Sölupöntun fyrir magnið 10
- **Birgðir eftir 14 daga:** Innkaupapöntun fyrir magnið 10

Núverandi framboð getur aðeins annað eftirspurn eftir þrjá daga. Hinsvegar eru vikmörk tafar tveir dagar. (Í þessu tilviki fela vikmörk tafa aðeins í sér neikvæðu dagana tvo. Eftirspurnardagurinn er ekki hafður með vegna þess að hann kemur á eftir afhendingartíma afurðar.) Þegar aðaláætlanagerð er keyrð er því áætluð pöntun fyrir magnið 10 stofnuð.
