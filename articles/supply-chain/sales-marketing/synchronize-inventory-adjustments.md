---
title: Samstilla birgðaflutninga og leiðréttingar úr Field Service við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/14/2019
ms.locfileid: "842416"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla birgðaleiðréttingar og flutninga úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.

**Sniðmát í gagnasamþættingu**
- Leiðrétting á birgðaskrá (Field Service til Fin and Ops)
- Gagnaflutningur á birgðum (Field Service til Fin and Ops)

**Verkefni í gagnasamþættingarverkum**
- Birgðaleiðréttingar
- Birgðaflutningar

## <a name="entity-set"></a>Einingastamstæða
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-færslubókarhausar og línur leiðréttingar á birgðaskrá |
| msdyn_inventoryadjustmentproducts | CDS-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá   |

## <a name="entity-flow"></a>Einingaflæði
Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Finance and Operations eftir að **Staða bókunar** breytist úr **Stofnað** í **Bókað**. Þegar þetta gerist verður leiðréttingin eða flutningspöntunin læst og verða aðeins skrifvarið. Þetta þýðir að bóka megi leiðréttingar og flutninga í Finance and Operations, en ekki er hægt að breyta þeim. Í Finance and Operations er hægt að setja upp runuvinnslu til að bóka færslubækur leiðréttinga og birgðaflutninga sjálfvirkt sem myndast við samþættinguna. Sjá eftirfarandi skilyrði til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service 
Reitnum **Birgðaeining** hefur verið bætt við **Afurðareiningu**. Þessi reitur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Finance and Operations, og þörf er á birgðaeiningunni fyrir birgðir í vöruhúsi í Finance and Operations.
Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildi afurðar í birgðum. Ef gildi finnst verður reitnum **Eining** læst á Afurð birgðaleiðréttingar.

Reitnum **Staða bókunar** hefur verið bætt við bæði einingu **Birgðaleiðréttingar** og einingu **Birgðaflutnings**. Þessi reitur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Finance and Operations. Sjálfgildi fyrir þennan reit er Stofnað (1), en það er hins vegar ekki sent til Finance and Operations. Þegar gildið er uppfært í Bókað (2) er það sent yfir í Finance and Operations, en eftir það verður ekki lengur hægt að breyta leiðréttingunni eða flutningnum eða bæta nýjum línum við.

Reitnum **Númeraröð** hefur verið bætt við eininguna **Afurð birgðaleiðréttingar**. Þessi reitur tryggir að samþættingin hafi einkvæmt númer, þannig að samþættingin geti búið til og uppfært leiðréttingu. Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í **P2C AutoNumber** einingunni til að viðhalda númeraröðunum og forskeytinu sem er notað.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="finance-and-operations"></a>Finance and Operations
Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með því að nota runuvinnslu. Þetta er virkjað í: **Birgðastjórnun > Reglubundin verkefni > CDS samþætting > Bóka samþættingarbirgðabækur**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Leiðrétting á birgðaskrá (Field Service til Fin and Ops): Leiðrétting á birgðaskrá

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Birgðaflutningur (Field Service til Fin and Ops): Birgðaflutningur

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)
