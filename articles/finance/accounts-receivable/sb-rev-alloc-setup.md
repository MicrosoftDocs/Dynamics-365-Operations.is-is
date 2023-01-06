---
title: Setja upp margþátta tekjuúthlutun
description: Í þessari grein er því lýst hvernig setja á upp færibreytur fyrir margþátta tekjuúthlutun í Áskriftarreikningi.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 23dae125e256e3e567e200024ee61a6c97cb1143
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903306"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Setja upp margþátta tekjuúthlutun

Margþátta tekjuúthlutun gerir þér kleift að setja upp mismunandi sniðmát sem eru notuð til að reikna út og úthluta tekjum á margar vörur. Þessi virkni getur hjálpað þér að fara eftir Accounting Standards Codification Topic 606 (ASC 606) og/eða International Financial Reporting Standard 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Margar færibreytur fyrir tekjuúthlutunarþátt

Notið síðuna **Margar færibreytur fyrir tekjuúthlutunarþátt** til að setja upp færibreytur fyrir margþátta tekjuúthlutun.

### <a name="standalone-selling-price-origin"></a>Uppruni sjálfstæðs söluverðs

**Uppruni sjálfstæðs söluverðs** reiturinn ákvarðar hvaðan sjálfstætt söluverð kemur. Þú getur uppfært gildið á síðunni **Stakt söluverð vöru** og í færslunni. Eftirtaldir valkostir eru í boði.

| Valkostur | Lýsing |
|--------|-------------|
| Upphæð | Stakt söluverð er upphæð sem þú tilgreinir að sé meira en 0 (núll). Upphæðin er umreiknuð á milli virkra og upprunalegra gjaldmiðla eftir þörfum. |
| Grunnsöluverð | Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar. |
| Reikningsverð | Sjálfstætt söluverð samsvarar reikningsverði vörunnar. |
| Prósenta vöru | Sjálfstætt söluverð er tilgreint sem prósentuvirði og er reiknað út frá verði vörunnar. Ef þessi kostur er valinn skal tilgreina sjálfgefna prósentu. |
| Úthluta afgangsupphæð | <p>Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsvirði yfirvöru* – *Heildarsamningsvirði undirvöru*:</p><ul><li>*Heildarsamningsvirði yfirvöru* er hrein eða skuldfærð fjárhæð.</li><li>*Heildarsamningsvirði undirvöru* er samtala framlengds eða samningsbundins sjálfstæðs söluverðs allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverð.</li></ul><p>Ef reiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þennan valkost er aðeins hægt að velja fyrir eina undireiningu í tekjuskiptingunni.</p> |
| Ekkert | Uppruni sjálfstæða söluverðsins byggir á undireiningu. Þessi valkostur á við um hluti sem eru skilgreindir sem yfireiningar í sniðmáti tekjuskiptingar. Ef gátreiturinn fyrir **Tekjuskipting** er valinn er þessi valkostur valinn sjálfkrafa og ekki er hægt að breyta stillingunni. |
| Prósenta af reikningsverði yfireiningar | Uppruni sjálfstæðs söluverðs er prósenta af reikningsverði yfirvörunnar. Hægt er að breyta sjálfgefna gildinu. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar. |
| Prósenta af stöðluðu verði yfireiningar | Uppruni sjálfstæðs söluverðs er prósenta af venjulegu verði yfirvörunnar. Hægt er að breyta sjálfgefna gildinu. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar. Það er sjálfgefni valkosturinn fyrir undireiningar. Þegr valkostinum fyrir undiratriði er breytt úr **Prósenta af stöðluðu verði yfireiningar** í **Prósenta af reikningsverði yfireiningar**, eða úr **Prósenta af reikningsverði yfireiningar** í **Prósenta af stöðluðu verði yfireiningar**, eru útreiknuðu gildi einnig uppfærð. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Lykill fyrir sléttunarmismun tekjuúthlutunar

Reiturinn **Lykill fyrir sléttunarmismun tekjuúthlutunar** tilgreinir lykilinn sem er notaður til að skrá allar breytingar á sléttun á upphæð tekna af samningi. Hann er tiltækur þegar endurtekin reikningagerð vegna samninga er notuð.

## <a name="item-standalone-selling-price"></a>Stakt söluverð vöru

Notaðu síðuna **Stakt söluverð vöru** til að tilgreina uppruna og sjálfstætt söluverð vöru. Gildin sem eru tilgreind á þessari síðu eru notuð sem sjálfgefin gildi á síðunni **Úthlutun tekna** í margfaldri tekjuúthlutun og endurtekinni reikningagerð vegna samninga.

### <a name="specify-item-standalone-selling-price"></a>Tilgreina sérstakt söluverð vöru

Til að tilgreina sjálfstætt verð fyrir vöru skal fylgja þessum skrefum.

1. Á síðunni **Stakt söluverð vöru**, í reitnum **Uppruni sjálfstæðs söluverðs** skal velja uppruna söluverðs.
2. Fylgdu einu af þessum skrefum, fer eftir gildinu sem þú valdir í reitnum **Uppruni sjálfstæðs söluverðs**:

    * Ef þú valdir **Prósenta vöru** skaltu tilgreina prósentuna í reitnum **Prósenta**.
    * Ef þú valdir **Upphæð** skaltu tilgreina upphæðina í reitnum **Sjálfstætt söluverð**.

2. Fyrir hverja vöru sem bæta á við listann skal velja **Bæta við**.
3. Á svæðinu **Vörukóði** skal velja vörukóðann. Veldu vöruvenslin í reitnum **Vöruvensl**. Fyrir vörur þar sem gátreitur fyrir **Tekjuskipting** er auður verður valin samsetning vörukóða og vöruvensla að vera einkvæmur.
4. Breyttu sjálfgildi **Uppruni sjálfstæðs söluverðs**, **Stakt söluverð vöru** eða **Prósenta** eins og þörf er.
5. Fyrir hverja yfirvöru sem bæta á við listann skal velja **Bæta við**.
6. Á svæðinu **Vörukóði** skal velja vörukóðann. Veldu vöruvenslin í reitnum **Vöruvensl**.
7. Veldu gátreitinn **Tekjuskipting**.
8. Veldu vöruvenslin í reitnum **Vöruvensl**. Listinn er uppfærður með yfirvörunni og öllum undirvörum.
9. Fyrir undirvöru, breyttu sjálfgildi **Uppruni sjálfstæðs söluverðs**, **Prósenta af stöðluðu verði yfireiningar**, **Prósenta af reikningsverði yfireiningar**, eða **Úthluta afgangsupphæð** reitum eins og þörf er á.
10. Veldu  **Bæta við vörum** til að bæta við nokkrum vörum í einu.
11. Uppfæra fyrirspurnina til að velja vörusviðið sem á að bæta við.
12. Veldu **Í lagi**, farðu yfir lista yfir vörur sem þú bættir við og veldu **Í lagi**.

### <a name="fields"></a>Svæði

Á síðunni **Stakt söluverð vöru** eru eftirfarandi reitir.

| Svæði | Lýsing |
|-------|-------------|
| Uppruni sjálfstæðs söluverðs | <p>Veljið uppruna sjálfstæðs söluverðs:</p><ul><li>**Upphæð** – Sjálfstætt söluverð er upphæð sem þú tilgreinir að sé hærri en 0 (núll). Upphæðin er umreiknuð á milli virkra og upprunalegra gjaldmiðla eftir þörfum.</li><li>**Grunnsöluverð** – Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar.</li><li>**Reikningsverð** – Sjálfstætt söluverð samsvarar reikningsverði vörunnar.</li><li>**Prósenta vöru** – Sjálfstætt söluverð er tilgreint sem prósentuvirði og er reiknað út frá verði vörunnar. Ef þessi kostur er valinn skal tilgreina sjálfgefna prósentu.</li></ul>**Úthluta afgangsupphæð** – Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsvirði yfirvöru* – *Heildarsamningsvirði undirvöru*:</p><ul><li>*Heildarsamningsvirði yfirvöru* er hrein eða skuldfærð fjárhæð.</li><li>*Heildarsamningsvirði undirvöru* er samtala framlengds eða samningsbundins sjálfstæðs söluverðs allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverð.</li></ul><p>Ef reiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þennan valkost er aðeins hægt að velja fyrir eina undireiningu í tekjuskiptingunni.</p></li><li>**Engin** – Uppruni sjálfstæða söluverðsins byggir á undireiningu. Þessi valkostur á við um hluti sem eru skilgreindir sem yfireiningar í sniðmáti tekjuskiptingar. Ef gátreiturinn fyrir **Tekjuskipting** er valinn er þessi valkostur valinn sjálfkrafa og ekki er hægt að breyta stillingunni.</li><li>**Prósenta af reikningsverði yfireiningar** – Uppruni sjálfstæðs söluverðs er prósenta af reikningsverði yfirvörunnar. Hægt er að breyta sjálfgefna gildinu. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar.</li><li>**Prósenta af stöðluðu verði yfireiningar** – Uppruni sjálfstæðs söluverðs er prósenta af venjulegu verði yfirvörunnar. Hægt er að breyta sjálfgefna gildinu. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar. Það er sjálfgefni valkosturinn fyrir undireiningar. Þegr valkostinum fyrir undiratriði er breytt úr **Prósenta af stöðluðu verði yfireiningar** í **Prósenta af reikningsverði yfireiningar**, eða úr **Prósenta af reikningsverði yfireiningar** í **Prósenta af stöðluðu verði yfireiningar**, eru útreiknuðu gildi einnig uppfærð.</li></ul> |
| Sjálfstætt söluverð | Tilgreina sjálfstætt söluverð vörunnar. Þetta svæði er tiltækt þegar **Uppruni sjálfstæðs söluverðs** er stillt á **Upphæð**. |
| Prósenta | Tilgreiniið prósentu sjálfstæðs söluverðs. Reiturinn er í boði þegar reiturinn **Uppruni sjálfstæðs söluverðs** er stilltur á **Prósenta vöru**, **Prósenta af reikningsverði yfireiningar** eða **Prósenta af stöðluðu verði yfireiningar**. |
| Tekjuskipting | <p>Tilgreina hvort lína noti tekjuskiptingu:</p><ul><li>**Valið** – Aðeins er hægt að velja vörur þar sem sniðmát fyrir tekjuskiptingu hafa verið sett upp fyrir í reitnum **Vöruvensl**. Gátreitinn er aðeins hægt að velja fyrir yfirvörur með sniðmáti tekjuskiptingar.</li><li>**Hreinsað** – Varan er stöðluð vara sem notar ekki tekjuskiptingu.</li></ul> |
| Vensl | Táknið gefur til kynna hvort varan er yfirvara eða undirvara í tekjuskiptingu. |
| Vörukóði | <p>Velja vörukóða: **Tafla** eða **Flokkur**.</p><p>Ef gátreiturinn **Tekjuskipting** er valinn er reiturinn stilltur á **Tafla** og ekki er hægt að breyta gildinu.</p> |
| Vöruvensl | <p>Veldu vörunúmer.</p><p>Ef gátreiturinn **Tekjuskipting** er valinn eru aðeins vörur sem eru yfirvörur með uppsett sniðmát fyrir tekjuskiptingu tiltækir fyrir val. Þegar yfirvaran er valin er listinn uppfærður sjálfkrafa með undireiningum hennar.</p> |
| Yfirvara | Fyrir yfirvörunna, í þessum reit birtist vörunúmerið. Fyrir undireiningar í tekjuskiptingu sýnir þetta vörunúmer yfirvörunnar. |

## <a name="mea-templates"></a>MEA sniðmát

Nota síðuna **MEA sniðmát** til að búa til og breyta kennum MEA-sniðmáta. Þessi kenni eru notuð á síðunni **Tekjuúthlutun** til að raða saman vörum.

### <a name="create-a-template"></a>Sniðmát stofnað

Til að setja upp MEA-sniðmát skal fylgja þessum skrefum:

1. Á síðunni **MEA sniðmát** skal velja **Nýtt**.
1. Í reitnum **MEA sniðmátsauðkenni** er fært inn einkvæmt kenni.
1. Í reitnum **Lýsing** skal færa inn lýsingu.
1. Í **Tekjulykill frestaðs samnings** reitinum veldu reikninginn sem á að nota fyrir dagbókarfærslur þegar MEA samningsreikningur er stofnaður. Þetta svæði er í boði fyrir endurtekin greiðsluáætlun samnings er virkjuð og notuð.
1. Veldu **Vista**.
