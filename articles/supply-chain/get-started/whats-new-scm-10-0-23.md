---
title: Forútgáfa af Dynamics 365 Supply Chain Management 10.0.23
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3cf30c203d936f171796d9dd8d766cbbb8c997e0
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647825"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023"></a>Forútgáfa af Dynamics 365 Supply Chain Management 10.0.23

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forútgáfu af útgáfu 10.0.23. Þessi útgáfa er með byggingarnúmer 10.0.1037 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun forútgáfu:** Október 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Desember 2021

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Í dálknum *Eiginleikar* eru tenglar í [útgáfuáætlunina](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) þar sem hægt er að skoða opinberar útgáfudagsetningar hvers eiginleika. Í dálknum *Frekari upplýsingar* eru frekari upplýsingar og/eða tenglar á tengd fylgiskjöl. Til að ákvarða hvernig eigi að virkja eiginleikann, sjá dálkinn *Virkjað af*. Nánari upplýsingar um notkun stjórnunar eiginleika er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Við gætum uppfært þetta efnisatriði til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Altæk aðsetursbók | Skilgreina sjálfgefið ríki/hérað fyrir hvert land/svæði í uppsetningu aðseturs | Nú getur þú skilgreint sjálfgefið ríki/hérað fyrir hvert land/svæði í uppsetningu aðseturs fyrir altæka aðsetursbók. Þegar sjálfgefið ríki/hérað er valið verður það sjálfgefið gildi sem slegið er inn í reitina ríki/hérað þegar þú stofnar nýja færslu sýslu eða borgar fyrir það land/svæði. Sjá einnig [Uppsetning aðseturs](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Virkja að sjálfgefnu. |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Gera hlé á verkum í farsímaforriti Warehouse Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis](../warehousing/warehouse-app-detours.md) | Eiginleikastjórnun (*Hjáleiðir forrits vöruhúsakerfis*) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Stighækkaðir reitir vöruhúsaforrits](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Skilgreina stighækkaða reiti fyrir skref í fartækinu](../warehousing/warehouse-app-promoted-fields.md)| Eiginleikastjórnun (*Stighækkaðir reitir vöruhúsaforrits*) |
| Framleiðslustýring | [Skýrsla um aukaafurðir og hliðarafurðir úr keyrsluviðmóti framleiðslugólfs](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Eiginleikastjórnun (*Skýrsla um aukaafurðir og hliðarafurðir úr keyrsluviðmóti framleiðslugólfs*) |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru nýjar í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum af þessum eiginleikum þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) þar sem þeir eru sýndir með heitinu sem sýnt er í dálknum *Eiginleikaheiti í eiginleikastjórnun* í eftirfarandi töflu.

| Kerfiseining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Eignastýring | Mótlyklar fyrir kostnað í færslubókum verkbeiðna | Þessi eiginleiki gerir þér kleift að tilgreina mótlykil fyrir allan kostnað í færslubók verkbeiðni. Hugsanlega tengir þú lánardrottnalykil yfirleitt við hvern kostnað fyrir sig, en aðrar gerðir lykla eru einnig studdar. Hann bætir tveimur nýjum dálkum (**Gerð mótlykils** og **Mótlykill**) við flýtiflipann **Kostnaður** á síðunni **Færslubók verkbeiðni**.|
| Birgða- og vöruhúsakerfi | \[Rússland\] Bóka fjárhagslegar Storno-birgðafærslur samkvæmt leiðréttingarflaggi í fjárhagsfylgiskjali fyrir sölupantanir | Þessi eiginleiki hefur áhrif á leiðréttingaraðgerð kreditnótu fyrir Rússland. Hann gerir kleift að bóka birgðafærslur fyrir sölureikninga í samræmi við valkost leiðréttingar í fjárhagnum. Þegar þessi eiginleiki er virkjaður er ekki lengur neitt misræmi milli flaggsins **Leiðrétting** í fjárhagsfylgiskjali birgðafærslu og flaggsins **Storno** í birgðafærslum. |
| Birgða- og vöruhúsakerfi | (Rússland) Keyra útreikninga veltuskýrslu birgðastöðu í runu | Fyrir rússneskar staðfæringar á Supply Chain Management býður þessi eiginleiki upp á möguleika á að keyra skýrsluna *Velta birgðastöðu* í runu, geyma hana og skoða skýrslur sem gerðar voru áður. |
| Birgða- og vöruhúsakerfi | (Rússland) Nota þýðingar á staðartungumál í lands- eða svæðisbundnum aðalskjámyndum í birgðastjórnun | Fyrir rússneskar staðfæringar á Supply Chain Management gerir þessi eiginleiki kleift að nota rússneskar þýðingar fyrir afurðir/vöruheiti og mælieiningar í eftirfarandi útprentunum rússneskra birgða: talningarlista (INV-3), talningarlista (INV-5) og talningarlista (INV-6). |
| Innkaup og aðföng | Hreinsa uppfærsluferil innkaupapöntunar | Þessi eiginleiki gerir þér kleift að hreinsa upp tímabundnar eldri færslur sem tengjast uppfærslum innkaupapöntunar. Hann bætir nýjum hnappi sem kallast **Hreinsa uppfærsluferil innkaupa** við aðgerðasvæðið á síðunni **Allar innkaupapantanir**. Þessi eiginleiki er sjálfgefið virkur. |
| Framleiðslustýring | (Forskoðun) Sjálfvirk tiltekt á efni sem virkjað er af vöruhúsi fyrir tiltektarlista sem bókaðir eru sjálfvirkt | Þessi eiginleiki býður upp á sjálfvirka tiltekt og leysa úr birgðavíddum fyrir sjálfvirka bókun á afleiddum og bakfærðum færslubókum tiltektarlista. |
| Framleiðslustýring | Sannprófa fyrningu hráefna á móti áætluðum notkunardegi | Þessi eiginleiki breytir því hvernig lokadagsetningar eru sannprófaðar þegar tekin er frá runa af hráefni til að nota við framleiðslu. Þegar þessi eiginleiki er virkjaður er lokadagsetning runu sannprófuð gagnvart áætluðum notkunardegi (dagsetningu hráefnis) eins og kemur fram í línu framleiðsluuppskriftar eða formúlulínu runupöntunar. Þegar slökkt er á þessum eiginleika er lokadagsetning runu sannprófuð gagnvart áætluðum afhendingardegi framleiðslu- eða runupöntunar (eins og áður). |
| Sala og markaðsstarf | Hreinsa uppfærsluferil sölupöntunar | Þessi eiginleiki gerir þér kleift að hreinsa upp tímabundnar eldri færslur sem tengjast uppfærslum sölupöntunar. Hann bætir við nýjum hnappi sem kallast **Hreinsa uppfærsluferil sölu** á aðgerðasvæði upplýsinga- og listasíðnanna fyrir sölupantanir. |
| Sala og markaðsstarf | Bæta afköst viðskiptavinaskýrslunnar „100 stærstu“ | Þessi eiginleiki bætir afköst viðskiptavinaskýrslunnar **100 stærstu** með því að keyra skýrsluna alltaf fyrir alla viðskiptavini (sem er fyrirhuguð notkun hennar) frekar en með því að leyfa sérsniðnar fyrirspurnir. Þegar þessi eiginleiki er virkjaður eru allar stillingar **Færslur til að taka með** gerðar óvirkar í skýrsluglugganum **100 stærstu**. |
| Vöruhúsakerfi | Stuðningur kvörðunareiningar fyrir losun í vöruhús á pöntunum á útleið | Þegar eiginleikinn er virkjaður er hægt að losa pantanir á útleið beint úr miðstöð í kvörðunareiningu þar sem pantanirnar verða uppfylltar. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þessi efnisatriði eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Umsjón hönnunarbreytinga | [Hönnunareigindir og leit að hönnunareigind](../engineering-change-management/engineering-attributes-and-search.md) lýsir nú hvernig erfðir hönnunareigindar virkar. |
| Áætlanagerð | [Aðaláætlanagerð með eftirspurnarspám](../master-planning/planning-optimization/demand-forecast.md) og [Minnkunarlyklar spár](../master-planning/reduction-keys.md) veita nú meiri upplýsingar um hvernig á að vinna með minnkunarlykla. |
| Áætlanagerð | [Uppfylling öryggisbirgða fyrir vörur](../master-planning/safety-stock-replenishment.md) veitir nú frekari upplýsingar um notkun lágmarks-/hámarkslykla. |
| Áætlanagerð | [Birgðaspár](../master-planning/inventory-forecast.md) veita nú meiri upplýsingar um úthlutun spáa. |
| Áætlanagerð | [Framboðsáætlun](../master-planning/supply-schedule.md) |
| Vöruhúsakerfi | [Altækar færibreytur fartækja](../warehousing/mobile-device-parameters.md) |
| Vöruhúsakerfi | [Festing](../warehousing/anchoring.md) |
| Sala og markaðsstarf | Viðskiptum innan samstæðu er nú lýst í þaula og byrjar á [Setja upp samstæðuviðskipti](../sales-marketing/intercompany-trade-set-up.md) og tengdum efnisatriðum. |
| Birgðir | Fylgigögn birgðasýnileika hafa verið stækkuð og uppfærð og byrja á [Yfirlit viðbótar fyrir sýnileika birgða](../inventory/inventory-visibility.md) og tengdum efnisatriðum. |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir forrit Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.23 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.23 í Finance and Operations-forritum (nóvember 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.23, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2021wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
