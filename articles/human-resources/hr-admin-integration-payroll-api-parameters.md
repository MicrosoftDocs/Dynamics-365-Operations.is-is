---
title: Samþættingarfæribreytur launaskrár
description: Þessi grein lýsir Dynamics 365 Human Resources Samþættingarbreytur launaskrár.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896098"
---
# <a name="payroll-integration-parameters"></a>Samþættingarfæribreytur launaskrár


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Áður en þú notar Dynamics 365 Human Resources Samþætting launaskrár, þú verður að setja upp breytur sem lýst er í þessari grein.

## <a name="enable-payroll-address"></a>Virkja aðsetur launaskrár

Til að geta notað aðsetur launaskrár þarf að virkja það úr [skjámynd yfir samnýttar færibreytur](hr-setup-shared-parameters.md) í samþættingarflipa launaskrár.

## <a name="define-the-identification-type"></a>Skilgreina gerð auðkennis

Til að sýna kenni auðkennisgerðar í [starfsmannaeiningu launaskrár](hr-admin-integration-payroll-api-payroll-employee.md) þarf að [skilgreina færibreytur mannauðs](hr-setup-shared-parameters.md) fyrir hvert fyrirtæki.

1. Í **Launastjórnun** vinnusvæðinu, undir tenglar, skal velja **Færibreytur mannauðs**. 
2. Í flipanum **Samþætting launaskrár** skal tilgreina gildi eftirfarandi reita.

| Svæði | lýsing |
| --- | --- |
| Nota auðkennisgerðir í launavinnslu | Þegar þessi valkostur er valinn verður valið auðkenni gerðar sýnt í starfsmannaeiningu launaskrár. |
| Gerð auðkennis | Gerð auðkennis sem á að sýna í reitnum **mshr_payrollemployeeentityid** í [starfsmannaeiningu launaskrár](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
