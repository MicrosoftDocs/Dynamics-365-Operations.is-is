---
title: Stofna verk fyrir samþættingu gagna
description: Þessi grein útskýrir hvernig á að stofna verk fyrir samþættingu gagna.
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
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876241"
---
# <a name="create-a-data-integration-project"></a>Stofna verk fyrir samþættingu gagna

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að stofna verk fyrir samþættingu gagna.

1. Innskráning í Microsoft Dynamics 365 Finance
2. Farið á **Vinnusvæði\> Gagnastjórnun** og veljið **Gagnaeiningar**. Bíða skal þar til allir gagnaeiningarnar hafa verið uppfærðar áður en farið er í næsta skref.
3. Opnaðu [Power Apps gáttina](https://make.powerapps.com/) og fylgdu eftirfarandi skrefum:

    1. Veljið viðeigandi umhverfi.
    2. Á yfirlitssvæðinu til vinstri skal velja **Dataverse\>Tengingar**.
    3. Tengjast við viðeigandi tilvik eftirfarandi atriða:

        - Dynamics 365
        - Dynamics 365 fyrir fin & Ops

4. Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:

    1. Veljið **Data Integration**.
    2. Veljið **Tengingasett**.
    3. Veljið **Nýtt tengingasett**.
    4. Færa skal inn heiti fyrir tenginguna.
    5. Velja viðeigandi tengingar fyrir eftirfarandi atriði:

        - Dynamics 365
        - Dynamics 365 fyrir fin & Ops

    6. Veljið viðeigandi fyrirtækjavörpun.
    7. Velja **Stofna**.

5. Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:  

    1. Stofna eitt gagnasamþættingarverk fyrir hvert eftirfarandi sniðmát með því að nota tengingarsett sem var verið að stofna:

        - Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin and Ops 10.0.17+)
        - Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)
        - Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)

      > [!NOTE]
      > Ef mörg samþættingarverkefni eru búin til fyrir hvert sniðmát geta villur komið upp sem loka á uppfærslurnar.

    2. Stillið viðeigandi áætlanagerð fyrir hvert verk.

> [!NOTE]
> Ef þú sérð ekki nauðsynlegar einingar í Dataverse, farðu þá í **Skuldir og innheimta** > **Uppsetning** > **Fjármálainnsýn** > **Fjármálainnsýn færibreytur**, virkjaðu eiginleikann, **Greiðsluspár viðskiptavinar** og veldu síðan **Stofna spálíkan**. Þegar innleiðingu á gervigreindarlíkani er lokið eru Dataverse-einingarnar sem nauðsynlegar eru fyrir samþættingu settar upp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
