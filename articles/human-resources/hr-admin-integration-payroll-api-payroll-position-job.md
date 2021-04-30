---
title: Launastöðuvinnsla
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir starfseiningu launastöðu í Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72f3109f5bea36a390b04b7165fc3831d777b640
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882008"
---
# <a name="payroll-position-job"></a>Launastöðuvinnsla

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir starftengilsseiningu launastöðu í Dynamics 365 Human Resources.

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Starfsauðkenni**<br>mshr_jobid<br>*Strengur* | Readp-only<br>Krafa |Kenni starfs. |
| **Gildir frá**<br>mshr_validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Dagsetning stöðunnar og starfssambandið gildir frá. |
| **Gildir til**<br>mshr_validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Dagsetningin sem staðan og starfssambandið gildir til.  |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>*Strengur* | Lesa eingöngu<br>Krafa | Auðkenni stöðunnar. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Krafa<br>Búið til af kerfi |  |
| **Gildi fyrir kenni vinnustöðu**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Kenni starfsins sem tengist stöðunni.|
| **Gildi fyrir kenni launafyrirkomulags fastra launa**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Kenni launafyrirkomulags fastra launa sem tengist stöðunni. |
| **Einingarkenni fyrir kenni launaeiningar**<br>mshr_payrollpositionjobentityid<br>*Guid* | Krafa<br>Búið til af kerfi. | GUID-gildi myndað af kerfinu til að auðkenna verk á einkvæman hátt.  |

