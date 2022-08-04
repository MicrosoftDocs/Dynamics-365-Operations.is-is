---
title: Yfirlit viðbótar fyrir sýnileika birgða
description: Þessi grein útskýrir hvað birgðasýnileiki er og lýsir eiginleikum þess.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066641"
---
# <a name="inventory-visibility-add-in-overview"></a>Yfirlit viðbótar fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]

Birgðasýnileikaviðbótin (einnig nefnd *Birgðasýnileikaþjónusta*) býður upp á óháða og mjög stigstærða örþjónustu sem gerir rauntíma birgðabreytingafærslum og sýnileikarakningu í öllum gagnaveitum þínum og rásum kleift. Það býður upp á vettvang sem gerir þér kleift að stjórna alþjóðlegum birgðum þínum með því að nota virkni sem inniheldur (en takmarkast ekki við) eftirfarandi lista:

- Fylgstu miðlægt með nýjustu birgðastöðu (eins og tiltæk, pantað, keypt, í flutningi, skilað og í sóttkví) yfir allar gagnaveitur þínar, vöruhús og staðsetningar með því að tengja birgðakeðjustjórnun þína eða flutningagagnaveitur þriðja aðila ( svo sem pöntunarstjórnunarkerfi, þriðja aðila áætlanagerð fyrirtækja\[ ERP\] kerfi, sölustaður\[ POS\] kerfi og vöruhúsastjórnunarkerfi) til birgðasýnileikaþjónustunnar.
- Spurðu um framboð á lager og skort og fáðu strax svör með því að hringja beint í birgðasýnileikaþjónustuna.
- Forðastu ofsölu, sérstaklega þegar eftirspurn þín kemur frá mismunandi rásum, með því að gera mjúkar pantanir í rauntíma í birgðasýnileikaþjónustunni.
- Stýrðu lofuðum pöntunum og væntingum viðskiptavina betur með því að gefa upp nákvæmar dagsetningar sem eru í boði eða næst, þannig að aðgerðin umnichannel available-to-promise (ATP) geti reiknað út væntanlegar pöntunardagsetningar.

## <a name="extensibility"></a>Stækkunarhæfni

Birgðasýnileiki þjónustan er mjög stækkanleg vegna þess að inntak og úttak gagna er ekki bundið við Microsoft forrit. Ytri kerfi geta nálgast þjónustuna í gegnum RESTful forritunarviðmót (API). Auk þess að nota út-af-kassa vörpunum sem eru veittar fyrir Supply Chain Management gagnagjafa og víddir, geturðu samþætt birgðasýnileika við mörg þriðja aðila kerfi með því að setja upp viðbótar gagnagjafa, mælingar á birgðastöðu (vísað til sem *líkamlegar ráðstafanir* í birgðasýnileikaþjónustu), og birgðavíddir í gegnum stillingarforritið. Á þennan hátt geturðu á sveigjanlegan hátt spurt og breytt mörgum gagnaveitum þínum og fyrirfram skilgreindum birgðavíddum.

Þar að auki, vegna þess að birgðasýnileiki er byggður á Microsoft Dataverse, gögn þess er hægt að nota til að byggja upp og samþætta við Power Apps. Þú getur líka notað Power BI til að búa til sérsniðin mælaborð sem uppfylla kröfur fyrirtækisins.

## <a name="scalability"></a>Skalanleiki

Hægt er að stækka birgðasýnileikaþjónustuna upp eða niður, allt eftir gagnamagni þínu. Stækkunarupplifunin er að mestu óaðfinnanleg og er framkvæmd af Microsoft vettvangsteyminu, byggt á sjálfvirkri uppgötvun og mati á magni viðskiptagagna þinna.

## <a name="feature-highlights"></a>Helstu atriði eiginleika

### <a name="get-a-global-view-of-real-time-inventory"></a>Fáðu heildarsýn yfir rauntíma birgðahald

Birgðasýnileiki tryggir að þú hafir aðgang að nýjustu birgðamagninu hverju sinni, á öllum rásum þínum, staðsetningum og vöruhúsum. Þú munt hagnast mest á því að nota það til að styðja við daglega rekstur þinn hvenær sem þú verður að fá birgðaskrár. Raunverulegar lagerbirgðir, selt magn og keypt magn er allt tiltækt úr kassanum. Þú getur líka stillt aðrar efnislegar birgðaráðstafanir (svo sem skilað, sett í sóttkví og sett gögn) eftir þörfum til að fá þessar upplýsingar í rauntíma. Birgðasýnileiki getur á skilvirkan hátt unnið úr milljónum birgðabreytingastaða. Þessum gögnum er hægt að safna saman og endurspeglast í nýjasta birgðamagninu í þjónustunni strax, á sekúndu eða á mínútu, allt eftir því á hvaða bili gögnin eru birt. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Mjúk fyrirvara til að forðast ofsölu á öllum pöntunarrásum

A *mjúkur fyrirvari* gerir þér kleift að úthluta eða merkja tiltekið magn til að uppfylla pöntun eða eftirspurn. Mjúkur frágangur hefur ekki áhrif á vörubirgðir, en hann dregur þó frá *hægt að panta* birgðamagn og veitir uppfært magn fyrir framtíðaruppfyllingu pöntunar. Þessi eiginleiki mun vera gagnlegur ef sölubeiðnir eða pantanir berast inn í fyrirtæki þitt frá einni eða fleiri rásum eða gagnaveitum sem eru utan kerfisskrárkerfis fyrirtækisins (ERP) kerfis.

Ef þú notar ekki mjúkar frátekningar í birgðasýnileikaþjónustunni verður þú að bíða þar til pöntunin er samstillt við og unnin af ERP kerfinu þínu til að fá uppfærslu á efnislegu birgðamagni. Þetta ferli hefur venjulega mikla leynd. Hins vegar taka mjúkar frátekningar strax gildi í hvert skipti sem sölubeiðni eða pöntun er mynduð í sölurásum þínum. Þess vegna hjálpa þeir til við að koma í veg fyrir ofsöluaðstæður með því að tryggja að umnichannel pantanir þínar trufli ekki hver aðra þegar þær að lokum ná ERP kerfinu. Mjúkar bókanir tryggja einnig að þú getir uppfyllt allar pantanir sem þú hefur lofað. Þess vegna hjálpa þeir þér að uppfylla væntingar viðskiptavina og viðhalda hollustu viðskiptavina. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Tafarlaust svar staðfestingar á ATP dagsetningum

Sýnileiki á áætluðum birgðum þínum í náinni framtíð (þar á meðal framboð, eftirspurn og áætlaðar upplýsingar um höndina) er mikilvægt, vegna þess að það hjálpar fyrirtækinu þínu að ná eftirfarandi markmiðum:

- Lágmarka birgðastig til að draga úr birgðastjórnunarkostnaði.
- Auðvelda innri pöntunarvinnslu, þannig að sölumenn geti reiknað út sendingar- og afhendingardagsetningar, byggt á framboði á vörum sem pantaðar eru.
- Veittu gagnsæi um hvenær viðskiptavinir geta búist við að vara sem er ekki til á lager verði fáanleg, með því að gefa upp næsta dagsetningu.

ATP eiginleikann er auðvelt að samþykkja í daglegu pöntunarferlinu þínu. Mikilvægast er, eins og önnur tilboð á birgðasýnileika, ATP eiginleikinn er það *alheims og rauntíma*. Þess vegna geturðu sett upp margar ATP útreikningsformúlur til að hafa allar fyrirspurnir um framboð á birgðum sem ná yfir allar viðskiptarásir þínar og gagnaveitur. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>Samhæfni við vöruhússtjórnunarferli (WMS) hluti

Microsoft stefnir að því að bjóða upp á samþættingu úr kassanum við vöruhússtjórnunarferli (WMS), svo að viðskiptavinir WMS geti einnig notið ávinningsins af birgðasýnileikaþjónustunni. Samkvæmt 2022 Wave 1 útgáfunni (opinber forskoðun í mars), styður birgðaþjónustan WMS vörufyrirspurnir og ATP. Mjúkur pöntunar- og úthlutunareiginleikinn verður studdur fyrir WMS viðskiptavini í næstu bylgju. Fyrir frekari upplýsingar, sjá [Stuðningur við birgðasýnileika fyrir WMS hluti](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Leyfisveiting

Birgðasýnileiki þjónustan er fáanleg í eftirfarandi útgáfum:

- **Birgðasýnileikaviðbót fyrir Microsoft Dynamics 365 Supply Chain Management** – Fyrir fyrirtæki sem hafa gilt leyfi fyrir birgðakeðjustjórnun er birgðasýnileiki fáanlegur án aukaleyfiskostnaðar. Þú getur byrjað að prófa það í dag. Fyrir upplýsingar um uppsetningu, sjá [Settu upp og settu upp Birgðasýnileika](inventory-visibility-setup.md).
- **Birgðasýnileikaþjónusta sem hluti af IOM** – Þessi útgáfa er annað hvort fyrir Intelligent Order Management (IOM) viðskiptavini eða fyrirtæki sem nota ekki Supply Chain Management sem ERP kerfi sitt. Leyfið er innifalið í IOM pakkanum. Fyrir frekari upplýsingar, sjá [Greindur pöntunarstjórnun yfirlit](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
