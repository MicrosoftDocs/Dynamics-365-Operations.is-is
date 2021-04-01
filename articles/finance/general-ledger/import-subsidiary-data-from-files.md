---
title: Flytja inn gögn dótturfyrirtækis úr skrám
description: Þetta efnisatriði útskýrir hvernig á að undirbúa gögn úr ytri kerfum þannig að hægt sé að flytja þau inn í Microsoft Dynamics 365 Finance.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f8e220599d8df9f560da1862f0909cbbaa3c7330
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249096"
---
# <a name="import-subsidiary-data-from-files"></a>Flytja inn gögn dótturfyrirtækis úr skrám

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að undirbúa gögn úr ytri kerfum þannig að hægt sé að flytja þau inn í Microsoft Dynamics 365 Finance. Síðan **Sameina við innflutning** (**Sameiningar \> Sameina við innflutning**) er notuð til að undirbúa flutning gagna dótturfyrirtækis úr ytri kerfum.

1. Stofna lögaðila dótturfyrirtækis fyrir sameininguna. Frekari upplýsingar um hvernig á að stofna lögaðila er að finna í [Stofna lögaðila](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Frekari upplýsingar er að finna í [Undirbúa lögaðila til að nota í sameiningarferlinu](prepare-company-for-consolidation.md) og [Setja upp dótturfyrirtæki lögaðila fyrir sameiningu](set-up-subsidiary-company-for-consolidation.md).

2. Undirbúið skrá sem mun innihalda gögnin sem eru flutt inn. Frekari upplýsingar um innflutningsferlið er að finna í yfirlitinu [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Flytjið gögnin út í skrá með því fylgja leiðbeiningnum í ferlinu „Ferli gagnainnflutnings/-útflutnings“ í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Hægt er að nota þetta ferli til að sameina gögn annaðhvort úr öðru tilviki af Dynamics 365 Finance eða úr Dynamics 365 Business Central. Ef verið er að flytja inn gögn úr ytri kerfum verða gögn að vera á því sniði sem lýst er í [Flytja út gögn dótturfyrirtækis í skrár](export-subsidiary-data-to-file.md).
4. Farið í **Sameiningar \> Sameina við innflutning**. Á síðunni **Sameina við innflutning**, í flipanum **Skilyrði**, skal gefa upplýsingar um skýrsluna og/eða innflutninginn með því að stilla eftirfarandi reiti.

    | Svæði                                 | Gildi fyrir skýrsluna | Gildi fyrir innflutninginn |
    |---------------------------------------|----------------------|----------------------|
    | lýsing                           | Ekki tiltækt | Færið inn lýsingu til að bera kennsl á innflutninginn. |
    | Aðallykill                          | Skilgreinið umfang lykla sem skýrslan á að innihalda. Ef umfang er ekki skilgreint verða allir lyklar teknir með. | Skilgreinið umfang lykla sem innflutningurinn á að taka með. Ef umfang er ekki skilgreint verða allir lyklar teknir með. |
    | Samstæðutímabil                  | Skilgreinið dagsetningabilið fyrir sameiningu. | Skilgreinið dagsetningabilið fyrir sameiningu. |
    | Taka raunupphæðir með                | Stillið þennan valkost á **Já** til að hafa með raunupphæðir. | Stillið þennan valkost á **Já** til að hafa með raunupphæðir. |
    | Taka áætlunarupphæðir með                | Stillið þennan valkost á **Já** til að hafa upphæðir fjárhagsáætlunar með í samstæðum. | Stillið þennan valkost á **Já** til að hafa upphæðir fjárhagsáætlunar með í samstæðum. |
    | Endurbyggja stöður við sameiningu | Stillið þennan valkost á **Já** ef endurbyggingarferlið á að hreinsa stöðuna og nýjar færslur að fullu og búa til stöðuna aftur frá upphafi. | Stillið þennan valkost á **Já** ef endurbyggingarferlið á að hreinsa stöðuna og nýjar færslur að fullu og búa til stöðuna aftur frá upphafi. |
    | Fjárhagsáætlunarlíkön                         | Ekki tiltækt | Ef valið var að flytja inn upphæðir fjárhagsáætlunar skal færa inn fjárhagsáætlunarlíkön sem á að sameina. |
    | Taxtagerð fjárhagsáætlunar                      | Ekki tiltækt | Færið inn gerð fjárhagsáætlunargengis. |

6. Ef um er að ræða aðra bókhaldsgjaldmiðla skal nota reitina í flipanum **Umreikningur gjaldmiðils** til að stilla umreikninginn sem er gerður við sameiningu.

    | Svæði                      | lýsing |
    |----------------------------|-------------|
    | Upprunalögaðili        | Veljið lögaðilann sem flutt er inn frá. |
    | Upprunabókhaldsgjaldmiðill | Þessi sjálfgefni gjaldmiðill er gjaldmiðillinn sem tengist upprunalegum lögaðila sem var valinn í reitnum **Upprunalegur lögaðili**. |
    | Frá og til lyklar       | Skilgreinið umfang lykla sem á að flytja inn úr upprunalegum lögaðila. |
    | Gerð gengis         | Veljið gerð gengis. Gerð gengis er úthlutað þegar aðallykill er stofnaður. Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-main-account.md). |
    | Beita gengi frá og með   | Færið inn dagsetningu til að nota gengið sem var í gildi á þeim degi. Einnig er hægt að færa inn gildið sem á að nota sem gengið. |
    | Gengi              | Sjálfgefna gildið er háð gerð gengis sem var valið í reitnum **Gerð gengir**. Ef fært var inn notandaskilgreint gengi er hægt að skilgreina taxta. |

7. Stillið valkostinn **Keyra í bakgrunni** á **Já** til að virkja innflutningsferlið þannig að það keyri í bakgrunni.
8. Stillið valkostinn **Runuvinnsla** á **Já** til að keyra sameininguna sem runuvinnslu á tilteknum tíma. Til að keyra sameiningu strax skal velja **Í lagi**. 

Færslurnar og stöðurnar sem tilgreindar voru fyrir samstæðu í dótturfyrirtækjunum er bætt við viðeigandi lykla sameinaða lögaðilans.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]