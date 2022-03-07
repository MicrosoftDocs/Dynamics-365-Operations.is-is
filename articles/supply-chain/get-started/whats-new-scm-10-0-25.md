---
title: Forútgáfa af Dynamics 365 Supply Chain Management 10.0.25 (apríl 2022)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 8a9b873b7b4bba43b7b3e6e83c389ac35b4e223e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102997"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Forútgáfa af Dynamics 365 Supply Chain Management 10.0.25 (apríl 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forútgáfu af útgáfu 10.0.25. Þessi útgáfa er með byggingarnúmer 10.0.1149 og er fáanlegt á eftirfarandi hátt:

- **Forútgáfa:** Febrúar 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Mars 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Apríl 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þetta efnisatriði til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða-&nbsp;og&nbsp;vörustjórnun | Viðbætur við hættuleg efni | Þessar endurbætur byggja á núverandi virkni hættulegra efna til að hjálpa fyrirtækjum að vera í samræmi við staðbundnar reglur þegar þeir flytja hættuleg efni yfir mismunandi landsvæði. <!-- KFM: Update to 2022w1 link when published -->| Eiginleikastjórnun:<br>*Viðbætur við hættuleg efni* |
| Birgða-&nbsp;og&nbsp;vörustjórnun | Pökkunarvinna fyrir pökkunarstöðvar | Þessi eiginleiki bætir mjög sveigjanleika og lipurð í pökkunar- og sendingaraðgerðum þínum. Meðan á pökkunarferlinu stendur geta starfsmenn vöruhúsa nú pakkað og sent einstaka pakka sem tengjast sömu sendingu og farmi. Pöntunarlínur sem eru hluti af sömu sendingu þurfa ekki endilega að vera sendar saman ef sumar vörur eru tilbúnar til sendingar strax. Hægt er að pakka einni pöntun og senda í mörgum bökkum á mismunandi sendingartímum, sem dregur úr biðtíma og eykur lipurð.<!-- KFM: Update to 2022w1 link when published --> | Eiginleikastjórnun:<br>*Pökkunarvinna fyrir pökkunarstöðvar* |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Skanna strikamerki í vöruhúsinu með GS1-sniðsstöðlum](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1-strikamerki og QR-kóðar](../warehousing/gs1-barcodes.md) | Eiginleikastjórnun:<br>*Skanna inn GS1-strikamerki* |
| Framleiðsla | [Efnisnotkun og fyrirvarar í framkvæmdarviðmóti framleiðslugólfs](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Eiginleikastjórnun:<br>*(Forútgáfa) Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (virkjað fyrir vöruhúsakerfi)* |
| Framleiðsla | [Skrá efnisnotkun á mælieiningum](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-manufacturing.md) | Eiginleikastjórnun:<br>*Skrá efnisnotkun í fartæki í kvörðunareiningu* |
| Áætlun | [Áætlanagerð Hagræðingartillögur til að hámarka núverandi framboð](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Aðgerðaboð](../master-planning/action-messages.md) | Sjálfgefið virkt |
| Áætlun | Áætlaðar pantanir einfaldaðar | [Áætlaðar pantanir einfaldaðar](../master-planning/planning-optimization/planned-orders-simplified.md ) | Eiginleikastjórnun:<br>*Áætlaðar pantanir einfaldaðar* |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Kerfiseining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Birgða- og vöruhúsakerfi | (Pólland) Leyfa tengingu nokkurra SAD-reikninga við eina innkaupapöntunarlínu í einu SAD | Þessi eiginleiki gerir þér kleift að skipta innkaupapöntunarlínum og tengja þær við eitt stjórnunarskjal (SAD) þegar þessar innkaupapöntunarlínur voru bókaðar fyrir nokkra mismunandi reikninga (eins og fyrir mismunandi sendingar). |
| Innkaup og aðföng | Sameina margar innkaupabeiðnir í eina innkaupapöntun eftir dagsetningu reikningsskila | Þessi eiginleiki gerir kleift að sameina margar innkaupabeiðnir í eina innkaupapöntun ef mismunandi innkaupabeiðnir hafa mismunandi bókhaldsdagsetningar. Stofnun innkaupapöntunar og samþjöppun eftirspurnar er hægt að setja reglur um innkaupastefnu til að gera sjálfvirkan ákvörðun um að flokka innkaupalínur eftir bókhaldsdagsetningu á innkaupapöntunarstigi. Sameining innkaupapöntunar eftir bókhaldsdagsetningu er ekki studd ef fjárhagsáætlunarstýring er virkjuð vegna þess að bókhaldsdagsetningin er notuð fyrir frátekningar fjárhagsáætlunar og kvað. Þess vegna ætti að geyma það á meðan skipt er frá innkaupabeiðni yfir í innkaupapöntun. |
| Innkaup og aðföng | Birta eldri útgáfu sjálfgefinna stillinga svarsvæðis fyrir tilboðsbeiðni | Þessi eiginleiki kynnir aftur eldri sjálfgefna beiðni um tilboð (RFQ) svarsviðsstillingar, sem áður voru fjarlægðar úr notendaviðmótinu. Þessar stillingar bjóða ekki upp á neina virkni beint úr kassanum, en hægt er að aðlaga þær til að veita hana eftir þörfum. Virkjaðu þennan eiginleika ef fyrirtækið þitt hefur þegar bætt við virkni fyrir sjálfgefna stillingar fyrir svarsvið beiðnir fyrir beiðni eða ætlar að gera það. Þegar þessi eiginleiki er virkur geturðu fengið aðgang að stillingunum með því að fara í **Innkaupa- og innkaupafæribreytur** síðu, opnaðu **Beiðni um tilboð** flipann og velja **Sjálfgefin svarreitir fyrir beiðni um tilboð**. |
| Innkaup og aðföng | Sameina fjárhagsvíddir frá lánardrottni við fjárhagsvídd virks víddartengils í innkaupapöntuninni | Þessi eiginleiki gerir þér kleift að sameina fjárhagsvíddir frá lánardrottnum með virkum víddartenglum fjárhagsvíddum eftir samþykki innkaupabeiðni ef þú setur upp tengingu milli fjárhagsvíddar og birgðavídd svæðisins. Stofnun innkaupapöntunar og samþjöppun eftirspurnar er hægt að setja reglur um innkaupastefnu til að keyra ákvörðunina um sameiningu fjárhagsvídda frá lánardrottnum með virka fjárhagsvídd víddartengds á hausstigi innkaupapöntunar. |
| Framleiðslustýring | (Rússland) Virkja sjálfgefna staðsetningaruppsetningu fyrir framleiðsluformúlu/uppskrift og sjálfvirka GTD frátekningu/neyslu í framleiðslu | Eiginleikinn gerir fleiri valkosti fyrir framleiðslu úr innfluttu hráefni kleift (aðeins rússnesk staðsetning):<ul><li>Valkostur til að stilla sjálfvirka sjálfgefna staðsetningu fyrir framleiðsluformúlur og efnisskrá bæði á tilfangaflokkum og vöruhúsum.</li><li>Sjálfvirk frátekt á hráefni af the *GTD númer* vídd í WMS-virkjuð vöruhúsum samkvæmt bókunaralgrími sem ekki er WMS. Þetta á við í þeim tilvikum þar sem vinnustefna fyrir *Hráefnistínsla* er til með **Vinnusköpunaraðferð** stillt á *Aldrei* og uppsetning vöruhúss, staðsetningar og vörunúmers passar við birgðafærslur framleiðslupöntunar (lotu).</li><li>Sjálfvirk neysla á hráefni eftir *GTD númer* vídd við færslu vallista, í samræmi við aflaða fyrirvara sem lýst var áður.</li></ul> |
| Vöruhúsakerfi | (Forútgáfa) Stuðningur kvörðunareiningar fyrir vöruhúsapantanir á inn- og útleið | Þessi eiginleiki veldur því að kerfið stofnar vöruhúsapantanir á útleið meðan á losun í vöruhús ferlið stendur og stofnar vöruhúsapantanir á innleið þegar flutningspantanir eru bókaðar sem sendar. Kerfið samstillir síðan hverja vöruhúsapöntun á innleið eða útleið við mælieininguna sem ber ábyrgð á sendingu eða móttöku pöntunarinnar. Athugaðu að eftir að hafa virkjað þennan eiginleika verður að uppfæra vinnuálag vöruhúsaframkvæmda. Frekari upplýsingar eru í [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Þessi eiginleiki krefst þess *Aftengdu frágangsvinnu frá ASN* eiginleiki og mun gera möguleika á að taka á móti flutningspöntunum með því að nota númeraplötumóttökuferlið í vöruhúsastjórnun farsímaforritinu. |

## <a name="feature-state-changes-in-this-release"></a>Eiginleikastöðubreytingar í þessari útgáfu

Eftirfarandi tafla sýnir eiginleika sem urðu skyldubundnir eða virkjaðir sjálfgefið frá og með 10.0.25. Allir þessir eiginleikar verða sjálfkrafa virkir fyrir kerfið þitt um leið og þú uppfærir í 10.0.25. Ekki er hægt að slökkva á lögboðnum eiginleikum, en samt er hægt að slökkva á eiginleikum sem eru sjálfgefið að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Taflan sýnir einnig eiginleika sem áður voru í opinberri forskoðun, en hafa breyst til að verða almennt fáanlegir í 10.0.25, sem þýðir að nú er mælt með þeim til notkunar í framleiðsluumhverfi. Sjálfgefið er slökkt á þessum eiginleikum nema annað sé tekið fram, svo þú verður að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja þau ef þú vilt nota þau.

| Kerfiseining | Heiti eiginleika | Staða eiginleika |
| --- | --- | --- |
| Eignastýring | [Notið reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Almennt tiltækt |
| Eignastýring | [Viðbætur viðhalds sem byggir á teljara](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Almennt tiltækt |
| Kostnaðarstýring | [Kostnaðarútreikningsstig](../cost-management/cost-calculation-level.md) | Almennt tiltækt |
| Kostnaðarstýring | Virkja uppsetningu rununúmers sem er skilgreind af notanda fyrir bakfærslu birgðalokunar | Almennt tiltækt |
| Kostnaðarstýring | [Ítarlegar upplýsingar um ferli birgðalokunar](whats-new-scm-10-0-21.md) | Almennt tiltækt |
| Kostnaðarstýring | [Valmöguleikar á að gera fjárhagsvíddir sjálfgefnar fyrir endurmat á staðalkostnaði birgða](../cost-management/manage-standard-cost-updates.md) | Almennt tiltækt |
| Kostnaðarstýring | Gagnahreinsun birgðavirðisskýrslu | Sjálfgefið kveikt |
| Kostnaðarstýring | [Geymsla birgðavirðisskýrslu](../cost-management/inventory-value-report-storage.md) | Sjálfgefið kveikt |
| Kostnaðarstýring | Sýna kladda birgðalokunar í hnitaneti | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Virkja breytingastjórnun á fyrirliggjandi afurðum](../engineering-change-management/change-management-existing-products.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Verkfræðibreytingastjórnun](../engineering-change-management/product-engineering-overview.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Hönnunartilkynningar fyrir framleiðslu](../engineering-change-management/engineering-change-management.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Bætt erfðaeigind fyrir umsjón hönnunarbreytinga](../engineering-change-management/engineering-attributes-and-search.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Stjórna breytingum á formúlum og innihaldsefnum þeirra](../engineering-change-management/manage-formula-changes.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Undirbúningsathuganir afurðar](../engineering-change-management/product-readiness.md) | Sjálfgefið kveikt |
| Umsjón hönnunarbreytinga | [Afbrigði útbúið fyrir hönnunarafurðir](../engineering-change-management/engineering-variants.md) | Sjálfgefið kveikt |
| Birgða- og vöruhúsakerfi | Leiðsögn í uppskriftarútgáfu frá uppskriftarlínum | Skylda |
| Áætlanagerð | [Runuhæf staðfesting og sameining fyrir áætlaðar runupantanir magns og pakka](whats-new-scm-10-0-20.md) | Almennt tiltækt |
| Áætlanagerð | Tilfangaáætlun með viðhaldsverki | Almennt tiltækt |
| Áætlanagerð | Virkja uppsetningarhjálparaðgerðir aðaláætlunar | Skylda |
| Áætlanagerð | [Val á spárlíkani fyrir upplýsingar um eftirspurnarspár](../master-planning/manual-adjustments-baseline-forecast.md) | Skylda |
| Áætlanagerð | [Myndræn framsetning á ferli aðaláætlanagerðar](../master-planning/tasks/monitor-master-planning-run.md) | Skylda |
| Áætlanagerð | [Samhliða staðfesting á áætluðum pöntunum](../master-planning/planning-optimization/planned-order-firming.md) | Skylda |
| Áætlanagerð | [Staðfesting áætlaðrar pöntunar með síun](../master-planning/planning-optimization/planned-order-firming.md) | Sjálfgefið kveikt |
| Áætlanagerð | [Vistuð yfirlit fyrir áætlaðar pantanir](saved-views-scm.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | Slökkva á endurstillingarhnappi fyrir dreifingu innkaupabeiðni | Almennt tiltækt |
| Innkaup og aðföng | [Virkja endurstillingu á verkflæðum sem tengjast innkaupum](whats-new-scm-10-0-20.md) | Almennt tiltækt |
| Innkaup og aðföng | Geta til að staðfesta samþykktar innkaupapantanir úr samstarfi lánardrottna í runu | Skylda |
| Innkaup og aðföng | Lokuð staða innkaupasamnings | Skylda |
| Innkaup og aðföng | Bæta línum við reikninga innkaupapantana sem tengjast innkaupasamningi | Sjálfgefið kveikt |
| Innkaup og aðföng | Reitur „Bæta við pöntuðu magni“ á síðuna Bókun innhreyfingarskjals afurða | Sjálfgefið kveikt |
| Innkaup og aðföng | [Leyfa lánardrottnum að sækja um innkaupaflokka með samstarfi lánardrottna](../procurement/category-requests-from-vendors.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | Innheimtir gjöld „frá og til“ upphæða í innkaupapöntunum | Sjálfgefið kveikt |
| Innkaup og aðföng | Uppsetning gjalda með vinnusvæði og vöruhúsi | Sjálfgefið kveikt |
| Innkaup og aðföng | Virkja útreikning innkaupagjalds sem byggist á árlegri verðskrá | Sjálfgefið kveikt |
| Innkaup og aðföng | [Ábyrgðaraðili innkaupasamnings](../procurement/purchase-agreements.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | [Vistuð yfirlit fyrir framleiðslupantanir](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruupplýsingastjórnun | [Öflug villuleit í sjálfgefnu pöntunarmagni](../production-control/default-order-settings.md) | Skylda |
| Vöruupplýsingastjórnun | Forvinnsla uppskriftarskýrslu til að koma í veg fyrir tímalokun | Sjálfgefið kveikt |
| Vöruupplýsingastjórnun | Gera hverja fjárhagsvídd fyrir sig sjálfgefna þegar vörusniðmát er notað | Sjálfgefið kveikt |
| Vöruupplýsingastjórnun | Virkja afurðavíddaflokka fyrir vörusniðmát | Sjálfgefið kveikt |
| Vöruupplýsingastjórnun | Endurgera heiti afurðarafbrigði í samræmi við nafnakerfi | Sjálfgefið kveikt |
| Vöruupplýsingastjórnun | [Endurbætur á tillögusíðu afbrigðis](../pim/tasks/create-predefined-product-variants.md) | Sjálfgefið kveikt |
| Framleiðslustýring | Endurbætt tiltekt á magni framleiðsluþyngdar afurðar | Almennt tiltækt |
| Framleiðslustýring | Nýr hnappur fyrir Stöðva hlé hefur verið bætt við síðu Starfskortastöðvar | Skylda |
| Framleiðslustýring | [Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðslustýring | Virkjaðu móttöku undirverktaka að hluta og lagfærðu vandamál með útreikning á rusli fyrir uppskriftarlínur af gerðinni Seljandi | Skylda |
| Framleiðslustýring | [Eiginleikinn til að læsa vinnsluspjaldstæki og afgreiðslustöð svo hægt sé að hreinsa tækin](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðslustýring | Endurbætur á svargluggum fyrir að samþykkt og flutning vinnsla | Skylda |
| Framleiðslustýring | [Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðslustýring | [Prenta merki úr verkspjaldstæki](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðslustýring | [Framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðslustýring | [Virkni eignarstýringar fyrir viðmót framkvæmdar á framleiðslugólfi](../production-control/production-floor-execution-configure.md) | Sjálfgefið kveikt |
| Framleiðslustýring | [Verkleit fyrir keyrsluviðmót framleiðslugólfs](../production-control/production-floor-execution-configure.md) | Sjálfgefið kveikt |
| Framleiðslustýring | [Hnekkja sjálfgefinni framleiðslufrátekningu](../production-control/override-default-reservation-principle.md) | Sjálfgefið kveikt |
| Framleiðslustýring | [Sýna öll raðnúmer, rununúmer og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins](whats-new-scm-10-0-21.md) | Sjálfgefið kveikt |
| Sala og markaðsstarf | [Aukin afköst sölupöntunarupplýsinga](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Almennt tiltækt |
| Sala og markaðsstarf | Aukin afköst sölutilboðsupplýsinga | Almennt tiltækt |
| Sala og markaðsstarf | Regla um útflutning gagna sem sölupöntunin vísar í | Skylda |
| Sala og markaðsstarf | [Eyðingarregla frá sölupöntunar- til innkaupapöntunarlínu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Skylda |
| Sala og markaðsstarf | [Regla um útflutning gagna sem sölutilboð vísar í](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Skylda |
| Sala og markaðsstarf | [Fínstilling á útflutningi gagnaeiningar tengiliðar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Sjálfgefið kveikt |
| Sala og markaðsstarf | Virkja uppflettingu á reitum upphafsorða og niðurlags í sölutilboðsskjölum | Sjálfgefið kveikt |
| Sala og markaðsstarf | [Bæta afköst viðskiptavinaskýrslunnar „100 stærstu“](whats-new-scm-10-0-23.md) | Sjálfgefið kveikt |
| Sala og markaðsstarf | Endurreikna áætlaða stöðu viðskiptavinar | Sjálfgefið kveikt |
| Sala og markaðsstarf | [Skráning skilapöntunarlínu ásamt nákvæmum aukastöfum með og án framleiðsluþyngdar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Sjálfgefið kveikt |
| Sala og markaðsstarf | [Vistað yfirlit fyrir sölu og markaðssetningu](saved-views-scm.md) | Sjálfgefið kveikt |
| Sala og markaðsstarf | Staðfesting sölupöntunar með einum smelli | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum](../warehousing/planned-cross-docking.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Gera væntanlegar innhreyfingar úr gæðapöntunum óvirkar sem taka sýni af læstum birgðum](../inventory/inventory-blocking.md) | Almennt tiltækt |
| Vöruhúsakerfi | Móttökuferill númeraplötu | Almennt tiltækt |
| Vöruhúsakerfi | [Viðmót efnismeðhöndlunarbúnaðar](../warehousing/mhax.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Slétta magn niður í næstu sölueiningu við losun í vöruhús](whats-new-scm-10-0-19.md) | Almennt tiltækt |
| Vöruhúsakerfi | Stuðningur kvörðunareiningar fyrir vinnulista vöruhúsaforrits | Almennt tiltækt |
| Vöruhúsakerfi | Upplýsingar um bylgjumerki sendingar | Almennt tiltækt |
| Vöruhúsakerfi | [Notaðu hraðvirkara API fyrir lokun/enduropnun gáma í pökkunarstöð](whats-new-scm-10-0-21.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Staðfesta sniðmát sem valin eru fyrir áfyllingarverk](whats-new-scm-10-0-20.md) | Almennt tiltækt |
| Vöruhúsakerfi | Leyfa áfyllingarsniðmáti að nota fyrirliggjandi tafarlausa áfyllingarvinnu (yfir allar einingar) | Skylda |
| Vöruhúsakerfi | Sjálfvirk úthlutun GUIDs við stofnun WHS notenda | Skylda |
| Vöruhúsakerfi | Sækja afurðarafbrigði og rakningarvíddir í vöruhúsaforritinu við móttöku á farmvöru | Skylda |
| Vöruhúsakerfi | [Breyta birgðastöðu atriða sem er stjórnað af rakningarvíddum](../inventory/inventory-statuses.md) | Skylda |
| Vöruhúsakerfi | [Breyta vinnuhópi á vinnu](../warehousing/change-work-pool-on-work.md) | Skylda |
| Vöruhúsakerfi | [Staðsetning klasa er full](../warehousing/cluster-position-full.md) | Skylda |
| Vöruhúsakerfi | [Eiginleiki fyrir frágang klasa](../warehousing/putaway-clusters.md) | Skylda |
| Vöruhúsakerfi | [Staðfesta og flytja](../warehousing/confirm-and-transfer.md) | Skylda |
| Vöruhúsakerfi | [Staðfesta sendingar á útleið úr runuvinnslum](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Skylda |
| Vöruhúsakerfi | [Stjórna því hvort á að birta yfirlitssíðu móttöku í fartækjum](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Skylda |
| Vöruhúsakerfi | [Frestun á úrvinnslu handvirkrar aðgerðar birgðahreyfingar](../warehousing/deferred-processing-manual-inventory-movement.md) | Skylda |
| Vöruhúsakerfi | Ekki leyfa að búa til álag sem uppfylla ekki kröfur um byggingarsniðmát fyrir bylgjuálag | Skylda |
| Vöruhúsakerfi | [Aukið skipulag á númeraplötumerki](../warehousing/document-routing-layout-for-license-plates.md) | Skylda |
| Vöruhúsakerfi | [Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Skylda |
| Vöruhúsakerfi | Fela reitinn „Heildarvirði“ á síðunum „Allar hleðslur“ og „Hleðsluupplýsingar“ | Skylda |
| Vöruhúsakerfi | Grunnstilling á smíð númeraplötumerkis | Skylda |
| Vöruhúsakerfi | Handvirk leiðrétting á farmlínu fyrir stjórnanda eða álíka trausta notendur | Skylda |
| Vöruhúsakerfi | [Númeraplötustaða staðsetningar](../warehousing/location-license-plate-positioning.md) | Skylda |
| Vöruhúsakerfi | [Blöndun á afurðarvídd staðsetningar](../warehousing/location-product-dimension-mixing.md) | Skylda |
| Vöruhúsakerfi | Opna fyrir breytingar á reit birgðastöðu fyrir birgðahreyfingu fartækis | Skylda |
| Vöruhúsakerfi | Handvirk tiltektarþjónusta sölulínu fyrir stjórnanda eða aðra trausta notendur | Skylda |
| Vöruhúsakerfi | [Koma í veg fyrir að númeraplötur, sem afgreiddar voru með flutningspöntun, verði notaðar í öðrum vöruhúsum en vöruhúsi áfangastaðar](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Skylda |
| Vöruhúsakerfi | Kvaðning um að leysa úr tvíræðni í heitum „Stað / NP“ | Skylda |
| Vöruhúsakerfi | [Gæðaskoðun](../warehousing/quality-check.md) | Skylda |
| Vöruhúsakerfi | [Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið](../warehousing/install-configure-warehouse-management-app.md) | Skylda |
| Vöruhúsakerfi | [Viðbótargögn um staðsetningu](../warehousing/additional-location-zones.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti](../warehousing/create-transfer-order-from-warehouse-app.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | Virkja hraðvirka prófun fyrir fartæki vöruhúss | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Hámarkskeyrslutími á hreinsunarvinnslu lagerbirgðafærslna vöruhúsakerfis](../warehousing/onhand-cleanup.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Myndræn framsetning vinnuálags á útleið](../warehousing/outbound-workload-visualization.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vinna úr viðburðum vöruhúsaforrits](../warehousing/warehouse-app-events.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vistað yfirlit fyrir vinnusvæði hleðsluáætlunar](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vistað yfirlit fyrir upplýsingasíðu vinnu](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vistað yfirlit fyrir bylgjuvinnslu](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vistuð yfirlit fyrir hleðsluvinnslu](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Vistuð yfirlit fyrir úrvinnslu sendingar](saved-views-scm.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Skoða upplýsingar um runuvinnslu](../warehousing/wave-processing.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Tilkynningar bylgjukeyrslu](../warehousing/wave-execution-notifications.md) | Sjálfgefið kveikt |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Supply Chain Management 10.0.25 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.25 af Finance and Operations forritum (apríl 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.25, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun](/dynamics365-release-plan/2022wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
