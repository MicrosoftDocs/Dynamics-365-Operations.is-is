---
title: Samstilla verklista úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5cb7f8b9a3107a7787c787ace71ab574457b1646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828491"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Samstilla verklista úr Supply Chain Management við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu verka úr Supply Chain Management í Field Service.

**Sniðmát í gagnasamþættingu**
- Verk (Supply Chain Management við Field Service)

**Verkefni í verki gagnasamþættingar**
- Verk

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:
- Lyklar (Sales til Supply Chain Management) 

## <a name="entity-set"></a>Einingastamstæða
| Field Service           | Birgðakeðjustjórnun  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Verk                |

## <a name="entity-flow"></a>Einingaflæði
Verkefni eru búin til í Supply Chain Management. Verk með **Gerð verks** stillt á **Tími og efni** og **Verkstig** still á **Í vinnslu** samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil. Listinn **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Supply Chain Management.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Einingin **Ytra verk** fær öll verkefnin úr Supply Chain Management. Reitnum **Ytra verk** hefur verið bætt við eininguna **Vinnupöntun**. Þetta er uppflettireitur, og með því að merkja verkbeiðnina með verki mun sölupöntun verða tengd við verk innan Supply Chain Management. Þegar **Kerfisstaða** breytist úr **Opin - Í vinnslu (690.970.000)** yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning
### <a name="supply-chain-management"></a>Birgðakeðjustjórnun
Virkja rakningarbreytingu fyrir verk gagnaeiningar.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Verk (Supply Chain Management við Field Service): Projects

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]