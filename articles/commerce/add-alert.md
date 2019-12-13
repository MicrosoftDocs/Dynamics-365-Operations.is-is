---
title: Viðvörunareining
description: Þetta efni fjallar um viðvörunareiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785353"
---
# <a name="alert-module"></a>Viðvörunareining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um viðvörunareiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Viðvörunareining er notuð til að sýna upplýsingarskilaboð á síðu. Viðvörunareiningar styðja textaskilaboð og tengil. Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta. 

Viðvörunareiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Dæmi um viðvörunareiningar í rafrænum viðskiptum

Hægt er að nota viðvörunareiningar í síðuhausnum til að gefa til kynna kynningar eða skilaboð á öllu svæðinu. Hér eru nokkur dæmi:

„Árlegri útsölu lýkur eftir 10 daga“

„Stórsparnaður með útsölu fyrir skólann. Verslaðu núna."

## <a name="alert-module-properties"></a>Eiginleikar viðvörunareiningar

| Nafn eiginleika  | Virði                              | Lýsing |
|----------------|------------------------------------|-------------|
| Texti           | Texti                               | Textaboðin sem birtast í viðvörunareiningunni. |
| Textajöfnun | **Hægri**, **Vinstri** eða **Miðja** | Gildi sem skilgreinir hvernig texti er samstilltur í viðvörunareiningunni. |
| Hunsa viðvörun  | **Satt** eða **Ósatt**              | Ef gildi er stillt á **Satt** getur viðskiptavinurinn hafnað viðvöruninni. |
| Tengill           | Vefslóð                                | Slóðin fyrir valfrjálsan tengil. |

## <a name="add-an-alert-module-to-a-page"></a>Bæta viðvörunareiningu við á síðu 

Fylgdu þessum skrefum til að bæta viðvörunareiningu við síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **viðvörunarsniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við viðvörunareiningu.
1. Skráðu brotið út í sniðmátinu og birtu það. 
1. Notaðu viðvörunarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **viðvörunarsíða**. 
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við viðvörunareiningu.
1. Sláðu inn viðvörunatexta í stillingum fyrir viðvörunareininguna. Þú getur breytt öðrum eiginleikum ef þú vilt sérsníða viðvörunareininguna frekar.
1. Vistaðu og forskoðaðu síðuna. Efst á síðunni ættirðu að sjá viðvörun sem hefur textann sem þú bættir við.
1. Athuga á síðunni og birtu hana. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Eiginleikaeining](add-feature-module.md)

[Hetjueining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
