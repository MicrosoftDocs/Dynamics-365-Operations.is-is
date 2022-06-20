---
title: Setja upp margþátta tekjuúthlutun
description: Þessi grein lýsir því hvernig á að setja upp færibreytur fyrir tekjuúthlutun margra þátta í áskriftarreikningi.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903306"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Setja upp margþátta tekjuúthlutun

Tekjuúthlutun margra þátta gerir þér kleift að setja upp mismunandi sniðmát sem eru notuð til að reikna út og úthluta tekjum á marga hluti. Þessi virkni getur hjálpað þér að uppfylla reikningsskilastaðla Codification Topic 606 (ASC 606) og/eða International Financial Reporting Standard 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Margar færibreytur fyrir tekjuúthlutunarþátt

Nota **Tekjuúthlutunarfæribreytur margra þátta** síðu til að setja upp færibreytur fyrir tekjuúthlutun margra þátta.

### <a name="standalone-selling-price-origin"></a>Uppruni sjálfstæðs söluverðs

The **Sjálfstætt söluverð uppruna** reit ákvarðar hvaðan sjálfstæða söluverðið kemur. Þú getur uppfært gildið á **Vara sjálfstætt söluverð** síðu og á viðskiptunum. Eftirtaldir valkostir eru í boði.

| Valkostur | Lýsing |
|--------|-------------|
| Upphæð | Sjálfstætt söluverð er upphæð sem þú tilgreinir sem er meira en 0 (núll). Upphæðinni er umreiknað á milli virks gjaldmiðils og upprunagjaldmiðils eftir þörfum. |
| Grunnsöluverð | Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar. |
| Reikningsverð | Sjálfstætt söluverð passar við reikningsverð vörunnar. |
| Prósenta vöru | Sjálfstætt söluverð er tilgreint sem prósentugildi og er reiknað út frá verði hlutarins. Ef þú velur þennan valkost skaltu tilgreina sjálfgefna prósentuna. |
| Úthluta afgangsupphæð | <p>Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsverðmæti yfirliðar* –*Heildar sjálfstætt söluverð á undirvörum*:</p><ul><li>*Heildarsamningsverðmæti yfirliðar* er nettó eða innheimt upphæð.</li><li>*Heildar sjálfstætt söluverð á undirvörum* er summan af framlengdu eða samningslausu söluverði allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverðsuppruna.</li></ul><p>Ef útreiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þessi valkostur er aðeins hægt að velja fyrir einn undirlið í tekjuskiptingu.</p> |
| Ekkert | Uppruni sjálfstæða söluverðsins byggist á undirhlutunum. Þessi valkostur á við um vörur sem eru skilgreindar sem yfirvörur í tekjuskiptingarsniðmáti. Ef **Tekjuskipting** gátreiturinn er valinn, þessi valkostur er sjálfkrafa valinn og ekki er hægt að breyta stillingunni. |
| Prósenta af reikningsverði yfireiningar | Uppruni sjálfstæða söluverðsins er hlutfall af reikningsverði móðurvörunnar. Þú getur breytt sjálfgefna gildinu. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti. |
| Prósenta af stöðluðu verði yfireiningar | Uppruni sjálfstæðs söluverðs er hundraðshluti af stöðluðu verði móðurvörunnar. Þú getur breytt sjálfgefna gildinu. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti. Það er sjálfgefinn valkostur fyrir undirhluti. Þegar valmöguleika fyrir undirhlut er breytt úr **Hlutfall af staðalverði foreldra** til **Hlutfall af verði móðurreiknings**, eða frá **Hlutfall af verði móðurreiknings** til **Hlutfall af staðalverði foreldra**, eru reiknuð gildi einnig uppfærð. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Lykill fyrir sléttunarmismun tekjuúthlutunar

The **Gerðu grein fyrir námundunarmun á tekjuúthlutun** reiturinn tilgreinir reikninginn sem er notaður til að skrá allar sléttunarleiðréttingar á samningstekjuupphæð. Það er tiltækt þegar endurtekinn samningsreikningur er notaður.

## <a name="item-standalone-selling-price"></a>Stakt söluverð vöru

Nota **Vara sjálfstætt söluverð** síðu til að tilgreina uppruna og sjálfstætt söluverð vöru. Gildin sem eru tilgreind á þessari síðu eru notuð sem sjálfgefin gildi á **Tekjuskipting** síðu í tekjuúthlutun margra þátta og endurteknum samningsreikningum.

### <a name="specify-item-standalone-selling-price"></a>Tilgreindu sjálfstætt söluverð vöru

Til að tilgreina sjálfstætt verð fyrir vöru skaltu fylgja þessum skrefum.

1. Á **Vara sjálfstætt söluverð** síðu, í **Sjálfstætt söluverð uppruna** reit, veldu uppruna sjálfstæða söluverðsins.
2. Fylgdu einu af þessum skrefum, allt eftir gildinu sem þú valdir í **Sjálfstætt söluverð uppruna** reit:

    * Ef þú valdir **Hlutfall af hlut**, tilgreindu prósentuna í **Prósenta** sviði.
    * Ef þú valdir **Magn**, tilgreindu upphæðina í **Sjálfstætt söluverð** sviði.

2. Veldu fyrir hvert atriði sem þú vilt bæta við listann **Bæta við**.
3. Í **Vörukóði** reit, veldu vörukóðann. Í **Atriðatengsl** reit, veldu hluttengsl. Fyrir hluti þar sem **Tekjuskipting** gátreiturinn er hreinsaður, valin samsetning vörukóða og vörutengsla verður að vera einstök.
4. Breyttu sjálfgefna gildinu á **Sjálfstætt söluverð uppruna**, **söluverð**, eða **Prósenta** reit eins og þú þarfnast.
5. Veldu fyrir hvert yfirlið sem þú vilt bæta við listann **Bæta við**.
6. Í **Vörukóði** reit, veldu vörukóðann. Í **Atriðatengsl** reit, veldu hluttengsl.
7. Veldu **Tekjuskipting** gátreit.
8. Í **Atriðatengsl** reit, veldu hluttengsl. Listinn er uppfærður með yfirliðinu og öllum undirliðum.
9. Breyttu sjálfgefna gildinu fyrir undirhlutinn **Sjálfstætt söluverð uppruna**, **af staðalverði foreldra**, **af verði móðurreiknings**, eða **Úthlutaðu afgangsmagni** reit eins og þú þarfnast.
10. Til að bæta við nokkrum hlutum í einu velurðu **Bæta við hlutum**.
11. Uppfærðu fyrirspurnina til að velja úrval af atriðum sem þú vilt bæta við.
12. Veldu **Allt í lagi**, skoðaðu listann yfir atriði sem þú bættir við og veldu **Allt í lagi**.

### <a name="fields"></a>Svæði

The **Vara sjálfstætt söluverð** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------|
| Uppruni sjálfstæðs söluverðs | <p>Veldu uppruna sjálfstæða söluverðsins:</p><ul><li>**Magn** – Sjálfstætt söluverð er upphæð sem þú tilgreinir sem er meira en 0 (núll). Upphæðinni er umreiknað á milli virks gjaldmiðils og upprunagjaldmiðils eftir þörfum.</li><li>**Grunnsöluverð** – Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar.</li><li>**Reikningsverð** – Sjálfstætt söluverð passar við reikningsverð vörunnar.</li><li>**Hlutfall af hlut** – Sjálfstætt söluverð er tilgreint sem prósentugildi og er reiknað út frá verði vörunnar. Ef þú velur þennan valkost skaltu tilgreina sjálfgefna prósentuna.</li></ul>**Úthlutaðu afgangsmagni** – Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsverðmæti yfirliðar* –*Heildar sjálfstætt söluverð á undirvörum*:</p><ul><li>*Heildarsamningsverðmæti yfirliðar* er nettó eða innheimt upphæð.</li><li>*Heildar sjálfstætt söluverð á undirvörum* er summan af framlengdu eða samningslausu söluverði allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverðsuppruna.</li></ul><p>Ef útreiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þessi valkostur er aðeins hægt að velja fyrir einn undirlið í tekjuskiptingu.</p></li><li>**Enginn** – Uppruni sjálfstæða söluverðsins byggist á undirhlutunum. Þessi valkostur á við um vörur sem eru skilgreindar sem yfirvörur í tekjuskiptingarsniðmáti. Ef **Tekjuskipting** gátreiturinn er valinn, þessi valkostur er sjálfkrafa valinn og ekki er hægt að breyta stillingunni.</li><li>**Hlutfall af verði móðurreiknings** – Uppruni sjálfstæðs söluverðs er hlutfall af reikningsverði móðurvöru. Þú getur breytt sjálfgefna gildinu. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti.</li><li>**Hlutfall af staðalverði foreldra** – Uppruni sjálfstæðs söluverðs er hlutfall af stöðluðu verði móðurvörunnar. Þú getur breytt sjálfgefna gildinu. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti. Það er sjálfgefinn valkostur fyrir undirhluti. Þegar valmöguleika fyrir undirhlut er breytt úr **Hlutfall af staðalverði foreldra** til **Hlutfall af verði móðurreiknings**, eða frá **Hlutfall af verði móðurreiknings** til **Hlutfall af staðalverði foreldra**, eru reiknuð gildi einnig uppfærð.</li></ul> |
| Sjálfstætt söluverð | Tilgreindu sjálfstætt söluverð vörunnar. Þessi reitur er tiltækur þegar **Sjálfstætt söluverð uppruna** reiturinn er stilltur á **Magn**. |
| Prósenta | Tilgreindu hlutfall af sjálfstæðu söluverði. Þessi reitur er tiltækur þegar **Sjálfstætt söluverð uppruna** reiturinn er stilltur á **Hlutfall af hlut**, **af verði móðurreiknings**, eða **Hlutfall af stöðluðu verði foreldra**. |
| Tekjuskipting | <p>Tilgreindu hvort lína notar tekjuskiptingu:</p><ul><li>**Valið** – Aðeins er hægt að velja hluti sem sniðmát fyrir tekjuskiptingu er sett upp fyrir í **Atriðatengsl** sviði. Þú getur aðeins valið þennan gátreit fyrir yfirliði sniðmáts fyrir skiptingu tekna.</li><li>**Hreinsað** – Liðurinn er staðall liður sem notar ekki tekjuskiptingu.</li></ul> |
| Vensl | Tákn gefur til kynna hvort varan sé yfir- eða undirliður í tekjuskiptingu. |
| Vörukóði | <p>Veldu vörukóða: **Tafla** eða **Hópur**.</p><p>Ef **Tekjuskipting** gátreiturinn er valinn, þessi reitur er stilltur á **Tafla**, og ekki er hægt að breyta gildinu.</p> |
| Vöruvensl | <p>Veldu vörunúmer.</p><p>Ef **Tekjuskipting** gátreiturinn er valinn, aðeins hlutir sem eru yfirvörur sem sniðmát fyrir tekjuskiptingu er sett upp fyrir eru tiltækar fyrir val. Þegar yfirliðið er valið er listinn sjálfkrafa uppfærður með undirliðum þess yfirliðs.</p> |
| Yfirvara | Fyrir yfirvöruna sýnir þessi reitur vörunúmerið. Fyrir undirliði í tekjuskiptingu sýnir það vörunúmer yfirliðsins. |

## <a name="mea-templates"></a>MEA sniðmát

Nota **MEA sniðmát** síðu til að búa til og breyta MEA-sniðmátaauðkennum. Þessi auðkenni eru notuð á **Tekjuskipting** síðu til að flokka hluti saman.

### <a name="create-a-template"></a>Sniðmát stofnað

Til að setja upp MEA sniðmát skaltu fylgja þessum skrefum.

1. Á **MEA sniðmát** síðu, veldu **Nýtt**.
1. Í **Auðkenni MEA sniðmáts** reit, sláðu inn einstakt auðkenni.
1. Í reitnum **Lýsing** skal færa inn lýsingu.
1. Í **Frestaða samningstekjureikningur** reit, veldu reikninginn sem þú vilt nota fyrir færslubókarfærslur þegar MEA samningsreikningur er stofnaður. Þessi reitur er tiltækur þegar endurtekinn samningsreikningur er virkjaður og notaður.
1. Veldu **Vista**.
