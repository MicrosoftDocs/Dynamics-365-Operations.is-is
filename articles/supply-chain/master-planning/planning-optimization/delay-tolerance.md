---
title: Vikmörk tafar (neikvæður dagafjöldi)
description: Í þessu efnisatriði er að finna upplýsingar um útreikning á vikmörkum tafar og hvernig það hefur áhrif á áætlaða stofnun pöntunar í fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ccf827983694eab2037c73aa3251846b051e66f1
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678568"
---
# <a name="delay-tolerance-negative-days"></a>Vikmörk tafar (neikvæður dagafjöldi)

[!include [banner](../../includes/banner.md)]

Virkni vikmarka tafar gerir fínstillingu skipulagningar kleift að taka til greina gildið fyrir **Neikvæðan dagafjölda** sem er stillt fyrir þekjuflokka. Hún er notuð til að víkka út tímabil vikmarka tafar sem er notað í aðaláætlanagerð. Þannig er hægt að komast hjá því að stofna nýjar framboðspantanir ef fyrirliggjandi framboð getur annað eftirspurn eftir stutta töf. Tilgangur virkninnar er að ákveða hvort skynsamlegt sé að búa til nýja framboðspöntun fyrir tiltekna eftirspurn.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Til að gera virkni fyrir vikmörk tafar aðgengilega í kerfinu skal fara í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Neikvæður dagafjöldi fyrir fínstillingu skipulagningar*.

## <a name="delay-tolerance-in-planning-optimization"></a>Vikmörk tafar í fínstillingu skipulagningar

Vikmörk tafar sýnir fjölda daga fram yfir afhendingartímann sem þú ert til í að bíða áður en þú pantar nýja áfyllingu þegar fyrirliggjandi framboð er þegar áætlað. Vikmörk tafar eru skilgreind með því að nota almanaksdaga, ekki viðskiptadaga.

Við aðaláætlanagerð, þegar kerfið reiknar út vikmörk tafar, tekur hún til greina stillinguna **Neikvæður dagafjöldi**. Hægt er að stilla gildið **Neikvæður dagafjöldi** á annaðhvort síðunni **Þekjuflokkar** eða síðunni **Vöruþekja**.

Kerfið tengir útreikning á vikmörkum tafar við *fyrstu áfyllingardagsetninguna*, sem jafngildir deginum í dag að viðbættum afhendingartímanum. Vikmörk tafar eru reiknuð út með því að nota eftirfarandi formúlu þar sem *hámark()* finnur stærra gildið af gildunum tveimur:

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
