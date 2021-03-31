---
title: Myndspilaraeining
description: Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13072c8d6839fef1ab0dd55d626c23a2a1084d4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209180"
---
# <a name="video-player-module"></a>Myndspilaraeining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

Myndspilaraeiningin er notuð til að styðja myndspilun. Hægt er að bæta henni við hvaða síðu sem er, að því tilskildu að myndbandsefni sé hlaðið upp á og tiltækt í efnisstjórnunarkerfinu (CMS). Myndbandsspilarann styður .mp4 miðlunargerðina.

## <a name="video-player-module"></a>Myndspilaraeining

Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu. Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð, hljóðlýsingum og lokuðum myndatexta. Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft. Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.

Myndbandsspilaeiningin styður einnig aðrar hljóðrásir. Þegar myndskeiði er hlaðið upp í CMS er einnig hægt að hlaða upp annari hljóðrás. Síðan getur myndskeiðsspilarinn spilað seinni hljóðrásina ef notandi velur það.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Dæmi um myndspilareiningar í rafrænni verslun

- Leiðbeinandi myndbönd á vöruupplýsingasíðum eða markaðssíðum
- Kynningarmyndbönd eða myndbönd um stefnu á hvaða markaðssíðu sem er
- Markaðssetningarmyndbönd sem varpa ljósi á vöruaðgerðir á upplýsingasíðum eða markaðssíðum

Eftirfarandi mynd sýnir dæmi um myndspilaraeiningu á heimasíðu.

![Dæmi um myndspilaraeiningu](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Eiginleikar myndspilaraeiningar

| Nafn eiginleika         | Virði                               | lýsing |
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

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Sniðmát myndspilara** og velja síðan **Í lagi**.
1. Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Myndspilari** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það. 
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja það sniðmát myndspilara sem var búið til. Undir **Síðuheiti** skal færa inn **Myndspilarasíða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Myndspilari** og síðan velja **Í lagi**.
1. Á eiginleikasvæði myndspilaraeiningar skal velja **Bæta við myndbandi**.
1. Í valmyndinni **Miðlaval** velurðu myndskeið og velur síðan **Hlaða upp nýjum miðli**.
1. Í File Explorer skal velja myndbandsskrá og velja síðan **Opna**.
1. Í glugganum **Hlaða upp margmiðlunarefni** skal slá inn titil og aðrar upplýsingar eftir þörfum og velja síðan **Í lagi**.
1. Í glugganum **Val á miðli** skal velja **Loka**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Þú ættir að sjá myndskeiðseininguna á síðunni. Þú getur breytt viðbótarstillingum til að sérsníða hegðun einingarinnar.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Tilboðsborðaeining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Textabálkseining](add-content-rich-block.md)

[Innihaldsbálkseining](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]