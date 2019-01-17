---
title: "Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla upplýsingar um birgðastöðu úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service 

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla upplýsingar um birgðastöðu úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á birgðastöðu á lager úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

**Heiti sniðmátsins í Gagnaflutningi:**
- Birgðir afurðar (Finance and Operations til Field Service)
  
**Heiti verksins í gagnasamþættingarverki:**
- Birgðir afurðar

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:
- Vöruhús (Finance and Operations til Field Service) 
- Afurðir Field Service með birgðaeiningu (Finance and Operations til Sales) 

## <a name="entity-set"></a>Einingastamstæða

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS-birgðir á lager eftir vöruhúsi     |

## <a name="entity-flow"></a>Einingaflæði
Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir. Upplýsingar um birgðastöðu innihalda: 
- Lagermagn (núgildandi skráð raunmagn sem er staðsett í vöruhúsinu)
- Pöntunarmagn (samtals skráð magn í pöntun - t.d. sölupöntun)
- Pantað magn (samtals skráð pantað magn - t.d. innkaupapöntun)

Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.

Í Field Service bjó samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service til að passa við stöðurnar í Finance and Operations.

Finance and Operations virkar sem aðalsniðmátið fyrir birgðastöður. Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Finance and Operations ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Finance and Operations.

Afurðir og vöruhús þar sem birgðastöður eru „mastered“ úr Finance and Operations er hægt að stjórna með ítarlegri fyrirspurn og afmörkun (Power Query).

Athugið: Mögulegt er að búa til mörg vöruhús í Field Services (með Er viðhaldið utan frá = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun. Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations. Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations. Sjá viðbótarupplýsingar í Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations og Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Birgðaeining ytri afurðar er ný eining sem er aðeins notuð fyrir bakvinnslu í samþættingunni. Hún fær gildi fyrir birgðastöðu úr Finance and Operations í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu. 

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="in-the-data-integration-project"></a>Í gagnasamþættingarverkinu
Nota síur með ítarlegri fyrirspurn og síun til að stýra því að eingöngu æskilegar afurðir og vöruhús sendi upplýsingar um birgðastöðu úr Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Birgðir afurðar (Finance and Operations til Field Service): Birgðir afurðar

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

