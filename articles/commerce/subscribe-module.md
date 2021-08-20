---
title: Áskriftareining
description: Þetta efni fjallar um áskriftareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6440d761c07a33139babb9e07bdb251c6cb49676
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638803"
---
# <a name="subscribe-module"></a>Áskriftareining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um áskriftareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Hægt er að nota áskriftareiningar á síðum vefsvæðis til að ná upplýsingum um viðskiptavini fyrir fréttabréf eða kynningar.

Eftirfarandi mynd sýnir dæmi um áskriftareiningu í síðufæti vefsíðu á vefsvæði Adventure Works.

![Dæmi um áskriftareiningu í síðufæti vefsíðu á vefsvæði Adventure Works](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Áskriftareiningin er tiltæk í einingasafni Commerce frá og með Dynamics 365 Commerce útgáfu 10.0.20.
> - Áskriftareiningin er sýnd í Adventure Works þemanu.
> - Áskriftareiningin þarf á viðbót gagnaaðgerðar til að virka með sumum tölvupóstþjónustum markaðsefnis þannig að hægt sé að senda fréttabréf eða kynningar í tölvupósti eftir að upplýsingar um viðskiptavin hafa verið fengnar.

## <a name="subscribe-module-properties"></a>Eiginleikar áskriftareiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Textafyrirsögn fyrir áskriftareininguna, svo sem **Gerast áskrifandi að fréttabréfinu** eða **Skráðu þig fyrir 10% afslætti**. |
| Efnisgrein     | Texti efnisgreinar | Áskriftareiningin styður texta í efnisgrein á RTF-sniði (Rich Text Format) til að bjóða upp á frekari upplýsingar fyrir kall á aðgerð í fyrirsögninni. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Bæta áskriftareiningu við nýja síðu

Til að bæta áskriftareiningu við nýja síðu og stilla nauðsynlega eiginleika í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og opnaðu markaðssetningarsniðmátið fyrir heimasíðu vefsvæðisins (eða búðu til nýtt sniðmát markaðssetningar).
1. Í hólfinu **Aðalsvæði** á Sjálfgefin síða skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Gerast áskrifandi** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og opnaðu heimasíðu vefsvæðisins (eða búðu til nýja heimasíðu með sniðmáti markaðssetningar).
1. Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Gerast áskrifandi** og síðan velja **Í lagi**.
1. Í eiginleikaglugga áskriftareiningar skal bæta við fyrirsögn eins og **Gerast áskrifandi**.
1. Bæta við nýjum texta efnisgreinar, t.d. **Nýjasta tíska og tilboð. Eru á listanum? Með því að gerast áskrifandi færðu öll nýjustu tilboðin!**
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Þema Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]