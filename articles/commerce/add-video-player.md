---
title: Myndspilaraeining
description: Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785330"
---
# <a name="video-player-module"></a>Myndspilaraeining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eininga myndspilara eru notaðar til að styðja myndspilun. Tvo myndspilarar má finna í upphafsbúnaðinum í versluninni: umhverfismyndspilaraeininguna og myndspilaraeininguna. Báðir spilarar styðja .mp4 miðlunargerðina.

## <a name="ambient-video-player-module"></a>Umhverfismyndspilaraeining

Umhverfismyndbandsspilaraeiningin styður stutt upplýsingamyndbönd. Hana ætti að nota fyrir myndskeið sem eru innan við fimm sekúndur að lengd. Þessi spilari styður takmarkaða getu myndspilunar, eins og spilun og hlé.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Dæmi um umhverfismyndspilareiningar í rafrænu verslun

- Stutt upplýsingamyndbönd sem varpa ljósi á nýjar vörur á heimasíðunni
- Stutt upplýsingamyndbönd sem varpa ljósi á eiginleika vöru á upplýsingasíðu vöru

### <a name="ambient-video-player-module-properties"></a>Eiginleikar umhverfismyndspilaraeiningar

| Nafn eiginleika     | Virði                 | Lýsing |
|-------------------|-----------------------|-------------|
| Sjálfvirk spilun          | **Satt** eða **Ósatt** | Þegar gildi er stillt á **Satt** er myndskeiðið sjálfkrafa spilað. |
| Þagga              | **Satt** eða **Ósatt** | Þegar gildi er stillt á **Satt** er skrúfað fyrir hljóðið. Fyrir þennan spilara er sjálfgildið **Satt**. Í Google Chrome vafranum er sjálfvirk spilun myndskeiða sjálfgefið þögguð og hljóðið er aðeins spilað ef notandinn spilar myndbandið handvirkt. |
| Lykkja              | **Satt** eða **Ósatt** | Þegar gildi er stillt á **Satt** er myndskeiðið endurtekið í lúppu. |
| Miðlar             |  Skráarslóð og -heiti myndskeiðs | Myndskeiðið sem er spilað af myndspilaranum. |
| Spilunarstýringar | **Satt** eða **Ósatt** | Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu. Ef gildi er stillt á **Ósatt** er spilunar-/hléshnappinn ekki sýndur, en notendur geta samt gert hlé á myndskeiðinu og haldið því áfram með því að nota lyklaborðið. |

## <a name="video-player-module"></a>Myndspilaraeining

Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu. Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð og lokuðum myndatexta. Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft. Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.

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
| Spilunarstýringar     | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu. Ef gildi er stillt á **Ósatt** er spilunar-/hléshnappinn ekki sýndur, en notendur geta samt gert hlé á myndskeiðinu og haldið því áfram með því að nota lyklaborðið. |
| Spila á öllum skjánum       | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið spilað á öllum skjánum. |
| Stýringar              | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** eru öll stjórntæki sýnd. Þessar stjórntæki fela í sér spilunar- og hléhnappa, framvinduvísir og lokaða myndatexta. |
| Fela plakatramma     | **Satt** eða **Ósatt**               | Myndskeið getur verið með plakatramma. Þegar gildið þessa eiginleika er stillt á **Satt** er plakatramminn falinn. |
| Sniðmátsstig            | Tölugildi frá **0** til og með **100** | Sniðmátið sem er beitt á myndskeiðið til útlitshönnun. |
| Táknstíll fyrir fullan skjá | **Ferningur** eða **Ör**             | Stíllinn á skjámyndinni á öllum skjánum sem sýndur er í myndspilaranum. |

## <a name="add-a-video-player-module-to-a-page"></a>Bæta við myndspilaraeiningu á síðu

Fylgdu þessum skrefum til að bæta myndspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **myndspilarasniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við gámaeiningu.
1. Bætið við myndspilara- og umhverfismyndspilaraeiningunum í gámaeiningunni.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu myndspilarasniðmátið sem þú bjóst til til að búa til síðu sem heitir **myndspilarasíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu umhverfismyndspilara.
1. Í stillingunum fyrir umhverfismyndspilarann ferðu í **Miðlar** og hleður upp myndskeiði. Hægt er að breyta **Sjálfspilun**, **Lykkju** og öðrum eiginleikum eftir þörfum.
1. Vistaðu og forskoðaðu síðuna.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu myndspilara.
1. Í stillingunum fyrir myndspilarann ferðu í **Miðlar** og hleður upp myndskeiði.
1. Vistaðu og forskoðaðu síðuna. Þú ættir að sjá báðar myndskeiðseiningarnar á síðunni. Þú getur breytt viðbótarstillingum til að sérsníða hegðun hverrar einingar.
1. Athuga á síðunni og birtu hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Viðvörunareining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Eiginleikaeining](add-feature-module.md)

[Hetjueining](add-hero-module.md)
