---
title: Aðgangsréttindi fyrir stjórnborð kostnaðarhluta
description: Þetta efnisatriði hefur að geyma upplýsingar um aðgangsréttindi fyrir stjórnborð kostnaðarhlutar.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c30a7c2765647aad17a475ba8705b8e688d166593adf242fcd15d90e49334189
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733030"
---
# <a name="access-rights-for-cost-object-controllers"></a>Aðgangsréttindi fyrir stjórnborð kostnaðarhluta

[!include [banner](../includes/banner.md)]

Á vinnusvæðinu **Kostnaðarstýring** er miðpunktur þar sem stjórnendur geta skoðað afköst kostnaðarhluta sinna. Þetta vinnusvæði gerir stjórnendum kleift að nota gögn kostnaðarbókhalds þrátt fyrir að þeir séu ekki kostnaðarbókarar. Af öryggisástæðum ættu stjórnendur aðeins að geta séð þau gögn kostnaðarbókhalds sem tengjast þeim kostnaðarhlutum sem þeir bera ábyrgð á.

Það eru fjögur einkvæm hlutverk í kostnaðarbókhaldi.

| Heiti hlutverks               | Leyfi      |
|-------------------------|--------------|
| Aðalbókari kostnaðarbókhalds | Verkþáttur     |
| Kostnaðarbókari         | Aðgerðir   |
| Starfsmaður kostnaðarbókara   | Aðgerðir   |
| Stjórnborð kostnaðarhlutar  | Hópmeðlimir |

Í þessu efnisatriði er útskýrt hvernig á að úthluta stjórnanda hlutverkinu **Stjórnborð kostnaðarhlutar**.

Þegar hlutverkinu **Stjórnborð kostnaðarhlutar** er úthlutað stjórnanda getur hann framkvæmt eftirfarandi verkefni:

- Fengið aðgang að vinnusvæðinu **Kostnaðarstýring** (í biðlaranum).

    - Kafað ofan í og fengið skoðunaraðgang að þeim síðum sem styðja köfun.

- Fengið aðgang að vinnusvæðinu **Kostnaðarstýring** (í fartækjaforritinu).

> [!NOTE]
> Hlutverkið **Stjórnborð kostnaðarhlutar** stýrir ekki hvaða kostnaðarhlutum notandi hefur aðgang að og skoðað gögn fyrir. Öryggi á línustigi fæst í gegnum stigveldi vídda og stigveldi aðgangslista.

## <a name="grant-access-rights"></a>Veita aðgangsréttindi
Eftirfarandi dæmi sýnir hvernig víddarstigveldi getur litið út.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd    | Heiti gerðar víddarstigveldis      | Stigveldi aðgangslista |
|--------------------------|--------------|------------------------------------|-----------------------|
| Fyrirtæki             | Kostnaðarstaðir | Stigveldi víddaflokkunar | **Já**               |

Hægt er að nota flýtiflipann **Notendur** í stigveldishönnuði til að setja eitt eða fleiri notendakenni í hvern hnút.

|             Hnútar                 | Notendur            | Úr víddarstaki     |   Til víddarstaks   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Stofnun/fyrirtæki                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Stjórnandi                 | Apríl            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Fjármál   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Mannauður        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Framleiðsla            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkning | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Smölun  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Kostnaðarbókarar skulu vera í efsta stigi stigveldisins svo þeir geti séð allar færslur í kostnaðarbókhaldi.

Áður en hægt er að nota stigveldi aðgangslista og öryggisstillingar þess verður að stilla valkostinn **Virkja skoðunaraðgang fyrir víddarstök kostnaðarhluta** á **Já** á flipanum **Almennt** á síðunni **Færibreytur kostnaðarbókhalds** (**Kostnaðarbókhald** > **Uppsetning** > **Færibreytur**).

Stillingar fyrir stigveldi aðgangslista eru notaðar til að stjórna gögnunum sem birtast á eftirfarandi svæðum:

- Vinnusvæðið **Kostnaðarstýring** (í biðlaranum):

    - Gögn á síðum sem notaðar eru til köfunar

- Vinnusvæðið **Kostnaðarstýring** (í fartækjaforritinu):

    - Stöður í spjöldum

- Microsoft Power BI:

    - Gögn sem eru sýnd í Power BI myndrænum framsetningum
    - Myndræn Power BI gagnaframsetning sem er felld inn í Dynamics 365 Finance biðlarann

> [!IMPORTANT]
> - Áður en stigveldi aðgangslista getur haft áhrif á gögnin í Power BI, verður að para saman stigveldi og öryggi á línustigi í Power BI. Nánari upplýsingar eru í [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Þetta efnisatriði sýnir nauðsynlegar forsendur þess að hægt sé að nota vinnusvæðið **Kostnaðarstýring**.

Frekari upplýsingar

- [Vinnusvæði kostnaðarstýringar](cost-control-workspace.md)
- [Víddarstigveldi](dimension-hierarchy.md)
- [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
