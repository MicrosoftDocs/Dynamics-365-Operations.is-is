---
title: Vinna með forstillt útlit
description: Þetta efni lýsir því hvernig á að vinna með forstillt skipulag í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413177"
---
# <a name="work-with-preset-layouts"></a>Vinna með forstillt útlit


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að vinna með forstillt skipulag í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Áður en þú lýkur við ferlin í þessu efni skaltu passa að lesa [Forstillt og sérsniðið skipulag](templates-layouts-overview.md#preset-and-custom-layouts). Fyrir almenna yfirsýn skal sjá [Yfirlit yfir sniðmát og skipulag](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Búa til nýtt forstillt skipulag

Tvær aðferðir eru við að stofna forstillt skipulag. Þú getur vistað núverandi sérsniðið skipulag sem nýtt forstillt skipulag, eða þú getur búið til forstillt skipulag frá grunni.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Búðu til forstillt skipulag úr núverandi sérsniðnu skipulagi

Til að stofna forstillt skipulag úr núverandi sérsniðnu skipulagi skaltu fylgja þessum skrefum.

1. Opnaðu fyrirliggjandi síðu sem notar ekki forstillt skipulag eins og er og sem er með einingarskipulag sem þú vilt endurnýta fyrir aðrar síður á vefsvæðinu.
1. Veldu **Breyta** til að skoða síðuna.
1. Veldu **Vista sem nýtt útlit**. Valmyndin **Vista sem nýtt skipulag** birtist.
1. Sláðu inn heiti og lýsingu fyrir forstillta skipulagið. Gildin sem þú slærð inn verða sýnd öðrum höfundum þegar þeir búa til nýjar síður úr útliti þínu eða skipta yfir í það. Sláðu því inn gildi sem munu nýtast síðuhöfundum.
1. Veljið **Í lagi**.

Forstillt skipulag verður nú tiltækt þegar þú býrð til nýjar síður eða velur annað skipulag fyrir síðu í sama stigveldi sniðmáts.

> [!TIP]
> Til að sjá fljótt hvort tiltekin síða er nú bundin við forstillt skipulag velurðu síðuna á síðulistaskjánum og skoðar lýsigögn skipulagsins í eiginleikaglugganum til hægri.

### <a name="create-a-new-preset-layout"></a>Búa til nýtt forstillt skipulag

Til að stofna forstillt skipulag frá byrjun skaltu fylgja þessum skrefum.

1. Í stýriglugganum vinstra megin velurðu **Skipulag**.
1. Veldu **Nýtt skipulag**. Valmyndin **Nýtt skipulag** birtist.
1. Veldu sniðmát sem á að nota fyrir forstillt skipulag.
1. Sláðu inn heiti og lýsingu fyrir forstillta skipulagið. Gildin sem þú slærð inn verða sýnd öðrum höfundum þegar þeir búa til nýjar síður úr útliti þínu eða skipta yfir í það. Sláðu því inn gildi sem munu nýtast síðuhöfundum.
1. Veldu **Í lagi** til að búa til nýtt forstillt skipulag og opnaðu skipulagsritilinn.
1. Í skipulagsritlinum bætirðu við og stillir einingar með útlínutrénu til vinstri og eiginleikaglugganum til hægri. (Ferlið líkist ferlinu til að bæta við og stilla einingar fyrir sniðmát í sniðmát ritstjórans.) Fyrirkomulag eininga og allar læstar sjálfgefnar stillingar verða miðstýrð einingastilling fyrir allar síður sem nota þetta forstillta skipulag.

## <a name="modify-a-preset-layout"></a>Breyta forstilltu skipulagi

Til að breyta forstilltu skipulagi skaltu fylgja þessum skrefum.

1. Í stýriglugganum vinstra megin velurðu **Skipulag**.
1. Í skipulagsritlinum í útlínutrénu til vinstri velurðu eininguna sem á að breyta. Fylgdu síðan einhverju af eftirfarandi skrefum:

    - Til að færa einingu upp eða niður í yfireiningu hennar skaltu velja úrfellingarhnappinn (**...**) fyrir eininguna og veldu síðan **Færa upp** eða **Færa niður**.
    - Til að breyta sjálfgefnum stillingum einingar skaltu nota eiginleikagluggann til að slá inn sjálfgefin gildi og læsa þeim mögulega fyrir allar forstreymissíður.
    - Til að bæta nýjum einingum eða brotum við gámaeiningar velurðu úrfellingarhnappinn og síðan **Bæta við einingu** eða **Bæta við broti**.
    - Til að fjarlægja einingu úr skipulaginu skaltu velja úrfellingarhnappinn og velja síðan **Eyða**.

## <a name="change-a-preset-layout-theme"></a>Breyta forstilltu skipulagsþema

Dæmigerð framkvæmd er að setja sjálfgefið þema fyrir allar síður sem nota forstillt skipulag.

Fylgdu þessum skrefum til að stilla eða breyta þema fyrir allar undirsíður sem nota forstillt skipulag.

1. Í skipulagsritlinum í útlínutrénu til vinstri velurðu síðugámseininguna. (Venjulega er þessi eining annar hnúturinn og heitir hann **Sjálfgefin síða**.)
1. Í eiginleikaglugganum hægra megin, í reitnum **Þema**, velurðu þema.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Vistaðu, skráðu inn, forskoðaðu og birtu forstillt skipulag.

Til að vista og skrá inn forstillt skipulag skal fylgja þessum skrefum.

1. Veldu **Vista** efst í skipulagsritli. Vistaðar breytingar hafa ekki áhrif á forstreymissíðum fyrr en þær eru skráðar inn.
1. Veldu **Ljúka við breytingar**. Nú er hægt að uppgötva breytingarnar fyrir forstreymisflæði.

Til að forskoða breytingarnar skaltu annaðhvort opna fyrirliggjandi síðu sem notar forstillt skipulag eða búa til nýja síðu úr skipulaginu.

Eftir að þú hefur forskoðað breytingarnar á forstilltu skipulagi skaltu fylgja einu af þessum skrefum til að birta skipulagið á lifandi vefsvæði:

* Farðu í **Skipulag**, veldu skipulagið og veldu síðan **Birta**.
* Veldu útlitsheiti til að opna útlitsritil og veldu svo **Birta**.
* Birta síðu sem vísar til óbirta skipulagsins. Skipulagið verður sjálfkrafa birt.

> [!WARNING]
> Með mörgum síðum er hægt að vísa í forstillt skipulag. Þegar þú birtir forstillt skipulag þarftu að hafa í huga að þú gætir haft áhrif á skipulag margra síðna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]