---
title: "Skilgreining aðgangsréttinda stjórnborða kostnaðarhlutar"
description: "Þetta efnisatriði hefur að geyma upplýsingar um aðgangsréttindi fyrir stjórnborð kostnaðarhlutar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 4d26d690e63898bfb463177da6654f1175ff35af
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017


---

## <a name="access-rights-of-a-cost-object-controller"></a>Aðgangsréttindi stjórnborðs kostnaðarhlutar

[!include[banner](../includes/banner.md)]

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

|                                   | Notendur            | Svið víddarstaks   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Hnútar**                         | **Notandakenni**      | **Úr víddarstaki** | **Til víddarstaks** |
| Fyrirtæki                      | Benjamin, Claire |                           |                         |
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

    - Gögn sem birtast í myndrænni framsetningu Power BI
    - Myndræn framsetning gagna í Power BI sem eru innfelldar í biðlaranum Microsoft Dynamics 365 for Finance and Operations, Enterprise edition

> [!IMPORTANT]
> - Áður en stigveldi aðgangslista getur haft áhrif á gögn í Power BI verður að para stigveldi aðgangslista og öryggi á línustigi í Power BI. Nánari upplýsingar eru í [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](/dynamics365/operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack).
> - Þetta efnisatriði sýnir nauðsynlegar forsendur þess að hægt sé að nota vinnusvæðið **Kostnaðarstýring**.

Sjá einnig

- [Vinnusvæði kostnaðarstýringar](cost-control-workspace.md)
- [Víddarstigveldi](dimension-hierarchy.md)
- [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](/dynamics365/operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack)
