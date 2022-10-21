---
title: Forútgáfa af Dynamics 365 Supply Chain Management 10.0.29 (október 2022)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 62e06f2348ca3524beaaef5d8879c199db56696f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689284"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.29 (október 2022)

[!include [banner](../includes/banner.md)]

Þessi grein sýnir eiginleika sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfa 10.0.29. Þessi útgáfa hefur byggingarnúmer 10.0.1326 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun á útgáfu:** ágúst 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** September 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Október 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að innihalda eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Úthlutaðu og pantaðu WMS vörur í Birgðasýnileika](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Væntanlegt | Sjálfgefið virkt |
| Birgða- og vörustjórnun | [Forhlaða straumlínulagaða birgðalista](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Nota Inventory Visibility-forritið](../inventory/inventory-visibility-power-platform.md) | Virkt með þjónustustillingu |
| Sjálfvirkt framboð með „framleiða eftir pöntun“ | [Sjálfvirkt framboð með „framleiða eftir pöntun“](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Sjálfvirkt framboð með „framleiða eftir pöntun“](../master-planning/make-to-order-supply-automation.md) | Eiginleikastjórnun:<br>*Sjálfvirkt framboð með „framleiða eftir pöntun“* |
| Áætlun | [Skoðaðu og notaðu nákvæma innsýn fyrir DDMRP](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Eftirspurnardrifin efnisþörf Skipulagsyfirlit](../master-planning/planning-optimization/ddmrp-overview.md) | Eiginleikastjórnun:<br>*(Forútgáfa) DDMRP fyrir fínstillingu áætlanagerðar* |
| Framleiðslustýring | [Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum](../production-control/deferred-posting.md) | Eiginleikastjórnun:<br>*(Forskoðun) Gera fullunnar vörur efnislega tiltækar áður en bókað er í færslubókum* |
| Vöruhúsakerfi | [Leitaðu að viðeigandi gögnum í vöruhúsafarsímaforritinu](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Fyrirspurn um gögn með farsímaforriti vöruhúsakerfis](../warehousing/warehouse-app-data-inquiry.md) | Eiginleikastjórnun:<br>*Flæði gagnafyrirspurnar forritsins Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það inn [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Kostnaðarstýring | Fínstilling á útreikningi biðverðs aukaafurðar | Þessi eiginleiki lagar átök sem geta stundum átt sér stað þegar verð samafurða er reiknað út með því að nota marga þræði. Það veldur því að kerfið tryggir að hvert samvöruverð sé reiknað aðeins einu sinni. Niðurstaða þess útreiknings er síðan notuð sem inntak fyrir alla aðra útreikninga. Ef biðverð er þegar til er það verð notað. |
| Áætlanagerð | Safna saman færslum í fínstillingu áætlanagerðar | Þessi eiginleiki getur hjálpað til við að fækka fyrirhuguðum pöntunum sem myndast til að útvega eina sölupöntunarlínu þegar þú ert að nota áætlanagerð fínstillingu. Þegar kveikt er á þessum eiginleika mun áætlanagerð fínstilling flokka allar birgðafærslur fyrir pöntunarlínu í eina kröfu fyrir allt magnið. (Þessi hegðun passar við innbyggða hegðun áætlanagerðarvélarinnar.) Framboð og eftirspurn eru flokkuð sérstaklega. Þess vegna hjálpar aðgerðin að draga úr færslumagni þegar þú ert með skiptar færslur og þegar þú notar víddir (eins og rununúmer eða raðnúmer) sem eru ekki þekjuvíddir. |
| Innkaup og aðföng | Setja lánardrottin í bið fyrir innkaupapantanir | Þessi eiginleiki gerir þér kleift að setja söluaðila í bið fyrir innkaupapantanir. Það bætir við nýju *Pöntun* biðtegund sem merkir lánardrottin sem í bið fyrir innkaupapantanir. Þú munt ekki geta búið til nýjar innkaupapantanir fyrir lánardrottna sem eru í bið fyrir innkaupapantanir, en þú munt samt geta haldið áfram með opna reikninga eða greiðslur fyrir þá lánardrottna. |
| Sala og markaðsstarf | Reikna nettóupphæð línu við innflutning | Þessi eiginleiki gerir þér kleift að stjórna því hvort kerfið ætti að endurreikna línutölur þegar þú flytur inn gögn í gegnum *Sölupöntunarlínur*, *·*, eða *Skilapöntunarlínur* eining sem notar OData eða tvískrift. Það hefur aðeins áhrif þegar þú ert líka með stefnu um mat á viðskiptasamningum sem takmarka breytingar á **Virði** reit fyrir sölupöntunarlínur, sölutilboðslínur og/eða skilapöntunarlínur. Það bætir við stillingu sem heitir **Reiknaðu nettóupphæð línu** til **Viðskiptakröfur > Uppsetning > Færibreytur viðskiptakrafna** síðu. Þegar þessi stilling er stillt á *Já*, kerfið mun alltaf endurreikna línuupphæðir þegar þess er þörf (þar með hunsa allar matsstefnur viðskiptasamninga fyrir nettóupphæð línunnar). Þegar stillingin er stillt á *Nei*, kerfið mun aldrei sjálfkrafa reikna út nettóupphæð línunnar, jafnvel þó að innkomnar breytingar á línuverði, magni og/eða afslætti myndu gefa til kynna að endurreikna ætti nettóupphæð línunnar. Þessi eiginleiki er sjálfgefið virkur og stilltur upphaflega **Reiknaðu nettóupphæð línu** til *Já*. The *Nei* stilling passar við kerfishegðun fyrir útgáfu 10.0.23 og er aðallega veitt til að styðja við eldri samþættingarsviðsmyndir.<br><br>Fyrir frekari upplýsingar, sjá [Endurreikna nettóupphæðir við innflutning á sölupantunum, tilboðum og skilum](../sales-marketing/calc-line-net-amounts-import.md). |
| Sala og markaðsstarf | Reikna heildarsölu með mörgum þráðum | Þessi eiginleiki hjálpar til við að bæta árangur með því að gera kerfinu kleift að nota samhliða vinnslu þegar það reiknar út sölutölur í lotu. Eiginleikinn bætir við nýju **Fjöldi þráða** sviði til **Reiknaðu sölutölur** valmynd. Ef þú velur að keyra útreikninginn í lotu geturðu notað þennan reit til að stilla hámarksfjölda þráða. Ef þú stillir gildið á *0* (núll) eða *1*, einn þráður verður notaður. Gildi yfir 1 gera multithreading kleift. |
| Sala og markaðsstarf | Uppfæra verð og afslætti sem færð voru inn handvirkt fyrir samstæðu | Þessi eiginleiki bætir við stuðningi við handvirkar breytingarstefnur fyrir pantanir milli fyrirtækja. Það felur í sér stuðning við að flytja handvirkar breytingarstefnur á milli sölu- og innkaupapantana milli fyrirtækja. Áður voru reglur um handvirkar breytingar aðeins studdar fyrir pantanir utan samstæðu. Þegar þessi eiginleiki er virkur mun kerfið gefa þér möguleika á að uppfæra verð og afslætti eftir að þú hefur vistað breytingar á pöntun innan fyrirtækja. Þessi valkostur gerir þér kleift að velja hvort þú vilt nota nýju verð- og afsláttarupplýsingarnar á millifyrirtækjapöntunina eða láta pöntunina óbreytta. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Við höfum nýlega bætt við eða uppfært umtalsvert eftirfarandi hjálpargreinar. Þessar greinar eru ekki endilega tengdar nýjum eiginleikum sem bætt var við fyrir þessa útgáfu, eins og skráð er í fyrri köflum. Hins vegar gætu þeir hjálpað þér að fá meira út úr núverandi eiginleikum.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Aðalskipulag, CTP | [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Aðalskipulag, DDMRP | [Eftirspurnardrifin efnisþörf Skipulagsyfirlit](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Kveiktu á DDMRP-eiginleikanum í þínu kerfi](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Birgðastaðsetning](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Forstilling öryggisbirgða og gildi](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Eftirspurnarstýrð áætlanagerð](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Sjónræn framkvæmd og samvinnuframkvæmd](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Vöruhúsakerfi | [Geymar til sendingar](../warehousing/packing-containers.md)<br>[Pökkunarvinna fyrir pökkunargáma og vinnslusendingar á útleið](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Eiginleikastöðubreytingar í þessari útgáfu

Eftirfarandi tafla sýnir eiginleika sem urðu nauðsynlegir eða virkir sjálfgefið í útgáfu 10.0.29. Kveikt verður á öllum þessum eiginleikum fyrir kerfið þitt um leið og þú uppfærir í útgáfu 10.0.29. Ekki er hægt að slökkva á lögboðnum eiginleikum, en samt sem áður er hægt að slökkva á eiginleikum sem eru sjálfgefnir með því að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Taflan sýnir einnig eiginleika sem áður voru í opinberri forskoðun en hafa breyst til að verða almennt fáanlegir í útgáfu 10.0.29. Þessi breyting gefur til kynna að nú sé mælt með eiginleikum til notkunar í framleiðsluumhverfi. Sjálfgefið er að slökkt sé á þessum eiginleikum nema annað sé tekið fram. Þess vegna verður þú að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja þau ef þú vilt nota þau.

| Eining | Heiti eiginleika | Nýtt eiginleiki ástand |
| --- | --- | --- |
| Eignastýring | [Virkni eignarstýringar fyrir viðmót framkvæmdar á framleiðslugólfi](../production-control/production-floor-execution-configure.md) | Skylda |
| Kostnaðarstýring | [Breyta merki afturköllunar í „Lokun og leiðrétting“ í Bakfæra](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Skylda |
| Kostnaðarstýring | Hreinsaðu upp upplýsingar um uppskriftarútreikninga yfir kostnaðarútgáfur | Skylda |
| Kostnaðarstýring | [Geymsla fyrir samanburð vöruverðs](../cost-management/compare-item-price.md) | Skylda |
| Kostnaðarstýring | [Kostnaðarútreikningsstig](../cost-management/cost-calculation-level.md) | Sjálfgefið kveikt |
| Kostnaðarstýring | Virkja uppsetningu rununúmers sem er skilgreind af notanda fyrir bakfærslu birgðalokunar | Sjálfgefið kveikt |
| Kostnaðarstýring | [Ítarlegar upplýsingar um ferli birgðalokunar](whats-new-scm-10-0-21.md) | Sjálfgefið kveikt |
| Kostnaðarstýring | [Geymsla birgðavirðisskýrslu](../cost-management/inventory-value-report-storage.md) | Skylda |
| Kostnaðarstýring | Gagnahreinsun birgðavirðisskýrslu | Skylda |
| Kostnaðarstýring | Hlaupandi meðaltal, röð varakostnaðar | Skylda |
| Kostnaðarstýring | Sýna kladda birgðalokunar í hnitaneti | Skylda |
| Kostnaðarstýring | Sýna samantekt af vörunum sem eru með færslum sem eru ekki að fullu jafnaðar | Skylda |
| Birgða- og vöruhúsakerfi | Leyfa auð gildi á runueigindum | Skylda |
| Birgða- og vöruhúsakerfi | Sjálfvirk aukning á línunúmerum birgðaflutningspöntunarlína | Skylda |
| Birgða- og vöruhúsakerfi | Búa til flutningspöntun úr sölulínu | Skylda |
| Birgða- og vöruhúsakerfi | Slökkva á línureit birgðabókar í verkflæði | Skylda |
| Birgða- og vöruhúsakerfi | Virkja viðvörunareiginleika fyrir færibreytur gæðastjórnunar birgða | Skylda |
| Birgða- og vöruhúsakerfi | (Kína) Undanskilja efnislega kvittun og birta kostnað miðað við meðalkostnað á mánuði | Sjálfgefið kveikt |
| Birgða- og vöruhúsakerfi | [Samþykktarverkflæði birgðabókar](../inventory/inventory-journal-workflow.md) | Skylda |
| Birgða- og vöruhúsakerfi | [Birgðalagersskýrsla](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Skylda |
| Birgða- og vöruhúsakerfi | [Vistaðar skoðanir fyrir birgðastjórnun](saved-views-scm.md) | Skylda |
| Birgða- og vöruhúsakerfi | Afpöntun millifærslupöntunar | Skylda |
| Birgða- og vöruhúsakerfi | Notkun mælieininga og einingarmagns í birgðabókum | Skylda |
| Birgða- og vöruhúsakerfi | Opnaðu birgðabók | Skylda |
| Framleiðsla | [Sjálfvirk tiltekt á efni sem virkjað er af vöruhúsi fyrir tiltektarlista sem bókaðir eru sjálfvirkt](whats-new-scm-10-0-23.md) | Almennt tiltækt |
| Framleiðsla | Virkja birtingu birgðavídda á efnalistanum fyrir framleiðsluleiðaraðgerðir | Skylda |
| Framleiðsla | [Virkjið til að færa inn runu og raðnúmer þegar tilkynnt er um lok í verkspjaldstækinu](../production-control/report-finished-job-device.md) | Sjálfgefið kveikt |
| Framleiðsla | Endurbætt tiltekt á magni framleiðsluþyngdar afurðar | Sjálfgefið kveikt |
| Framleiðsla | [Verkleit fyrir keyrsluviðmót framleiðslugólfs](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðsla | [Samþætting framleiðslukerfis](../production-control/mes-integration.md) | Sjálfgefið kveikt |
| Framleiðsla | [Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs](../production-control/production-floor-execution-configure.md) | Sjálfgefið kveikt |
| Framleiðsla | [Athugun á efnisframboði eftirspurnar fyrir framleiðslupantanir](whats-new-scm-10-0-24.md) | Sjálfgefið kveikt |
| Framleiðsla | [Hnekkja sjálfgefinni framleiðslufrátekningu](../production-control/override-default-reservation-principle.md) | Skylda |
| Framleiðsla | [Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (ekki vöruhúsakerfi)](../production-control/production-floor-execution-configure.md) | Almennt tiltækt |
| Framleiðsla | [Skýrsla um vörur með framleiðsluþyngd úr keyrsluviðmóti framleiðslugólfs](../production-control/production-floor-execution-configure.md) | Almennt tiltækt |
| Framleiðsla | [Skýrsla um aukaafurðir og hliðarafurðir úr keyrsluviðmóti framleiðslugólfs](../production-control/production-floor-execution-configure.md) | Sjálfgefið kveikt |
| Framleiðsla | [Skýrsla um áætlunarvörur í keyrsluviðmóti framleiðslugólfs](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Sjálfgefið kveikt |
| Framleiðsla | [Vistuð yfirlit fyrir framleiðslustýringu](saved-views-scm.md) | Skylda |
| Framleiðsla | [Sýna öll raðnúmer, rununúmer og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins](../production-control/production-floor-execution-configure.md) | Skylda |
| Framleiðsla | [Sannprófa fyrningu hráefna á móti áætluðum notkunardegi](whats-new-scm-10-0-23.md) | Sjálfgefið kveikt |
| Áætlanagerð | [Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar](../master-planning/planning-optimization/planned-order-firming.md) | Skylda |
| Áætlanagerð | [Runuhæf staðfesting og sameining fyrir áætlaðar runupantanir magns og pakka](whats-new-scm-10-0-20.md) | Sjálfgefið kveikt |
| Áætlanagerð | [Hafa atriði með á lager þegar forvinnslusíurnar eru virkjaðar](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Sjálfgefið kveikt |
| Áætlanagerð | [Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar](../master-planning/planning-optimization/infinite-capacity-planning.md) | Sjálfgefið kveikt |
| Áætlanagerð | [Hlutfall fyrir fínstillingu áætlanagerðar](../master-planning/planning-optimization/safety-margins.md) | Skylda |
| Áætlanagerð | [Neikvæðir dagar fyrir fínstillingu skipulagningar](../master-planning/planning-optimization/delay-tolerance.md) | Skylda |
| Áætlanagerð | [Samhliða heimild leiðréttrar eftirspurnarspár](whats-new-scm-10-0-20.md) | Skylda |
| Áætlanagerð | [Staðfesting áætlaðrar pöntunar með síun](../master-planning/planning-optimization/planned-order-firming.md) | Skylda |
| Áætlanagerð | [Áætlaðar framleiðslutillögur fyrir fínstillingu áætlanagerðar](../master-planning/planning-optimization/production-planning.md) | Skylda |
| Áætlanagerð | [Kaupsamningar fyrir fínstillingu áætlanagerðar](../master-planning/planning-optimization/purchase-trade-agreement.md) | Skylda |
| Áætlanagerð | [Vistuð yfirlit fyrir áætlaðar pantanir](saved-views-scm.md) | Skylda |
| Innkaup og aðföng | Gjöld frá og til fjárhæða á innkaupapantunum | Skylda |
| Innkaup og aðföng | Slökkva á dreifingu innkaupabeiðni Endurstillingarhnappur | Sjálfgefið kveikt |
| Innkaup og aðföng | [Virkja endurstillingu á verkflæðum sem tengjast innkaupum](whats-new-scm-10-0-20.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | [Takmarka fjölda innkaupapöntunarlína á hvert runuverk](whats-new-scm-10-0-27.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | [Sameina fjárhagsvíddir frá lánardrottni við fjárhagsvídd virks víddartengils í innkaupapöntuninni](whats-new-scm-10-0-25.md) | Skylda |
| Innkaup og aðföng | [Bóka skráð magn afurða í birgðum og það sem eftir er af afurðum sem ekki eru í birgðum fyrir kvittanir og reikninga lánardrottna](whats-new-scm-10-0-26.md) | Almennt tiltækt |
| Innkaup og aðföng | [Koma í veg fyrir ofnotkun almennra frátekta fjárhagsáætlunar þegar margar innkaupabeiðnir eru í verkflæði](whats-new-scm-10-0-21.md) | Sjálfgefið kveikt |
| Innkaup og aðföng | [Ábyrgðaraðili innkaupasamnings](../procurement/purchase-agreements.md) | Skylda |
| Innkaup og aðföng | [Vistuð yfirlit fyrir framleiðslupantanir](saved-views-scm.md) | Skylda |
| Vöruupplýsingastjórnun | Forvinnsla uppskriftarskýrslu til að koma í veg fyrir tímalokun | Skylda |
| Vöruupplýsingastjórnun | Gera hverja fjárhagsvídd fyrir sig sjálfgefna þegar vörusniðmát er notað | Skylda |
| Vöruupplýsingastjórnun | Virkja afurðavíddaflokka fyrir vörusniðmát | Skylda |
| Vöruupplýsingastjórnun | Atriði - Endurbætur strikamerkjaeiningar | Skylda |
| Vöruupplýsingastjórnun | Endurgera heiti afurðarafbrigði í samræmi við nafnakerfi | Skylda |
| Vöruupplýsingastjórnun | [Vistuð yfirlit fyrir útgefnar afurðir](saved-views-scm.md) | Skylda |
| Vöruupplýsingastjórnun | [Endurbætur á tillögusíðu afbrigðis](../pim/tasks/create-predefined-product-variants.md) | Skylda |
| Sala og markaðsstarf | [Úthlutun gjalda í sölupöntun](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Skylda |
| Sala og markaðsstarf | Hreinsa uppfærsluferil sölupöntunar | Skylda |
| Sala og markaðsstarf | [Hreinsa uppfærsluferil sölu eftir aldri](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Skylda |
| Sala og markaðsstarf | [Fínstilling á útflutningi gagnaeiningar tengiliðar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Skylda |
| Sala og markaðsstarf | Afrita lokaafsláttarflokk fyrir kreditnótu sölu | Skylda |
| Sala og markaðsstarf | [Virkja uppflettingu á reitum upphafsorða og niðurlags í sölutilboðsskjölum](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Skylda |
| Sala og markaðsstarf | [Bæta afköst viðskiptavinaskýrslunnar „100 stærstu“](whats-new-scm-10-0-23.md) | Skylda |
| Sala og markaðsstarf | Hafa biðfærslur með í hreinsunarverki ferils | Skylda |
| Sala og markaðsstarf | Takmarka fjölda innkaupapöntunarlína í runuverki | Sjálfgefið kveikt |
| Sala og markaðsstarf | [Takmarka fjölda sölupantana sem hægt er að velja fyrir bókun](whats-new-scm-10-0-21.md) | Skylda |
| Sala og markaðsstarf | Endurreikna áætlaða stöðu viðskiptavinar | Skylda |
| Sala og markaðsstarf | [Skráning skilapöntunarlínu ásamt nákvæmum aukastöfum með og án framleiðsluþyngdar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Skylda |
| Sala og markaðsstarf | [Vistuð yfirlit fyrir sölu og markaðssetningu](saved-views-scm.md) | Skylda |
| Sala og markaðsstarf | [Staðfesting sölupöntunar með einum smelli](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Skylda |
| Flutningsstjórnun | Leyfa að fjarlægja jöfnun farmbréfa og farmreikningslína án bókaðrar reikningsbókar lánardrottins | Sjálfgefið kveikt |
| Flutningsstjórnun | [Virkja stofnun reikningabókar lánardrottins þegar farmbréfi er fleygt](whats-new-scm-10-0-20.md) | Sjálfgefið kveikt |
| Flutningsstjórnun | [Sending lítilla pakka](../warehousing/small-parcel-shipping.md) | Skylda |
| Flutningsstjórnun | [Skjal USMCA-upprunavottorðs](../transportation/usmca-certification-of-origin.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Viðbótargögn um staðsetningu](../warehousing/additional-location-zones.md) | Skylda |
| Vöruhúsakerfi | [Hætta við vinnu](../warehousing/cancel-warehouse-work.md) | Skylda |
| Vöruhúsakerfi | [Sameina sendingu](../warehousing/configure-shipment-consolidation-policies.md) | Skylda |
| Vöruhúsakerfi | [Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti](../warehousing/create-transfer-order-from-warehouse-app.md) | Skylda |
| Vöruhúsakerfi | Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Aftengja frágangsvinnu frá ASN (tilkynningum um sendingu)](whats-new-scm-10-0-21.md) | Skylda |
| Vöruhúsakerfi | [Frestuð frágangsaðgerð](../warehousing/deferred-processing-manual-inventory-movement.md) | Skylda |
| Vöruhúsakerfi | Frestaður frágangur - gámur | Sjálfgefið kveikt |
| Vöruhúsakerfi | Frestuð frágangsvinnsla – virkja fyrir eiginleika endurskoðunarsniðmáts þar sem virkjunartilvik er stillt á „Fyrra“ | Skylda |
| Vöruhúsakerfi | [Gera væntanlegar innhreyfingar úr gæðapöntunum óvirkar sem taka sýni af læstum birgðum](../inventory/inventory-blocking.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | Virkja hraðvirka prófun fyrir fartæki vöruhúss | Skylda |
| Vöruhúsakerfi | [Bættur þáttari fyrir GS1-strikamerki](../warehousing/gs1-barcodes.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Sveigjanleg frátekt á númeraplötu ráðstafaðrar pöntunar](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Skylda |
| Vöruhúsakerfi | [Sveigjanleg frátekt á vídd vöruhúsastigs](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Skylda |
| Vöruhúsakerfi | [Nýting á staðsetningu samstæðuvöru](../warehousing/item-consolidation-location-utilization.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | Móttökuferill númeraplötu | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Handvirk sameining sendingar](../warehousing/consolidate-shipments-manual-workbench.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur](whats-new-scm-10-0-28.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Viðmót efnismeðhöndlunarbúnaðar](../warehousing/mhax.md) | Skylda |
| Vöruhúsakerfi | [Nýjar síður á vinnubekknum áætlanagerð](whats-new-scm-10-0-24.md) | Almennt tiltækt |
| Vöruhúsakerfi | [Myndræn framsetning vinnuálags á útleið](../warehousing/outbound-workload-visualization.md) | Skylda |
| Vöruhúsakerfi | [Áætluð dreifing frá dreifingarstöð](../warehousing/planned-cross-docking.md) | Skylda |
| Vöruhúsakerfi | [Vinna úr viðburðum vöruhúsaforrits](../warehousing/warehouse-app-events.md) | Skylda |
| Vöruhúsakerfi | Endurbætur fyrirspurnar fyrir vinnusniðmát frágangs aukaafurða og hliðarafurða | Skylda |
| Vöruhúsakerfi | [Slétta magn niður í næstu sölueiningu við losun í vöruhús](whats-new-scm-10-0-19.md) | Skylda |
| Vöruhúsakerfi | [Vistað yfirlit fyrir vinnusvæði hleðsluáætlunar](saved-views-scm.md) | Skylda |
| Vöruhúsakerfi | [Vistað yfirlit fyrir upplýsingasíðu vinnu](saved-views-scm.md) | Skylda |
| Vöruhúsakerfi | [Vistað yfirlit fyrir bylgjuvinnslu](saved-views-scm.md) | Skylda |
| Vöruhúsakerfi | [Vistuð yfirlit fyrir hleðsluvinnslu](saved-views-scm.md) | Skylda |
| Vöruhúsakerfi | [Vistuð yfirlit fyrir úrvinnslu sendingar](saved-views-scm.md) | Skylda |
| Vöruhúsakerfi | [Skanna inn GS1-strikamerki](../warehousing/gs1-barcodes.md) | Almennt tiltækt |
| Vöruhúsakerfi | Upplýsingar um bylgjumerki sendingar | Skylda |
| Vöruhúsakerfi | [Setja blandaðar einingar í hólf](whats-new-scm-10-0-21.md) | Skylda |
| Vöruhúsakerfi | [Notaðu hraðvirkara API fyrir lokun/enduropnun gáma í pökkunarstöð](whats-new-scm-10-0-21.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Staðfesta sniðmát sem valin eru fyrir áfyllingarverk](whats-new-scm-10-0-20.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Stighækkaðir reitir vöruhúsaforrits](../warehousing/warehouse-app-promoted-fields.md) | Skylda |
| Vöruhúsakerfi | [Leiðbeiningar fyrir skref vöruhúsaforrits](../warehousing/mobile-app-titles-instructions.md) | Skylda |
| Vöruhúsakerfi | [Staðsetningarstaða vöruhúss](../warehousing/warehouse-location-status.md) | Skylda |
| Vöruhúsakerfi | [Hjáleiðir forrits Warehouse Management](../warehousing/warehouse-app-detours.md) | Sjálfgefið kveikt |
| Vöruhúsakerfi | [Skoða upplýsingar um runuvinnslu](../warehousing/wave-processing.md) | Skylda |
| Vöruhúsakerfi | [Tilkynningar bylgjukeyrslu](../warehousing/wave-execution-notifications.md) | Skylda |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Supply Chain Management 10.0.29 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.29 af Finance and Operations forritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingar sem fylgja hverri uppfærslu sem er hluti af útgáfu 10.0.29 skaltu skrá þig inn á Lifecycle Services (LCS) og skoða [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2022wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

The [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) grein lýsir eiginleikum sem hafa verið eða áætlað er að verði fjarlægðir eða úreltir fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um úreldingu tilkynnt í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) grein 12 mánuðum fyrir brottnám.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
