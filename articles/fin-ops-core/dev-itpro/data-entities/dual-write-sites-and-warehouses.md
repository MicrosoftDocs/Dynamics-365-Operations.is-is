---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770990"
---
# <a name="integrated-sites-and-warehouses"></a>Innbyggð svæði og vöruhús

[!include [banner](../includes/banner.md)]

Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service. Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management. Þau eru notuð til að móta aðfangakeðju fyrirtækisins.

## <a name="templates"></a>Sniðmát

Með samþættingunni við Common Data Service eru þessi hugtök og allar tengdar upplýsingar fáanleg í Common Data Service með því að nota gagnaeiningar svæðanna og vöruhúsanna í eftirfarandi töflu.

Forrit Finance and Operations | Önnur Dynamics 365 forrit | Lýsing
--------------------------|---------------------------|---
Svæði | msdyn_operationalsites | 
Vöruhús | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

