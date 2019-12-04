---
title: Leiðbeiningar úrræðaleitar gagnasamþættingar
description: Þetta efni veitir úrræðaleitarupplýsingar um samþættingu gagna á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771026"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Leiðbeiningar úrræðaleitar gagnasamþættingar

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Kveiktu á viðbótarrakningarklöddum í Common Data Service og athugaðu upplýsingar um villuleiðbeiningar við tvískipta viðbót

[!include [banner](../includes/banner.md)]

Ef þú lendir í vandræðum eða villum við samstillingu við tvískipta skrifun skaltu fylgja þessum skrefum til að skoða villurnar í rakningakladdanum.

1. Áður en þú getur skoðað villurnar verður þú að virkja viðbótarrakningarkladda fyrst. Fyrir leiðbeiningar skal sjá kaflann „Rakningarkladda“ í [Kennsluefni: Skrifaðu og skráðu viðbót](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Núna geturðu skoðað villurnar.

2. Skrá inn á Microsoft Dynamics 365 Sales.
3. Veldu hnappinn **Stillingar** (gírtáknið) og síðan **Ítarlegar stillingar**.
4. Í valmyndinni **Stillingar** velurðu **Sérstillingar \> Rakningarkladdi viðbótar**.
5. Veldu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** sem tegundarheiti til að sýna villuupplýsingarnar.

## <a name="inspect-dual-write-synchronization-errors"></a>Skoðaðu villur í tvöföldum skrifum við samstillingu

Fylgdu þessum skrefum til að skoða villur við prófun.

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Opnaðu LCS verkefnið til að gera tvískipt próf fyrir.
3. Veldu **Umhverfi í skýi**.
4. Búðu til tengingu fjartengds skjáborðs við sýndarvél (VM) forritsins með því að nota staðbundinn reikning sem er sýndur í LCS.
5. Opnaðu tilvikayfirlit. 
6. Farðu í **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**. Villurnar og smáatriðin eru sýnd.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Aftengdu eitt Common Data Service umhverfi úr forritinu og tengdu annað umhverfi

Fylgið eftirfarandi skrefum til að uppfæra tengla:

1. Farðu í umhverfi forritsins.
2. Opnaðu Gagnastýringu.
3. Veldu **Tengil við CDS fyrir forrit**.
4. Veldu allar varpanir sem eru í gangi og veldu síðan **Hætta**.
5. Veldu allar varpanir og smelltu svo á **Eyða**.

    > [!NOTE]
    > Valkosturinn **Eyða** er ekki tiltækur ef sniðmátið **ViðskiptavinurV3-lykill** er valið. Hreinsaðu valið á þessu sniðmáti eftir þörfum. **ViðskiptavinurV3-lykill** er eldra útvegað sniðmát og vinnur með lausninni Prospect to Cash. Þar sem það er gefið út á heimsvísu birtist það undir öllum sniðmátum.

6. Veldu **Aftengja umhverfi**.
7. Veldu **Já** til að staðfesta aðgerðina.
8. Til að tengja nýja umhverfið skaltu fylgja skrefunum í [uppsetningarhandbók](https://aka.ms/dualwrite-docs).
