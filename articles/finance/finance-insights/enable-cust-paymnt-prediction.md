---
title: Virkja greiðsluspár viðskiptavinar
description: Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.
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
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 16ccd7f2e11f0b46aaa646de272e668d29ccc0c0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752929"
---
# <a name="enable-customer-payment-predictions"></a>Virkja greiðsluspár viðskiptavinar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn. Þú kveikir á eiginleikanum í **Eiginleikastjórnun** vinnusvæði og sláðu inn stillingar á **Uppsetning fjármálainnsýnar** síðu. Þetta efnisatriði inniheldur einnig upplýsingar sem geta aðstoðað þig við að nota eiginleikann á skilvirkan hátt.

> [!NOTE]
> Áður en eftirfarandi skrefum er lokið skal ganga úr skugga um að ljúka undirbúningsskrefunum í efnisatriðinu [Skilgreining fyrir fjármál](configure-for-fin-insites.md).

1. Kveiktu á eiginleikanum fyrir greiðsluspá viðskiptavina:

    1. Opnaðu vinnusvæðið **Eiginleikastjórnun**.
    2. Veldu **Leita að uppfærslum**.
    3. Á **Allt** flipi, leitaðu að **Greiðsluspá viðskiptavina**. Ef þú finnur ekki þann eiginleika skaltu leita að **(Forskoðun) Greiðsluspá viðskiptavina**. 
    4. Kveiktu á eiginleikanum.

    Nú er kveikt á eiginleikum greiðsluspáa viðskiptavina og tilbúið til að stilla hana.

2. Skilgreina innsýnareiginleika greiðslu viðskiptavinar:

    1. Fara til **Inneign og innheimtur \> Uppsetning \> Innsýn í fjármálum \> Greiðsluspá viðskiptavina**.
    2. Á **Uppsetning fjármálainnsýnar** síðu, á **Greiðsluspá viðskiptavina** flipa, veldu **Skoðaðu gagnareitina sem notaðir eru í spálíkaninu** að opna **Gagnareitir fyrir spálíkan** síðu. Þar er hægt að skoða sjálfgefinn lista yfir svæði sem eru notuð til að stofna spálíkan gervigreindar (AI) fyrir greiðsluspár viðskiptavinar.

        Til að nota sjálfgefna lista yfir reiti til að búa til spálíkanið skaltu loka **Gagnareitir fyrir spálíkan** síðu og síðan á **Uppsetning fjármálainnsýnar** síðu, stilltu **Virkja eiginleika** valmöguleika til **Já**.

    3. Tilgreinið færslutímabil „mjög seint“ til að skilgreina hvað spáramminn **Mjög seint** þýðir fyrir fyrirtækið þitt.

        Fyrir hvern opinn reikning spáir kerfið því að líkur á greiðslu í þremur römmum: **Á réttum tíma**, **Seint** og **Mjög seint**.

        - **Á tíma** - Þessi rammi inniheldur reiðslur sem áætlað er að verði greiddar á eða fyrir gjalddaga færslunnar.
        - **Seint** - Þessi rammi inniheldur greiðslur sem áætlað er að verði greiddar eftir gjalddaga færslunnar en fyrir tímabilið sem telst mjög á eftir áætlun.
        - **Mjög seint** – Þessi rammi innheldur greiðslur sem spáð er að verði borgaðar eftir upphafsdag færslutímabilsins „mjög seint“.

        > [!NOTE]
        > Þegar færslutímabilinu „mjög seint“ er breytt og **Breyta viðmiðunarmörkum fyrir seint** er valið eftir að spálíkan gervigreindar fyrir greiðslur viðkiptavinar hefur verið stofnað, er fyrirliggjandi spálíkani eytt og nýtt líkan stofnað. Nýja spálíkanið flytur færslur yfir í tímabilið „mjög seint“ miðað við stillingarnar sem voru slegnar inn til að skilgreina það.

    4. Þegar búið er að skilgreina færslutímabilið „mjög seint“ skal velja **Stofna spálíkan** til að stofna spálíkanið. The **Spálíkan** kafla um **Uppsetning fjármálainnsýnar** síða sýnir stöðu spálíkansins.

        > [!NOTE]
        > Á meðan spálíkanið er stofnað er hægt að velja **Endurstilla stofnun spálíkans** hvenær sem er til að endurræsa ferlið.

    Eiginleikinn hefur nú verið skilgreindur og er tilbúinn til notkunar.

Eftir að kveikt hefur verið á eiginleikanum og hann stilltur, og spálíkanið hefur verið búið til og virkar, **Spálíkan** kafla í **Færibreytur fjármálainnsýnar** síða sýnir nákvæmni líkansins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
