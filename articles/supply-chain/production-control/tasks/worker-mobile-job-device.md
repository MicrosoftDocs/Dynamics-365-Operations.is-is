---
title: Skilgreina starfsmann með fartæki
description: Þetta efni útskýrir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.
author: ShylaThompson
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe4e195763f5329ee7732a2f087094acbad595a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810943"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Skilgreina starfsmann með fartæki

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Gakktu úr skugga um að starfsmanni sé úthlutað ákveðið hlutverk

Fyrir þetta dæmi, staðfestið að notandinn „SHANNON“ hefur hlutverk stjórnanda vélarinnar áður en þú stillir starfsmannareikninginn.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur**.
2. Leitaðu að notanda í hraðsíunni. Í þessu dæmi skal færa inn `shannon`.
3. Veldu tengilinn í **notandanafn** dálkur notendareikningsins sem birtist.
4. Í trénu **Notendahlutverk** velurðu **Hlutverk > Starfsmaður á vél**.
5. Lokaðu **upplýsingar um notendur** og **notendur** síður til að fara aftur á heimasíðuna.

## <a name="configure-worker-account"></a>Skilgreina notandareikning starfkrafts
1. Fara til **Skoðunargluggi > Kerfiseiningar > Mannauður > Starfskraftar > Starfskraftar**.
2. Leitaðu að notanda í hraðsíunni. Í þessu dæmi skal færa inn `shannon`.
3. Veldu tengilinn í **Heiti** dálkur notendareikningsins sem birtist.
4. Veldu flipann **Tímaskráning**.
5. Veldu **Virkja á skráningarstöðvum**.
6. Færðu inn eða veldu gildi í eftirfarandi svæði:  

    - **Reikniflokkur**  
    - **Sjálfgefinn útreikningaflokkur**  
    - **Samþykkisflokkur**  
    - **Stöðluð forstilling**  
    - **Forstillingarflokkur**  

7. Veljið **Í lagi**.
8. Veldu **Breyta** til að færa inn númer korti fyrir nýja starfsmaður sem sinnir tímaskráningu. Færðu inn gildi í reitnum **Kortkenni**.
9. Veljið **Vista**.
10. Lokaðu **Upplýsingar um starfsmann** og **Verkamenn**.

## <a name="assign-worker-to-device-group"></a>Úthluta starfskrafti á tækjaflokk.
1. Fara í **Framleiðslustýringar > Uppsetning > Framkvæmd framleiðslu > Skilgreina verkspjald fyrir tæki**.
2. Veljið **Bæta við**.
3. Á listanum, skal velja viðeigandi strafskraft. Í þessu dæmi, velja **SHANNON**.
4. Veljið **Í lagi**.
5. Veljið **Breyta**.
6. Í svæðið **eining Framleiðslu** er hægt að setja síu sjálfgefið fyrir starfsmann. Þetta mun tryggja að eingöngu vinnslur fyrir valda framleiðslueiningu eru birtar þegar starfsmaður skráir sig inn á tækinu. Færa inn æskilegt gildi.
7. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]