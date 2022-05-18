---
title: Úthlutun tekna
description: Þetta efni útskýrir hvernig á að nota tekjuúthlutun í áskriftarreikningi.
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
ms.openlocfilehash: 09d3e9295f1fb753156aa603b00372316173721e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695247"
---
# <a name="revenue-allocation"></a>Úthlutun tekna

Þetta efnisatriði útskýrir hvernig á að setja upp tekjuúthlutunarfæribreytur fyrir innheimtuáætlun. Þú getur sett upp eða breytt tekjuúthlutun þegar þú býrð til innheimtuáætlunina. Þegar þú opnar **Tekjuskipting** síðu fyrir virka eða hætt innheimtuáætlun, eru reitirnir skrifvarinn.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Tilgreindu tekjuúthlutun fyrir innheimtuáætlun

Til að tilgreina tekjuúthlutun fyrir innheimtuáætlun skaltu fylgja þessum skrefum.

1. Á **Allar/virkar innheimtuáætlanir** listasíðu, veldu innheimtuáætlun eða innheimtuáætlunarlínu.
2. Á **Tekjuskipting** flipann efst á síðunni, veldu **Tekjuskipting**.
3. Í **Gerð margfeldis fyrirkomulags** reit, veldu tegund margfeldisfyrirkomulags (MEA).
4. Í **Fyrirkomulagsnúmer margra þátta** reit, tilgreinið MEA númerið. Þá, í **Frestaða samningstekjureikningur** reit, tilgreinið frestað samningstekjureikning.

    Ef þú stillir **Gerð margfeldis fyrirkomulags** sviði til **Einhleypur**, það sama **Fyrirkomulagsnúmer margra þátta** og **Frestaða samningstekjureikningur** gildi gilda fyrir hverja línu. Ef þú stillir **Fyrirkomulag margfeldisþátta** sviði til **Margfeldi**, þú getur tilgreint mismunandi **Fyrirkomulagsnúmer margra þátta** og **Frestaða samningstekjureikningur** gildi fyrir hverja línu.
    
    Aðeins er hægt að úthluta MEA númeri á tvo eða fleiri hluti. Ein lína getur ekki haft sitt eigið MEA númer.

5. Veldu **Vista**.

### <a name="fields"></a>Svæði

The **Fyrirkomulag margra þátta** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|---|---| 
| Gerð margþátta ráðstöfunar | <p>Veldu MEA tegund fyrir færsluna:</p><ul><li>**Margfeldi** – Línuatriðin í viðskiptunum eru hluti af MEA, eða fleiri en eitt fyrirkomulag er til.</li><li>**Enginn** – Færslan er staðlað viðskipti sem hafa enga tekjuskiptingu.</li><li>**Einhleypur** - Allir hlutir í viðskiptunum eru hluti af einni MEA.</li></ul> |
| Númer margþátta ráðstöfunar | <p>MEA númerið fyrir línuna. Þessi reitur er tiltækur þegar **Gerð margfeldis fyrirkomulags** reiturinn er stilltur á **Margfeldi**.</p><p>Ef þessi reitur er auður og þú úthlutar MEA númeri, **Sjálfstætt söluverð uppruna** og **Sjálfstætt söluverð** reitirnir eru sjálfkrafa uppfærðir út frá gildunum frá **Vara sjálfstætt söluverð** síðu. Aðeins MEA númerin sem eru úthlutað öðrum línum í sölupöntuninni eru tiltæk.</p> |
| Tekjulykill frestaðs samnings | Tilgreindu reikninginn sem á að nota fyrir dagbókarfærslur þegar MEA samningsreikningur er stofnaður. Þessi reitur er aðeins tiltækur þegar endurtekinn samningsreikningur er notaður. |
| **Línur** | |
| Númer vöruvíddasamsetningar | Afbrigðisnúmerið úr sölupöntuninni. |
| Vörunúmer | Vörunúmerið úr sölupöntuninni. |
| Greiðslutíðni | Tíðni úthlutunar tekna: **Daglega**, **·**, **·**, **·**, eða **Árlega**. |
| Magn | Gildið frá sölupöntuninni. |
| Samningsvirði | Samningsverðmæti. |
| Númer margþátta ráðstöfunar | <p>MEA númerið fyrir línuna. Þessi reitur er tiltækur þegar **Gerð margfeldis fyrirkomulags** reiturinn er stilltur á **Margfeldi**.</p><p>Ef þessi reitur er auður og þú úthlutar MEA númeri, **Sjálfstætt söluverð uppruna** og **Sjálfstætt söluverð** reitirnir eru sjálfkrafa uppfærðir út frá gildunum frá **Vara sjálfstætt söluverð** síðu. Aðeins MEA númerin sem eru úthlutað öðrum línum í sölupöntuninni eru tiltæk. Ef þessi gildi eru ekki sett upp fyrir hlutinn munu gildin frá **Tekjuúthlutunarfæribreytur margra þátta** síðu eru notuð.</p> | 
| Uppruni sjálfstæðs söluverðs | <p>Uppruni sjálfstæðs söluverðs:</p><ul><li>**Magn** – Sjálfstætt söluverð er upphæð sem þú tilgreinir sem er meira en 0 (núll). Upphæðinni er umreiknað á milli virks gjaldmiðils og upprunagjaldmiðils eftir þörfum.</li><li>**Grunnsöluverð** – Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar.</li><li>**Reikningsverð** – Sjálfstætt söluverð passar við reikningsverð vörunnar.</li><li>**Hlutfall af hlut** – Sjálfstætt söluverð er tilgreint sem prósentugildi og er reiknað út frá verði hlutarins. Ef þessi valkostur er valinn skaltu tilgreina sjálfgefna prósentuna.</li><li>**Úthlutaðu afgangsmagni** – Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsverðmæti yfirliðar* –*Heildar sjálfstætt söluverð á undirvörum*:</p><ul><li>*Heildarsamningsverðmæti yfirliðar* er nettó eða innheimt upphæð.</li><li>*Heildar sjálfstætt söluverð á undirvörum* er summan af framlengdu eða samningslausu söluverði allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverðsuppruna.</li></ul><p>Ef útreiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þessi valkostur er aðeins hægt að velja fyrir einn undirlið í tekjuskiptingu.</p></li><li>**Enginn** – Uppruni sjálfstæða söluverðsins byggist á undirhlutunum. Þessi valkostur á við um vörur sem eru skilgreindar sem yfirvörur í tekjuskiptingarsniðmáti. Ef **Tekjuskipting** gátreiturinn er valinn, þessi valkostur er sjálfkrafa valinn og ekki er hægt að breyta stillingunni.</li><li>**Hlutfall af verði móðurreiknings** – Uppruni sjálfstæðs söluverðs er hlutfall af reikningsverði móðurvöru. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti.</li><li>**Hlutfall af staðalverði foreldra** – Uppruni sjálfstæðs söluverðs er hlutfall af stöðluðu verði móðurvörunnar. Þessi valkostur er aðeins tiltækur fyrir undirvörur í tekjuskiptingarsniðmáti. Þegar valmöguleika fyrir undirhlut er breytt úr **Hlutfall af staðalverði foreldra** til **Hlutfall af verði móðurreiknings**, eða frá **Hlutfall af verði móðurreiknings** til **Hlutfall af staðalverði foreldra**, eru reiknuð gildi einnig uppfærð.</li></ul> |
| Sjálfstætt söluverð | <p>Sjálfstætt söluverð fyrir línuna, í viðskiptagjaldmiðlinum.</p><p>Gildið í **Magn** reiturinn er annaðhvort færður inn eða reiknaður.</p> |
| Stakt söluverð samnings | Samningurinn sjálfstætt söluverð. |
| Eftirstöðvar samningstekna | Eftirstöðvar tekjuupphæðar fyrir samninginn. Þessi upphæð er summa allra lína sem reikningar hafa ekki enn verið stofnaðir fyrir. |
| Samtals samningstekjur | Heildarupphæð samningstekna fyrir línuna. Þessi upphæð er summa allra lína, óháð því hvort reikningar hafa verið búnir til fyrir þær. |
| Tekjulykill frestaðs samnings | <p>Tilgreindu reikninginn sem á að nota fyrir dagbókarfærslur þegar MEA samningsreikningur er stofnaður.</p><p>Þessi reitur er aðeins tiltækur þegar endurtekinn samningsreikningur er notaður.</p> |
| Villa | Allar villur sem komu upp við úthlutun tekna. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Notaðu tekjuúthlutun á sölupöntun

Til að nota tekjuúthlutunaraðgerðina á sölupöntun skal fylgja þessum skrefum.

1. Á **Allar sölupantanir** síðu, búðu til sölupöntun sem inniheldur vörur.
2. Á **Reikningur** flipi, undir **Tekjuskipting**, veldu **Tekjuskipting**.
3. Í **Gerð margfeldis fyrirkomulags** reit, veldu MEA gerð.
4. Í **Fyrirkomulagsnúmer margra þátta** reit, tilgreinið MEA númerið.
5. Ef **Gerð margfeldis fyrirkomulags** reiturinn er stilltur á **Margfeldi**, veldu línurnar sem þú vilt og veldu síðan **Sækja um valið**.
6. Veldu **Vista**.

Ef þú notar frestun tekna og kostnaðar er frestunin sjálfkrafa búin til. Þú getur skoðað það á **Allar frestunaráætlanir** síðu.
