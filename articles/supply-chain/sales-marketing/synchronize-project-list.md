---
title: "Samstilla verklista úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Samstilla verklista úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á verkum úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

**Heiti sniðmátsins í Gagnaflutningi:**
- Verk (Finance and Operations til Field Service)

**Heiti verksins í gagnasamþættingarverki:**
- Verk

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:
- Lyklar (Sales til Finance and Operations) 

## <a name="entity-set"></a>Einingastamstæða
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Verk                |

## <a name="entity-flow"></a>Einingaflæði
Verk eru búin til í Finance and Operations. Verk með **Gerð verks** tími og efni og **Verkstig** í vinnslu samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil. Listinn yfir **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Finance and Operations.
Ytra verk CRM-lausnir Field Service er ný eining sem fær öll verkin úr Operations.
Reitnum Ytri verk hefur verið bætt við eininguna Vinnupantanir. Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Operations. Þegar kerfisstaða breytist í Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum Ytri verk læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning
### <a name="in-finance-and-operations"></a>Í Finance and Operations
Virkja rakningarbreytingu fyrir verk gagnaeiningar

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Verk (Finance and Operations til Field Service): Verk

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)

