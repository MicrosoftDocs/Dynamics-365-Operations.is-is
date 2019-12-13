---
title: Myndaræmueining
description: Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785238"
---
# <a name="carousel-module"></a>Myndaræmueining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Myndaræmueining er notuð til að setja margar kynningarvörur í myndaræmu sem viðskiptavinir geta skoðað. Hún er sérstök gámaeining sem hýsir aðrar einingar. Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.

Þú getur bætt hetju- og eiginleikaeiningum í myndaræmueiningu. Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Dæmi um myndaræmueiningar í rafrænum viðskiptum

- Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.
- Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.
- Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.

## <a name="carousel-module-properties"></a>Eiginleikar myndaræmueiningar

| Nafn eiginleika             | Virði                                | Lýsing |
|---------------------------|--------------------------------------|-------------|
| Sjálfvirk spilun                  | **Satt** eða **Ósatt**                | Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa. Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar. |
| Tími á milli skyggna | Gildi í sekúndum                   | Bilið fyrir umbreytingar milli atriða. |
| Skiptimynd      | **Renna** eða **Hverfa**                | Umskiptaáhrifin. |
| Breidd                     | **Passa í gám** eða **Fylla skjáinn** | Ef gildi er stillt á **Passa í gám** eru hlutirnir í hringekjunni takmarkaðir við breidd myndaræmunnar. Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd myndaræmunnar en geta farið í stillingar fyrir allan skjáinn. Þú getur breytt gildi til að ná tilætluðu útliti. |

## <a name="add-a-carousel-module-to-a-page"></a>Bæta myndaræmueiningu við síðu

Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **myndaræmusniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við myndaræmueiningu.
1. Bættu hetjueiningu við myndaræmueininguna.
1. Bættu eiginleikaeiningu við myndaræmueininguna.
1. Skráðu brotið út í sniðmátinu og birtu það. 
1. Notaðu myndaræmusniðmátið sem þú bjóst til til að búa til síðu sem heitir **myndaræmusíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við myndaræmueiningu.
1. Stilltu eiginleikann **Breidd** í myndaræmueiningunni á **Fylla skjáinn**. 
1. Stilltu eiginleikann **Skiptimynd** á **Renna**.
1. Bættu hetjueiningu við myndaræmueininguna.
1. Bættu við mynd og fyrirsögn í hetjueiningunni og veldu síðan **Vista**.
1. Bættu eiginleikaeiningu við myndaræmueininguna.
1. Bættu við mynd, fyrirsögn og efnisgrein í eiginleikaeiningunni.
1. Vistaðu og forskoðaðu síðuna. Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining). Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.
1. Athuga á síðunni og birtu hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Viðvörunareining](add-alert.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Eiginleikaeining](add-feature-module.md)

[Hetjueining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
