---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þetta efnisatriði útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7a66b7624655aaf976aaa63b2626f65c54d0ea38
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898816"
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
2. Stofnið umhverfið með því að fylgja leiðbeiningunum í [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
