---
title: Fjarlægðu skipulagslausnir fyrir tvískrifa forrit
description: Þetta efnisatriði lýsir því hvernig á að fjarlægja tvískrifa forritaskipunarlausnir.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 781b2cb19a563d5712fa65718c93bfdc242f0c4a
ms.sourcegitcommit: abfaef124c8747827d6f297821f01f1f6fbca6b7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455309"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Fjarlægðu skipulagslausnir fyrir tvískrifa forrit

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að fjarlægja tvískrifa forritaskipunarlausnir.

Sumir viðskiptavinir setja óviljandi upp tvískrifaða forritaskipunarpakkann sem setur upp margar lausnir í Microsoft Dataverse umhverfi. Uppsetning á óviðkomandi lausnum í pakkanum getur valdið óvæntum og óæskilegum vandamálum.

Til að laga vandamál sem tengjast uppsetningu á tvískrifa forritaskipunarpakkanum skaltu fjarlægja óæskilegar tvískriftarlausnir í eftirfarandi röð:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (ef til staðar)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Til að fjarlægja þessa lausn verður þú að opna stuðningsmiða hjá Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAnd OperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Ef lausnir aðila og alþjóðlegra heimilisfangabóka voru settar upp skaltu fjarlægja lausnirnar í eftirfarandi röð:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAnd OperationsDualWriteEntity Maps
1. msdyn_DualWriteCore
1. Dynamics365 AssetManagementApp
1. Dynamics365 AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCM Common
1. Dynamics365FinanceAndOperationsCommon
1. Aðili
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. Field Service Common
