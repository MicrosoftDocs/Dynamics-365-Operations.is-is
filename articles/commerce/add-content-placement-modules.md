---
title: Staðsetningareining efnis
description: Þetta efni fjallar um staðsetningu efnis og staðsetningareiningar efnis og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785301"
---
# <a name="content-placement-module"></a>Staðsetningareining efnis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um staðsetningu efnis og staðsetningareiningar efnis og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Staðsetningareining efnis er sérstakur gámur sem hægt er að setja aðrar einingar inn í í tilteknu skipulagi. Staðsetningareiningar efnis styðja eftirfarandi gerðir af einingum sem undireiningar: staðsetningarlið efnis, móttökulið reiknings, pöntunarlið reiknings, óskalistalið reiknings og forstillingarlið reiknings.

Staðsetningareiningar efnis fá gögn úr undireiningunum sem þær styðja. Þess vegna er hægt að nota staðsetningareiningar efnis á ýmsa vegu, allt eftir þeim einingum sem bætt er við það.

Staðsetningareiningar efnis nota bæði myndir og texta til að sýna kynningar, stefnur og vöruaðgerðir. Til dæmis er hægt að nota einingu staðsetningarliðar efnis á heimasíðunni til að sýna stefnu um verslun eða sendingarupplýsingar. Einingar staðsetningarliðar efnis eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er. Hins vegar er aðeins hægt að nota þær í staðsetningareiningu efnis.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Dæmi um staðsetningareiningar efnis í rafrænum viðskiptum

* Hægt er að nota staðsetningareiningar efnis sem innihalda einingar staðsetningarliðar efnis á heimasíðu eða markaðssíðum til að sýna vörueiginleika, kynningar, verslunarstefnu, sendingarupplýsingar og aðrar upplýsingar í gegnum bæði myndir og texta.
* Hægt er að nota staðsetningareiningar efnis sem innihalda einingar staðsetningarliðar efnis á upplýsingasíðum til að sýna eiginleika vöru.
* Hægt er að nota staðsetningareiningar efnis sem innihalda móttökulið reiknings eða pöntunarlið reiknings á síðum reikningastjórnunar.

## <a name="content-placement-module-properties"></a>Eiginleikar staðsetningareiningar efnis

| Nafn eiginleika | Virði | Lýsing |
|---------------|-------|-------------|
| Breidd         | **Passa í gám** eða **Fylla skjáinn** | Ef gildi er stillt á **Passa í gám** eru hlutirnir í staðsetningareiningu efnis takmarkaðir við breidd staðsetningareiningar efnis. Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd staðsetningareiningar efnis en geta farið í stillingar fyrir allan skjáinn. |

## <a name="content-placement-item-module-properties"></a>Eiginleikar staðsetningarliðareiningar efnis

| Nafn eiginleika | Virði | Lýsing |
|---------------|-------|-------------|
| Fyrirsögn       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sérhver staðsetningarliðareiningar efnis getur haft fyrirsögn. Eiginleikinn **Fyrirsögn** styður fyrirsagnamerki. Sjálfgefið er að fyrirsagnarmerkið **H2** sé notað, en hægt er að breyta fyrirsagnarmerkinu svo að það uppfylli kröfur um aðgengi. |
| Efnisgrein     | Texti efnisgreinar | Staðsetningarliðareiningar efnis styðja málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Mynd         | Myndaskrá | Hægt er að tengja mynd við textann. |
| Tengill          | Slóð og texti tengils | Hægt er að bæta við tengli í textann til að beina notendum á ákveðna síðu. |
| Stærð reits     | Tölugildi frá **1** til og með **12** | Fyrir hvern efnisstaðsetningarlið skilgreinir þessi eiginleiki fjölda hólfa sem hluturinn ætti að fylla út í staðsetningareiningu efnis. Hámarksstærð staðsetningareiningar efnis er 12 hólf. Ef heildarreitastærðin fyrir fyrstu *n* hlutina í staðsetningraeiningu efnis fer yfir 12 hólf er hlutirnir eru pakkaðir í næstu röð. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Bæta við staðsetningareiningu efnis sem inniheldur staðsetningarliðareiningu efnis á síðu

Fylgdu þessum skrefum til að bæta við staðsetningareiningu efnis sem inniheldur staðsetningarliðareiginleika efnis á nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til sniðmát sem heitir **sniðmát efnisstaðsetningar**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við staðsetningareiningu efnis.
1. Í staðsetningareiningu efnis bætirðu við staðsetningarliðareiningu efnis.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu efnisstaðsetningarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnisstaðsetningarsíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við staðsetningareiningu efnis.
1. Í staðsetningareiningu efnis bætirðu við staðsetningarliðareiningu efnis.
1. Í eiginleikaglugganum fyrir einingu staðsetningarliðar efnis velurðu mynd, bætir við fyrirsögn, bætir við málsgrein, bætir við tengli, setur slóð fyrir tengilinn og stillir stærð reitar á **6**.
1. Endurtaktu skref 7 og 8 til að bæta við annarri einingu fyrir vistun efnis sem hefur sömu reitastærð.
1. Vistaðu og forskoðaðu síðuna. Þú ættir að sjá tvo efnisstaðsetningarliði sem birtast hlið við hlið. Þú getur breytt eiginleikanum **Reitastærð** fyrir hverja staðsetningareiningu efnis eða bætt við fleiri einingum til að ná tilætluðu skipulagi.
1. Athuga á síðunni og birtu hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Viðvörunareining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Eiginleikaeining](add-feature-module.md)

[Hetjueining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
