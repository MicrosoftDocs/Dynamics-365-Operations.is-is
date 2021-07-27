---
title: Auglýsingaborðaeining
description: Þetta efni fjallar um tilboðsborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3158916f96522bec6e7511f2d9daf61d36ffe8c6
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479353"
---
# <a name="promo-banner-module"></a>Tilboðsborðaeining

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efni fjallar um tilboðsborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

Auglýsingaborðaeiningar eru notaðar til að sýna upplýsingarskilaboð á síðu. Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta. 

Auglýsingaborðaeiningar styðja textaskilaboð og tengil. Ef mörgum skilaboðum er bætt við auglýsingaborðaeiningar verður til myndaræmuborði sem snýst og gerir viðskiptavinum kleift að fletta í gegnum öll skilaboðin. 

Auglýsingaborðaeiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Dæmi um notkun auglýsingaborða í rafrænum viðskiptum

Hægt er að nota auglýsingaborða í haus síðunnar til að sýna kynningar eða skilaboð á vefnum, eins og í eftirfarandi dæmum.

„Árlegri útsölu lýkur eftir 10 daga“

„Stórsparnaður með útsölu fyrir skólann. Verslaðu núna."

„Verslaðu á þakkargjörðarútsölunni!“ 

Eftirfarandi mynd sýnir dæmi um tilboðsborða.

![Dæmi um einingu tilboðsborða.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Eiginleikar auglýsingaborðaeiningar

| Nafn eiginleika             | Virði                              | lýsing |
|---------------------------|------------------------------------|-------------|
| Skilaboð vefborða           | Texti og tenglar                     | Úrval texta og tengla. |
| Sjálfvirk spilun                  | **Satt** eða **Ósatt**              | Gildi sem gefur til kynna hvort skilaboðum sé sjálfkrafa hleypt í gegn, ef mörg skilaboð eru stillt. |
| Tími á milli skyggna | Fjöldi millisekúnda (ms)      | Bilið sem er notað til að fletta í gegnum skilaboð. |
| Leyfa höfnun             | **Satt** eða **Ósatt**              | Ef gildi er stillt á **Satt** geta viðskiptavinir hafnað viðvöruninni. |
| Sýna myndaræmuflipa     | **Satt** eða **Ósatt**              | Gildi sem gefur til kynna hvort sýna ætti myndaræmuflipana svo viðskiptavinir geti flett handvirkt í gegnum marga borðahluti. |
| Textajöfnun            | **Hægri**, **Vinstri** eða **Miðja** | Textajöfnunin í auglýsingaborðaeiningunni. |
| Tengill                      | Slóð                              | Slóðin fyrir valfrjálsan tengil. |
|Textajöfnun             | **Hægri**, **Vinstri** eða **Miðja** | Þessi eiginleiki er í boði sem þemaviðbót við þema Adventure Works. Hann gerir notanda kleift að stilla af textann í auglýsingaborðanum. |

> [!IMPORTANT]
> Þema Adventure Works er í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.

## <a name="add-a-promo-banner-module-to-a-page"></a>Bæta auglýsingaborðaeiningu við síðu 

Fylgdu þessum skrefum til að bæta auglýsingaborðaeiningu við síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn **Sniðmát tilboðsborða** og velja síðan **Í lagi**.
1. Undir **Útlínur síðu** bætirðu við einingunni **Sjálfgefin síða** við hólfið **Meginmál**. 
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það. 
1. Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **Auglýsingaborðasíða**. 
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu. 
1. Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla gám**.
1. Undir **Útlínur síðu** bæirðu auglýsingaborðaeiningu við gámaeininguna.
1. Bættu við einum eða fleiri borðaskilaboðum í stillingunum fyrir borðaeininguna. Hver skilaboð geta verið með texta ásamt tengli. Þú getur breytt öðrum eiginleikum til að sérsníða eininguna frekar.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Efst á síðunni ættirðu að sjá viðvörun sem sýnir textann sem þú bættir við.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

> [!NOTE]
> Auglýsingaborði er venjulega notaður í hólfi síðuhausa eða hólfi undirhauss.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Textabálkseining](add-content-rich-block.md)

[Eining fyrir bálk með efni](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
