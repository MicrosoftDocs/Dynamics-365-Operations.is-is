---
title: "Samstilla vöruhús úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Samstilla vöruhús úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á vöruhúsum úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

**Heiti sniðmátsins í Gagnaflutningi:**
- Vöruhús (Finance and Operations til Field Service)

**Heiti verksins í gagnasamþættingarverki:**
- Vöruhús

## <a name="entity-set"></a>Einingastamstæða
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Vöruhús                             |

## <a name="entity-flow"></a>Einingaflæði
Vöruhús sem eru búin til og unnið með í Finance and Operations er hægt að samstilla við Field Service í gegnum verk gagnasamþættingar Common Data Service (CDS). Æskileg vöruhús sem samstillast við Field Service er hægt að stýra með ítarlegri fyrirspurn og síun í verkinu. Vöruhús sem samstillast úr Finance and Operations eru búin til í Field Service með reitinn Er viðhaldið utanfrá stilltan á Já og færslan er gerð skrifvarin.
CRM-lausn Field Service Til að styðja við samþættingu milli Field Service og Finance and Operations, er þörf á frekari virkni frá CRM-lausn Field Service. Lausnin inniheldur eftirfarandi breytingar.
Reitnum **Er viðhaldið utanfrá** hefur verið bætt við eininguna **Vöruhús (msdyn_warehouses)**. Þessi reitur hjálpar til við að bera kennsl á hvort vöruhúsið sé meðhöndlað í Operations eða ef það er aðeins til í Field Service.
- Já – Vöruhús á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.
- Nei - Vöruhúsið var fært beint inn í Field Service og er unnið með það hér.

Reiturinn **Er viðhaldið að utan** hjálpar til við að stjórna samstillingu á birgðastöðum, leiðréttingum, flutningum og notkun á vinnupöntunum. Aðeins vöruhús með **Er viðhaldið að utan** = Já er hægt að nota til að samstilla beint við sama vöruhúsið í öðru kerfi. 

Athugið: Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá** = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun. Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations. Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations. Sjá viðbótarupplýsingar í Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations og Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning
### <a name="in-the-data-integration-project"></a>Í gagnasamþættingarverkinu
Á undan samstillingu vöruhúsa skal ganga úr skugga um að uppfæra ítarlega fyrirspurn og síun á verkinu til að hafa eingöngu með vöruhús sem þú vilt taka með úr Finance and Operations og yfir í Field Service. Athugaðu að þú þarft vöruhúsið í Field Service til að nota það fyrir vinnupantanir, leiðréttingar og flutninga.  

Gakktu úr skugga um að **Samþættingarlykill** sé til fyrir **msdyn_warehouses**
1. Farðu í gagnasamþættingu
2. Veldu flipann **Tenging stillt**
3. Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar
4. Veldu flipann **Samþættingarlykill**
5. Finndu msdyn_warehouses og athugaðu hvort lyklinum **msdyn_name (heiti)** hafi verið bætt við. Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Vöruhús (Finance and Operations til Field Service): Vöruhús

[![Sniðmátsvörpun í Gagnasamþættingu](./media/Warehouse1.png)](./media/Warehouse1.png)

