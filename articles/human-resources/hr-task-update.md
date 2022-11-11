---
title: Settu upp verkefni í Verkefnastjórnun
description: Þessi grein útskýrir hvernig á að setja upp verkefni í Verkefnastjórnun í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745421"
---
# <a name="set-up-tasks-in-task-management"></a>Settu upp verkefni í Verkefnastjórnun

[!INCLUDE [PEAP](../includes/peap-1.md)]

Í útgáfum af Microsoft Dynamics 365 Human Resources fyrir útgáfu 10.0.30 þurftu notendur sem vildu breyta verki að breyta því verkefni fyrir sig á hverjum gátlista sem innihélt það. Hins vegar, frá og með mannauðsútgáfu 10.0.30, geta notendur valið hvernig breytt verkefni eru meðhöndluð. Ef verkefni sem verið er að breyta er á gátlista, skal **Virkja uppfærslu verkefnastjórnunar** valkostur verður að vera valinn á **Verkefnastjórnun** flipi á **Mannauður sameiginlegar breytur** síðu til að gera gátlistann kleift að nota breytta verkefnið.

[![Virkja uppfærsluvalkost verkstjórnunar á síðunni Samnýtt færibreytur mannauðs.](./media/task-update.png)](./media/task-update.png)

Ef beita ætti breytingum á verkum á öll tengd gátlistaverk, verður tengsl þegar að vera á milli verksins í verkasafninu og verkefnisins á gátlistanum. Möguleiki var bætt við til að skapa tengsl á milli bókasafnsverkefnisins og gátlistaverkefnisins.

Þú getur búið til verkefni fyrir sig og síðan endurnýtt þau í mörgum gátlistum. Til að búa til verkefni, á **Uppsetning um borð** síðu, á **Verkefni** flipa, veldu **Nýtt**.

## <a name="set-up-tasks"></a>Settu upp verkefni

Til að úthluta búið verki á marga gátlista velurðu verkefnið og velur svo **Sækja um gátlista** á matseðlinum.

Að öðrum kosti geturðu bætt verkefnum beint við gátlista. Til að bæta verkefni við gátlista, á **Uppsetning um borð** síðu, á **Tékklisti** flipa, annað hvort búa til nýjan gátlista til að bæta verkefninu við eða bæta verkefninu við núverandi gátlista.

Til að breyta bókasafnsverkefni velurðu **Breyta** á valmynd verkasafnsins. Ef verkefnið er tengt einhverjum gátlistum munu þeir gátlistar birtast á **Breyta verkefni** síðu. Ef þú vilt að verkefnin á einhverjum af gátlistunum séu uppfærð með breytingunum skaltu velja þá gátlista í **Sækja um gátlista** kafla.

Til að eyða verkefnum úr verkefnasafninu skaltu velja **Eyða**. Ef verkefnið er tengt gátlista mun þessi aðgerð ekki eyða verkinu af gátlistanum. Sérstök aðgerð er nauðsynleg til að fjarlægja verkefni af gátlista.

### <a name="set-up-checklists"></a>Settu upp gátlista

Gátlisti er hópur verkefna. Þú getur búið til eins marga gátlista og þú þarft og þú getur úthlutað sömu verkefnum á marga gátlista. Þegar þú býrð til gátlista tilgreinir þú eiganda og dagatal.

Til að búa til nýtt verkefni á gátlista skaltu velja **Nýtt** á verkefnavalmyndarstikunni. Þegar þú býrð til nýtt verkefni geturðu valfrjálst bætt verkefninu við verkefnasafnið, svo hægt sé að deila því á marga gátlista. Til að bæta verkefninu við verkefnasafnið verður þú að stilla **Sækja verkefni á bókasafn** valmöguleika til **Já**. Ef þú velur að bæta verkefninu við verkefnasafnið geturðu líka bætt verkefninu við aðra gátlista á sama tíma með því að velja þá gátlista í **Sækja um gátlista** kafla. Ef þú velur að bæta verkefninu ekki við verkefnasafnið verður verkefnið aðeins til á gátlistanum þar sem þú býrð það til.

Til að breyta verki á gátlista velurðu **Breyta** á verkefnavalmyndinni. Ef verkefnið er tengt einhverjum gátlistum munu þeir gátlistar birtast á **Breyta verkefni** síðu. Ef þú vilt að verkefnin á einhverjum af hinum gátlistunum séu uppfærð með breytingunum skaltu velja þá gátlista í **Sækja um gátlista** kafla.

Til að fjarlægja verkefni af gátlista skaltu velja **Fjarlægja**. Þessi aðgerð mun fjarlægja verkefnin af gátlistanum. Hins vegar mun það ekki eyða verkefnum úr verkefnasafninu. Til að eyða verkefnum úr verkefnasafninu skaltu opna **Verkefnasafn** síðu og veldu **Eyða**.
