---
title: Forskoðun Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813170"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Forskoðun Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efni sýnir eiginleika sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forskoðunarútgáfa 10.0.28. Þessi útgáfa hefur byggingarnúmer 10.0.1264 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun á útgáfu:** maí 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Júlí 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Júlí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þetta efni til að innihalda eiginleika sem var bætt við bygginguna eftir að þetta efni var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Landað kostnaðarsamþættingareiningar fyrir flutningsmiðlara þriðja aðila](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Yfirlit yfir landaða kostnaðaraðila](../landed-cost/landed-cost-entities-overview.md) | Sjálfgefið virkt |
| Áætlun | [Stuðningur við skipulagningu hagræðingar fyrir geymsluþol](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Væntanlegt <!-- KFM: Vendor is preparing this. Expected May 20. --> | Sjálfgefið virkt |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það inn [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Birgða- og vöruhúsakerfi | Virkja á milli fyrirtækja á lager til að sýna aðeins magn sem ekki er núll | Þessi eiginleiki gerir þér kleift að velja hvort vörur með núll birgðamagn eigi að vera með í birgðalistanum milli fyrirtækja. Þú getur stjórnað þessum valkosti með því að nota **Ekki sýna vörur með núll birgðamagni á millifyrirtækjalistanum** stilling, sem þessi eiginleiki bætir við **Birgða- og vöruhúsastjórnunarfæribreytur** síðu. |
| Birgða- og vöruhúsakerfi | (Indland) Fyrir reglur um flutningsverð skal hunsa staðsetningu þegar „Frá vöruhúsakóði“ er stilltur á „Allt“ | <p>Þessi eiginleiki á aðeins við um staðsetningar á Indlandi. Það gerir ferlið við að setja upp flutningsverð fyrir vörur í birgðaflutningum leiðandi.</p><p>Þú setur upp millifærsluverð með því að stilla hverja vöru með milliverðsreglum. Ein leið til að gera þessa stillingu er að innihalda reglulínu þar sem **Frá vöruhúsakóða** reiturinn er stilltur á *Allt*. Þessi stilling gefur til kynna að flutningsverðið sem er skilgreint af línunni ætti að gilda óháð vöruhúsi sem varan er tekin úr. Þegar þessi eiginleiki er virkur, gilda millifærsluverðsreglur þar sem **Frá vöruhúsakóða** reiturinn er stilltur á *Allt* mun hunsa **Staðsetning** stilling. Þess vegna mun reglan gilda óháð staðsetningu sem tilgreind er á millifærslupöntuninni. Þessi hegðun er líklega það sem búist er við, vegna þess að staðsetning er fyrir neðan vöruhús í stigveldi geymsluvíddar.</p><p>Án þessa eiginleika mun kerfið aðeins nota reglur af þessari gerð þegar staðsetningin á flutningspöntuninni samsvarar nákvæmlega staðsetningunni sem er stillt fyrir regluna. (Ef auð staðsetning er stillt fyrir regluna mun kerfið nota regluna aðeins til að flytja pantanir sem hafa einnig autt gildi fyrir staðsetninguna.)</p> |
| Birgða- og vöruhúsakerfi | Gagnahreinsun lagerbirgðaskýrslu | Þessi eiginleiki veitir leið til að hreinsa upp gögnin sem eru notuð til að búa til *Geymsla birgðaskýrslu á hendi* skýrslur. |
| Framleiðslustýring | Úthluta verkþáttum fyrir þjónustusamning og þjónustupöntunarlínur | Þessi eiginleiki bætir við reit sem er nefndur **Verkefnavirkni** til þjónustusamnings og þjónustupöntunarlína, þannig að hægt sé að stilla verkvirkni fyrir þær. Eiginleikinn mun hjálpa til við að koma í veg fyrir blokkunarvillur þegar þú bókar þjónustustjórnunarverkefnabækur sem krefjast þess að verkvirkni sé stillt.  |
| Vöruhúsakerfi | Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur | Þessi eiginleiki gerir stjórnendum kleift að velja birgðafærslur handvirkt sem tengjast flutningslínum. Þessar línur innihalda línur sem þegar hafa verið losaðar í vöruhúsið. Stjórnendur ættu aðeins að velja í undantekningartilvikum, svo sem þegar kerfið er í skemmdu ástandi. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Við höfum nýlega bætt við eða uppfært umtalsvert eftirfarandi hjálparefni. Þessi efni eru ekki endilega tengd nýju eiginleikum sem bætt var við fyrir þessa útgáfu, eins og skráð er í fyrri köflum. Hins vegar gætu þeir hjálpað þér að fá meira út úr núverandi eiginleikum.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Kostnaðarstýring | [Fast kostnaðarverð](../cost-management/fixed-receipt-price.md) |
| Kostnaðarstýring | [Algengar spurningar um birgðakostnað](../cost-management/inventory-costing-faq.md) |
| Kostnaðarstýring | [Bóka til gjaldfærslu reikningsskilareglu](../cost-management/post-to-charge-account-accounting-principle.md) |
| Birgðir | [Upplýsingar um birgðafærslur](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Supply Chain Management 10.0.28 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.28 af Finance and Operations forritum (júní 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.28, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

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
