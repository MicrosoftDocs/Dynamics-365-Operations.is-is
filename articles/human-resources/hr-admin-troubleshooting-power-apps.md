---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þessi grein útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053348"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps

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