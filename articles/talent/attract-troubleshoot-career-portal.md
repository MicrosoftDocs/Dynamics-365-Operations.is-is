---
title: Attract-notendur geta ekki sótt um störf á starfagátt
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem Attract notendur geta ekki sótt um störf á starfagáttinni.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461485"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-notendur geta ekki sótt um störf á starfagátt

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Úthreyfing

Attract-notendur geta ekki sótt um störf á starfagátt. Þegar þeir reyna að sækja um starf sem var stofnað á Dynamics 365 Talent: Attract hleður vafrinn síðuna stöðugt og klárar ekki aðgerðina.

## <a name="cause"></a>Orsök

Þetta vandamál kemur upp þegar Talent Relationship Team er ekki með Talent notandahlutverkið.

## <a name="resolution"></a>Upplausn

Úthlutið Talent notandahlutverkinu í Talent Relationship Team.

1. Skráðu þig inn á [Power Platform stjórnendamiðstöðina](https://admin.powerplatform.microsoft.com) með einhverjum eftirtalinna skilríkja stjórnanda:

   - Dynamics 365 stjórnandi
   - Altækur stjórnandi
   - Power Platform stjórnandi

2. Í yfirlitssvæðinu skal velja **Umhverfi**, og síðan umhverfið þar sem á að úthluta Talent notandahlutverkinu á Talent Relationship Team.

   ![Velja umhverfi](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Í svæðinu **Umhverfi** skal velja **Umhverfisveffang** og skrá inn í stjórnendagátt umhverfis (til dæmis, https:<orgname>.crm.dynamics.com).

4. Veljið **Stillingar**, veljið **Kerfi** og svo **Öryggi**.

   ![Skoða öryggi](./media/attract-troubleshoot-career-portal-security.png)

5. Velja **teymi**.

   ![Velja teymi](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Leitið að **Talent Relationship Team** í leitarglugganum og veljið svo teymið úr leitarniðurstöðunum.

7. Veljið **STJÓRNA HLUTVERKUM** á borðanum.

8. Í svarglugganum **Stjórna teymishlutverkum** skal velja **Talent notandi** af listanum yfir tiltæk hlutverk og síðan velja **Í lagi** til að nota hlutverkið.

   ![Nota hlutverk](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Prófaðu breytingarnar:

   1. Skráðu þig inn í starfagátt úr nýjum vafraglugga.
   2. Sækja um starfið í starfagátt. 