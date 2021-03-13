---
title: Samstilla birgðaflutninga og leiðréttingar úr Field Service við Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: a598f0356034a22ee7fc0902360b8862a1944558
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010973"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Samstilla birgðaflutninga og leiðréttingar úr Field Service við Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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

## <a name="table-set"></a>Töflusett
| Field Service                     | Birgðakeðjustjórnun                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataverse Færslubókarhausar og færslubókarlínur leiðréttingar á birgðaskrá |
| msdyn_inventoryadjustmentproducts | Dataverse-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá   |

## <a name="table-flow"></a>Töfluflæði
Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Supply Chain Management eftir að **Staða bókunar** breytist úr **Stofnað** í **Bókað**. Þegar þetta gerist verður leiðréttingin eða flutningspöntunin læst og verða aðeins skrifvarið. Þetta þýðir að bóka megi leiðréttingar og flutninga í Supply Chain Management, en ekki er hægt að breyta þeim. Í Supply Chain Management er hægt að setja upp runuvinnslu til að bóka færslubækur leiðréttinga og birgðaflutninga sjálfvirkt sem myndast við samþættinguna. Sjá eftirfarandi skilyrði til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service 
Dálknum **Birgðaeining** hefur verið bætt við töfluna **Afurðareining**. Þessi dálkur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Supply Chain Management, og þörf er á birgðaeiningunni fyrir birgðir í vöruhúsi í Supply Chain Management.
Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildi afurðar í birgðum. Ef gildi finnst verður dálknum **Eining** læst á Afurð birgðaleiðréttingar.

Dálkinum **Staða bókunar** hefur verið bætt við bæði töfluna **Birgðaleiðréttingar** og töflu **Birgðaflutnings**. Þessi dálkur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Supply Chain Management. Sjálfgildi fyrir þennan dálk er Stofnað (1), en það er hins vegar ekki sent til Supply Chain Management. Þegar gildið er uppfært í Bókað (2) er það sent yfir í Supply Chain Management, en eftir það verður ekki lengur hægt að breyta leiðréttingunni eða flutningnum eða bæta nýjum línum við.

Dálkinum **Númeraröð** hefur verið bætt við töfluna **Afurð birgðaleiðréttingar**. Þessi dálkur tryggir að samþættingin hafi einkvæmt númer, þannig að samþættingin geti búið til og uppfært leiðréttingu. Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í **P2C AutoNumber** töflunni til að viðhalda númeraröðunum og forskeytinu sem er notað.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="supply-chain-management"></a>Birgðakeðjustjórnun
Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með því að nota runuvinnslu. Þetta er virkjað í: **Birgðastjórnun > Reglubundin verkefni > Dataverse samþætting > Bóka samþættingarbirgðabækur**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Birgðaleiðrétting (Field Service við Supply Chain Management): Inventory adjustment

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Birgðaflutningur (Field Service við Supply Chain Management): Inventory transfer

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)
