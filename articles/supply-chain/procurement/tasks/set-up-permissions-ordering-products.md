---
title: Setja upp heimildir fyrir pöntun afurða fyrir hönd annarra
description: Þetta efni útskýrir hvernig á að veita starfsmönnum heimild til að undirbúa innkaupabeiðnir fyrir hönd annarra starfsmanna.
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf39040bef2ccd0c643ce0d034348807ecdc50c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914802"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Setja upp heimildir fyrir pöntun afurða fyrir hönd annarra

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efni útskýrir hvernig á að veita starfsmönnum heimild til að undirbúa innkaupabeiðnir fyrir hönd annarra starfsmanna. Með öðrum orðum getur „undirbúningsaðili“ innkaupabeiðni stofnað beiðni fyrir aðra „umsækjanda.“ Ferlið sýnir einnig hvernig á að veita starfskrafti heimild til að panta vörur og þjónustu í öðrum lögaðilum eða rekstrareiningum. Þessi verk eru yfirleitt gert af innkaupastjóra. Hægt er að nota þetta ferli í annað hvort fyrir gögn fyrir sýnigögn USMF- fyrirtækisins eða þín eigin gögn.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Veita heimildir til að færa inn innkaupabeiðnir fyrir hönd annan starfsmann
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Heimildir innkaupabeiðni**. Gangið úr skugga um að reiturinn **Núverandi yfirlit** er stillt á **Af undirbúningsaðila**. Á listanum í vinstri rúðunni sýnir fólki sem getur fengið heimild til að undirbúa beiðnir fyrir hönd annars fólks.  
2. Veljið einstakling sem veita á heimildir (undirbúningsaðili).
3. Veljið **Bæta við**.
4. Finna og velja einstaklinginn sem er bætt við sem umsækjanda.
    - Umsækjandinn er sá aðili, fyrir hvers hönd undirbúningsaðili getur stofnað beiðnir fyrir.  
    - Í svæðinu **Heimild** skal velja **Tiltekinn** ef undirbúningsaðili á að geta stofna innkaupabeiðnir fyrir hönd valins starfsmanns. Veljið **skýrslugjöf** ef undirbúningsaðili á einnig að geta stofnað innkaupabeiðnir fyrir hönd allra starfsmanna sem ber skylda til skýrslugjafar til þess aðila.  
5. Í reitinn **Tekur gildi** skal færa inn dagsetningu.
6. **Í reitinn lokadagsetning, skal færa inn dagsetningu.**

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Skoða undirbúningsaðila sem hafa heimild til að stofna innkaupabeiðnir fyrir valinn starfsmann
1. Í reitnum **Núverandi yfirlit** skal velja **Eftir umsækjanda**. Þetta yfirlit sýnir lista yfir undirbúningsaðila sem hafa fengið heimild til að stofna innkaupabeiðnir fyrir hönd valins starfsmanns.  
2. Nota flýtiafmörkun til að finna starfsmann sem var nýverið bætt við sem umsækjanda.
3. Veljið umsækjanda Listi Undirbúningsaðila sýnir fólk sem hefur heimild til að panta hluti fyrir hönd umsækjandans sem er valinn á rúðunni vinstra megin.  Hægt er að bæta við fleiri undirbúningsaðilum hér. Þetta yfirlit leyfir þér einnig að veita umsækjanda heimild til að stofna beiðnir í lögaðilum og rekstrareiningum sem eru ekki aðal lögaðili eða rekstrareining þess einstaklings.  

