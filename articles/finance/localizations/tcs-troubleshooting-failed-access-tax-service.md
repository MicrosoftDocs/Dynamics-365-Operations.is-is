---
title: Ekki tókst að fá aðgang að skattþjónustu
description: Í þessari grein er útskýrt hvernig hægt er að leysa úr mistökum við að fá aðgang að skattaútreikningsþjónustu.
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
ms.openlocfilehash: 65d819b97be3d1238bc0ecfc201b4e24edac8616
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861223"
---
# <a name="failed-to-access-tax-service"></a>Ekki tókst að fá aðgang að skattþjónustu

[!include [banner](../includes/banner.md)]


Í þessari grein er útskýrt hvernig á að laga villuna „Ekki tókst að fá aðgang að skattþjónustu“ í Skattaútreikningsþjónustunni.

## <a name="symptoms"></a>Einkenni

Í Microsoft Dynamics 365 Finance ferðu í **Uppsetning** \> **skatts** \> **Skattaskilgreining** \> **Færibreytur skattþjónustu**. Á flipanum **Almennt** er valkosturinn **Virkja skattaútreikning** virkjaður. Ef síðan er reynt að velja gildi í **Uppsetningarheiti eiginleika** reitnum kemur upp villa. Villuskilaboðin sýna „Ekki tókst að fá aðgang að skattþjónustu.“

## <a name="cause"></a>Orsök

Þessi villa kemur upp vegna þess að Finance hefur ekki aðgang að þjónustu fyrir skattútreikning.

## <a name="resolution"></a>Upplausn 

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Á síðunni **Umhverfi** á **Innbætur umhverfis** flipanum skal finna **Skattaútreikningur** og fara yfir stöðu þess. Staða ætti að vera **Setur upp** eða **Uppsett**. Ef innbót skattaútreikningsþjónustan er ekki uppsett færðu villu.

## <a name="mitigation"></a>Mildun

1. Í LCS, á síðunni **Finance**, í hlutanum **Samþætting Power platform**, velurðu **Setja upp nýja innbótin**.
2. Flettu neðst á síðuna og veldu innbótina **Skattaútreikningur** til að setja hana upp.
3. Farðu aftur í Finance umhverfið þitt og reyndu að fá aðgang að skattaútreikningsþjónustu.

> [!NOTE]
> Áður en Skattaútreikningsþjónustan er sett upp skaltu skoða [ Forsendur Skattaútreikningsþjónustunnar](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Ef þú getur ekki sett upp innbótina vegna þess að **Samþætting Power Platform** er ekki tiltækur skaltu skoða [Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Ef þú lendir enn í villunni eftir að þú hefur sett upp innbótina skaltu hafa samband við kerfisstjórann.
