---
title: Stofna verk til að setja upp samþættingu gagna (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að stofna erk til að setja upp samþættingu gagna.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: a32ad6eb1b1874a9f9ec452def3c213cd160c5faa2aec02b655a86e160e2b509
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768988"
---
# <a name="create-a-data-integrator-project-preview"></a>Stofna verk til að setja upp samþættingu gagna (forskoðun)

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna erk til að setja upp samþættingu gagna.

1. Skrá inn á Microsoft Dynamics 365 Finance.
2. Farið á **Vinnusvæði\> Gagnastjórnun** og veljið **Gagnaeiningar**. Bíða skal þar til allir gagnaeiningarnar hafa verið uppfærðar áður en farið er í næsta skref.
3. Opnaðu [Power Apps gáttina](https://make.powerapps.com/) og fylgdu eftirfarandi skrefum:

    1. Veljið viðeigandi umhverfi.
    2. Á vinstra yfirlitssvæðinu skal velja **Gagna \> Tengingar**.
    3. Tengjast við viðeigandi tilvik eftirfarandi atriða:

        - Dynamics 365
        - Dynamics 365 fyrir fin & Ops

4. Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:

    1. Veljið **Data Integrator**.
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

        - Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)
            - Ef útgáfa 10.0.17 eð‘a nýrri er notuð þarf að nota sniðmát sem kallast Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops 10.0.17+).
        - Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)
        - Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)

    2. Stillið viðeigandi áætlanagerð fyrir hvert verk.

> [!NOTE]
> Ef áskildar einingar eru ekki til staðar í CDS skal fara í **Skuldir og innheimta > Uppsetning > Fjármálainnsýn > Færibreytur fjármálainnsýnar**, virkja eiginleikann „Greiðsluspár viðskiptavinar“ og smella á hnappinn **Búa til spárlíkan**. Þegar innleiðingu á AI-líkani er lokið (tókst eða mistókst) eru CDS-einingarnar sem nauðsynlegar eru fyrir samþættingu settar upp í í CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
