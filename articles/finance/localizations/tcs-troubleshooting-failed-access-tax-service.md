---
title: Ekki tókst að fá aðgang að skattþjónustu
description: Þetta efnisatriði útskýrir hvernig á að leysa bilun í aðgangi að skattreikningsþjónustunni.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612317"
---
# <a name="failed-to-access-tax-service"></a>Ekki tókst að fá aðgang að skattþjónustu

[!include [banner](../includes/banner.md)]


Þetta efnisatriði útskýrir hvernig á að laga villuna „Mistókst að fá aðgang að skattaþjónustu“ í skattaútreikningsþjónustunni.

## <a name="symptoms"></a>Einkenni

Í Microsoft Dynamics 365 Fjármál, þú ferð til **Skattur** \> **Uppsetning** \> **Skattstilling** \> **Færi skattaþjónustu**. Á **Almennt** flipann, virkjarðu á **Virkjaðu skattaútreikning** valmöguleika. Ef þú reynir síðan að velja gildi í **Heiti eiginleikauppsetningar** reit, kemur upp villa. Villuskilaboðin segja, "Mistókst að fá aðgang að skattaþjónustu."

## <a name="cause"></a>Orsök

Þessi villa kemur upp vegna þess að Finance hefur ekki aðgang að skattaútreikningsþjónustunni.

## <a name="resolution"></a>Upplausn 

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Á **Umhverfi** síðu, á **Umhverfisviðbætur** flipa, finndu **Skattútreikningur** atriði, og farið yfir stöðu hans. Staðan ætti að vera **Er að setja upp** eða **Uppsett**. Ef viðbótarskattsútreikningsþjónustan er ekki sett upp færðu villuna.

## <a name="mitigation"></a>Mildun

1. Í LCS, á **Fjármál** síðu, í **Power pallur samþætting** kafla, veldu **Settu upp nýja viðbót**.
2. Skrunaðu neðst á síðunni og veldu **Skattútreikningur** viðbót til að setja það upp.
3. Farðu aftur í fjármálaumhverfið þitt og reyndu að fá aðgang að skattreikningsþjónustunni.

> [!NOTE]
> Áður en þú setur upp skattaútreikningsþjónustuna skaltu skoða [Forsendur skattreikningsþjónustu](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Ef þú getur ekki sett upp viðbótina vegna þess að **Power pallur samþætting** kafla er ekki í boði, sjá [Yfirlit yfir viðbætur](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Ef þú lendir enn í villunni eftir að þú hefur sett upp viðbótina skaltu hafa samband við kerfisstjórann þinn.
