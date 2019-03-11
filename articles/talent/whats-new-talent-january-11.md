---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (11. janúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304867"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (11. janúar 2019)

[!include [banner](includes/banner.md)]

**Smíði 8.1.2100**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="changes"></a>Breytingar

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Sannprófa leyfisbeiðnir með því að spá fyrir um tiltæka stöðu
Breytingar sem gerðar eru í þessari útgáfu leyfa starfsmönnum að biðja um leyfi fram í tímann án þess að draga frá núverandi stöðu. Stöðluð verkflæði verða notuð fyrir allar beiðnir fram í tímann. Nánari upplýsingar er að finna í [Uppsöfnun frís sem byggist á vinnustundum](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Skoðaðu áætlaða stöðu leyfis í ESS og Fólk
Þessi eiginleiki gerir mannauðsstjóra, stjórnendum og starfsmönnum kleift að skoða stöður fyrir leyfistímabil fram í tímann. Starfsmenn geta skoðað framtíðarstöður á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna** og mannauðsstjóri hefur aðgang að sömu upplýsingum með vinnusvæðinu **Fólk**.

### <a name="notifications-for-changing-leave-balances"></a>Tilkynningar um breytingar á stöðum leyfa
Leyfisstöður munu sýna núverandi stöðu starfsmanna. Framtíðarstöður er að finna á vinnusvæðunum **Sjálfsafgreiðsla starfsmanna** og **Fólk** með því að slá inn „frá og með dagsetningu“ til að reikna út áætlaða stöðu.

Leiðsögn hefur verið bætt við til að skoða áætlaðar stöður á eftirfarandi svæðum:
  - Spjaldið **Frítími** á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna**.
  - Spjaldið **Leyfi og fjarvistir** á vinnusvæðinu **Sjálfsafgreiðsla stjórnanda**.
  - Síðan **Leyfi og fjarvistir** á vinnusvæðinu **Fólk**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Leyfa aukastafi fyrir breytilegt launafyrirkomulag (reiðufjáráætlanir)
Breytileg umbun og áætlanir reiðufjár er nú með aukalegan sveigjanleika fyrir upphæðir og hnekkingar fyrir gildi þar sem upphæðir eru með aukastöfum.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Ekki er hægt að breyta dagsetningum fyrir skráningar á breytilegum launum eftir að áætlunin er vistuð
Þessi breyting gerir kleift að uppfæra lokadag áætlunar (lengd eða útrunnin) eftir að áætlunin hefur verið vistuð. Enn er hægt að kveikja og slökkva á áætlunum óháð upphafs- og lokadögum.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Launaupplýsingar eru tiltækar þegar öryggishlutverki launastjóra hefur verið úthlutað
Hlutverk launastjóra hefur verið uppfært til að hafa aðgang að launaupplýsingum á meðan beiðnin er í ferli.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Sjálfsafgreiðsla starfsmanns | Köfun niður í stöðustigveldi úr reit mistekst að sækja yfirhnút
Breytingar hafa verið gerðar til að koma í veg fyrir villu sem átti sér stað þegar stöðustigveldinu var bætt við ný vinnusvæði og við flettingu í skipulagseiningum fyrirtækis.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Ný villuleitarboð þegar númer starfsmanns er notað
Breyting hefur verið gerð til að skýra hvað vandamálið er þegar starfsmaður er ráðinn og næsta starfsmannanúmer er í notkun.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Vinnusvæði fyrir sjálfsafgreiðslu starfsmanns valið sem upphafssíða
Þegar vinnusvæðið **Sjálfsafgreiðsla starfsmanna** er valið sem upphafssíða fyrir notanda og þessum notanda er ekki úthlutað hlutverki starfsmanns mun kerfið beina honum að sjálfgefna yfirlitinu.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Ástæðukóði uppsagnar uppfærir skrá stöðuverkefnis
Ástæðukóði uppsagnar uppfærir nú stöðuverkefnið þegar starfsmanni er sagt upp störfum og stöðunni er lokað. 
