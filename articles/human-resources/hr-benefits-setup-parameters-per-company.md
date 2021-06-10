---
title: Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki
description: Skilgreina færibreytur fyrir fríðindastjórnun á fyrirtæki í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057623"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fyrir hvert fyrirtæki sem býður upp á fríðindi verður að skilgreina stillingar fyrir staðfestingartölvupóst fyrir fríðindi.

## <a name="configure-confirmation-email-settings"></a>Skilgreina stillingar staðfestingartölvupósts

1. Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.

2. Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti: 

   | Svæði | lýsing |
   | --- | --- |
   | **Senda staðfestingarpóst** | Þegar kveikt er á þessum eiginleika er staðfestingartölvupóstur sendur á starfsmenn þegar þeir skrá sig út úr fríðindaskráningu í sjálfsafgreiðslu starfsmanna. |
   | **Sniðmát fyrir staðfestingartölvupóst** | Veljið tölvupóstssniðmát fyrirtækis sem á að nota þegar staðfesting skráningar er send. Ef þú velur ekki sniðmát er eftirfarandi almennur tölvupóstur sendur:<br><br>%EmployeeFirstName%,<br><br>Til hamingju! Fríðindaskráningu hefur verið lokið.<br><br>Takk fyrir,<br><Company/Org name> Fríðindi. |
   | **Sjálfgefið netfang sendanda** | Netfangið sem á að nota þegar staðfestingarpóstur er sendur. |

3. Veljið **Vista**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]