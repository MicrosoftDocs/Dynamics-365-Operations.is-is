---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679321"
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

