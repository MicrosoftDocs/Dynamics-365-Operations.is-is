---
title: Hólfeining
description: Þetta efni fjallar um gámaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697061"
---
# <a name="container-module"></a>Hólfeining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um gámaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Gámaeining er eining sem hýsir aðrar einingar. Það er algengasti gámurinn sem er notaður í Dynamics 365 Commerce. Megintilgangur gámaeiningar er að skilgreina með eiginleikum sem eru settir fyrir það skipulag eininganna sem eru í henni. Til dæmis geta þessir einingar birst hlið við hlið í tveggja dálka, þriggja dálka, fjögurra dálka eða sex dálka skipulagi. Þær geta einnig verið takmarkaðar við breidd gámsins, eða þær geta fyllt skjáinn. Einnig er hægt að bæta við fyrirsögn í hverja gámaeiningu.

Það eru þrjár staðlaðar gerðir gámaeininga: gámur, gámur með 2 hólfum og gámur með 3 hólfum. Hægt er að setja einingar af hvaða gerð einingar sem er í þessa gáma. Það eru líka til sérstakar gerðir gámaeininga, svo sem myndaræma, eining með fjölbreyttu efni, staðsetning innihalds, karfa, kassi, kaupbox, fyrirsögn og neðanmálseinig. Þessir gámar hafa sérstakan tilgang og aðeins er hægt að setja sérstakar studdar gerðir af einingum í þær.

Við mælum með að þú setjir einingar í gám, svo að þær geti takmarkast við breidd gámsins.

## <a name="examples-of-container-modules-in-e-commerce"></a>Dæmi um gámaeiningar í rafrænum viðskiptum

- Vefhöfundur vill þriggja dálka skipulag, þar sem þrjár einingar birtast hlið við hlið. Þess vegna notar vefhöfundur gámaeiningu gáms af 3 hólfa gerð.
- Vefhöfundur vill sex dálka skipulag, þar sem sex einingar birtast hlið við hlið. Þess vegna notar vefhöfundur gám af efnisgerðinni sem hefur sex dálka í sér.
- Vefhöfundur vill setja einingu á síðu en vill ekki að hún fylli skjáinn. Þess vegna bætir vefhöfundur einingunni við gámaeininguna og stillir eiginleikann **Breidd** á **Passa í gám** fyrir gáminn.

## <a name="container-module-properties"></a>Eiginleikar geymiseiningar

| Nafn eiginleika     | Gildi | Lýsing |
|-------------------|--------|-------------|
| Fyrirsögn           | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Hægt er að veita valfrjálsa fyrirsögn fyrir gáminn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Breidd             | **Passa í gám** eða **Fylla skjáinn** | Ef gildi er stillt á **Passa í gám** (sjálfgildið) eru einingarnr í myndaræmunni takmarkaðir við breidd gámsins. Ef gildið er stillt á **Fylla skjáinn** eru einingarnar ekki takmarkaðar við breidd gámsins en geta fyllt allan skjáinn. |
| Fjöldi dálka | **1**, **2**, **3**, **4**, **6**, eða **12** | Þessi eiginleiki skilgreinir fjölda dálka í gámnum. Gámur getur haft allt að 12 dálka. |

## <a name="container-with-2-slots"></a>Hólf með tveimur svæðum

Gámurinn af 2 hólfa gerð er fínstilltur fyrir tveggja dálka skipulag. Þessi tegund gáms hefur tvö hólf til að leyfa skoðun hlið við hlið á einingunum innan í.

Hægt er að nota viðbótareiginleika til að hámarka skipulag fyrir mismunandi skjágáttir (farsímar, spjaldtölvur, tölvur og svo framvegis). Hægt er að skilgreina breidd hvers dálks fyrir hverja skjágátt. Eftirfarandi stillingar dálkabreiddar eru tiltækar:

- **75%/25%** - Fyrri einingin er með dálkbreidd 75 prósent og seinni einingin dálkabreidd 25 prósent. Valkosturinn **25% / 75%** er einnig í boði.
- **50% / 50%** - Báðar einingarnar hafa sömu dálkabreidd.
- **67%/33%** - Fyrri einingin er með dálkbreidd 67 prósent og seinni einingin dálkabreidd 33 prósent. Valkosturinn **33% / 67%** er einnig í boði.
- **100%** – Báðar einingarnar eru með fulla dálkabreidd. Þess vegna er einingunum staflað lóðrétt í stökum dálki. Þrátt fyrir að þetta skipulag með einum dálki gangi gegn tilgangi gámsins af 2 hólfa gerð gæti það verið æskilegt fyrir sumar skoðunargáttir (til dæmis auka litlar skoðunargáttir svo sem fartæki).

### <a name="container-with-2-slots-properties"></a>Gámur með 2 hólfa eiginleikum

| Nafn eiginleika                   | Gildi | Lýsing |
|---------------------------------|--------|-------------|
| Fyrirsögn                         | Texti og merki fyrirsagna | Hægt er að veita valfrjálsa fyrirsögn fyrir gáminn. |
| Stilling afar lítillar skjágáttar | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eða **100%** | Þessi eiginleiki skilgreinir skipulag fyrir afar litlar skoðunargáttir. |
| Stilling lítillar skjágáttar   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eða **100%** | Þessi eiginleiki skilgreinir skipulag fyrir litlar skoðunargáttir, eins og fartæki. |
| Stilling miðlungs skjágáttar  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eða **100%** | Þessi eiginleiki skilgreinir skipulag fyrir miðlungs skoðunargáttir, eins og spjaldtölvur. |
| Stilling stórrar skjágáttar   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eða **100%** | Þessi eiginleiki skilgreinir skipulag fyrir stórar skoðunargáttir, eins og tölvur. |

## <a name="container-with-3-slots"></a>Hólf með þremur svæðum

Gámurinn af 3 hólfa einingagerð er fínstilltur fyrir þriggja dálka skipulag.

Hægt er að nota viðbótareiginleika til að hámarka skipulag fyrir mismunandi skjágáttir. Hægt er að skilgreina breidd hvers dálks fyrir hverja skjágátt. Eftirfarandi stillingar dálkabreiddar eru tiltækar:

- **33%/33%/33%** – Allar þrjár einingarnar eru með jafna dálkabreidd.
- **50%/25%/25%** - Fyrsta einingin er með dálkabreidd 50 prósent og hvor af einingunum tveimur sem eftir er með 25 prósenta dálkabreidd. Valkostirnir **25%/50%/25%** og **25%/25%/50%** eru einnig í boði.
- **16%/16%/67%** - Báðar fyrstu einingarnar eru með dálkabreidd 16 prósent og þriðja einingin er með 67 prósenta dálkabreidd. Valkostirnir **16%/67%/16%** og **67%/16%/16%** eru einnig í boði.

### <a name="container-with-3-slots-properties"></a>Gámur með 3 hólfa eiginleikum

| Nafn eiginleika                   | Gildi | Lýsing |
|---------------------------------|--------|-------------|
| Fyrirsögn                         | Texti og merki fyrirsagna | Hægt er að bæta valfrjálsri fyrirsögn við gáminn. |
| Stilling afar lítillar skjágáttar | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eða **67%/16%/16%** | Þessi eiginleiki skilgreinir skipulag fyrir afar litlar skoðunargáttir. |
| Stilling lítillar skjágáttar   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eða **67%/16%/16%** | Þessi eiginleiki skilgreinir skipulag fyrir litlar skoðunargáttir, eins og fartæki. |
| Stilling miðlungs skjágáttar  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eða **67%/16%/16%** | Þessi eiginleiki skilgreinir skipulag fyrir miðlungs skoðunargáttir, eins og spjaldtölvur. |
| Stilling stórrar skjágáttar   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eða **67%/16%/16%** | Þessi eiginleiki skilgreinir skipulag fyrir stórar skoðunargáttir, eins og tölvur. |

## <a name="add-a-container-module-to-a-page"></a>Bæta gámaeiningu við síðu

Fylgdu þessum skrefum til að bæta gámaspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **gámasniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við gámaeiningu.
1. Í gámaeiningunni bætirðu við eiginleikaeiningu.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu gámasniðmátið sem þú bjóst til til að búa til síðu sem heitir **gámasíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.
1. Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Fjöldi dálka** á **1** og eiginleikann **Breidd** á **Passa í gám**.
1. Í gámaeiningunni bætirðu við eiginleikaeiningu.
1. Stilltu fyrirsögn í eiginleikareit fyrir eiginleikaeininguna.
1. Vistaðu og forskoðaðu síðuna. Þú ættir að sjá eina eiginleikaeiningu sem passar innan breiddar gámaeiningarinnar.
1. Í eiginleikaglugganum fyrir gámaeininguna skaltu breyta gildi eiginleikans **Fjöldi dálka** í **3**.
1. Bættu tveimur eiginleikaeiningum í viðbót við gámaeininguna.
1. Vistaðu og forskoðaðu síðuna. Núna ættirðu að sjá þrjár eiginleikaeiningar sem birtast hlið við hlið.
1. Eftir að þú hefur náð því skipulagi sem þú vilt skaltu skrá síðuna inn og birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Kaupkassaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)