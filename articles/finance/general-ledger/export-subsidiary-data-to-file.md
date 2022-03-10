---
title: Flytja út gögn dótturfyrirtækis í skrár
description: Þetta efnisatriði útskýrir hvernig á að undirbúa útflutning gagna úr Microsoft Dynamics 365 Finance og síðan flytja þau inn í sameinaðan lögaðila.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 02ae9945f7b67fb64be78a024910d7e1151c7446fd54b71034c5ba448c00b081
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768772"
---
# <a name="export-subsidiary-data-to-files"></a>Flytja út gögn dótturfyrirtækis í skrár

[!include [banner](../includes/banner.md)]

Síðan **Flytja út** (**Kerfisstjórnun \> Vinnusvæði \> Flytja inn/út**) er notuð til að undirbúa útflutning á gögnum dótturfyrirtækis í skrár sem síðan verður hægt að flytja inn í sameinaðan lögaðila. Frekari upplýsingar um inn- og útflutningsferlið er að finna í [Yfirliti yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Stofnið lögaðila fyrir sameiningarferlið. Frekari upplýsingar um hvernig á að stofna lögaðila er að finna í [Stofna lögaðila](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Frekari upplýsingar er að finna í [Undirbúa lögaðila til að nota í sameiningarferlinu](prepare-company-for-consolidation.md) og [Setja upp dótturfyrirtæki lögaðila fyrir sameiningu](set-up-subsidiary-company-for-consolidation.md). 

2. Farið í **Sameiningar \> Flytja út stöður fyrirtækis**. Á síðunni **Flytja út stöður fyrirtækis**, í flipanum **Skilyrði**, skal tilgreina upplýsingar um sameininguna með því að stilla eftirfarandi reiti.

    | Svæði                             | lýsing |
    |-----------------------------------|-------|
    | Aðallykill                      | Tilgreinið lyklana sem á að sameina. Til að hafa alla lykla með skal skilja þennan reit eftir auðan. |
    | Nota samstæðulykil         | Ef samstæðulyklar hafa verið tilgreindir skal stilla þennan valkost á **Já**. |
    | Velja samstæðulykil frá | Veljið annaðhvort **Aðallykil** eða **Flokk samstæðulykla**. |
    | Flokkur samstæðulykla       | Veljið flokk samstæðulykla fyrir samstæðulykilinn sem var valinn. |
    | Samstæðutímabil              | Tilgreinið „frá“ og „til“ dagsetningar fyrir samstæðuna. |
    | Taka raunupphæðir með            | Stillið þennan valkost á **Já** til að hafa með raunupphæðir. |
    | Taka áætlunarupphæðir með            | Stillið þennan valkost á **Já** til að hafa upphæðir fjárhagsáætlunar með í samstæðum. |
    | Fjárhagsáætlunarlíkön                     | Tilgreinið fjárhagsáætlunarlíkanið sem á að hafa með. |

3. Í flipanum **Fjárhagsvíddir** skal tilgreina upplýsingar um samstæðuna:

    - Tilgreinið upplýsingar um fjárhagsvíddir sem á að flytja úr færslunum í lyklum dótturfyrirtækis og yfir í færslurnar í sameinuðum lögaðila.
    - Veljið fjárhagsvíddir úr listanum.
    - Auðkennið rétta forskrift fyrir hverja fjárhagsvídd sem er sameinuð. Tiltækir valmöguleikar fela í sér **Vídd**, **Flokkavídd**, **Lyklar fyrirtækis** og **Lykill**.

        > [!NOTE]
        > Valkosturinn **Flokkavídd** gerir kleift að skilgreina víddargildi sem er notað af fyrirtækjahópnum sem verið er að sameina.

    - Tilgreinið hlutaröðina til að sameina í.

4. Í flipanum **Lögaðilar** skal fylgja þessum skrefum til að tilgreina lögaðilann sem á að flytja út:

    1. Veljið **Nýtt**.
    2. Í reitinn **Upprunalegur lögaðili** skal færa inn lögaðilann.

        Ef sama skilyrðið er notað á nokkur dótturfyrirtæki sem eru í sama gagnagrunninum, er hægt að flytja gögn úr þessum dótturfyrirtækjum til þess aðskilja útflutningsskrár í einni aðgerð:

        1. Stofnið línu fyrir hvern lögaðila dótturfyrirtækis þar sem á að flytja út lykla í skrár. Þessar skrár eru fluttar inn í samstæðufyrirtæki lögaðilanna seinna.
        2. Fyrir hvert dótturfyrirtæki er fært inn nafn dótturfyrirtækis og nafn útflutningsskrárinnar sem stofnuð verður í útflutningsvinnslunni.

    3. Í reitnum **Lyklagerð umreikningsmismunar** skal velja **Hagnaður og tap** eða **Efnahagsreikningur**.
    4. Færið inn skráarheiti fyrir útflutningsskrána sem verður stofnuð.

5. Veljið **Í lagi** til að keyra útflutninginn.

Þegar útflutningi er lokið koma upp skilaboð sem sýna fjölda færslna sem var vistaður í hverja skrá. Síðan er hægt að flytja inn skrárnar í sameinuðu lögaðilanna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]