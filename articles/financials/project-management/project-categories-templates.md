---
title: "Samstilla kostnaðarflokka verks frá Project Service Automation"
description: "Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.

> [!NOTE]
> Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation og Finance and Operations

Samþættingarlausn Project Service Automation og Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða umi kostnaðarfærsluflokka verks milli Finance and Operations og Project Service Automation.

Ef kostnaðarflokkar verks eru "mastered" í Finance and Operations er samþættingarflæðið fyrst frá Finance and Operations til Project Service Automation og síðan uppfærsla á samþættingum auðkenna fyrir kostnaðarflokka verks með því að samstilla frá Project Service Automation við Finance and Operations.

Ef kostnaðarflokkar verks eru "mastered" í Project Service Automation er samþættingarflæðið fyrst frá Project Service Automation til Finance and Operations. Verkflokkarnir verða þegar að vera skilgreindir í Finance and Operations fyrir samstillingu frá Project Service Automation. Síðan skal samtilla frá Finance and Operations og baka til Project Service Automation og síðan frá Project Service Automation til Finance and Operations aftur. Þetta tryggir að flokkarnir séu tengdir og afrit eru ekki búin til.

> [!NOTE]
> Venjulega verða kostnaðarflokkar verks "mastered" í Finance and Operations. Ef þetta eru ekki þínar kringumstæður eða þú ert þegar með kostnaðarflokka stofnaða í Project Service Automation verður þú fyrst að samstilla með því að nota kostnaðarfærsluflokka verks (PSA til Fin and Ops) og þá samstilla með kostnaðarfærsluflokka verks (Fin og Ops til PSA). Þú ættir síðan að keyra samstillingu frá PSA til Fin and Ops einu sinni enn.

> Ef fyrst er samstillt frá Project Service Automation verða verkflokkarnir að vera þegar uppsettir í Finance and Operations og allir verkflokkar sem þarf að samstilla við kostnaðarfærslur Project Service Automation verða að vera settir upp til að vera **Virkt í færslubókum**.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltæku sniðmátunum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Finance and Operations til Project Service Automation:

-  **Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (Fin Ops til PSA)
-  **Heiti verkefnis í verkinu:** Samstilla flokka við PSA

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Samþættingareining fyrir flokka    | Færsluflokkar        |

## <a name="entity-flow"></a>Einingaflæði

Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query til að stilla reikningsgerðina á færsluflokknum þegar samstillt er við Project Service Automation. Sniðmát kostnaðarfærsluflokka verks (Fin and Ops til PSA) hefur sjálfgefinn dálk og vörpun sem þegar hefur verið veitt. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við skilyrtum dálki í Power Query.
- Opnaðu snið Advance Query and Filtering innan vörpunar á verkefni fyrir kostnaðarflokka verks.
- Veldu **Bæta við skilyrtum dálki**.
- Gefðu nýja dálkinum heiti á borð við BillingType.
- Sláðu inn eftirfarandi skilyrði: ef **CATEGORYID er ekki jafnt og núll þá 19235001, annars núll**.
- Smelltu á **Í lagi** í dálkinum.
- Vertu viss um að varpa þessum nýja dálki á vörpunarsíðunni.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Finance and Operations við Project Service Automation.

[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Project Service Automation til Finance and Operations:

-**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (PSA til Fin and Ops) -**Heiti verkefnis í verkinu:** Samstilla flokka við Fin Ops

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Færsluflokkar          | Samþættingareining fyrir flokka  | 

## <a name="entity-flow"></a>Einingaflæði

Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar. Samstillingin til baka við Finance and Operations uppfærir auðkenni samþættingarinnar frá Project Service Automation í verkflokki Finance and Operations.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.

> [!NOTE]
> Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

