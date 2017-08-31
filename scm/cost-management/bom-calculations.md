---
title: "BOM útreikninguar"
description: "Samantekt kostnaðar og útreikningar söluverðs kallast uppskriftaútreikningar og eru ræstir á síðunni Útreikningur. Þetta efnisatriði veitir upplýsingar um útreikning uppskrifta."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, SalesQuotationTable, SalesTable, SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 127c74a0d04c20da86b7890be162c64b3cb07d72
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="bom-calculations"></a>BOM útreikninguar

[!include[banner](../includes/banner.md)]


Samantekt kostnaðar og útreikningar söluverðs kallast uppskriftaútreikningar og eru ræstir á síðunni Útreikningur. Þetta efnisatriði veitir upplýsingar um útreikning uppskrifta.

Samantekt kostnaðar og útreikningar söluverðs kallast uppskriftaútreikningar og eru ræstir á síðunni **Útreikningur**. Smellið á síðuna **Útreikningar** til að framkvæma eftirfarandi verkefni:

-   Reikna út kostnað framleiddrar vöru og til að stofna tengda kostnaðarfærslu vöru innan kostnaðarútgáfu.
-   Reikna út söluverð framleiddrar vöru og til að stofna tengda söluverðsfærslu vöru innan kostnaðarútgáfu.

Notkun síðunnar **Útreikningar** er örlítið breytileg, eftir því hvernig uppskriftaútreikningarnir eru ræstir. Notkun síðunnar **Útreikninguar** fer einnig eftir því hvort uppskriftaútreikningarnir fela í sér kostnaðarútgáfu fyrir staðlaðan kostnað eða áætlaðan kostnað, og eftir ýmsum reglum sem hafa verið skilgreindar innan þeirrar kostnaðarútgáfu sem verið er að nota í uppskriftaútreikningunum. **Athugið:** Afbrigði af skjámyndinni **Útreikningar** er notað í samhengi við sölupantanir, sölutilboð eða vöru þjónustupöntunarlínu. Útreikningarnir eru kallað pöntunar-sértækir uppskriftaútreikningar. Uppskriftarútreikningur fyrir pöntun myndar ekki vörukostnaðarfærslu innan kostnaðarútgáfu. Í staðinn myndar hann útreikningsfærslu sem birtist á síðunni **Útreikningur uppskrifta**. Útreikningsfærslan inniheldur útreiknaðan kostnað og útreiknað söluverð. Hægt er að opna síðuna **Útreikningar** fyrir eina framleiðsluvöru eða kostnaðarútgáfu:

-   Ræsið Útreikningur uppskrifta í skjámyndinni **Vöruverð** til þess að reikna út kostnað fyrir einstaka framleidda vöru. Síðan **Útreikningar** efir sjálfkrafa auðkenni vörunnar. Kostnaðarútgáfa, Uppskriftarútgáfa, leiðarútgáfa, útreiknað magn, dagsetning útreikninga og setur verður að vera tilgreint.
    -   Uppskriftarútgáfa og leiðarútgáfa eru sjálfkrafa stilltar á virka útgáfu fyrir vöru, svæði, dagsetningu og útreikning magns. Hins vegar hægt að hnekkja sjálfgildunum með samþykktum útgáfum.
    -   Útreikningsmagn er sjálfkrafa stillt á staðlað pöntunarmagn vörunnar. Hins vegar er hægt að hnekkja sjálfgildi.
    -   Hægt er að krefjast dagsetningar útreiknings eða svæðis í kostnaðarútgáfu, eða leyfa gildi skilgreind af notanda þegar dagsetningar eða svæðis er ekki krafist í kostnaðarútgáfu. Framtíðardagsetning útreikninga ákvarðar notkun kostnaðarfærslna sem eru í biðstöðu. Uppskriftaútreikningar munu nota kostnaðarfærslu í biðstöðu sem stendur næst tilgreindri frá-dagsetningu eða fyrir-dagsetningu útreikninga.
-   Til að reikna út kostnað fyrir allar framleiddar vörur eða fyrir valdar vörur, eða til að uppfæra vöru samkvæmt því hvar hún hefur verið notuð er Útreikningur uppskrifta ræstur af síðunni **Uppsetning kostnaðarútgáfu** eða síðunni **Viðhald kostnaðarútgáfu**. Síðan **Útreikningar** erfir sjálfkrafa kostnaðarútgáfuna.
    -   Í útreikningum er sjálfkrafa gert ráð fyrir notkun virkrar uppskriftarútgáfu og leiðarútgáfu fyrir framleidda vöru (og tengda staðsetningu, dagsetningu, og magn), nema ef framleiddur þáttur hefur skilgreindan undiruppskrift eða undirleið.
    -   Fyrir útreikninga er gert ráð fyrir því að staðlað pöntunarmagn sé notað fyrir framleiddar vörur. Staðlað pöntunarmagn myndar grunninn fyrir útreikninga á magni einstakra þátta, til þess að ákvarða viðeigandi uppskriftaútgáfur og leiðarútgáfur (þegar notaðar eru magnháðar uppskrifta- og leiðarútgáfur), og til að afskrifa/greiða fastan kostnað. Þegar framleiddur þáttur hefur línugerð uppskriftar af tegundinni **framleiðsla** eða **Lánardrottinn**, eða þegar notuð er framleiðsla eftir pöntun niðurbrotshamur fyrir útreikning uppskrifta, vegna þess að magnið endurspeglar sérstakt skilgreint útreiknað magn.
    -   Hægt er að krefjast dagsetningar útreiknings eða svæðis í kostnaðarútgáfu, eða leyfa gildi skilgreind af notanda þegar dagsetningar eða svæðis er ekki krafist í kostnaðarútgáfu.

Annar breytileiki í uppskriftaútreikningum endurspeglar kostnaðartegund og takmarkanir kostnaðarútgáfunnar:

-   Uppskriftaútreikninga sem nota staðlaðan kostnað verður að afmarka með reglum kostnaðarútgáfu vegna þess að takmarkanirnar tryggja að um staðlaða kostnaðarreglu sé að ræða. Stöðluð kostnaðarregla krefst þess að ákv. takmörkunum sé framfylgt varðandi notkun staðlaðs kostnaðar fyrir keypta vöru, eins stigs niðurbrotshamur, og að tekin séu með hin mismunandi gjöld í einingaverði.
-   Uppskriftaútreikningar sem nota áætlaðan kostnað þurfa ekki að fara eftir staðlaðri kostnaðarreglu. Þessir uppskriftaútreikningar geta notað ólíka niðurbrotshami, mismunandi heimildir um kostnaðargögn fyrir keypta vörur, og valið eftirfylgni með þeim takmörkunum sem gilda innan kostnaðarútgáfunnar.

### <a name="bom-calculations-that-use-standard-costs"></a>Uppskriftarútreikningar sem nota staðalkostnað.

Reglur innan kostnaðarútgáfunnar (fyrir staðlaðan kostnað) geta krafist þess að framfylgt sé fimm reglum varðandi uppskriftaútreikninga. Valkosturinn **Takmarkanir á skráningu** sem er innan kostnaðarútgáfunnar krefst einnar af þessum reglum, þar sem mismunandi gjöld verða að vera tekin með í einingaverði vörunnar. Hægt er að færa inn handvirkt mismunandi gjöld fyrir innkeypta vöru,  á meðan mismunandi gjöld fyrir framleidda vöru endurspegla útreiknaðar afskriftir á föstum kostnaði. Valkosturinn **Takmarkanir á útreikningum** innan kostnaðarútgáfunnar krefst hinna fjögurra reglnanna sem gilda um uppskriftaútreikninga.

-   Kostnaðarframlag keyptrar vöru verður að byggja á staðalkostnaði. Uppskriftaútreikningar verða þannig að nota kostnaðarfærslur vörunnar innan tilgreindrar kostnaðarútgáfu, eða innan þess varakerfis sem inniheldur staðlað kostnaðarverð.
-   Til að tryggja nákvæma og samræmda útreikninga á stöðluðu kostnaðarverði þarf niðurbrotið að vera eins stigs.
-   Hagnaðarstilling verður að vera krafa til þess að hægt sé að fá fram samræmdar niðurstöður við útreikninga á söluverði vörunnar. Aðeins er hægt að nota hagnaðarstillinguna, og mynda söluverðsfærslu, ef kostnaðarútgáfan leyfir söluverð.
-   Fyrirmæli verða að vera um varaúrræði sem hægt er að stilla á **Ekkert**, v**Virkt** (fyrir virkar kostnaðarfærslur), eða **Kostnaðarútgáfa** (fyrir tiltekna kostnaðarútgáfu.

### <a name="bom-calculations-that-use-planned-costs"></a>Uppskriftaútreikningar sem notaða áætlaðan kostnað

Reglur innan kostnaðarútgáfunnar (fyrir áætlaðan kostnað) geta mögulega krafist framfylgni hinna fimm reglna um uppskriftaútreikning. Einnig geta reglur einfaldlega innihaldið sjálfgildi. Valkosturinn **Takmarkanir á skráningu** innan kostnaðarútgáfunnar ákvarðar hvort að reglna uppskriftaútreikninganna um hin mismunandi gjöld verði krafist, eða gegna hlutverki sem sjálfgefin gildi. Hægt er að taka mismunandi gjöld með í einingaverði. Valkosturinn **Takmarkanir á útreikningum** innan kostnaðarútgáfunnar ákvarðar hvort að hinna fjögurra reglnanna um uppskriftaútreikninga verður krafist eða hvort að þær gilda sem sjálfgefin gildi.

-   Uppruni kostnaðarframlegðar fyrir keypta vöru getur verið vörukostnaðarfærsla innan kostnaðarútgáfu. Einnig er hægt að skilgreina uppruna eftir flokki uppskriftarútreiknings sem er tengdur við hana. Til dæmis gæti útreikningaflokkurinn ákvarðað innkaupaverð í viðskiptasamningum sem uppruna gagna um kostnaðarframlag.
-   Niðurbrotshamur getur verið eins stigs, fjölstiga, sniðinn að pöntun, eða byggður á línuatriði uppskriftar. Niðurbrotshamur fyrir línuatriði uppskriftar afritar reglur við útreikning kostnaðar fyrir mat á framleiðslupöntunum.
-   Hægt er að krefjast hagnaðarstillinga eða þau geta verið sjálfgefin gildi. Aðeins er hægt að nota hagnaðarstillinguna, og mynda söluverðsfærslu, ef kostnaðarútgáfan leyfir söluverð.
-   Hægt er að krefjast varaúrræðis eða þá að það getur verið sjálfgefið gildi. Hægt er að stilla varaúrræði á **Ekkert**, **Virkt** (fyrir virkar kostnaðarfærslur), eða **Kostnaðarútgáfa** (fyrir tiltekna kostnaðarútgáfu.

Uppskriftaútreikningar stofna viðvörunartilkynningar og aðrar tilkynningar. Nokkrar útreikningareglur uppskrifta ákvarða tegund tilkynninga. Viðvörunarskilyrði eru skilgreind í þeim hópi uppskriftarútreikninga sem tengdur er við hluti. Hins vegar er hægt að skrifa yfir þessi viðvörunarskilyrði þegar uppskriftaútreikningar eru settir af stað. Þegar varaúrræði er notað getur verið gagnlegt að birta úrræðið sem upplýsingaskilaboð. Þegar reynt er að uppfæra reiknaðan kostnað fyrir vörur sem vantar kostnaðarfærslur í getur einnig verið gagnlegt ef upplýsingaboðin bera kennsl á þær vörur sem voru ekki uppfærðar.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Uppskriftaútreikningar sem nota varaúrræði
Eftirfarandi aðstæður skýra notkun varareglunnar:

-   **Tveggja útgáfa nálgun á uppfærslur staðalkostnaðar** - Kostnaðarútgáfa getur innihaldið stigvaxandi breytingar á stöðluðum kostnaði, til dæmis kostnaðarfærslur í bið sem tákna nýjar vörur eða breytingar á kostnaði. Í þessu tilfelli getur varareglan gert grein fyrir notkun virks staðalkostnaðar sem finna má í öðrum kostnaðarútgáfum.
-   **Hermun áhrif á kostnaðarbreytingar með því að nota áætlaðan kostnað** -Kostnaðarútgáfan fyrir áætlaðan kostnað getur innihaldið breytingar vegna hermunar. Þessi kostnaðarútgáfa mun innihalda kostnaðarfærslur í bið sem tákna hermun kostnaðarbreytinga á vörur, kostnaðartegundir og reikniformúlur óbeins kostnaðar. Í þessu tilfelli getur varareglan gert grein fyrir notkun virks staðalkostnaðar sem finna má í öðrum kostnaðarútgáfum.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Uppskriftarútreikning á ráðlögðu söluverði
Með því að nota nálgunina kostnaður-plús álagning, endurspeglar reiknað söluverð vörunnar safn af hlutfalli hagnaðaraðferðar sem er tilgreint fyrir uppskriftarútreikning og kostnaðinn sem er tengdur við íhlutavörur, leiðaaðgerðir, og viðeigandi framleiðslurekstur. Álagningin endurspeglar hlutfall hagnaðaraðferðar sem eru tengdar kostnaðarflokkum og kostnaðarflokkunum sem var úthlutað til vara, kostnaðartegundir fyrir leiðaaðgerðir, og reikningsformúlur óbeins kostnaðar fyrir framleiðslurekstur. Stillingar hlutfalls hagnaðaraðferðar eru merktar **Staðlað**, **Hagnaður 1**, **Hagnaður 2**, og **Hagnaður 3**. Innan stillingar Hagnaðar 1, til dæmis, getur 50 prósent hlutfall hagnaðaraðferðar verið skilgreint fyrir kostnaðarflokk sem er úthlutaður innkeyptu efni, og 80 prósent hlutfall hagnaðaraðferðar fyrir kostnaðarflokk sem er úthlutaður kostnaðartegundum fyrir leiðaaðgerðir. Samhengi uppskriftarútreiknings ákvarðar hvernig niðurstöður reiknaðs söluverðs eru meðhöndlaðar.

-   **Uppskriftarútreikningur fyrir vöru og tilgreinda kostnaðarútgáfu** − Uppskriftarútreikningurinn myndar söluverðsskrá í bið innan kostnaðarútgáfunnar. Þessi söluverðsskrá er upphafspunktur fyrir nákvæma skoðun á útreikningi, (eins og síðuna **Reikna vörukostnað**). Söluverðsskráin er aðallega til tilvísunar, og er ekki notuð sem grundvöllur fyrir söluverð á sölupöntunum.
-   **Pöntunartengdur uppskriftarútreikningur** - Afbrigði af skjámyndinni **Uppskriftarútreikningur** er notað í samhengi við sölupantanir, sölutilboð eða vöru þjónustupöntunarlínu. Pöntunartengdur uppskriftarútreikningur býr ekki til færslu innan kostnaðarútgáfu. Í staðinn myndar hann útreikningsfærslu sem birtist á síðunni **Niðurstöður uppskriftarútreiknings**. Þessi útreikningsfærsla er upphafspunktur fyrir nákvæma skoðun á útreikningi, (eins og síðuna **Reikna vörukostnað**). Upplýsingar um valda útreikningsskrá er hægt að flytja í upphaflegu línuvöru. Til dæmis er hægt að flytja reiknað söluverð í sölupöntunarlínu.

## <a name="orderspecific-bom-calculations"></a>Pöntunartengdur uppskriftarútreikningur
Uppskriftarútreikningur sem á við eina pöntun er samsetning uppskriftarútreikninga fyrir framleidda vöru. Pöntunartengdur uppskriftarútreikningur er gerður í samhengi við sölupöntun, sölutilboð eða sölupöntunarlínu. Pöntunartengdur uppskriftarútreikningur stofnar útreikningsfærslu sem birtist á síðunni **Niðurstöður uppskriftarútreiknings**. Í útreikningsfærslunni er reiknuð þyngd, reiknaður kostnaður samkvæmt virkum kostnaðarfærslum og reiknað söluverð. Útreikningsfærslan sem sérhver pöntunartengdur uppskriftarútreikningur myndar á síðunni **Niðurstöður uppskriftarútreiknings** fær einkvæmt útreikningsnúmer. Niðurstöður útreikningsfærslunnar má flytja yfir á upphaflega línuatriðið. Uppskriftarútreikningur fyrir pöntun er ólíkur uppskriftarútreikningi fyrir framleidda vöru á tvenna vegu:

-   Uppskriftarútreikningur fyrir pöntun myndar ekki vörukostnaðarfærslu innan kostnaðarútgáfu. Þetta þýðir að reglur um uppskriftarútreikninga eiga ekki við um stofnun vörukostnaðarfærslu eða skrif yfir kostnaðarfærslu.
-   Í öðru lagi notar uppskriftarútreikningur fyrir pöntun alltaf virkar kostnaðarfærslur fyrir íhluti, kostnaðartegundir og reikniformúlur óbeins kostnaðar.






