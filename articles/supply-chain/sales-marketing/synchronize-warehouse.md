---
title: Samstilla vöruhús úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "340316"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Samstilla vöruhús úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu vöruhúss milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Field Service.

**Sniðmát í gagnasamþættingu**
- Vöruhús (Finance and Operations til Field Service)

**Verkefni í verki gagnasamþættingar**
- Vöruhús

## <a name="entity-set"></a>Einingastamstæða
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Vöruhús                             |

## <a name="entity-flow"></a>Einingaflæði
Vöruhús sem eru búin til og unnið með í Finance and Operations er hægt að samstilla við Field Service í gegnum verk gagnasamþættingar Common Data Service (CDS). Vöruhús sem á að samstilla við Field Service er hægt að stýra með ítarlegri fyrirspurn og síun í verkinu. Vöruhús sem samstillast úr Finance and Operations eru búin til í Field Service með reitinn **Er viðhaldið utan frá** stilltan á **Já** og færslan er gerð skrifvarin.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Til að styðja við samþættingu milli Field Service og Finance and Operations, er þörf á frekari virkni frá CRM-lausn Field Service. Í lausninni hefur reitnum **Er viðhaldið utan frá** verið bætt við eininguna **Vöruhús (msdyn_warehouses)**. Þessi reitur hjálpar til við að bera kennsl á hvort vöruhúsið sé meðhöndlað í Finance and Operations eða ef það er aðeins til í Field Service. Stillingar fyrir þennan reit innihalda:
- **Já** – Vöruhús á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.
- **Nei** - Vöruhúsið var fært beint inn í Field Service og er unnið með það hér.

Reiturinn **Er viðhaldið að utan** hjálpar til við að stjórna samstillingu á birgðastöðum, leiðréttingum, flutningum og notkun á vinnupöntunum. Aðeins ef **Er viðhaldið að utan** vöruhúss er stillt á **Já** er hægt að nota til að samstilla beint við sama vöruhúsið í öðru kerfi. 

> [!NOTE]
> Mögulegt er að búa til mörg vöruhús í Field Service (með **Er viðhaldið utan frá** = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun. Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations. Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations. Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning
### <a name="data-integration-project"></a>Gagnasamþættingarverk
Á undan samstillingu vöruhúsa skal ganga úr skugga um að uppfæra ítarlega fyrirspurn og síun á verkinu til að hafa eingöngu með vöruhús sem þú vilt taka með úr Finance and Operations og yfir í Field Service. Athugaðu að þú þarft vöruhúsið í Field Service til að nota það fyrir vinnupantanir, leiðréttingar og flutninga.  

Til að ganga skugga um að **Samþættingarlykill** sé til fyrir **msdyn_warehouses**:
1. Farðu í gagnasamþættingu.
2. Veldu flipann **Tengistilling**.
3. Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar.
4. Veldu flipann **Samþættingarlykill**.
5. Finndu msdyn_warehouses og gakktu úr skugga um að lyklinum **msdyn_name (heiti)** hafi verið bætt við. Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi mynd sýnir sniðmátsvörpunina í Gagnasamþættingu.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Vöruhús (Finance and Operations til Field Service): Vöruhús

[![Sniðmátsvörpun í Gagnasamþættingu](./media/Warehouse1.png)](./media/Warehouse1.png)