---
title: Myndspilaraeining
description: Þessi grein fjallar um einingar fyrir myndbandsspilara og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 919446981f7439d61b01deb57b206cd457eed919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269295"
---
# <a name="video-player-module"></a>Myndspilaraeining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um einingar fyrir myndbandsspilara og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Myndspilaraeiningin er notuð til að styðja myndspilun. Hægt er að bæta henni við hvaða síðu sem er, að því tilskildu að myndbandsefni sé hlaðið upp á og tiltækt í efnisstjórnunarkerfinu (CMS). Myndbandsspilarann styður .mp4 miðlunargerðina.

## <a name="video-player-module"></a>Myndspilaraeining

Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu. Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð, hljóðlýsingum og lokuðum myndatexta. Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft. Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.

Myndbandsspilaeiningin styður einnig aðrar hljóðrásir. Þegar myndskeiði er hlaðið upp í CMS er einnig hægt að hlaða upp annari hljóðrás. Síðan getur myndskeiðsspilarinn spilað seinni hljóðrásina ef notandi velur það.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Dæmi um myndspilareiningar í rafrænni verslun

- Leiðbeinandi myndbönd á vöruupplýsingasíðum eða markaðssíðum
- Kynningarmyndbönd eða myndbönd um stefnu á hvaða markaðssíðu sem er
- Markaðssetningarmyndbönd sem varpa ljósi á vöruaðgerðir á upplýsingasíðum eða markaðssíðum

Eftirfarandi mynd sýnir dæmi um myndspilaraeiningu á heimasíðu.

![Dæmi um myndspilaraeiningu.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Eiginleikar myndspilaraeiningar

| Nafn eiginleika         | Virði                               | lýsing |
|-----------------------|-------------------------------------|-------------|
| Haus               | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina, en breyta má merkinu til að uppfylla kröfur um aðgengi. |
| Sniðinn texti             | Texti efnisgreinar | Einingin styður málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og tengla og feitletrun, undirstrikun og skáletrun texta. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill                  | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og valið **Opnaðu hlekk í nýjum flipa** | Einingin styður einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |
| Texti efnis              | Fyrirsögn, texti eða tenglar | Hægt er að bæta við öðru samhengi fyrir myndspilaraeininguna, svo sem nafni höfundar eða hönnuðar eða tenglum á persónuleg blogg. |
| Sjálfvirk spilun             | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið sjálfkrafa spilað. |
| Þagga                  | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er skrúfað fyrir hljóðið. Fyrir þennan spilara er sjálfgildið **Ósatt**. Í Chrome-vafranum er sjálfvirk spilun myndskeiða sjálfgefið þögguð og hljóðið er aðeins spilað ef notandinn spilar myndbandið handvirkt. |
| Lykkja                  | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið endurtekið í lúppu. |
| Miðlar                 | Skráarslóð og -heiti myndskeiðs | Myndskeiðið sem er spilað í myndspilaranum. |
| Spila á öllum skjánum       | **Satt** eða **Ósatt**               | Þegar gildi er stillt á **Satt** er myndskeiðið spilað á öllum skjánum. |
| Spila/hlé    | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu. |
| Stýringar myndspilara | **Satt** eða **Ósatt**               | Þegar gildið er stillt á **Satt** eru öll stjórntæki myndbandsspilarans sýnd. Þessar stjórntæki fela í sér spilunar- og hléhnappa, framvinduvísir og valkosti fyir lokaða myndatexta. |
| Fela forsíðumynd     | **Satt** eða **Ósatt**               | Myndskeið getur verið með plakatramma. Þegar gildið þessa eiginleika er stillt á **Satt** er plakatramminn falinn. |
| Sniðmátsstig            | Tölugildi frá **0** til og með **100** | Sniðmátið sem er beitt á myndskeiðið til útlitshönnun. |

> [!IMPORTANT]
> Eiginleikarnir **Fyrirsögn**, **Ríkur texti**, **Tengill** og **Undirtexti** eru í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.

## <a name="add-a-video-player-module-to-a-page"></a>Bæta við myndspilaraeiningu á síðu

> [!NOTE] 
> Áður en þú býrð til myndspilaraeiningu verðurðu fyrst að hlaða upp myndskeiði á fjölmiðlasafnið.

Fylgdu þessum skrefum til að bæta myndspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í **Nýtt sniðmát** svargluggi, undir **Nafn sniðmáts**, koma inn **Sniðmát fyrir myndbandsspilara**, og veldu síðan **Allt í lagi**.
1. Í **Líkami** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Sjálfgefin síða** mát og veldu síðan **Allt í lagi**.
1. Í **Aðal** rifa á **Sjálfgefin síða** mát, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Myndbandsspilari** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það. 
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Myndspilara síða**, og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Sniðmát fyrir myndbandsspilara** sem þú bjóst til og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**.
1. Í **Aðal** rauf á nýju síðunni, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Myndbandsspilari** mát og veldu síðan **Allt í lagi**.
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
