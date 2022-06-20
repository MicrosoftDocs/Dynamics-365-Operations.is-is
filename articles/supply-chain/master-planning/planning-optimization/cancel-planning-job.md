---
title: Hætta við áætlunarverk
description: Þessi grein útskýrir hvernig á að hætta við virka áætlunarvinnu sem notar hagræðingaraðgerðina áætlanagerð.
author: t-benebo
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0474c50157295d9ecd2341b700c07f4fbf1ed51f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900942"
---
# <a name="cancel-a-planning-job"></a>Hætta við áætlunarverk

[!include [banner](../../includes/banner.md)]

Í Microsoft Dynamics 365 Supply Chain Management er hægt að hætta við virka áætlunarvinnslu sem notar virknina fínstillingu skipulagningar. Þegar þú velur **Hætta við** í glugganum þegar fínstillingarvinnsla áætlunar virkjast beint úr notendaviðmótinu (ekki í bakgrunni) mun þetta ekki afturkalla fínstillingarvinnsluna. Jafnvel þó þú fáir viðvörun eins og „Aðgerð afturkölluð“, verður þú samt að nota eftirfarandi skref til að hætta við áætlunarvinnslu með fínstillingu áætlanagerðar.


Fylgdu þessum skrefum til að hætta við virka áætlunarvinnslu. 

> [!NOTE]
> Aðeins er hægt að hætta við virkar vinnslur.

1. Farðu í **Aðaláætlanagerð \> Uppsetning \> Áætlanir**.
2. Veldu viðeigandi áætlun fyrir keyrslu áætlanagerðar.
3. Veldu **Saga**.
4. Veldu áætlunarvinnslu sem á að hætta við.
5. Veldu **Hætta við**.

Vinnslustaðan verður **Hættir við** þar til fínstillingarþjónusta áætlunargerðar staðfestir að vinnslunni hafi verið aflýst. Stöðunni verður síðan breytt í **Hætt við**.

> [!NOTE]
> Til að sjá stöðubreytingar verður þú að endurnýja síðuna með því að velja hnappinn **Endurhlaða**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]