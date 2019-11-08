---
title: Samstilla birgðaflutninga og leiðréttingar úr Field Service við Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552234"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Samstilla birgðaflutninga og leiðréttingar úr Field Service við Supply Chain Management

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla birgpaleiðréttingar og -flutning úr Field Service í Supply Chain Management.

**Sniðmát í gagnasamþættingu**
- Birgðaleiðréttingar (Field Service við Supply Chain Management)
- Birgðaflutningur (Field Service við Supply Chain Management)

**Verkefni í gagnasamþættingarverkum**
- Birgðaleiðréttingar
- Birgðaflutningar

## <a name="entity-set"></a>Einingastamstæða
| Field Service                     | Birgðakeðjustjórnun                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-færslubókarhausar og línur leiðréttingar á birgðaskrá |
| msdyn_inventoryadjustmentproducts | CDS-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá   |

## <a name="entity-flow"></a>Einingaflæði
Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Supply Chain Management eftir að **Staða bókunar** breytist úr **Stofnað** í **Bókað**. Þegar þetta gerist verður leiðréttingin eða flutningspöntunin læst og verða aðeins skrifvarið. Þetta þýðir að bóka megi leiðréttingar og flutninga í Supply Chain Management, en ekki er hægt að breyta þeim. Í Supply Chain Management er hægt að setja upp runuvinnslu til að bóka færslubækur leiðréttinga og birgðaflutninga sjálfvirkt sem myndast við samþættinguna. Sjá eftirfarandi skilyrði til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service 
Reitnum **Birgðaeining** hefur verið bætt við **Afurðareiningu**. Þessi reitur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Supply Chain Management, og þörf er á birgðaeiningunni fyrir birgðir í vöruhúsi í Supply Chain Management.
Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildi afurðar í birgðum. Ef gildi finnst verður reitnum **Eining** læst á Afurð birgðaleiðréttingar.

Reitnum **Staða bókunar** hefur verið bætt við bæði einingu **Birgðaleiðréttingar** og einingu **Birgðaflutnings**. Þessi reitur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Supply Chain Management. Sjálfgildi fyrir þennan reit er Stofnað (1), en það er hins vegar ekki sent til Supply Chain Management. Þegar gildið er uppfært í Bókað (2) er það sent yfir í Supply Chain Management, en eftir það verður ekki lengur hægt að breyta leiðréttingunni eða flutningnum eða bæta nýjum línum við.

Reitnum **Númeraröð** hefur verið bætt við eininguna **Afurð birgðaleiðréttingar**. Þessi reitur tryggir að samþættingin hafi einkvæmt númer, þannig að samþættingin geti búið til og uppfært leiðréttingu. Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í **P2C AutoNumber** einingunni til að viðhalda númeraröðunum og forskeytinu sem er notað.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="supply-chain-management"></a>Birgðakeðjustjórnun
Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með því að nota runuvinnslu. Þetta er virkjað í: **Birgðastjórnun > Reglubundin verkefni > CDS samþætting > Bóka samþættingarbirgðabækur**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Birgðaleiðrétting (Field Service við Supply Chain Management): Inventory adjustment

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Birgðaflutningur (Field Service við Supply Chain Management): Inventory transfer

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)
