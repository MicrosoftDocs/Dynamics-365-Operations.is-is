---
title: Samstilla verklista úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "312509"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Samstilla verklista úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á verkum milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Field Service.

**Sniðmát í gagnasamþættingu**
- Verk (Finance and Operations til Field Service)

**Verkefni í verki gagnasamþættingar**
- Verk

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:
- Lyklar (Sales til Finance and Operations) 

## <a name="entity-set"></a>Einingastamstæða
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Verk                |

## <a name="entity-flow"></a>Einingaflæði
Verk eru búin til í Finance and Operations. Verk með **Gerð verks** stillt á **Tími og efni** og **Verkstig** still á **Í vinnslu** samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil. Listinn **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Finance and Operations.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Einingin **Ytra verk** fær öll verkefnin úr Finance and Operations. Reitnum **Ytra verk** hefur verið bætt við eininguna **Vinnupöntun**. Þetta er uppflettireitur og með því að merkja vinnupöntunina þína við verk mun sölupöntunin tengjast við verkið innan Finance and Operations. Þegar **Kerfisstaða** breytist úr **Opin - Í vinnslu (690.970.000)** yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning
### <a name="finance-and-operations"></a>Finance and Operations
Virkja rakningarbreytingu fyrir verk gagnaeiningar.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Verk (Finance and Operations til Field Service): Verk

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)
