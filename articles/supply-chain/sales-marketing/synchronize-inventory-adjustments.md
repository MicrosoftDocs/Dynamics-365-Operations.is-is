---
title: "Samstilla birgðaflutninga og leiðréttingar úr Field Service við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla birgðaleiðréttingar og færslur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla birgðaleiðréttingar og færslur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni
Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu birgðaleiðréttinga og færslna úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.

**Heiti sniðmátanna í gagnasamþættingu:**
- Birgðaleiðrétting (Field Service til Finance and Operations)
- Birgðaflutningar (Field Service til Finance and Operations)

**Heiti verka í gagnasamþættingarverkum:**
- Birgðaleiðréttingar
- Birgðaflutningar

## <a name="entity-set"></a>Einingastamstæða
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-færslubókarhausar og línur leiðréttingar á birgðaskrá |
| msdyn_inventoryadjustmentproducts | CDS-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá   |

## <a name="entity-flow"></a>Einingaflæði
Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Finance and Operations um leið og **Staða bókunar** breytist frá stofnað til bókað. Þegar þetta gerist læsist leiðréttingin eða flutningspöntunin og verður skrifvarin því að leiðréttingar og flutningar kunna að vera bókaðar í Finance and Operations og er þar af leiðandi ekki hægt að breyta.
Í Finance and Operations er hægt að setja upp runuvinnslu til að bóka breytingarnar sjálfvirkt og flytja birgðabækur sem myndast við samþættinguna. Sjá forsendur hér að neðan til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service 
Reitnum Birgðaeining hefur verið bætt við Afurðareiningu. Þessi reitur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Operations, og við þurfum birgðaeininguna fyrir Birgðir í vöruhúsi í Operations.
Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildinu fyrir afurð birgðaafurðar. Ef gildi finnst verður reitnum Eining læst á Afurð birgðaleiðréttingar

Reitnum Staða bókunar hefur verið bætt við bæði einingu Birgðaleiðréttingar og einingu Birgðaflutnings. Þessi reitur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Operations. Reiturinn er sjálfgefinn á Stofnað (1) og er þá ekki sendur yfir í Operations. Þegar honum er breytt í Bókað (2) er hann sendur yfir í Operations, en þá verður ekki lengur hægt að breyta neinu í Leiðréttingum eða Flutningi eða bæta nýjum línum við hann.
Reitnum Númeraröð hefur verið bætt við afurðareiningu birgðaleiðréttingar. Þessi reitur hjálpar samþættingunni að hafa einkvæmt númer svo samþættingin viti hvenær verið er að stofna og hvenær uppfæra. Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í P2C AutoNumber einingunni til að viðhalda númeraröðunum og forskeytinu sem er notað.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="in-finance-and-operations"></a>Í Finance and Operations
Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með runuvinnslu. Þetta er virkjað í: Birgðastjórnun > Reglubundin verkefni > CDS samþætting > Bóka samþættingarbirgðabækur

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Birgðaleiðrétting (Field Service til Finance and Operations): Birgðaleiðrétting

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Birgðaflutningar (Field Service til Finance and Operations): Birgðaflutningur

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)

