---
title: Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "356784"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service 

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla stig birgða á lager úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

**Sniðmát í gagnasamþættingu**
- Birgðir afurðar (Finance and Operations til Field Service)
  
**Verkefni í verki gagnasamþættingar**
- Birgðir afurðar

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:
- Vöruhús (Finance and Operations til Field Service) 
- Afurðir Field Service með birgðaeiningu (Finance and Operations til Sales) 

## <a name="entity-set"></a>Einingastamstæða

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS-birgðir á lager eftir vöruhúsi     |

## <a name="entity-flow"></a>Einingaflæði
Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir. Upplýsingarnar um birgðastöðu fela í sér: 
- Lagermagn (núgildandi skráð efnislegt magn sem er staðsett í vöruhúsinu)
- Pöntunarmagn (heildarskráð magn í pöntun, t.d. sölupantanir)
- Pantað magn (samtals skráð pantað magn, t.d. innkaupapantanir)

Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.

Í Field Service býr samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service passi við stöðurnar í Finance and Operations.

Finance and Operations virkar sem aðalsniðmátið fyrir birgðastöður. Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Finance and Operations ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Finance and Operations.

Afurðir og vöruhús þar sem birgðastöður eru „mastered“ úr Finance and Operations er hægt að stjórna með ítarlegri fyrirspurn og afmörkun (Power Query).

> [!NOTE]
> Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá = Nei**) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun. Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi eingöngu uppfærslur til Finance and Operations. Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations. Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Einingin **Ytri birgðir afurðar** er aðeins notuð fyrir bakvinnslu í samþættingunni. Þessi eining fær gildi fyrir birgðastöðu úr Finance and Operations í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="data-integration-project"></a>Gagnasamþættingarverk
Hægt er að nota síur með ítarlegri fyrirspurn og síun þannig að eingöngu ákveðnar afurðir og vöruhús sendi upplýsingar um birgðastöðu úr Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Birgðir afurðar (Finance and Operations til Field Service): Birgðir afurðar

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
