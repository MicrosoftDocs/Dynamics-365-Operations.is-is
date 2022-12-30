---
title: Vikmörk tafar (neikvæður dagafjöldi)
description: Í þessari grein er að finna upplýsingar um útreikning á vikmörkum tafar og hvernig það hefur áhrif á áætlaða stofnun pöntunar í fínstillingu skipulagningar.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 78ba4236705f1a200d9fe796eb80d0241b0fa537
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740469"
---
# <a name="delay-tolerance-negative-days"></a>Vikmörk tafar (neikvæður dagafjöldi)
<!-- KFM: Split topic into PO and classic -->

[!include [banner](../../includes/banner.md)]

Virkni vikmarka tafar gerir fínstillingu skipulagningar kleift að taka til greina gildið fyrir **Neikvæðan dagafjölda** sem er stillt fyrir þekjuflokka, þekju vöru og/eða aðaláætlun. Hún er notuð til að víkka út tímabil vikmarka tafar sem er notað í aðaláætlanagerð. Þannig er hægt að komast hjá því að stofna nýjar framboðspantanir ef fyrirliggjandi framboð getur annað eftirspurn eftir stutta töf. Tilgangur virkninnar er að ákveða hvort skynsamlegt sé að búa til nýja framboðspöntun fyrir tiltekna eftirspurn.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Kveikja eða slökkva á eiginleika fyrir vikmörk tafar

Til að gera virkni fyrir vikmörk tafar aðgengilega í kerfinu skal fara í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum:

- *Neikvæður dagafjöldi til að fínstilla áætlanagerð* – Þessi eiginleiki gerir kleift að stilla neikvæða daga fyrir þekjuflokka og vöruþekju. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.)
- *Sjálfvirkt framboð með „framleiða eftir pöntun“* – Þessi eiginleiki virkjar stillingar neikvæðs dagafjölda fyrir aðaláætlanir. (Frekari upplýsingar er að finna í [Sjálfvirkt framboð með „framleiða eftir pöntun“](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Vikmörk tafar í fínstillingu skipulagningar

Vikmörk tafar sýnir fjölda daga fram yfir afhendingartímann sem þú ert til í að bíða áður en þú pantar nýja áfyllingu þegar fyrirliggjandi framboð er þegar áætlað. Vikmörk tafar eru skilgreind með því að nota almanaksdaga, ekki viðskiptadaga.

Við aðaláætlanagerð, þegar kerfið reiknar út vikmörk tafar, tekur hún til greina stillinguna **Neikvæður dagafjöldi**. Hægt er að stilla gildið **Neikvæður dagafjöldi** á síðunni **Þekjuflokkar** eða síðunni **Vöruþekja** eða á síðunni **Aðaláætlanir**. Ef neikvæðum dögum er úthlutað á fleiri en einu stigi beitir kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef neikvæðir dagar eru virkir á síðunni **Aðaláætlanir**, hnekkir sú stilling allar aðrar neikvæðar dagastillingar þegar áætlunin er keyrð.
- Ef neikvæðir dagar eru stilltir á síðunni **Vöruþekja**, hnekkir sú stilling þekjuflokksstillingunni.
- Neikvæðir dagar sem eru skilgreindir á síðunni **Þekjuflokkar** eiga aðeins við ef neikvæðir dagar hafa ekki verið skilgreindir fyrir viðeigandi vöru eða áætlun.

Kerfið tengir útreikning á vikmörkum tafar við *fyrstu áfyllingardagsetninguna*, sem jafngildir deginum í dag að viðbættum afhendingartímanum. Vikmörk tafar eru reiknuð út með því að nota eftirfarandi formúlu þar sem *hámark()* finnur stærra gildið af gildunum tveimur:

*hámark(Fyrsti áfyllingardagur, lokadagur eftirspurnar)* – *Lokadagur eftirspurnar* + *Neikvæður dagafjöldi*

Þessi formúla tryggir að aðaláætlanagerð búi ekki til nýjar framboðspantanir þegar næg eftirspurn er til meðan afhendingartími afurðar er í gangi.

> [!NOTE]
> Útreikningur vikmarka tafar í fínstillingu skipulagningar notar alltaf útreikning kvikra neikvæðra daga úr úreltu aðaláætlunarvélinni. Stillingin **Nota kvika neikvæða daga** á síðunni **Færibreytur aðaláætlanagerðar** hefur engin áhrif á þessa hegðun.

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
