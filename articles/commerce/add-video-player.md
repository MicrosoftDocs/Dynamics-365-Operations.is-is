---
title: Myndspilaraeining
description: Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025650"
---
# <a name="video-player-module"></a>Myndspilaraeining


[!include [banner](includes/banner.md)]

Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Myndspilaraeiningin er notuð til að styðja myndspilun. Hægt er að bæta henni við hvaða síðu sem er, að því tilskildu að myndbandsefni sé hlaðið upp á og tiltækt í efnisstjórnunarkerfinu (CMS). Myndbandsspilarann styður .mp4 miðlunargerðina.

## <a name="video-player-module"></a>Myndspilaraeining

Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu. Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð, hljóðlýsingum og lokuðum myndatexta. Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft. Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.

Myndbandsspilaeiningin styður einnig aðrar hljóðrásir. Þegar myndskeiði er hlaðið upp í CMS er einnig hægt að hlaða upp annari hljóðrás. Síðan getur myndskeiðsspilarinn spilað seinni hljóðrásina ef notandi velur það.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Dæmi um myndspilareiningar í rafrænni verslun

- Leiðbeinandi myndbönd á vöruupplýsingasíðum eða markaðssíðum
- Kynningarmyndbönd eða myndbönd um stefnu á hvaða markaðssíðu sem er
- Markaðssetningarmyndbönd sem varpa ljósi á vöruaðgerðir á upplýsingasíðum eða markaðssíðum

### <a name="video-player-module-properties"></a>Eiginleikar myndspilaraeiningar

| Nafn eiginleika         | Virði                               | Lýsing |
|-----------------------|-------------------------------------|-------------|
| Sjálfvirk spilun             | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið sjálfkrafa spilað. |
| Þagga                  | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er skrúfað fyrir hljóðið. Fyrir þennan spilara er sjálfgildið **Ósatt**. Í Chrome-vafranum er sjálfvirk spilun myndskeiða sjálfgefið þögguð og hljóðið er aðeins spilað ef notandinn spilar myndbandið handvirkt. |
| Lykkja                  | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið endurtekið í lúppu. |
| Miðlar                 | Skráarslóð og -heiti myndskeiðs | Myndskeiðið sem er spilað í myndspilaranum. |
| Spila á öllum skjánum       | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið spilað á öllum skjánum. |
| Spila/hlé    | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu. |
| Stýringar myndspilara | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** eru öll stjórntæki myndbandsspilarans sýnd. Þessar stjórntæki fela í sér spilunar- og hléhnappa, framvinduvísir og valkosti fyir lokaða myndatexta. |
| Fela forsíðumynd     | **Satt** eða **Ósatt**               | Myndskeið getur verið með plakatramma. Þegar gildið þessa eiginleika er stillt á **Satt** er plakatramminn falinn. |
| Sniðmátsstig            | Tölugildi frá **0** til og með **100** | Sniðmátið sem er beitt á myndskeiðið til útlitshönnun. |

## <a name="add-a-video-player-module-to-a-page"></a>Bæta við myndspilaraeiningu á síðu

> [!NOTE] 
> Áður en þú býrð til myndspilaraeiningu verðurðu fyrst að hlaða upp myndskeiði á fjölmiðlasafnið.

Fylgdu þessum skrefum til að bæta myndspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **myndspilarasniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við gámaeiningu.
1. Bætið við myndspilara- og umhverfismyndspilaraeiningunum í gámaeiningunni.
1. Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.
1. Notaðu myndspilarasniðmátið sem þú stofnaðir til að búa til síðu sem heitir **myndspilarasíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu myndspilara.
1. Í eiginleikaglugganum fyrir myndspilaraeininguna velurðu **Bæta við myndskeiði**.
1. Í valmyndinni **Miðlaval** velurðu myndskeið og velur síðan **Hlaða upp nýjum miðli**.
1. Vistaðu og forskoðaðu síðuna. Þú ættir að sjá myndskeiðseininguna á síðunni. Þú getur breytt viðbótarstillingum til að sérsníða hegðun einingarinnar.
1. Ljúktu við að breyta síðunni, vistaðu hana og birtu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Kynningarborðaeining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Textabálkseining](add-content-rich-block.md)

[Innihaldsbálkseining](add-hero-module.md)
