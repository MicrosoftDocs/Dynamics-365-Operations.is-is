---
title: Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250508"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Dynamics 365 Finance og Dynamics 365 Project Service Automation.

> [!NOTE]
> - Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í útgáfu 8.0.
> - Samþætting á rauntölum er í boði í útgáfu 8.0.1 eða nýrri.
> - Ef þú notar Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Gagnaflæði fyrir Project Service Automation og Finance

Samþættingarlausn Project Service Automation og Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða umi kostnaðarfærsluflokka verks milli Finance og Project Service Automation.

Ef kostnaðarflokkar verks eru „mastered“ í Finance er samþættingarflæðið fyrst frá Finance til Project Service Automation. Ef samþættingarkenni kostnaðarflokka verks eru síðan uppfærðir með samstillingu frá Project Service Automation í Finance.

Ef kostnaðarflokkar verks eru "mastered" í Project Service Automation er samþættingarflæðið fyrst frá Project Service Automation til Finance. Verkflokkarnir verða þegar að vera skilgreindir í Finance fyrir samstillingu frá Project Service Automation. Síðan skal samtilla frá Finance og baka til Project Service Automation og síðan frá Project Service Automation til Finance aftur. Þannig hjálpar þú að tryggja að flokkarnir séu tengdir og að engar tvítekningar séu búnar til.

> [!NOTE]
> Venjulega eru kostnaðarflokkar verks „mastered“ í Finance. Ef þeir eru það hins vegar ekki eða ef kostnaðarflokkar hafa þegar verið búnir til í Project Service Automation verður þú fyrst að samstilla með því að nota sniðmát fyrir kostnaðarfærsluflokka verks (PSA til Fin og Ops). Samstilltu síðan með sniðmáti fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA). Þú ættir þá að keyra samstillingu frá Project Service Automation í Finance einu sinni enn.
>
> Ef þú samstillir fyrst frá Project Service Automation verður að uppfylla eftirfarandi skilyrði í Finance áður en samstillingin er keyrð:
>
> - Samnýttur flokkur sem passar við verktegundina sem er sett upp í Project Service Automation verður að vera til og hann verður að vera virkur fyrir bæði **Verk** og **Kostnað**.
> - Fyrir hvern lögaðila Finance sem þarf að samþætta við, verða eftirfarandi verktegundir að vera til staðar:
>
>     - **Verktegund** er til staðar. 
>     - **Nota í kostnað** er virkt.
>     - **Virkt í færslubók** er virkt.
>     - **Færslugerð** er stillt á **Kostnaður**.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Samstilling á kostnaðarflokki verks frá Finance í Project Service Automation

### <a name="template-and-task"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla kostnaðarflokka verks úr Finance við Project Service Automation:

- **Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (Fin Ops til PSA)
- **Heiti verkefnis í verkinu:** Samstilla flokka við PSA

### <a name="entity-set"></a>Einingastamstæða

| Fjármál                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Samþættingareining fyrir flokka | Færsluflokkar     |

### <a name="entity-flow"></a>Einingaflæði

Kostnaðarflokkum verks er stjórnað í Finance og þeir eru samstilltir við Project Service Automation sem færsluflokkar.

### <a name="power-query"></a>Power Query

Þegar þú samstillir í Project Service Automation verður þú að nota Microsoft Power Query fyrir Excel til að stilla reikningsgerðina á færsluflokknum. Sniðmát fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA) veitir sjálfgefinn dálk og vörpun. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við skilyrtum dálki í Power Query. Fylgdu eftirfarandi skrefum.

1. Smelltu á örina til að opna vörpunina á verkefni fyrir kostnaðarflokka verks í sniðmáti fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA).
2. Smelltu á tengilinn **Ítarleg fyrirspurn og síun** til að opna Power Query.
2. Veldu **Bæta við skilyrtum dálki**.
3. Sláðu inn heiti á nýja dálknum, t.d. **BillingType**.
4. Sláðu inn eftirfarandi skilyrði: **ef CATEGORYID er ekki jafnt og núll, þá 19235001, annars núll**.
5. Smelltu á **Í lagi** í dálkinum.
6. Vertu viss um að varpa þessum nýja dálki á vörpunarsíðunni.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar úr Finance við Project Service Automation.

[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Samstilling á kostnaðarflokki verks úr Project Service Automation við Finance

### <a name="template-and-task"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla kostnaðarflokka verks úr Project Service Automation við Finance:

- **Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (PSA til Fin and Ops)
- **Heiti verkefnis í verkinu:** Samstilla flokka við Fin Ops

### <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Fjármál                           |
|----------------------------|-----------------------------------|
| Færsluflokkar     | Samþættingareining fyrir flokka |

### <a name="entity-flow"></a>Einingaflæði

Kostnaðarflokkum verks er stjórnað í Finance og þeir eru samstilltir við Project Service Automation sem færsluflokkar. Samstillingin til baka í Finance uppfærir verktegundina í Finance með samþættingarkennið frá Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.

> [!NOTE]
> Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance.

[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
