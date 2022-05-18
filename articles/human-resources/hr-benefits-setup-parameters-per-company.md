---
title: Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki
description: Þetta efnisatriði lýsir hvernig á að skilgreina færibreytur fyrir fríðindastjórnun á fyrirtæki í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c5e53d3dec4c6fc8be573b8a1ad3ba8fb01b490
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689945"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fyrir hvert fyrirtæki sem býður upp á fríðindi verður að skilgreina stillingar fyrir staðfestingartölvupóst fyrir fríðindi.

## <a name="configure-confirmation-email-settings"></a>Skilgreina stillingar staðfestingartölvupósts

1. Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.

2. Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti: 

   | Svæði | lýsing |
   | --- | --- |
   | **Senda staðfestingarpóst** | Þegar kveikt er á þessum eiginleika er staðfestingartölvupóstur sendur á starfsmenn þegar þeir skrá sig út úr fríðindaskráningu í **sjálfsafgreiðslu starfsmanna**. |
   | **Sniðmát fyrir staðfestingartölvupóst** | Veljið tölvupóstssniðmát fyrirtækis sem á að nota þegar staðfesting skráningar er send. Ef þú velur ekki sniðmát er eftirfarandi almennur tölvupóstur sendur:<br><br>%EmployeeFirstName%,<br><br>Til hamingju! Fríðindaskráningu hefur verið lokið.<br><br>Takk fyrir,<br><Company/Org name> Fríðindi. |
   | **Sjálfgefið netfang sendanda** | Netfangið sem á að nota þegar staðfestingarpóstur er sendur. |

3. Veljið **Vista**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
