---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þessi grein útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419001"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps

**Úthreyfing**

- Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
- Leyfi sem gefur notendum réttindi til að framkvæma skrefið fyrir stofnun umhverfis, sem hefur ekki verið úthlutað beint á notandann sem framkvæmir skrefið.

**Lausn**

Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi beint á notandann sem kemur til með að framkvæma skref stofnunar. Hér eru þjónustuáætlanir Microsoft Dynamics sem veita þessi réttindi.

| Heildarbirgðahaldseining afurðar (SKU)       | Power Apps P2 þjónustuáætlun  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps fyrir Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps fyrir Dynamics 365 |

Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2. Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.

1. Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Stofnið umhverfið með því að fylgja leiðbeiningunum í [Ráðstafa Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
