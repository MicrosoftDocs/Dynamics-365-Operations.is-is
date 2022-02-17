---
title: Samstilla upplýsingar um birgðastöðu úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: Henrikan
ms.date: 05/07/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8dfba2d2dc2fdd4af136e3cb20061d794369011f
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060946"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Samstilla upplýsingar um birgðastöðu úr Supply Chain Management við Field Service 

[!include[banner](../includes/banner.md)]



Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla lagerstig birgða úr Supply Chain Management í Field Service.

**Sniðmát í gagnasamþættingu**
- Vörubirgðir (Supply Chain Management til Field Service)
  
**Verkefni í verki gagnasamþættingar**
- Birgðir afurðar

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:
- Vöruhús (Supply Chain Management við Field Service) 
- Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales) 

## <a name="entity-set"></a>Einingastamstæða

| Field Service                      | Birgðakeðjustjórnun                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse birgðir á lager eftir vöruhúsi     |

## <a name="entity-flow"></a>Einingaflæði
Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir. Upplýsingarnar um birgðastöðu fela í sér: 
- Lagermagn (núgildandi skráð efnislegt magn sem er staðsett í vöruhúsinu)
- Pöntunarmagn (heildarskráð magn í pöntun, t.d. sölupantanir)
- Pantað magn (samtals skráð pantað magn, t.d. innkaupapantanir)

Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.

Í Field Service býr samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service passi við stöðurnar í Supply Chain Management.

Supply Chain Management virkar sem aðalsniðmátið fyrir birgðastöður. Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Supply Chain Management ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Supply Chain Management.

Hægt er að stjórna vörum og vöruhúsum þar sem birgðastigum er náð frá Supply Chain Management með ítarlegri fyrirspurn og síun (Power Query).

> [!NOTE]
> Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá = Nei**) og síðan varpa þeim í stakt vöruhús í Supply Chain Management, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun. Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi eingöngu uppfærslur til Supply Chain Management. Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Supply Chain Management. Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Einingin **Ytri birgðir afurðar** er aðeins notuð fyrir bakvinnslu í samþættingunni. Þessi eining fær gildi fyrir birgðastöðu úr Supply Chain Management í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="data-integration"></a>Samþætting gagna
Til að verkið virki þarf að tryggja að samþættingarlykillinn sé uppfærður fyrir msdynce_externalproductinventories.
1.  Farið í **Gagnasamþætting > Tengjasöfn**.
2.  Veljið notaða tengjasafnið.
3.  Í flipanum **Samþættingarlykill** skal ganga úr skugga um að eftirfarandi lyklum sé bætt við msdynce_externalproductinventories:
      - msdynce_productnumber (afurðarnúmer)
      - msdynce_warehouseid (auðkenni vöruhúss)
      
### <a name="data-integration-project"></a>Gagnasamþættingarverk
Hægt er að nota síur með ítarlegri fyrirspurn og síun þannig að eingöngu ákveðnar afurðir og vöruhús sendi upplýsingar um birgðastöðu Supply Chain Management til Field Service.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Vörubirgðir (Supply Chain Management við Field Service): Product inventory

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]