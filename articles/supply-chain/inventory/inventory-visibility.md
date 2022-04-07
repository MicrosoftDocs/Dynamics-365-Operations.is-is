---
title: Yfirlit viðbótar fyrir sýnileika birgða
description: Í þessu efnisatriði er útskýrt hvað birgðasýnileiki er og eiginleikum hans er lýst.
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
ms.openlocfilehash: 9ee6229937ea27adf231dcd1c9921878e53bd981
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524494"
---
# <a name="inventory-visibility-add-in-overview"></a>Yfirlit viðbótar fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]

Birgðasýnileikaviðbótin (einnig nefnd *Birgðasýnileikaþjónusta*) býður upp á óháða og mjög stigstærða örþjónustu sem gerir rauntíma birgðabreytingafærslum kleift og sýnileikarakningu á öllum gagnaveitum þínum og rásum. Það býður upp á vettvang sem gerir þér kleift að stjórna alþjóðlegum birgðum þínum með því að nota virkni sem inniheldur (en takmarkast ekki við) eftirfarandi lista:

- Fylgstu miðlægt með nýjustu birgðastöðunni (eins og tiltæk, pantað, keypt, í flutningi, skilað og í sóttkví) yfir allar gagnaveitur þínar, vöruhús og staðsetningar með því að tengja birgðakeðjustjórnun þína eða flutningagagnaveitur þriðja aðila ( svo sem pöntunarstjórnunarkerfi, þriðja aðila áætlanagerð fyrirtækja\[ ERP\] kerfi, sölustaður\[ POS\] kerfi og vöruhúsastjórnunarkerfi) til birgðasýnileikaþjónustunnar.
- Leitaðu að framboði á lager og skorti og fáðu strax svör með því að hringja beint í birgðasýnileikaþjónustuna.
- Forðastu ofsölu, sérstaklega þegar eftirspurn þín kemur frá mismunandi rásum, með því að gera mjúkar pantanir í rauntíma í birgðasýnileikaþjónustunni.
- Stýrðu betur lofuðum pöntunum og væntingum viðskiptavina með því að gefa upp nákvæmar dagsetningar sem eru tiltækar á næstunni, þannig að aðgerðin umnichannel available-to-promise (ATP) geti reiknað út væntanlegar pöntunardagsetningar.

## <a name="extensibility"></a>Stækkunarhæfni

Birgðasýnileiki þjónustan er mjög stækkanleg vegna þess að inntak og úttak gagna er ekki bundið við Microsoft forrit. Ytri kerfi geta nálgast þjónustuna í gegnum RESTful forritunarviðmót (API). Auk þess að nota út-af-kassa kortlagningar sem eru veittar fyrir gagnagjafa og víddir Supply Chain Management, geturðu samþætt birgðasýnileika við mörg þriðja aðila kerfi með því að setja upp viðbótargagnagjafa, mælikvarða á birgðastöðu (vísað til sem *líkamlegar ráðstafanir* í birgðasýnileikaþjónustu), og birgðavíddir í gegnum stillingarforritið. Á þennan hátt geturðu á sveigjanlegan hátt spurt og breytt mörgum gagnaveitum þínum og fyrirfram skilgreindum birgðavíddum.

Auk þess vegna þess að birgðasýnileiki er byggður á Microsoft Dataverse, gögn þess er hægt að nota til að byggja upp og samþætta við Power Apps. Þú getur líka notað Power BI til að búa til sérsniðin mælaborð sem uppfylla kröfur fyrirtækisins.

## <a name="scalability"></a>Skalanleiki

Hægt er að stækka birgðasýnileikaþjónustuna upp eða niður, allt eftir gagnamagni þínu. Stækkunarupplifunin er að mestu óaðfinnanleg og er framkvæmd af Microsoft vettvangsteyminu, byggt á sjálfvirkri uppgötvun og mati á magni viðskiptagagna þinna.

## <a name="feature-highlights"></a>Helstu atriði eiginleika

### <a name="get-a-global-view-of-real-time-inventory"></a>Fáðu heildarsýn yfir rauntíma birgðahald

Birgðasýnileiki tryggir að þú hafir aðgang að nýjustu birgðamagninu hverju sinni, á öllum rásum þínum, staðsetningum og vöruhúsum. Þú munt hagnast mest á því að nota það til að styðja við daglegan rekstur þinn hvenær sem þú verður að fá birgðaskrár. Líkamleg lagerbirgðir, selt magn og keypt magn er allt fáanlegt úr kassanum. Þú getur líka stillt aðrar efnislegar mælingar (svo sem skilað, sett í sóttkví og sett gögn) eins og þú þarfnast, til að fá þessar upplýsingar í rauntíma. Birgðasýnileiki getur unnið úr milljónum birgðabreytinga á skilvirkan hátt. Þessum gögnum er hægt að safna saman og endurspeglast í nýjasta birgðamagninu í þjónustunni strax, á sekúndu eða á mínútu, allt eftir því á hvaða bili gögnin eru birt. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Mjúk fyrirvara til að forðast ofsölu á öllum pöntunarrásum

A *mjúkur fyrirvari* gerir þér kleift að úthluta eða merkja tiltekið magn til að uppfylla pöntun eða eftirspurn. Mjúkur frágangur hefur ekki áhrif á vörubirgðir, en hann dregur frá *hægt að panta* birgðamagn og veitir uppfært magn fyrir framtíðaruppfyllingu pöntunar. Þessi eiginleiki mun vera gagnlegur ef sölubeiðnir eða pantanir koma inn í fyrirtæki þitt frá einni eða fleiri rásum eða gagnaveitum sem eru utan kerfisbundins fyrirtækisáætlunar (ERP) kerfis þíns.

Ef þú notar ekki mjúkar frátekningar í birgðasýnileikaþjónustunni verður þú að bíða þar til pöntunin er samstillt við og unnin af ERP kerfinu þínu til að fá uppfærslu á efnislegu birgðamagni. Þetta ferli hefur venjulega mikla leynd. Hins vegar taka mjúkar frátekningar strax gildi í hvert sinn sem sölubeiðni eða pöntun er mynduð í sölurásum þínum. Þess vegna hjálpa þeir til við að koma í veg fyrir ofsöluaðstæður með því að tryggja að umnichannel pantanir þínar trufli ekki hver aðra þegar þær að lokum ná ERP kerfinu. Mjúkar bókanir tryggja líka að þú getir uppfyllt allar pantanir sem þú hefur lofað. Þess vegna hjálpa þeir þér að uppfylla væntingar viðskiptavina og viðhalda hollustu viðskiptavina. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Tafarlaust svar við staðfestingu ATP dagsetninga

Sýnileiki á áætluðum birgðum þínum í náinni framtíð (þar á meðal framboð, eftirspurn og áætlaðar upplýsingar um fyrir hendi) er mikilvægt, vegna þess að það hjálpar fyrirtækinu þínu að ná eftirfarandi markmiðum:

- Lágmarka birgðastig til að draga úr birgðastjórnunarkostnaði.
- Auðvelda innri pöntunarvinnslu, þannig að sölumenn geti reiknað út sendingar- og afhendingardagsetningar, byggt á framboði á vörum sem pantaðar eru.
- Veittu gagnsæi um hvenær viðskiptavinir geta búist við að vara sem er ekki til á lager verði fáanleg, með því að gefa upp næsta dagsetningu.

ATP eiginleikann er auðvelt að samþykkja í daglegu pöntunarferlinu þínu. Mikilvægast er, eins og önnur tilboð á birgðasýnileika, þá er ATP eiginleikinn *alheims og rauntíma*. Þess vegna getur þú sett upp margar ATP útreikningsformúlur til að hafa allar fyrirspurnir um framboð á birgðum sem ná yfir allar viðskiptarásir þínar og gagnaveitur. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Samhæfni við háþróaða vöruhússtjórnunarhluti

Microsoft stefnir að því að bjóða upp á samþættingu úr kassanum við háþróaða vöruhúsastjórnun (WHS), svo að viðskiptavinir WHS geti einnig notið ávinningsins af birgðasýnileikaþjónustunni. Samkvæmt útgáfu Wave 1 2022 (opinber forskoðun í mars), styður birgðaþjónustan WHS vörufyrirspurnir og ATP. Mjúkur pöntunar- og úthlutunareiginleikinn verður studdur fyrir WHS viðskiptavini í næstu bylgju. <!-- KFM: Add this link when target is published: For more information, see [Inventory Visibility support for WHS items](inventory-visibility-whs-support.md). -->

## <a name="licensing"></a>Leyfisveiting

Birgðasýnileiki þjónustan er fáanleg í eftirfarandi útgáfum:

- **Birgðasýnileikaviðbót fyrir Microsoft Dynamics 365 Supply Chain Management** – Fyrir fyrirtæki sem hafa gilt leyfi fyrir birgðakeðjustjórnun er birgðasýnileiki í boði án aukaleyfiskostnaðar. Þú getur byrjað að prófa það í dag. Fyrir upplýsingar um uppsetningu, sjá [Settu upp og settu upp Birgðasýnileika](inventory-visibility-setup.md).
- **Birgðasýnileikaþjónusta sem hluti af IOM** – Þessi útgáfa er annað hvort fyrir Intelligent Order Management (IOM) viðskiptavini eða fyrirtæki sem eru ekki að nota Supply Chain Management sem ERP kerfi sitt. Leyfið er innifalið í IOM pakkanum. Fyrir frekari upplýsingar, sjá [Greindur pöntunarstjórnun yfirlit](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
