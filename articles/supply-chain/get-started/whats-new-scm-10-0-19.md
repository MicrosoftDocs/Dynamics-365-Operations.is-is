---
title: Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management útgáfu 10.0.19 (júní 2021)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bd82ad9a0eb2f8f85bc7dad0ae174726234ad84f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474893"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management útgáfu 10.0.19 (júní 2021)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.19. Þessi útgáfa er með byggingarnúmer 10.0.837 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun útgáfu:** Apríl 2021
- **Almennt framboð losunar (handvirk uppfærsla):** Júní 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Júní 2021

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Í dálknum *Eiginleikar* eru tenglar í [útgáfuáætlunina](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) þar sem hægt er að skoða opinberar útgáfudagsetningar hvers eiginleika. Í dálknum *Frekari upplýsingar* eru frekari upplýsingar og/eða tenglar á tengd fylgiskjöl.

Flestir þessara eiginleika verða að vera virkir með [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) áður en þú getur notað þá.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar |
|---|---|---|
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Samþykkja og vista sendar bankaupplýsingar lánardrottins](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Vinna með bankareikningsupplýsingar lánardrottna](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Birgða- og vörustjórnun | [Fínstilling á útflutningi gagnaeiningar tengiliðar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Þegar þessi eiginleiki er virkur, leiða breytingar á gögnum sem vísað er til ekki til þess að tengdir tengiliðir verði teknir með í næsta stigvaxandi útflutningi. Þegar þessi eiginleiki er gerður óvirkur leiða breytingar á gögnum sem vísað er í til þess að tengdir tengiliðir verði teknir með í næsta stigvaxandi útflutningi. |
| Birgða- og vörustjórnun | [Smávægilegar endurbætur fyrir keyrsluhæfni vöruhúss með kvarðaeiningum](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Skilaboð um skilaboðaúrvinnslu](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Birgðaleiðrétting vöruhúss](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Birgða- og vörustjórnun | [Flettivirkni fyrir reiti upphafsorða og lokaorða skjala á sölutilboðssíðu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Þessi eiginleiki bætir við uppflettivirkni fyrir reitina **Skjalakynning** og **Skjalaniðurstaða** á síðunni **Sölutilboð**.<br><br>Þessi eiginleiki er sjálfgefið virkur. |
| Birgða- og vörustjórnun | [Vöruhúsakeyrsla með jaðareiningakvörðum á sérsniðnum vélbúnaði](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Framleiðsla | [Framkvæmd framleiðslu með jaðareiningakvörðum á sérsniðnum vélbúnaði](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Áætlun | [Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Röðun með ótakmarkaða getu](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Áætlun | Fyrirspurnarbyggð staðfesting áætlaðrar pantanar | [Staðfesta áætlaðar pantanir](../master-planning/planning-optimization/planned-order-firming.md) |
| Vöruupplýsingastjórnun | [Endurbætur á tillögusíðu afbrigðis](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Stofna forskilgreind afurðarafbrigði](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur í þessari útgáfu. Hver þeirra býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram). Ef nota á einhvern þessara eiginleika þarf að virkja þá sérstaklega í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eiginleikasvæði | Eiginleika&nbsp;heiti&nbsp;í eiginleika&nbsp;stjórnun | Meiri upplýsingar |
|---|---|---|
| Sala og markaðsstarf | Endurbætur á afköstum hreinsunar á söluferli | Hreinsun söluferils getur tekið langan tíma ef hún er sjaldan keyrð í umhverfum þar sem er mikið um söluuppfærslur. Til að stytta tímann og auka áreiðanleikann mun þessi eiginleiki skipta hreinsun niður í runur og keyra þær í stuttan tíma í einu. Ef mögulegt mun geta gagnagrunnsins vera notuð til að lágmarka læsingu og forðast að sameina færslutöflur við hreinsun. |
| Sala og markaðsstarf | Uppfæra umbeðna móttökudagsetningu með staðfestri dagsetningu fyrir pantanir innan samstæðu | Þessi eiginleiki gerir kleift að stjórna því hvað gerist fyrir reitargildi sölu- og innkaupadagsetninga þegar beinar afhendingar innan samstæðu eru notaðar. Hægt er að velja hvort kerfið uppfæri umbeðnar dagsetningar eða sleppi því að uppfæra þær. Ef uppfærslunni er sleppt munu umbeðnar dagsetningar sýna það sem viðskiptavinurinn hefur óskað eftir. Ef uppfærslur eru virkjaðar munu umbeðnar dagsetningar (þegar stjórnun afhendingardagsetningar er notuð) aðeins sýna í upphafi það sem viðskiptavinurinn hefur óskað eftir. Stjórnun afhendingardags, þegar hann er annar en *Enginn*, mun hnekkja því sem var óskað eftir í upphafi. Hægt er að stjórna þessum valkosti með nýju stillingunni **Uppfæra umbeðna móttökudagsetningu með staðfestri dagsetningu** í stillingum lánardrottins eða viðskiptavinar innan samstæðu.<br><br>Ef slökkt er á eiginleikanum mun kerfið skrifa yfir umbeðna móttökudagsetningu á upprunalegum sölupöntunum samkvæmt reglu um stjórnun afhendingardagsetningar, en umbeðin flutningsdagsetning helst óbreytt. |
| Vöruhúsakerfi | Slétta magn niður í næstu sölueiningu við losun í vöruhús | Þessi eiginleiki bætir við valkosti sem getur takmarkað pöntunarmagn við losun í vöruhús. Þegar hann er virkur verður pöntunarmagn sléttað niður í næstu heilu sölueiningu og losun á pöntunum sem innihalda magn sem nemur minna en einni sölueiningu verður hafnað. |
| Vöruhúsakerfi | Bylgjuaðferðin „Áætla stofnun vinnu“ fyrir allt fyrirtækið | Við virkjun á þessum eiginleika verður bylgjuaðferðin *Áætla stofnun vinnu* skilgreind til að keyra samhliða í öllum lögaðilum. Nokkrar stillingar í viðbót verða einnig fyrir áhrifum. Fyrir ítarlegar upplýsingar skal skoða [Áætla stofnun vinnu í bylgju](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þær eru ekki endilega tengdar við nýja eiginleika sem bætt er við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta, en þær geta hjálpað notendum að fá meira út úr fyrirliggjandi eiginleikum.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Umsjón hönnunarbreytinga | [Algengar spurningar um hönnunarbreytingar](../engineering-change-management/change-management-faq.md) |
| Innkaup og aðföng | [Tegundarbeiðni frá lánardrottnum](../procurement/category-requests-from-vendors.md) |
| Vöruupplýsingastjórnun | [Stjórna mælieiningu](../pim/tasks/manage-unit-measure.md)<br><br>[Útreikningar afbrigðalíkans afurðar](../pim/config-model-calculations.md) |
| Framleiðslustýring | [Samræmd númeraröð fyrir vinnslukenni](../production-control/unified-job-ids.md) |
| Flutningsstjórnun | [LTL-klasar](../transportation/ltl-class.md)<br><br>[NMFC-kóðar](../transportation/nmfc-codes.md) |
| Vöruhúsakerfi, stofnun og meðhöndlun bylgju | [Stofnun og meðhöndlun bylgju](../warehousing/wave-processing.md)<br><br>[Færibreytur vöruhúss fyrir bylgjuvinnslu](../warehousing/wave-warehouse-parameters.md)<br><br>[Bylgjusniðmát](../warehousing/wave-templates.md)<br><br>[Bylgjuúthlutun](../warehousing/wave-allocation-method.md)<br><br>[Áætla stofnun vinnu í bylgju](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Gámun](../warehousing/wave-containerization.md)<br><br>[Tilkynningar bylgjukeyrslu](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir forrit Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.19 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.19 í Finance and Operations-forritum (júní 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.19, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 útgáfa bylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Skoðaðu [Dynamics 365: 2021 útgáfu bylgju 1 áætlun](/dynamics365-release-plan/2021wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
