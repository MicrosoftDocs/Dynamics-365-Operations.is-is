---
title: Auglýsingaborðaeining
description: Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025621"
---
# <a name="promo-banner-module"></a>Auglýsingaborðaeining


[!include [banner](includes/banner.md)]

Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Auglýsingaborðaeiningar eru notaðar til að sýna upplýsingarskilaboð á síðu. Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta. 

Auglýsingaborðaeiningar styðja textaskilaboð og tengil. Ef mörgum skilaboðum er bætt við auglýsingaborðaeiningar verður til myndaræmuborði sem snýst og gerir viðskiptavinum kleift að fletta í gegnum öll skilaboðin. 

Auglýsingaborðaeiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Dæmi um notkun auglýsingaborða í rafrænum viðskiptum

Hægt er að nota auglýsingaborða í haus síðunnar til að sýna kynningar eða skilaboð á vefnum, eins og í eftirfarandi dæmum.

„Árlegri útsölu lýkur eftir 10 daga“

„Stórsparnaður með útsölu fyrir skólann. Verslaðu núna."

## <a name="promo-banner-module-properties"></a>Eiginleikar auglýsingaborðaeiningar

| Nafn eiginleika             | Value                              | Lýsing |
|---------------------------|------------------------------------|-------------|
| Skilaboð vefborða           | Texti og tenglar                     | Úrval texta og tengla. |
| Sjálfvirk spilun                  | **Satt** eða **Ósatt**              | Gildi sem gefur til kynna hvort skilaboðum sé sjálfkrafa hleypt í gegn, ef mörg skilaboð eru stillt. |
| Tími á milli skyggna | Fjöldi millisekúnda (ms)      | Bilið sem er notað til að fletta í gegnum skilaboð. |
| Leyfa höfnun             | **Satt** eða **Ósatt**              | Ef gildi er stillt á **Satt** geta viðskiptavinir hafnað viðvöruninni. |
| Sýna myndaræmuflipa     | **Satt** eða **Ósatt**              | Gildi sem gefur til kynna hvort sýna ætti myndaræmuflipana svo viðskiptavinir geti flett handvirkt í gegnum marga borðahluti. |
| Textajöfnun            | **Hægri**, **Vinstri** eða **Miðja** | Textajöfnunin í auglýsingaborðaeiningunni. |
| Tengill                      | Slóð                              | Slóðin fyrir valfrjálsan tengil. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Bæta auglýsingaborðaeiningu við síðu 

Fylgdu þessum skrefum til að bæta auglýsingaborðaeiningu við síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **Auglýsingaborðasniðmát**.
1. Undir **Útlínur síðu** bætirðu við einingunni **Sjálfgefin síða** við hólfið **Meginmál**. 
1. Skráðu brotið út í sniðmátinu og birtu það. 
1. Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **Auglýsingaborðasíða**. 
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu. 
1. Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla gám**.
1. Undir **Útlínur síðu** bæirðu auglýsingaborðaeiningu við gámaeininguna.
1. Bættu við einum eða fleiri borðaskilaboðum í stillingunum fyrir borðaeininguna. Hver skilaboð geta verið með texta ásamt tengli. Þú getur breytt öðrum eiginleikum til að sérsníða eininguna frekar.
1. Vistaðu og forskoðaðu síðuna. Efst á síðunni ættirðu að sjá viðvörun sem sýnir textann sem þú bættir við.
1. Ljúktu við að breyta síðunni, vistaðu hana og birtu. 

> [!NOTE]
> Auglýsingaborði er venjulega notaður í hólfi síðuhausa eða hólfi undirhauss.


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Textabálkseining](add-content-rich-block.md)

[Innihaldsbálkseining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
