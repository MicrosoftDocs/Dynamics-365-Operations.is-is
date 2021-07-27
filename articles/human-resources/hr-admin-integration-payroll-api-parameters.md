---
title: Samþættingarfæribreytur launaskrár
description: Þetta efnisatriði lýsir samþættingarfæribreytum Dynamics 365 Human Resources launaskrár.
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
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314415"
---
# <a name="payroll-integration-parameters"></a>Samþættingarfæribreytur launaskrár

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Áður en samþætting Dynamics 365 Human Resources launaskrár er notuð þarf að setja upp færibreyturnar sem lýst er í þessu efnisatriði.

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
