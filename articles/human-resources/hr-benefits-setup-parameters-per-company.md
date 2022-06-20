---
title: Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki
description: Þessi grein lýsir því hvernig á að stilla færibreytur fyrir fríðindastjórnun fyrir hvert fyrirtæki í Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: e9516977002280e17ee82bf7581d8d7c5060de2a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904218"
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
