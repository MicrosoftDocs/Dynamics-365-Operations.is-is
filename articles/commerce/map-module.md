---
title: Kortaeining
description: Þessi grein fjallar um kortaeiningar og lýsir því hvernig á að stilla þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d72091baf2f216bfbe33950950f8917c3ba1ba5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283347"
---
# <a name="map-module"></a>Kortaeining

[!include [banner](includes/banner.md)]


Þessi grein fjallar um kortaeiningar og lýsir því hvernig á að stilla þær í Microsoft Dynamics 365 Commerce.

Kortaeining sýnir staðsetningar verslana á gagnvirku korti sem er sett fram með því að nota [Bing Maps V8 vefstýringu](/bingmaps/v8-web-control/). API-lykill Bing-korta er nauðsynlegur og verður að bæta honum við samnýtta færibreytusíðu í Commerce Headquarters. Kortaeiningar bjóða upp á mismunandi sjónarhorn, t.d. af vegi, úr lofti og af götunni, sem notendur geta valið til að skoða kortastaðsetningar. Þær leyfa einnig aðgerðir eins og aðdrátt og nota staðsetningu notanda.

Kortaeining vinnur með verslunarvalseiningunni til að ákvarða landfræðilegar staðsetningar á verslunum sem sýna þarf á korti. Verslunarvals- og kortaeiningar vinna saman þegar notandi velur verslun í annarri hvorri einingunni á svæði síðu. Hægt er að nota kortaeiningar í öðrum aðstæðum, sem tengjast ekki verslunarvalseiningum. Hins vegar er sérstilling einingar nauðsynleg.

> [!NOTE]
> Kortaeiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.13.

Eftirfarandi mynd sýnir dæmi um kortaeiningu sem er notuð á staðsetningarsíðu verslunar.

![Dæmi um verslunarvalseiningu.](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Haus | Texti | Fyrirsögn einingarinnar. |
| Valkostir teiknibólu: Sjálfgefið tákn | Mynd | Myndatákn teiknibólunnar sem er notaðfyrir verslanir sem sjást á korti. |
| Valkostir teiknibólu: Virkt tákn | Mynd | Myndatákn teiknibólunnar sem er notað fyrir verslun sem er valin á korti. |
| Valkostir teiknibólu: Sjálfgefinn litur tákns | Stafastrengur | Textinn eða sextándakerfisgildið fyrir litinn á teiknibólutákni á korti. |
| Valkostir teiknibólu: Litur virks tákns | Stafastrengur | Textinn eða sextándakerfisgildið fyrir litinn á völdu teiknibólutákni á korti. |
| Sýna atriðaskrá | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt**, sýna öll teiknibólutákn sem standa fyrir verslun atriðaskrá. Þessi atriðaskrá samsvarar atriðaskránni í listayfirlitinu sem verslunarvalseiningin sýnir. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Bæta leyfðum kortavefslóðum við öryggisleiðbeiningar um innihald vefsvæðis

Til þess að kortaeining geti unnið með Bing-korti, þarf að ganga úr skugga um að eftirfarandi kortavefslóðir séu leyfðar í öryggisreglum vefsvæðisins. Þessi uppsetning er gerð í Commerce-vefsmiðnum með því að bæta leyfðum vefslóðum við ýmsar öryggisleiðbeiningar vefsvæðis (t.d. **img-src**). Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md). 

- Í leiðbeininguna **connect-src** skal bæta við **&#42;.bing.com**.
- Í leiðbeininguna **img-src** skal bæta við **&#42;.virtualearth.net**.
- Í leiðbeininguna **script-src** skal bæta við **&#42;.bing.com, &#42;.virtualearth.net**.
- Í leiðbeininguna **script style-src** skal bæta við **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Bæta kortaeiningu við síðu

Ítarlegar upplýsingar um hvernig á að skilgreina kortaeiningu á síðu er að finna í [Eining til að velja verslun](store-selector.md). 
 
## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Eining til að velja verslun](store-selector.md)

[Stjórna Bing-kortum fyrir þitt fyrirtæki](./dev-itpro/manage-bing-maps.md)

[Bing-kort V8 Vefstýringar](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
