---
title: Búðu til gagnasamþættingarverkefni
description: Þetta efnisatriði útskýrir hvernig á að búa til gagnasamþættingarverkefni.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7841f8b31e0ac1a40dce9acaac747f5f378236e0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752665"
---
# <a name="create-a-data-integration-project"></a>Búðu til gagnasamþættingarverkefni

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að búa til gagnasamþættingarverkefni.

1. Skrá inn á Microsoft Dynamics 365 Finance.
2. Farið á **Vinnusvæði \> Gagnastjórnun** og veljið **Gagnaeiningar**. Bíða skal þar til allir gagnaeiningarnar hafa verið uppfærðar áður en farið er í næsta skref.
3. Opnaðu [Power Apps gáttina](https://make.powerapps.com/) og fylgdu eftirfarandi skrefum:

    1. Veljið viðeigandi umhverfi.
    2. Í vinstri yfirlitsrúðunni, veldu **Dataverse\> Tengingar**.
    3. Tengjast við viðeigandi tilvik eftirfarandi atriða:

        - Dynamics 365
        - Dynamics 365 fyrir fin & Ops

4. Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:

    1. Veldu **Samþætting gagna**.
    2. Veljið **Tengingasett**.
    3. Veljið **Nýtt tengingasett**.
    4. Færa skal inn heiti fyrir tenginguna.
    5. Velja viðeigandi tengingar fyrir eftirfarandi atriði:

        - Dynamics 365
        - Dynamics 365 fyrir fin & Ops

    6. Veljið viðeigandi fyrirtækjavörpun.
    7. Velja **Stofna**.

5. Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:  

    1. Stofna gagnasamþættingarverk fyrir eftirfarandi sniðmát með því að nota tengingarsett sem var verið að stofna:

        - Greiðsla innsýn viðskiptavinar (CDS to Fin and Ops 10.0.17+)
        - Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)
        - Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)

    2. Stillið viðeigandi áætlanagerð fyrir hvert verk.

> [!NOTE]
> Ef áskildar einingar eru ekki til staðar í CDS skal fara í **Skuldir og innheimta > Uppsetning > Fjármálainnsýn > Færibreytur fjármálainnsýnar**, virkja eiginleikann „Greiðsluspár viðskiptavinar“ og smella á hnappinn **Búa til spárlíkan**. Þegar innleiðingu á AI-líkani er lokið (tókst eða mistókst) eru CDS-einingarnar sem nauðsynlegar eru fyrir samþættingu settar upp í í CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
