---
title: Textabálkseining
description: Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025598"
---
# <a name="text-block-module"></a>Textabálkseining


[!include [banner](includes/banner.md)]

Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Textabálkseining er eining sem er notuð til að bæta við textainnihaldi. Þetta efni getur verið upplýsandi eða kynningar.

Textabálkseiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er. Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Dæmi um textabálkseiningar í rafrænum viðskiptum

Hægt er að nota textabálkseiningar á eftirfarandi hátt:

* Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.
* Til upplýsinga á hvaða síðu sem er. Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.
* Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu. (til dæmis „Ókeypis sending fyrir pantanir yfir $50“).
* Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).

## <a name="text-block-module-properties"></a>Eiginleikar textabálkseiningar

| Nafn eiginleika     | Value                                            | Lýsing |
|-------------------|--------------------------------------------------|-------------|
| RTF-snið         | RTF-snið                                        | Texti efnisgreinar. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta. |
| Sérsniðið heiti klasa | Klasaheiti Cascading Style Sheets (CSS)        | Heiti sérsniðins CSS-klasa sem forritari veitir til að forsníða þessa einingu. Skilgreina ætti klasaheitið í þemapakkanum. |
| Leturtærð         | **Lítil**, **Miðlungs**, **Stór** eða **X-stór** | Leturstærð fyrir innihaldið. |

## <a name="add-a-text-block-module-to-a-page"></a>Bæta við textabálkseiningu á síðu

Fylgdu þessum skrefum til að bæta textabálkseiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **Efnissniðmát**. 
1. Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.
1. Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.
1. Notaðu efnissniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnissíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.
1. Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.
1. Bættu textabálkseiningu við gámaeininguna. 
1. Í eiginleikaglugga textabálkseiningarinnar bætirðu texta við í reitinn **Mótaður texti**.
1. Ljúktu við að breyta síðunni, vistaðu hana og birtu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Kynningarborðaeining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Innihaldsbálkseining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)

