---
title: Úthlutun tekna
description: Í þessari grein er útskýrt hvernig á að nota tekjuúthlutun í Áskriftargreiðslur.
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
ms.openlocfilehash: 18739e0871592bc9eefcdf00f67dd4dd18f5d6f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864369"
---
# <a name="revenue-allocation"></a>Úthlutun tekna

Þessi grein útskýrir hvernig á að setja upp færibreytur fyrir tekjuúthlutun fyrir greiðsluáætlun. Hægt er að setja upp eða breyta tekjuúthlutun þegar greiðsluáætlun er útbúin. Þegar þú opnar síðuna **Tekjuúthlutun** fyrir virka eða lokna greiðsluáætlun eru reitirnir ritvarðir.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Tilgreina tekjuúthlutun fyrir greiðsluáætlun

Til að tilgreina tekjuúthlutun fyrir greiðsluáætlun skal fylgja þessum skrefum.

1. Á **Allar/Virkar greiðsluáætlanir** skal velja greiðsluáætlun eða línu í greiðsluáætlun.
2. Á **Tekjuúthlutun** flipanum efst á síðunni velurðu **Tekjuúthlutun**.
3. Í reitnum **Gerð margþátta ráðstöfunar** vekurðu gerð margþátta fyrirkomulags (MEA).
4. Í **Númer margþátta ráðstöfunar** skal tilgreina MEA-númer. Svo, í reitnum **Tekjulykill frestaðs samnings**, tilgreinið tekjureikning vegna frestaðs samnings.

    Ef reiturinn **Gerð margþátta ráðstöfunar** er stilltur á **Einfalt**, gilda sömu **Númer margþátta ráðstöfunar** og **Tekjulykill frestaðs samnings** gildi fyrir hverja línu. Ef reiturinn **Gerð margþátta ráðstöfunar** er stilltur á **Mörg**, er hægt að tilgreina önnur **Númer margþátta ráðstöfunar** og **Tekjulykill frestaðs samnings** gildi fyrir hverja línu.
    
    Aðeins er hægt að úthluta MEA-númeri á tvo eða fleiri hluti. Ein lína getur ekki haft eigið MEA-númer.

5. Veldu **Vista**.

### <a name="fields"></a>Svæði

Á síðunni **Margþátta fyrirkomulag** eru eftirfarandi reitir.

| Svæði | Lýsing |
|---|---| 
| Gerð margþátta ráðstöfunar | <p>Veljið MEA gerð fyrir færsluna:</p><ul><li>**Mörg** – Línuatriðin á færslunni eru hluti af MEA, eða fleiri en eitt fyrirkomulag er til.</li><li>**Ekkert** – Færslan er hefðbundin færsla með enga tekjuúthlutun.</li><li>**Stakt** – Öll atriðin á færslunni eru hluti af einu MEA.</li></ul> |
| Númer margþátta ráðstöfunar | <p>MEA- númerið fyrir línuna. Þessi reitur er í boði þegar reiturinn **Gerð margþátta ráðstöfunar** er stilltur á **Margar**.</p><p>Ef reiturinn er auður og þú úthlutar MEA-númeri eru reitirnir **Uppruni sjálfstæðs söluverðs** og **Sjálfstætt söluverð** sjálfkrafa uppfærðir miðað við gildin á síðunni **Stakt söluverð vöru**. Aðeins MEA-númer sem er úthlutað á aðrar línur í sölupöntuninni eru tiltæk.</p> |
| Tekjulykill frestaðs samnings | Skilgreindu reikninginn sem á að nota fyrir dagbókarfærslur þegar MEA samningsreikningur er stofnaður. Þetta svæði er aðeins í boði fyrir endurtekin greiðsluáætlun samnings er notuð. |
| **Línur** | |
| Númer vöruvíddasamsetningar | Númer vöruvíddasamsetningar úr sölupöntun. |
| Vörunúmer | Vörunúmer úr sölupöntun. |
| Greiðslutíðni | Tíðnin fyrir tekjuúthlutunina: **Daglega**, **Mánaðarlega**, **Ársfjórðungslega**, **Hálfs árs fresti**, eða **Árlega**. |
| Magn | Gildið úr sölupöntun. |
| Samningsvirði | Samningsgildið. |
| Númer margþátta ráðstöfunar | <p>MEA- númerið fyrir línuna. Þessi reitur er í boði þegar reiturinn **Gerð margþátta ráðstöfunar** er stilltur á **Margar**.</p><p>Ef reiturinn er auður og þú úthlutar MEA-númeri eru reitirnir **Uppruni sjálfstæðs söluverðs** og **Sjálfstætt söluverð** sjálfkrafa uppfærðir miðað við gildin á síðunni **Stakt söluverð vöru**. Aðeins MEA-númer sem er úthlutað á aðrar línur í sölupöntuninni eru tiltæk. Ef þessi gildi eru ekki sett upp fyrir vöruna eru gildin á síðunni **Margar færibreytur fyrir tekjuúthlutunarþátt** notuð.</p> | 
| Uppruni sjálfstæðs söluverðs | <p>Uppruni sjálfstæðs söluverðs:</p><ul><li>**Upphæð** – Sjálfstætt söluverð er upphæð sem þú tilgreinir að sé hærri en 0 (núll). Upphæðin er umreiknuð á milli virkra og upprunalegra gjaldmiðla eftir þörfum.</li><li>**Grunnsöluverð** – Sjálfstætt söluverð samsvarar grunnsöluverði vörunnar.</li><li>**Reikningsverð** – Sjálfstætt söluverð samsvarar reikningsverði vörunnar.</li><li>**Prósenta vöru** – Sjálfstætt söluverð er tilgreint sem prósentuvirði og er reiknað út frá verði vörunnar. Ef þessi möguleiki er valinn skal tilgreina sjálfgefna prósentu.</li><li>**Úthluta afgangsupphæð** – Uppruni sjálfstæðs söluverðs er reiknaður sem *Heildarsamningsvirði yfirvöru* – *Heildarsamningsvirði undirvöru*:</p><ul><li>*Heildarsamningsvirði yfirvöru* er hrein eða skuldfærð fjárhæð.</li><li>*Heildarsamningsvirði undirvöru* er samtala framlengds eða samningsbundins sjálfstæðs söluverðs allra undirvara, nema undirvörunnar sem notar þetta sjálfstæða söluverð.</li></ul><p>Ef reiknuð upphæð er neikvætt gildi er upphæðin stillt á 0 (núll).</p><p>**Athugið:** Þennan valkost er aðeins hægt að velja fyrir eina undireiningu í tekjuskiptingunni.</p></li><li>**Engin** – Uppruni sjálfstæða söluverðsins byggir á undireiningu. Þessi valkostur á við um hluti sem eru skilgreindir sem yfireiningar í sniðmáti tekjuskiptingar. Ef gátreiturinn fyrir **Tekjuskipting** er valinn er þessi valkostur valinn sjálfkrafa og ekki er hægt að breyta stillingunni.</li><li>**Prósenta af reikningsverði yfireiningar** – Uppruni sjálfstæðs söluverðs er prósenta af reikningsverði yfirvörunnar. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar.</li><li>**Prósenta af stöðluðu verði yfireiningar** – Uppruni sjálfstæðs söluverðs er prósenta af venjulegu verði yfirvörunnar. Þessi valkostur er aðeins í boði fyrir yfirvörur í sniðmáti tekjuskiptingar. Þegr valkostinum fyrir undiratriði er breytt úr **Prósenta af stöðluðu verði yfireiningar** í **Prósenta af reikningsverði yfireiningar**, eða úr **Prósenta af reikningsverði yfireiningar** í **Prósenta af stöðluðu verði yfireiningar**, eru útreiknuðu gildi einnig uppfærð.</li></ul> |
| Sjálfstætt söluverð | <p>Sjálfstæða söluverðið fyrir línuna, í færslugjaldmiðlinum</p><p>Gildið í reitnum **Upphæð** er annað hvort skráð eða reiknað.</p> |
| Stakt söluverð samnings | Sjálfstætt söluverð samnings. |
| Eftirstöðvar samningstekna | Tekjuafgangsupphæð samningsins. Þessi upphæð er samtala allra lína sem reikningar hafa ekki enn verið stofnaðir fyrir. |
| Samtals samningstekjur | Tekjuupphæð samnings alls fyrir línuna. Þessi upphæð er samtala allra lína, óháð því hvort reikningar hafi verið stofnaðir fyrir þær. |
| Tekjulykill frestaðs samnings | <p>Skilgreindu reikninginn sem á að nota fyrir dagbókarfærslur þegar MEA samningsreikningur er stofnaður.</p><p>Þetta svæði er aðeins í boði fyrir endurtekin greiðsluáætlun samnings er notuð.</p> |
| Villa | Allar villur sem komu upp við tekjuúthlutunina. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Nota tekjuúthlutun á sölupöntun

Til að nota virkni tekjuúthlutun á sölupöntun skal fylgja þessum skrefum.

1. Stofnið sölupöntun með vörum á síðunni **Allar sölupantanir**.
2. Á flipanum **Reikningur**, undir **Tekjuúthlutun**, skal velja **Tekjuúthlutun**.
3. Í reitnum **Gerð margþátta ráðstöfunar** velurðu MEA-gerð.
4. Í **Númer margþátta ráðstöfunar** skal tilgreina MEA-númer.
5. Ef reiturinn fyrir **Gerð margþátta ráðstöfunar** er stilltur á **Margar**, veldu línurnar sem þú vilt og veldu svo línurnar **Nota á valið**.
6. Veldu **Vista**.

Ef þú notar tekju- og kostnaðarfrestanir er frestunaráætlunin stofnuð sjálfkrafa. Hægt er að skoða það á síðunni **Allar frestunaráætlanir**.
