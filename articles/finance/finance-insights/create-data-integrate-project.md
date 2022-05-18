---
title: Búðu til gagnasamþættingarverkefni
description: Þetta efnisatriði útskýrir hvernig á að búa til gagnasamþættingarverkefni.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4d69ffcb6ccfcc7bae2891f2539941f7b6bbf86e
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722884"
---
# <a name="create-a-data-integration-project"></a>Búðu til gagnasamþættingarverkefni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að búa til gagnasamþættingarverkefni.

1. Skrá inn Microsoft Dynamics 365 Fjármál.
2. Farið á **Vinnusvæði\> Gagnastjórnun** og veljið **Gagnaeiningar**. Bíða skal þar til allir gagnaeiningarnar hafa verið uppfærðar áður en farið er í næsta skref.
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

    1. Búðu til eitt gagnasamþættingarverkefni fyrir hvert af eftirfarandi sniðmátum með því að nota tengingarsettið sem þú bjóst til:

        - Greiðsla innsýn viðskiptavinar (CDS to Fin and Ops 10.0.17+)
        - Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)
        - Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)

      > [!NOTE]
      > Að búa til mörg gagnasamþættingarverkefni fyrir hvert sniðmát getur valdið villum sem loka fyrir uppfærslurnar.

    2. Stillið viðeigandi áætlanagerð fyrir hvert verk.

> [!NOTE]
> Ef þú sérð ekki nauðsynlegar einingar í Dataverse, fara til **Inneign og innheimtur** > **Uppsetning** > **Fjármálainnsýn** > **Færibreytur fjármálainnsýnar**, virkjaðu eiginleikann, **Greiðsluspá viðskiptavina**, og veldu síðan **Búðu til spálíkan**. Þegar uppsetningu gervigreindarlíkans er lokið, mun Dataverse aðilar sem þarf til að skapa samþættingu verða settir á vettvang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
