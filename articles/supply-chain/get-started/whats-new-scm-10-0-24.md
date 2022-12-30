---
title: Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management 10.0.24. (febrúar 2022)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9b4b538e6d50013626739e19fee2a050b630bf7f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334806"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management 10.0.24. (febrúar 2022)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.24. Þessi útgáfa er með byggingarnúmer 10.0.1084 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun á útgáfu:** desember 2021
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Janúar 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Febrúar 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þessi grein var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Dreifð blönduð grannfræði | [Endurbætt vinnuálag vöruhúsakeyrslu í kvörðunareiningum](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-warehousing.md) | Virkja að sjálfgefnu. |
| Dreifð blönduð grannfræði | [Hefja framleiðslupöntun á vinnuálagi vöruhúsakerfis fyrir kvörðunareiningu skýs og jaðars.](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-manufacturing.md) | Eiginleikastjórnun (*Hefja framleiðslupöntun á vinnuálagi vöruhúsakerfis fyrir kvörðunareiningu skýs og jaðars.*)  |
| Áætlun | [Stuðningur við fínstillingu áætlanagerðar fyrir mörk endurpöntunar og útgáfu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Öryggismörk](../master-planning/planning-optimization/safety-margins.md) | Virkja að sjálfgefnu. |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum þessara eiginleika þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Framleiðslustýring | Athugun á efnisframboði eftirspurnar fyrir framleiðslupantanir | Þessi eiginleiki er fljótari að opna síðuna **Framleiðslupantanir til að losa** sem er í boði á vinnusvæðinu **Stjórnun á framleiðslugólfi**. Án þessa eiginleika athugar kerfið sjálfkrafa hvort efni séu í boði fyrir allar skráðar framleiðslupantanir um leið og þú opnar síðuna, sem getur tekið umtalsverðan tíma ef þú ert með mikinn fjölda pantana. Þegar þessi eiginleiki er gerður virkur veitir kerfið í staðinn tækjastikuhnapp, sem hægt er að nota til að hefja efnisathugun aðeins fyrir valdar pantanir og þegar þörf krefur. |
| Framleiðslustýring | Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (ekki vöruhúsakerfi) | Þessi eiginleiki gerir starfsmönnum kleift að nota keyrsluviðmót framleiðslugólfsins til að skrá efnisnotkun, rununúmer og raðnúmer. Eiginleikinn styður aðeins atriði sem eru ekki virkjuð til að nota vöruhúsakerfisferla (WMS). Stuðningur við WMS-virka hluti er áætlaður fyrir framtíðarútgáfu.<p>Sumir framleiðendur, sérstaklega þeir sem eru í framleiðsluiðnaði, verða að skrá sérstaklega efnismagn sem er notað fyrir hverja runu eða framleiðslupöntun. Til dæmis gætu starfskraftar notað vog til að vigta magn efnis sem er notað á meðan þeir vinna. Til að tryggja fullan rekjanleika efnisins þurfa þessi fyrirtæki einnig að skrá hvaða rununúmer voru notuð við framleiðslu hverrar vöru. |
| Framleiðslustýring | Skrá sem tilbúið vinnuálag vöruhúsakerfis fyrir skýið og jaðareiningarkvarða | Þessi eiginleiki gerir starfsmönnum kleift að nota farsímaforrit vöruhúsakerfisins til að tilkynna framleiðslu- eða runupöntun sem lokið þegar forritið keyrir á móti vinnuálagi vöruhúsakerfis í skýja- eða kvörðunareiningu. Frekari upplýsingar eru í [Tilkynna sem lokið og ganga frá á einingakvarða](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Vöruhúsakerfi | Nýjar síður vinnusvæðis hleðsluáætlunar | Bætir við tveimur síðum fyrir vinnusvæði hleðsluáætlunar: **Vinnusvæði hleðsluáætlunar á innleið** og **Vinnusvæði hleðsluáætlunar á útleið**. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálpargreinum verið bætt við eða þau uppfærð. Þessi grein eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Kostnaðarstýring | [Birgðavirðisskýrslur](../cost-management/inventory-value-report-storage.md) |
| Kostnaðarstýring | [Dæmi og rök fyrir birgðavirðisskýrslu](../cost-management/inventory-value-report-examples.md) |
| Áætlanagerð | [Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar](../master-planning/planning-optimization/date-time-used.md) |
| Áætlanagerð | [Uppsetning eftirspurnarspár](../master-planning/demand-forecasting-setup.md) |
| Áætlanagerð | [Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur](../master-planning/safety-stock-journal.md) |
| Framleiðslustýring | [Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-customize.md) |
| Framleiðslustýring | [Hanna keyrsluviðmót framleiðslugólfsins](../production-control/production-floor-execution-styles.md) |
| Sala og markaðsstarf | [Tímasetja gagnahreinsun söluferils](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Vöruhúsakerfi | [Notandareikningar fartækis](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir fjármála- og rekstrarforrit.

Microsoft Dynamics 365 Supply Chain Management 10.0.24 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.24 á fjármála- og rekstrarforritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.24, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2021wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Greinin [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í greininni [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

