---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 184da494b9998e3e1cf6bd1639b452192d7e7857
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427821"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)

[!include [banner](../includes/banner.md)]

Þessi grein sýnir eiginleika sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfa 10.0.28. Þessi útgáfa hefur byggingarnúmer 10.0.1264 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun á útgáfu:** maí 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Júlí 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Júlí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að innihalda eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Landað kostnaðarsamþættingareiningar fyrir flutningsmiðlara þriðja aðila](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Yfirlitseiningar heildarkostnaðar](../landed-cost/landed-cost-entities-overview.md) | Sjálfgefið virkt |
| Áætlun | [Eftirspurnarstýrð efnisþarfaráætlun (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Eftirspurnardrifin efnisþörf Skipulagsyfirlit](../master-planning/planning-optimization/ddmrp-overview.md) | Eiginleikastjórnun:<br>*(Forútgáfa) DDMRP fyrir fínstillingu áætlanagerðar* |
| Áætlun | [Stuðningur við skipulagningu hagræðingar fyrir lofað geta (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Eiginleikastjórnun:<br>*(Forútgáfa) CTP-afhendingargeta fyrir fínstillingu áætlanagerðar* |
| Áætlun | [Stuðningur við skipulagningu hagræðingar fyrir geymsluþol](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Aðaláætlanagerð fyrir vörur með takmarkað geymsluþol](../master-planning/planning-optimization/shelf-life.md) | Sjálfgefið virkt |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það inn [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Birgða- og vöruhúsakerfi | Virkja lagerbirgðir innan samstæðu til að sýna aðeins lagerbirgðir með annað en núll í magni | Þessi eiginleiki gerir þér kleift að velja hvort vörur með núll birgðamagn eigi að vera með á millifyrirtækjalistanum. Þú getur stjórnað þessum valkosti með því að nota **Ekki sýna vörur með núll birgðamagni á millifyrirtækjalistanum** stilling, sem þessi eiginleiki bætir við **Færibreytur birgða- og vöruhúsastjórnunar** síðu. |
| Birgða- og vöruhúsakerfi | (Indland) Fyrir reglur um flutningsverð skal hunsa staðsetningu þegar „Frá vöruhúsakóði“ er stilltur á „Allt“ | <p>Þessi eiginleiki á aðeins við um staðsetningar á Indlandi. Það gerir ferlið við að setja upp flutningsverð fyrir vörur í birgðaflutningum leiðandi.</p><p>Þú setur upp millifærsluverð með því að stilla hverja vöru með milliverðsreglum. Ein leið til að gera þessa stillingu er að innihalda reglulínu þar sem **Frá vörugeymslukóða** reiturinn er stilltur á *Allt*. Þessi stilling gefur til kynna að flutningsverðið sem er skilgreint af línunni ætti að gilda óháð vöruhúsi sem varan er tekin úr. Þegar þessi eiginleiki er virkur, gilda millifærsluverðsreglur þar sem **Frá vörugeymslukóða** reiturinn er stilltur á *Allt* mun hunsa **Staðsetning** stilling. Þess vegna mun reglan gilda óháð staðsetningu sem tilgreind er á millifærslupöntuninni. Þessi hegðun er líklega það sem búist er við, vegna þess að staðsetning er fyrir neðan vöruhús í stigveldi geymsluvíddar.</p><p>Án þessa eiginleika mun kerfið aðeins nota reglur af þessu tagi þegar staðsetningin á millifærslupöntuninni samsvarar nákvæmlega staðsetningunni sem er stillt fyrir regluna. (Ef auð staðsetning er stillt fyrir regluna mun kerfið nota regluna aðeins til að flytja pantanir sem hafa einnig autt gildi fyrir staðsetninguna.)</p> |
| Birgða- og vöruhúsakerfi | Gagnahreinsun lagerbirgðaskýrslu | Þessi eiginleiki veitir leið til að hreinsa upp gögnin sem eru notuð til að búa til *Geymsla birgðaskýrslu á hendi* skýrslur. |
| Framleiðslustýring | Úthluta verkþáttum fyrir þjónustusamning og þjónustupöntunarlínur | Þessi eiginleiki bætir við reit sem er nefndur **Verkefnavirkni** til þjónustusamnings og þjónustupöntunarlína, þannig að hægt sé að stilla verkvirkni fyrir þær. Eiginleikinn mun hjálpa til við að koma í veg fyrir blokkunarvillur þegar þú bókar þjónustustjórnunarverkefnabækur sem krefjast þess að verkvirkni sé stillt.  |
| Vöruhúsakerfi | Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur | Þessi eiginleiki gerir stjórnendum kleift að velja birgðafærslur handvirkt sem tengjast flutningslínum. Þessar línur innihalda línur sem þegar hafa verið losaðar í vöruhúsið. Stjórnendur ættu aðeins að velja í undantekningartilvikum, eins og þegar kerfið er í skemmdu ástandi. Fyrir frekari upplýsingar, sjá [Meðhöndla handvirkt undantekningar frá sölu og flutningslínutínslu](../warehousing/manual-order-line-picking-exception-handling.md). |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Við höfum nýlega bætt við eða uppfært umtalsvert eftirfarandi hjálpargreinar. Þessar greinar eru ekki endilega tengdar nýjum eiginleikum sem bætt var við fyrir þessa útgáfu, eins og skráð er í fyrri köflum. Hins vegar gætu þeir hjálpað þér að fá meira út úr núverandi eiginleikum.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Kostnaðarstýring | [Fast kostnaðarverð](../cost-management/fixed-receipt-price.md) |
| Kostnaðarstýring | [Algengar spurningar um birgðakostnað](../cost-management/inventory-costing-faq.md) |
| Kostnaðarstýring | [Reikningsskilaregla bóka á gjaldalykil](../cost-management/post-to-charge-account-accounting-principle.md) |
| Birgðir | [Birgðafærsluupplýsingar](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Uppfærslur á vettvangi fyrir fjármála- og rekstraröpp

Microsoft Dynamics 365 Supply Chain Management 10.0.28 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.28 af fjármála- og rekstrarforritum (ágúst 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.28, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun](/dynamics365-release-plan/2022wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

The [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) grein lýsir eiginleikum sem hafa verið eða áætlað er að verði fjarlægðir eða úreltir fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um úreldingu tilkynnt í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) grein 12 mánuðum fyrir brottnám.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

