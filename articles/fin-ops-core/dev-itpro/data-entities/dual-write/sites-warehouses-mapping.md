---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173063"
---
# <a name="integrated-sites-and-warehouses"></a>Samþætt svæði og vöruhús

[!include [banner](../../includes/banner.md)]



Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Common Data Service. Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management. Þau eru notuð til að móta aðfangakeðju fyrirtækisins.

## <a name="templates"></a>Sniðmát

Með samþættingunni við Common Data Service eru þessi hugtök og allar tengdar upplýsingar fáanleg í Common Data Service með því að nota gagnaeiningar svæðanna og vöruhúsanna í eftirfarandi töflu.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | Lýsing
--------------------------|---------------------------|---
Svæði | msdyn_operationalsites | 
Vöruhús | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

