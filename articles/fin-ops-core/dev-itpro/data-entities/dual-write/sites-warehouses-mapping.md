---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Dataverse.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560362"
---
# <a name="integrated-sites-and-warehouses"></a>Samþætt svæði og vöruhús

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Dataverse. Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management. Þau eru notuð til að móta aðfangakeðju fyrirtækisins.

## <a name="templates"></a>Sniðmát

Með samþættingu við Dataverse eru þessi hugtök og allar tengdar upplýsingar þeirra aðgengilegar í Dataverse með því að nota gagnatöflur fyrir svæði og vöruhús í eftirfarandi töflu.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | lýsing
--------------------------|---------------------------|---
Svæði | msdyn_operationalsites | 
Vöruhús | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]