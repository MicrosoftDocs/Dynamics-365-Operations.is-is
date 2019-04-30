---
title: Algengar spurningar um aðgerðir starfsfólks
description: Þetta efnisatriði inniheldur svörum við spurningum sem gæti verið ef fyrirtækið notar aðgerðir starfsfólks. Aðgerðir starfsfólks eru viðbótarskref sem þarf að ljúka þegar þú framkvæmt ákveðnum verkefni tengdar starfsfólks.
author: andreabichsel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 91b154a2379d6f0bdf8bea322c99be9e1c1925c9
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859852"
---
# <a name="personnel-actions-faq"></a>Algengar spurningar um aðgerðir starfsfólks

[!include [banner](includes/banner.md)]

Þetta efnisatriði inniheldur svörum við spurningum sem gæti verið ef fyrirtækið notar aðgerðir starfsfólks. Aðgerðir starfsfólks eru viðbótarskref sem þarf að ljúka þegar þú framkvæmt ákveðnum verkefni tengdar starfsfólks. Dæmi um verk sem gætu krafist aðgerða starfsfólks eru þegar að stofna nýjar stöður, breyta fyrirliggjandi gildi stöðu, ráða nýja starfsmenn, flytja starfsmenn, breyta launum starfsmanns, breyta stöðuverkefni eða segja upp starfsmönnum.

**Ath:** Aðgerðir starfskrafts eru aðeins í boði ef reitirnir **Kveikja á aðgerðum starfskrafts** og **Kveikja á stöðuaðgerðum** eru stilltir á **Já**, í fliplanum **Aðgerðir starfskrafts** á síðunni **Samnýttar færibreytur fyrir mannauð**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hvernig get ég séð ef fyrirtækið krefst aðgerðir starfsfólks?
Aðgerðir starfsfólks er krafist af fyrirtækinu ef þú ert beðinn um að velja aðgerð starfsfólks þegar stofna á nýjar stöður, breyta stöðum, ráða nýja starfsmenn, flytja starfsmenn, breyta launum starfsmanns, breyta stöðuverkefni, segja starfsmönnum upp eða setja starfsmenn í leyfi. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Það er mismunur stöðuaðgerð starfsmannaaðgerð?
Til eru tvær gerðir aðgerða starfsfólks:

- Stöðuaðgerð - Stöðuaðgerð er framkvæmd á núverandi stöðum eða nýjum stöðum. Til dæmis stöðuaðgerð gæti verið nauðsynleg ef gildinu á fyrirliggjandi stöðu er breytt eða ef stofnað er ný árstíðarbundinna stöðu. Nákvæmar upplýsingar um hvernig á að nota stöðuaðgerðir má fá í Lykilverk: Núverandi stöður starfskrafts eða Lykilverk: Nýjar stöður starfskrafts.

- Starfsmannaaðgerð - Starfsmannaaðgerð er framkvæmd fyrir núverandi starfsmenn eða nýja starfsmenn. Til dæmis starfsmannaaðgerð gæti verið nauðsynlegt þegar nýr starfsmaður er ráðinn eða fyrirliggjandi starfsmanns fær stöðuhækkun. Nákvæmar upplýsingar um hvernig á að nota starfsmannaaðgerðir má sjá í Úthluta starfsfólksaðgerðum á starfsmenn.

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Hvað á stöðu aðgerða starfsfólks sannvottunarskemanu þau?
Starfsfólksaðgerðir geta haft eftirfarandi stöður:

- **Drög** – Sé verkflæði notað hefur aðgerðin ekki verið send. Ef verkflæðinu er ekki notað aðgerð hefur ekki verið lokið.
- **Í yfirferð** – Starfsfólksaðgerðin hefur verið send í verkflæði en verkflæði er ekki lokið.
- **Samþykkt, bíður** – Verkflæðinu er lokið en breytingarnar eru enn í vinnslu. Hætt við - Hætt var við verkflæðið eða starfsfólksaðgerðin afturkölluð. Hafnað - Beiðni um aðgerð var hafnað af samþykkjanda.
- **Aðgerð í vinnslu** – Aðgerðarbeiðnin hefur verið samþykkt og breytingarnar eru í vinnslu.
- **Verkflæði lokið**  – Verkflæðinu er lokið og breytingarnar hafa verið gerðar. Mistókst - Verkflæðið mistókst vegna þess að upplýsingar eru úreltar. Smelltu á Endurvirkja til að birta nýjustu upplýsingar og halda áfram.
- **Lokið** – Það tókst að stofna eða breyta stöðunni eða starfsmaður var ráðinn, fluttur eða hann hættur störfum, eða það varð breyting á launum. Villa - Vandamál kom upp annað en að upplýsingar séu úreltar. Opnaðu Skilaboðakladda starfsfólksaðgerða til að komast að ástæðu villunnar.
- **Hafnað** – Aðgerðarbeiðni var hafnað af samþykkjanda.

## <a name="can-i-delete-a-personnel-action"></a>Get ég eytt aðgerðar starfsfólks?
Já, þú getur eytt aðgerðum starfsfólks sem hafa stöðuna **Drög**, **Villa**, **Mistókst**, or **Hætt við**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Hvað er hraðasta leið til að athuga stöðu beiðni um aðgerð starfsfólks?
Opnaðu einhverja listasíðu starfsfólksaðgerða og veldu starfsfólksaðgerð.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Hvað skuli I? ef mistekst beiðni um aðgerð starfsfólks
Ef beiðni um aðgerð starfsfólks mistekst, skal fylgja þessum skrefum til að leysa þessa villu og endursenda beiðnina:

> 1. Á **Aðgerðarúðu** skaltu smella á hnappinn **Villutexti** til að skoða skilaboðatexta sem lýsir vandamálinu.
> 
> 2. Á **Aðgerðarúðu** skaltu smella á **Endurvirkja** til að sækja nýjustu upplýsingar og stilla stöðu starfsfólksaðgerða aftur á **Drög**.
> 
> 3. Leystu villuna og smelltu svo á **Ljúka** eða **Senda**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Hvað gerist aðgerð starfsfólks sem notar verkflæði þegar lokalínu samþykktarferlisins er lokið?
Ef engar villur eru á aðgerð starfsfólks verður aðeins til lestrar. (Hægt er að skoða sögu á listasíðunni **Allar aðgerðir starfsmanns** en ekki er hægt að breyta starfsfólksaðgerðinni.) Þegar staða starfsfólksaðgerðar er **Lokið** hefur staða eða skrá starfsmanns þegar verið uppfærð. Til að skoða breytingar sem voru gerðar skaltu opna listasíðuna **Stöður** eða **Starfskraftar**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Hvers vegna fæ ég eftirfarandi villu þegar ég færi inn núllgildi inn í svæðið Laun? „Gildið er utan gildra marka - það verður að vera á milli og 0,00 og 0,00“
Þessi boð berast þér vegna þess að reiturinn Stig í skjámyndinni Starf er auður fyrir starfið sem tengist valdri stöðu.

Til að lagfæra þessa villu, skal fylgja þessum skrefum:

> 1. Í skjámyndinni Stöðuverkefni starfskrafts skaltu smella á reitinn Staða.  
> 2. Smelltu á gildið í reitnum Starf til að opna starfssíðuna.
> 3. Smelltu á Breyta í Aðgerðarúðunni.
> 4. Smelltu á flipann Laun.
> 5. Veldu stig í reitnum Stig.
> 6. Lokaðu síðunni Starf.
> 7. Lokaðu síðunni Staða.
> 8. Farðu aftur í flipann Laun á síðunni Starfskraftur og veldu Föst laun.  Veldu Ný og skráðu stöðu starfsmanns í reitnum Staða.  Færðu inn gildi í reitinn Áætlun og færðu svo inn laun starfsmannsins í reitinn Launataxti.

## <a name="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form"></a>Af hverju get ég ekki breytt upphafsdagsetningu í haus starfsmannaaðgerðarskjámyndar?
Ekki er hægt að breyta gildisdagsetningu þar sem svæðið er fyllt með dagsetningu nýjustu röklegt fyrir gerðina aðgerð.

Dæmi:

- Upphafsdagsetning í haus aðgerðarinnar **Segja starfskrafti upp** er dagsetningin sem þú skráðir í reitinn **Starfslokadagur**.
- Upphafsdagsetning í aðgerðinni **Ráða starfskraft** er dagsetningin sem þú skráðir í reitinn **Upphafsdagur starfs**.
- Upphafsdagsetning í aðgerðinni **Flytja starfskraft** er dagsetningin sem þú skráðir í reitinn **Upphafsdagsetning verkefnis** fyrir starfskraftinn.

