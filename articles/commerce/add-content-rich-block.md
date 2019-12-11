---
title: Eining með fjölbreyttu efni
description: Þetta efni fjallar um einingar með fjölbreyttu efni og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785422"
---
# <a name="content-rich-block-module"></a>Eining með fjölbreyttu efni

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um einingar með fjölbreyttu efni og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eining með fjölbreyttu efni er sérstakur gámur sem hægt er að setja eina eða fleiri einingar með fjölbreyttu efni í. Einingar með fjölbreyttu efni eru notaðar fyrir textaefni á síðu. Þetta efni getur verið annaðhvort upplýsandi eða kynningar.

Einingar með fjölbreyttu efni eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er. Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Dæmi um einingar með fjölbreyttu efni í rafrænum viðskiptum

Hægt er að nota einingar með fjölbreyttu efni á eftirfarandi hátt:

* Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.
* Til upplýsinga á hvaða síðu sem er. Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.
* Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu. (til dæmis „Ókeypis sending fyrir pantanir yfir $50“).
* Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).

## <a name="content-rich-block-module-properties"></a>Eiginleikar einingar með fjölbreyttu efni

| Nafn eiginleika     | Virði                                 | Eiginleiki |
|-------------------|---------------------------------------|----------|
| Fjöldi dálka | Tölugildi frá **1** til og með **4**     | Fjöldi dálka í bálki með fjölbreyttu efni. Það geta verið allt að fjórir dálkar. |
| Breidd             | **Fylla gám** eða **Fylla skjáinn** | Ef gildi er stillt á **Fylla gám** eru hlutirnir í gámnum takmarkaðir við breidd gámsins. Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd gámsins en geta farið í stillingar fyrir allan skjáinn. Þú getur breytt gildi til að ná tilætluðu útliti. |

## <a name="content-rich-block-item-module-properties"></a>Eiginleikar einingar bálkaliðar með fjölbreyttu efni

| Nafn eiginleika | Virði          | Lýsing |
|---------------|----------------|-------------|
| Efnisgrein     | Texti efnisgreinar | Textinn sem fylgir sérhverjum dálkalið með fjölbreyttu efni. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Bæta við einingu með fjölbreyttu efni á síðu

Fylgdu þessum skrefum til að bæta einingu bálks með fjölbreyttu efni við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til síðusniðmát sem heitir **Efnissniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við einingu bálks með fjölbreyttu efni.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu efnissniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnissíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu bálks með fjölbreyttu efni.
1. Í eiginleikum einingar bálks með fjölbreyttu efni skaltu stilla fjölda dálka á **2**.
1. Í einingu bálks með fjölbreyttu efni velurðu **Bæta við einingu** og bætir við dálkalið með fjölbreyttu efni (til dæmis, **item1**).
1. Bættu við efnisgreinatexta í nýja bálkalið með fjölbreyttu efni.
1. Í einingu bálks með fjölbreyttu efni velurðu **Bæta við einingu** og bætir við dálkalið með fjölbreyttu efni (til dæmis, **item2**).
1. Bættu við efnisgreinatexta í nýja bálkalið með fjölbreyttu efni.
1. Vistaðu síðuna og forskoðaðu breytingarnar. Þú ættir að sjá tvær sniðnar textablokkir í tveggja dálka mynd.
1. Athuga á síðunni og birtu hana.

> [!NOTE]
> Ef þú bætir við þriðja sniðna reitnum fyrir efnið verður það staflað fyrir neðan þá tvo hluti sem þú bætir við áður. Með því að breyta fjölda dálka og atriða í gámnum geturðu náð mismunandi skipulagi fyrir textaefni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Viðvörunareining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Eiginleikaeining](add-feature-module.md)

[Hetjueining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)

