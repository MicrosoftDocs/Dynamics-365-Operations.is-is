---
title: Forskoðun Dynamics 365 Supply Chain Management 10.0.24 (febrúar 2022)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f6402d7f9f433ca621c475bd62553529943dbe62
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920549"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>Forskoðun Dynamics 365 Supply Chain Management 10.0.24 (febrúar 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forútgáfu af útgáfu 10.0.24. Þessi útgáfa er með byggingarnúmer 10.0.1084 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun á útgáfu:** desember 2021
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Janúar 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Febrúar 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þetta efnisatriði til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Dreifð blönduð grannfræði | [Aukið álag á framkvæmd vöruhúsa á mælieiningum](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-warehousing.md) | Virkja að sjálfgefnu. |
| Áætlun | [Stuðningur við skipulagningu hagræðingar fyrir endurpöntunarbil og útgáfubil](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Öryggismörk](../master-planning/planning-optimization/safety-margins.md) | Virkja að sjálfgefnu. |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Kerfiseining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Framleiðslustýring | Athugun á efnisframboði eftirspurnar fyrir framleiðslupantanir | Þessi eiginleiki gerir það hraðari að opna **Framleiðslupantanir til að gefa út** síðu, sem er aðgengileg frá **Stjórnun framleiðslugólfs** vinnurými. Án þessa eiginleika athugar kerfið sjálfkrafa hvort efni sé tiltækt fyrir allar skráðar framleiðslupantanir um leið og þú opnar síðuna, sem getur tekið töluverðan tíma ef þú ert með mikinn fjölda pantana. Þegar þessi eiginleiki er virkur býður kerfið í staðinn upp tækjastikuhnapp, sem þú getur notað til að hefja efnisskoðun aðeins fyrir valdar pantanir og þegar þörf krefur. |
| Framleiðslustýring | (Forútgáfa) Skrá efnisnotkun í keyrsluviðmóti framleiðslugólfs (ekki vöruhúsakerfi) | Þessi eiginleiki gerir starfsmönnum kleift að nota framkvæmdarviðmót framleiðslugólfs til að skrá efnisnotkun, lotunúmer og raðnúmer. Þessi eiginleiki styður aðeins hluti sem eru ekki virkjaðir til að nota háþróaða vöruhúsaferla (WMS). Stuðningur við WMS-virka hluti er áætlaður í framtíðarútgáfu.<p>Sumir framleiðendur, sérstaklega þeir sem eru innan vinnsluiðnaðarins, þurfa að skrá sérstaklega magn efnis sem neytt er fyrir hverja lotu eða framleiðslupöntun. Til dæmis gætu starfsmenn notað vog til að vega magn efnis sem neytt er á meðan þeir vinna. Til að tryggja fullan rekjanleika efnis þurfa þessar stofnanir einnig að skrá hvaða lotunúmer voru notuð við framleiðslu hverrar vöru. |
| Framleiðslustýring | Tilkynntu sem lokið um vinnuálag vöruhúsastjórnunar fyrir skýja- og brúnkvarðaeininguna | Þessi eiginleiki gerir starfsmönnum kleift að nota Vöruhússtjórnun farsímaforritið til að tilkynna framleiðslu- eða lotupöntun eins og hún er lokið þegar appið er í gangi gegn vöruhúsastjórnunarvinnuálagi á skýja- eða brúnkvarðaeiningu. Fyrir frekari upplýsingar, sjá [Tilkynntu sem lokið og settu í burtu á mælikvarðaeiningu](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Framleiðslustýring | Hefja framleiðslupöntun á vinnuálagi vöruhúsastjórnunar fyrir skýja- og jaðarkvarðaeininguna | Þessi eiginleiki gerir starfsmönnum kleift að nota Vöruhússtjórnun farsímaforritið til að hefja framleiðslu eða lotupöntun þegar appið er í gangi gegn vöruhúsastjórnunarvinnuálagi á skýja- eða jaðarkvarðaeiningu. |
| Vöruhúsakerfi | Nýjar síður á vinnubekknum áætlanagerð | Virkjar tvær nýjar vinnubekkssíður fyrir áætlanagerð: **Vinnubekkur fyrir skipulagningu álags á innleið** og **Áætlunarbekkur á útleið**. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þessi efnisatriði eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Kostnaðarstýring | [Birgðavirðisskýrslur](../cost-management/inventory-value-report-storage.md) |
| Kostnaðarstýring | [Dæmi og rök fyrir birgðavirðisskýrslu](../cost-management/inventory-value-report-examples.md) |
| Áætlanagerð | [Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar](../master-planning/planning-optimization/date-time-used.md) |
| Áætlanagerð | [Uppsetning eftirspurnarspár](../master-planning/demand-forecasting-setup.md) |
| Áætlanagerð | [Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur](../master-planning/safety-stock-journal.md) |
| Framleiðslustýring | [Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-customize.md) |
| Framleiðslustýring | [Hanna keyrsluviðmót framleiðslugólfsins](../production-control/production-floor-execution-styles.md) |
| Sala og markaðsstarf | [Afkastaendurbætur á hreinsun söluferils](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Vöruhúsakerfi | [Notandareikningar fartækis](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir forrit Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.24 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.24 í Finance and Operations-forritum (nóvember 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.24, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

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