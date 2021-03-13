---
title: Stofna verk til að setja upp samþættingu gagna (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að stofna erk til að setja upp samþættingu gagna.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009447"
---
# <a name="create-a-data-integrator-project-preview"></a>Stofna verk til að setja upp samþættingu gagna (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
        - Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)
        - Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)

    2. Stillið viðeigandi áætlanagerð fyrir hvert verk.

> [!NOTE]
> Ef áskildar einingar eru ekki til staðar í CDS skal fara í **Skuldir og innheimta > Uppsetning > Fjármálainnsýn > Færibreytur fjármálainnsýnar**, virkja eiginleikann „Greiðsluspár viðskiptavinar“ og smella á hnappinn **Búa til spárlíkan**. Þegar innleiðingu á AI-líkani er lokið (tókst eða mistókst) eru CDS-einingarnar sem nauðsynlegar eru fyrir samþættingu settar upp í í CDS.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.
