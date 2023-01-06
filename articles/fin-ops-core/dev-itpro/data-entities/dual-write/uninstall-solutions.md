---
title: Fjarlægja skipulagslausnir fyrir tvöfalda skráningu forrita
description: Þessi grein útskýrir hvernig á að fjarlægja skipulagslausnir fyrir tvöfalda skráningu forrita.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: fd9dc98ec1323a2ef262a330a400a6bd3833e554
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288731"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Fjarlægja skipulagslausnir fyrir tvöfalda skráningu forrita

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að fjarlægja skipulagslausnir fyrir tvöfalda skráningu forrita.

Sumir viðskiptavinir setja óvart upp pakka fyrir tvöfalda skráningu forrita sem setur upp margar lausnir í Microsoft Dataverse umhverfinu þeirra. Uppsetning utanaðkomandi lausna í pakkanum getur leitt til óvæntra og óæskilegra vandamála.

Til að laga vandamál sem tengjast uppsetningu á pakka fyrir tvöfalda skráningu forrita skal fjarlægja óæskilegar lausnir tvöfaldrar skráningar í eftirfarandi röð:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (ef til staðar)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Til að fjarlægja þessa lausn þarf að opna þjónustubeiðni hjá Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Ef lausnir aðila og altækrar aðsetursbókar voru uppsettar skal fjarlægja lausnirnar í eftirfarandi röð:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Aðili
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
