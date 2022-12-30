---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.28.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427821"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.28 (ágúst 2022)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.28. Þessi útgáfa er með smíðarnúmer 10.0.1264 og er í boði á eftirfarandi áætlun:

- **Forskoðun á útgáfu:** maí 2022
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Júlí 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Júlí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að hafa með eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Samþættingareiningar heildarkostnaðar fyrir flutningsmiðlara þriðja aðila](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Yfirlitseiningar heildarkostnaðar](../landed-cost/landed-cost-entities-overview.md) | Virkja að sjálfgefnu |
| Áætlun | [Eftirspurnarstýrð efnisþarfaráætlun (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Eftirspurnarstýrð efnisþarfaráætlun yfirlit](../master-planning/planning-optimization/ddmrp-overview.md) | Stjórnun eiginleika:<br>*(Forútgáfa) DDMRP fyrir fínstillingu áætlanagerðar* |
| Áætlun | [Stuðningur fyrir fínstillingu áætlanagerðar fyrir óhætt að lofa (CTP-afhendingargetu)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [Reikna afhendingardaga sölupöntunar með CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | Stjórnun eiginleika:<br>*(Forútgáfa) CTP-afhendingargeta fyrir fínstillingu áætlanagerðar* |
| Áætlun | [Stuðningur fyrir fínstillingu áætlanagerðar fyrir endingartíma](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [Aðaláætlanagerð fyrir vörur með takmarkaðan endingartíma](../master-planning/planning-optimization/shelf-life.md) | Virkja að sjálfgefnu |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum þessara eiginleika þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Birgða- og vöruhúsakerfi | Virkja lagerbirgðir innan samstæðu til að sýna aðeins lagerbirgðir með annað en núll í magni | Þessi eiginleiki gerir þér kleift að velja hvort eig að taka með vörur með núll í birgðamagni í lagerbirgðalista samstæðunnar. Hægt er að stjórna þessum valkosti með stillingunni **Ekki sýna atriði með núll í lagerbirgðum á listanum yfir lagerbirgðir innan samstæðu** sem þessi eiginleiki bætir við á síðuna **Færibreytur birgða- og vöruhúsakerfis**. |
| Birgða- og vöruhúsakerfi | (Indland) Fyrir reglur um flutningsverð skal hunsa staðsetningu þegar „Frá vöruhúsakóði“ er stilltur á „Allt“ | <p>Þessi eiginleiki á aðeins við um staðfæringu fyrir Indland. Það gerir ferlið við að setja upp flutningsverð fyrir hluti í birgðaflutnings innsæisríkara.</p><p>Flutningsverð eru sett upp með því að skilgreina hverja vörur með verðlagningarreglum flutnings. Ein leið til að gera þessa skilgreiningu er að hafa með reglulínu þar sem reiturinn **Kóði „Frá vöruhúsi“** er stilltur á *Öll*. Þessi stilling gefur til kynna að flutningsverðið sem er skilgreint af línunni eigi að gilda óháð vöruhúsinu sem varan er sótt úr. Þegar þessi eiginleiki er gerður virkur munu reglur um flutningsverð þar sem reiturinn **Kóði „Frá vöruhúsi“** er stilltur á *Öll* hunsa stillinguna **Staðsetning**. Því mun reglan gilda óháð staðsetningu sem tilgreind er á flutningspöntuninni. Þessi hegðun er líklega það sem búist er við vegna þess að staðsetning er fyrir neðan vöruhús í geymsluvíddastigveldinu.</p><p>Án þessa eiginleika mun kerfið aðeins beita reglum af þessu tagi þegar staðsetningin í flutningspöntuninni stemmir nákvæmlega við staðsetninguna sem er valin fyrir regluna. (Ef auður staður er stilltur fyrir regluna mun kerfið aðeins nota regluna til að flytja pantanir sem hafa einnig autt gildi fyrir staðsetninguna.)</p> |
| Birgða- og vöruhúsakerfi | Gagnahreinsun lagerbirgðaskýrslu | Þessi eiginleiki býður upp á leið til að hreinsa gögn sem notuð eru til að búa til *Birgðalagersskýrslur*. |
| Framleiðslustýring | Úthluta verkþáttum fyrir þjónustusamning og þjónustupöntunarlínur | Þessi eiginleiki bætir reit sem heitir **Verkþáttur** við þjónustusamning og þjónustupöntunarlínur þannig að hægt sé að velja verkþátt fyrir þær. Eiginleikinn hjálpar til við að koma í veg fyrir útilokunarvillur þegar bókaðar eru færslubækur þjónustustjórnunar sem þurfa valinn verkþátt.  |
| Vöruhúsakerfi | Handvirk tiltektarþjónusta flutningslínu fyrir stjórnanda eða aðra trausta notendur | Þessi eiginleiki gerir stjórnendum kleift að velja birgðafærslur sem tengjast flutningslínum á handvirkan hátt. Þessar línur innihalda línur sem þegar hafa verið losaðar í vöruhúsið. Stjórnendur ættu aðeins að framkvæma þessa tínslu í undantekningartilvikum, t.d. þegar skemmdir verða á kerfinu. Frekari upplýsingar er að finna í [Afgreiða undantekningar á tiltekt sölu- og flutningslína handvirkt](../warehousing/manual-order-line-picking-exception-handling.md). |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálpargreinum verið bætt við eða þau uppfærð. Þessi grein eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hlutum. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Kostnaðarstýring | [Fast kostnaðarverð](../cost-management/fixed-receipt-price.md) |
| Kostnaðarstýring | [Algengar spurningar um birgðakostnað](../cost-management/inventory-costing-faq.md) |
| Kostnaðarstýring | [Reikningsskilaregla bóka á gjaldalykil](../cost-management/post-to-charge-account-accounting-principle.md) |
| Birgðir | [Birgðafærsluupplýsingar](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir fjármála- og rekstrarforrit.

Microsoft Dynamics 365 Supply Chain Management 10.0.28 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.28 á fjármála- og rekstrarforritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.28, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun](/dynamics365-release-plan/2022wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Greinin [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í greininni [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

