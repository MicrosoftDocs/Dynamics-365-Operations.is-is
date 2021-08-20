---
title: Yfirlit yfir fínstillingu skipulagningar
description: Þessi grein veitir yfirlit yfir virkni fínstillingar áætlunargerðar.
author: ChristianRytt
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8fd73313b82319c35eb5fccbd68cd305403bfe3f635f6b267fb408943af3396c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739060"
---
# <a name="planning-optimization-overview"></a>Yfirlit yfir fínstillingu skipulagningar

[!include [banner](../../includes/banner.md)]

Viðbótin Fínstilling skipulagningar fyrir Microsoft Dynamics 365 Supply Chain Management gerir útreikning á aðaláætlunargerð mögulega utan Dynamics 365 Supply Chain Management og tengds SQL gagnagrunns. Ávinningurinn sem tengist virkninni fínstilling skipulags felur í sér bætt afköst og lágmarks áhrif á SQL gagnagrunn meðan á keyrslu aðaláætlunargerðar stendur. Hægt er að framkvæma skjótar áætlunarkeyrslur jafnvel á skrifstofutíma, þannig að skipuleggjendur geta strax brugðist við breytingum á kröfum eða færibreytum.

Til að nota fínstillingu skipulags verður þú að setja upp viðbótina fínstilling skipulags úr verkinu í Microsoft Dynamics Lifecycle Services (LCS) og kveikja á virkninni fínstilling skipulagningar í Supply Chain Management. Frekari upplýsingar er að finna í [Hafist handa með fínstillingu skipulags](get-started.md).

Eftirfarandi mynd sýnir kostinn við að keyra fínstillingu skipulags á skrifstofutíma.

![Ávinningur af því að keyra fínstillingu skipulagningar á vinnutíma.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Bætt afköst

Fínstillingu skipulags er hægt að nota í atburðarásum sem fela í sér tímafrekar aðaláætlanir. Hún er sérstaklega hönnuð fyrir afar hraða útreikninga sem fela í sér mjög mikið magn af gögnum. Vegna þess að hún er byggð sem kvarðanleg fjölhæf þjónusta geta mörg tilvik unnið saman samtímis til að reikna áætlunina. Að auki fjarlægir skipulagsþjónustan álag aðaláætlunar úr kerfinu og vinnur með gagnastrreymi sem lágmarkar álag á netþjóninn.

Fínstilling skipulags getur hjálpað þér að ná eftirfarandi markmiðum:

- Bæta áætlunarafköst með styttri keyrslutíma.
- Draga úr áhrifum á aðra ferla meðan á keyrslu aðaláætlunargerðar stendur.
- Gera tíðari áætlunarkeyrslur. (Þú takmarkast ekki við daglega keyrslu.)
- Treystu því að framtíðarvöxtur fyrirtækisins mun ekki leggja of mikið á áætlunarkerfið.

## <a name="architecture-and-data-flow"></a>Skipulag og gagnaflæði

Þegar viðbótin fínstilling áætlunargerðar er sett upp úr LCS er komið á öruggri tengingu við þjónustuna Fínstilling skipulags. Þjónustan er staðsett í sama landi eða svæði gagnaversins og tengd tilvik af Supply Chain Management. Þegar fínstilling skipulagningar hefur verið sett upp eru aðalgögn og færslugögn send úr Supply Chain Management í þjónustu Fínstilling skipulags þegar aðaláætlunargerð er keyrð.

Ef viðbótin fínstilling skipulagningar er fjarlægð eru öll tengd gögn í þjónustu fínstillingar skipulags fjarlægð.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Hátt stig gagnaflæðis fyrir endurmyndunarkeyrslur

1. Biðlari Supply Chain Management sendir merki til að biðja um áætlunarkeyrslu úr Fínstillingu skipulagningar.
2. Fínstilling skipulagningar fer fram á nauðsynleg gögn um samþætt tengi.
3. SQL gagnagrunnurinn sendir umbeðnar upplýsingar um uppsetningar-, meistara- og færslugögn til fínstillingar skipulags í gegnum tengið. Tengingin þýðir upplýsingar á milli þjónustunnar Supply Chain Management og fínstillingar skipulagningar.
4. Þjónustan Fínstilling skipulags geymir áætlunargerðarstengd gögn í minni og gerir nauðsynlega útreikninga.
5. Niðurstöður áætlunar eru sendar í gagnagrunn Supply Chain Management í gegnum tengið. Niðurstöðurnar innihalda upplýsingar eins og fyrirhugaðar pantanir og upplýsingar um þarfarakningu. Fínstilling skipulags sendir merki til Supply Chain Management til að gefa til kynna að áætlunarkeyrslunni sé lokið. Hún sendir einnig viðeigandi skilaboð og viðvaranir.

Eftirfarandi skýringarmynd sýnir gagnaflæðið.

![Gagnaflæði fyrir keyrslur endurmyndunar.](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Tengd tilföng

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]