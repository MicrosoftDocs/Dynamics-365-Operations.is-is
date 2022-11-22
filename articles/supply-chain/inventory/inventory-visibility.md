---
title: Yfirlit viðbótar fyrir Inventory Visibility
description: Þessi grein útskýrir hvað birgðasýnileiki er og lýsir eiginleikum þess.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762808"
---
# <a name="inventory-visibility-add-in-overview"></a>Yfirlit viðbótar fyrir Inventory Visibility

[!include [banner](../includes/banner.md)]

Birgðasýnileikaviðbótin (einnig nefnd *Birgðasýnileikaþjónusta*) býður upp á óháða og mjög stigstærða örþjónustu sem gerir rauntíma birgðabreytingafærslum og sýnileikarakningu í öllum gagnaveitum þínum og rásum kleift. Það býður upp á vettvang sem gerir þér kleift að stjórna alþjóðlegum birgðum þínum með því að nota virkni sem inniheldur (en takmarkast ekki við) eftirfarandi lista:

- Fylgstu miðlægt með nýjustu birgðastöðunni (eins og tiltæk, pantað, keypt, í flutningi, skilað og í sóttkví) yfir allar gagnaveitur þínar, vöruhús og staðsetningar með því að tengja birgðakeðjustjórnun þína eða flutningagagnaveitur þriðja aðila ( eins og pöntunarstjórnunarkerfi, áætlanagerð þriðja aðila fyrirtækja\[ ERP\] kerfi, sölustaður\[ POS\] kerfi og vöruhúsastjórnunarkerfi) til birgðasýnileikaþjónustunnar.
- Spurðu um framboð á lager og skort og fáðu strax svör með því að hringja beint í birgðasýnileikaþjónustuna.
- Forðastu ofsölu, sérstaklega þegar eftirspurn þín kemur frá mismunandi rásum, með því að gera mjúkar pantanir í rauntíma í birgðasýnileikaþjónustunni.
- Stýrðu betur lofuðum pöntunum og væntingum viðskiptavina með því að gefa upp nákvæmar dagsetningar sem eru í boði eða næst, þannig að aðgerðin umnichannel available-to-promise (ATP) geti reiknað út væntanlegar uppfyllingardagsetningar pantana.

## <a name="extensibility"></a>Stækkunarhæfni

Birgðasýnileiki þjónustan er mjög stækkanleg vegna þess að inntak og úttak gagna er ekki bundið við Microsoft forrit. Ytri kerfi geta nálgast þjónustuna í gegnum RESTful forritunarviðmót (API). Auk þess að nota út-af-kassa kortlagningu sem eru veittar fyrir gagnagjafa og víddir Supply Chain Management, geturðu samþætt birgðasýnileika við mörg kerfi þriðja aðila með því að setja upp viðbótargagnagjafa, mælikvarða á birgðastöðu (vísað til sem *líkamlegar ráðstafanir* í birgðasýnileikaþjónustu), og birgðavíddir í gegnum stillingarforritið. Á þennan hátt geturðu á sveigjanlegan hátt spurt og breytt mörgum gagnaveitum þínum og fyrirfram skilgreindum birgðavíddum.

Þar að auki, vegna þess að birgðasýnileiki er byggður á Microsoft Dataverse, gögn þess er hægt að nota til að byggja upp og samþætta við Power Apps. Þú getur líka notað Power BI til að búa til sérsniðin mælaborð sem uppfylla kröfur fyrirtækisins.

## <a name="scalability"></a>Skalanleiki

Hægt er að stækka birgðasýnileikaþjónustuna upp eða niður, allt eftir gagnamagni þínu. Stækkunarupplifunin er að mestu óaðfinnanleg og er framkvæmd af Microsoft vettvangsteyminu, byggt á sjálfvirkri uppgötvun og mati á magni viðskiptagagna þinna.

Eftirfarandi mynd sýnir arkitektúr birgðasýnileika.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title=" Birgðasýnileiki arkitektúr" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Helstu atriði eiginleika

### <a name="get-a-global-view-of-real-time-inventory"></a>Fáðu heildarsýn yfir rauntíma birgðahald

Birgðasýnileiki tryggir að þú hafir aðgang að nýjustu birgðamagninu á öllum tímum, á öllum rásum þínum, staðsetningum og vöruhúsum. Þú munt hagnast mest á því að nota það til að styðja við daglegan rekstur þinn hvenær sem þú þarft að fá birgðaskrár. Raunverulegar lagerbirgðir, selt magn og keypt magn er allt tiltækt úr kassanum. Þú getur líka stillt aðrar efnislegar birgðaráðstafanir (svo sem skilað, sett í sóttkví og sett gögn) eftir þörfum til að fá þessar upplýsingar í rauntíma. Birgðasýnileiki getur á skilvirkan hátt unnið úr milljónum birgðabreytingastaða. Þessum gögnum er hægt að safna saman og endurspeglast í nýjasta birgðamagninu í þjónustunni strax, á sekúndu eða á mínútu, allt eftir því á hvaða bili gögnin eru birt. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki opinber API](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Miðlæg birgðaleiðrétting

Birgðasýnileiki gerir ytri kerfum kleift að hringja í API þess til að birta breytingar á birgðum. Breytingarnar taka strax gildi í Birgðasýnileika. Þess vegna er birgðahald strax dregið frá.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Mjúk fyrirvara til að forðast ofsölu á öllum pöntunarrásum

A *mjúkur fyrirvari* gerir þér kleift að úthluta eða merkja tiltekið magn til að uppfylla pöntun eða eftirspurn. Mjúkur frágangur hefur ekki áhrif á vörubirgðir, en hann dregur þó frá *hægt að panta* birgðamagn og veitir uppfært magn fyrir framtíðaruppfyllingu pöntunar. Þessi eiginleiki mun vera gagnlegur ef sölubeiðnir eða pantanir koma inn í fyrirtæki þitt frá einni eða fleiri rásum eða gagnaveitum sem eru utan kerfisbundins fyrirtækisáætlunar (ERP) kerfis þíns.

Ef þú notar ekki mjúkar frátekningar í birgðasýnileikaþjónustunni verður þú að bíða þar til pöntunin er samstillt við og unnin af ERP kerfinu þínu til að fá uppfærslu á efnislegu birgðamagni. Þetta ferli hefur venjulega mikla leynd. Hins vegar taka mjúkar frátekningar strax gildi í hvert skipti sem sölubeiðni eða pöntun er mynduð í sölurásum þínum. Þess vegna hjálpa þeir til við að koma í veg fyrir ofsöluaðstæður með því að tryggja að umnichannel pantanir þínar trufli ekki hver aðra þegar þær að lokum ná ERP kerfinu. Mjúkar bókanir tryggja einnig að þú getir uppfyllt allar pantanir sem þú hefur lofað. Þess vegna hjálpa þeir þér að uppfylla væntingar viðskiptavina og viðhalda hollustu viðskiptavina. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>Tafarlaust svar á ATP magni og dagsetningum

Sýnileiki á áætluðum birgðum þínum í náinni framtíð (þar á meðal framboð, eftirspurn og áætlaðar upplýsingar um höndina) er mikilvægt, vegna þess að það hjálpar fyrirtækinu þínu að ná eftirfarandi markmiðum:

- Lágmarka birgðastig til að draga úr birgðastjórnunarkostnaði.
- Auðvelda innri pöntunarvinnslu, þannig að sölumenn geti reiknað út sendingar- og afhendingardagsetningar, byggt á framboði á vörum sem pantaðar eru.
- Veittu gagnsæi um hvenær viðskiptavinir geta búist við að vara sem er ekki til á lager verði fáanleg, með því að gefa upp næsta dagsetningu.

ATP eiginleikann er auðvelt að samþykkja í daglegu pöntunarferlinu þínu. Mikilvægast er, eins og önnur tilboð á birgðasýnileika, ATP eiginleikinn er það *alheims og rauntíma*. Þess vegna getur þú sett upp margar ATP útreikningsformúlur til að hafa allar fyrirspurnir um framboð á birgðum sem ná yfir allar viðskiptarásir þínar og gagnaveitur. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Forúthlutaðu hlutabréfum þínum til mikilvægra rása eða viðskiptavina með birgðaúthlutun

Úthlutunareiginleikinn Birgðasýnileiki gerir þér kleift að vernda og girða verðmæta birgðabirgðir þínar fyrir mikilvægar rásir, viðskiptavinahópa eða staðsetningar. Eftir að birgðaúthlutun hefur verið úthlutað er birgðanotkun bundin við úthlutaða safnið og magnið sem er eftir í safninu verður dregið frá í næstum rauntíma til að endurspegla magnið sem er enn til neyslu. Fyrir frekari upplýsingar, sjá [Birgðasýnileiki birgðaúthlutun](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>Samhæfni við WMS hluti

Microsoft stefnir að því að bjóða upp á samþættingu við vöruhússtjórnunarferla (WMS), svo að viðskiptavinir WMS geti einnig notið ávinningsins af birgðasýnileikaþjónustunni. Samkvæmt 2022 Wave 1 útgáfunni (opinber forskoðun í mars), styður birgðaþjónustan WMS vörufyrirspurnir og ATP. Mjúkur pöntunar- og úthlutunareiginleikinn verður studdur fyrir WMS viðskiptavini í næstu bylgju. Fyrir frekari upplýsingar, sjá [Stuðningur við birgðasýnileika fyrir WMS hluti](inventory-visibility-whs-support.md).

Eftirfarandi mynd sýnir yfirlit yfir núverandi eiginleika og hvernig hægt er að staðsetja þá í gagnaflæðinu.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title=" Yfirlit yfir eiginleika birgðasýnileika" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Leyfisveiting

Birgðasýnileiki þjónustan er fáanleg í eftirfarandi útgáfum:

- **Birgðasýnileikaviðbót fyrir Microsoft Dynamics 365 Supply Chain Management** – Fyrir fyrirtæki sem hafa gilt leyfi fyrir birgðakeðjustjórnun er birgðasýnileiki í boði án aukakostnaðar. Vegna þess að Birgðasýnileiki byggist á Microsoft Power Platform, það er háð Microsoft Power Platform geymslurými og API takmörk. Supply Chain Management leyfið þitt ætti að innihalda sjálfgefið geymslurými og API getu. Ef þú þarft meira geymslupláss og API getu geturðu keypt atvinnuleyfi. Fyrir upplýsingar um sjálfgefna API úthlutun og fagleyfi, sjá [Óska eftir takmörkunum og úthlutunum](/power-platform/admin/api-request-limits-allocations) og [Leyfisyfirlit fyrir Microsoft Power Platform](/power-platform/admin/pricing-billing-skus). Með sjálfgefna geymslu og API úthlutun geturðu byrjað að prófa Birgðasýnileika viðbótina í dag. Fyrir upplýsingar um uppsetningu, sjá [Settu upp og settu upp Birgðasýnileika](inventory-visibility-setup.md). Ef áætluð API- og geymslunotkun þín fer yfir staðlaða úthlutun geturðu haft samband við sölufulltrúann þinn og beðið þá um að hafa samband við vettvangsteymið fyrir undanþágu.
- **Birgðasýnileikaþjónusta sem hluti af IOM** – Þessi útgáfa er annað hvort fyrir Intelligent Order Management (IOM) viðskiptavini eða fyrirtæki sem eru ekki að nota Supply Chain Management sem ERP kerfi sitt. Leyfið er innifalið í Intelligent Order Management pakkanum. Fyrir frekari upplýsingar, sjá [Greindur pöntunarstjórnun yfirlit](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Birgðasýnileiki hugtök

Það er mikilvægt að þú skiljir eftirfarandi hugtök og hugtök þegar þú ert að vinna með Birgðasýnileika viðbótinni:

- **Uppruni gagna** – Gagnagjafi táknar kerfið sem gögnin þín eru frá.
- **Mál** – Mál auðkenna eiginleika vörunnar. Þau geta verið geymslustærðir (eins og staður eða vöruhús) eða vörustærðir (eins og litur, stærð eða stíll).
- **Líkamlegar ráðstafanir** – Líkamlegar mælingar eru magn sem mæla mismunandi birgðastöðu, svo sem á lager, keypt, á pöntun eða selt.
- **Reiknaðar ráðstafanir** – Reiknaðir mælikvarðar eru magnmælingar sem eru reiknaðar út frá safni líkamlegra mælikvarða. Til dæmis, the *Samtals í boði* reiknuð mælikvarði er reiknaður sem *Á hendi* + *Keypt* –*Á pöntun* –*Seldur*.
- **Skipting** – Skipting skilgreinir stigveldi fyrir hvernig birgðasýnileiki mun dreifa mótteknum gögnum. Eins og er er sjálfgefna skiptingin síða og staðsetning.
- **Vísitala stigveldi** – Vísitölustigveldi skilgreinir frekar hvernig þú vilt spyrjast fyrir um birgðahald og fá niðurstöður sem hafa meiri nákvæmni.

Fyrir frekari upplýsingar um þessi hugtök og hugtök, sjá [Stilla birgðasýnileika](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
