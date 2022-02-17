---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þetta efnisatriði útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 937b372fa95c8076666aed14c2b34b12e8029c4d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067705"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

- Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
- Notandinn er ekki með leyfi sem veitir rétt til að stofna umhverfi.

**Lausn**

Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi til notanda sem stofnar umhverfið. Eftirfarandi Microsoft Dynamics þjónustuáætlanir veita heimildir til að stofna umhverfi:

| Heildarbirgðahaldseining       | Power Apps P2 þjónustuáætlun  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps fyrir Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps fyrir Dynamics 365 |

Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2. Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.

1. Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Stofnið umhverfið með því að fylgja leiðbeiningunum í [Ráðstafa Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
