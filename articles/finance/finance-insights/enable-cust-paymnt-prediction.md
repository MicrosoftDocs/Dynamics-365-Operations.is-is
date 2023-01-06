---
title: Virkja greiðsluspár viðskiptavinar
description: Þessi grein útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
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
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898208"
---
# <a name="enable-customer-payment-predictions"></a>Virkja greiðsluspár viðskiptavinar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í Finance Insights. Kveikt er á aðgerðinni á vinnusvæðinu **Eiginleikastjórnun** og skilgreiningarstillingar eru færðar inn á síðunni **Skilgreining Finance insights**. Þessi grein inniheldur einnig upplýsingar sem geta aðstoðað þig við að nota eiginleikann á skilvirkan hátt.

> [!NOTE]
> Áður en eftirfarandi skrefum er lokið skal ganga úr skugga um að ljúka undirbúningsskrefunum í greininni [Stilla fyrir Finance Insights](configure-for-fin-insites.md).

1. Kveikja á eiginleikanum greiðsluspá viðskiptavinar:

    1. Opnaðu vinnusvæðið **Eiginleikastjórnun**.
    2. Veldu **Leita að uppfærslum**.
    3. Á flipanum **Allt** skal leita að **Greiðsluspár viðskiptavinar**. Ef þú finnur ekki þennan eiginleika skaltu leita að **(Forútgáfa) Greiðsluspár viðskiptavinar**. 
    4. Kveiktu á eiginleikanum.

    Kveikt er á eiginleikanum greiðsluspá viðskiptavinar og hann er tilbúin til skilgreiningar.

2. Skilgreina innsýnareiginleika greiðslu viðskiptavinar:

    1. Opnaðu **Skuldir og innheimta \> Uppsetning \> Finance insights \> Greiðsluspár viðskiptavinar**.
    2. Á síðunni **Skilgreining Finance Insights** á flipanum **Greiðsluspár viðskiptavinar** skal velja **Skoða gagnareitina sem eru notaðir í spálíkaninu** til að opna síðuna **Gagnareitir fyrir spálíkan**. Þar er hægt að skoða sjálfgefinn lista yfir svæði sem eru notuð til að stofna spálíkan gervigreindar (AI) fyrir greiðsluspár viðskiptavinar.

        Til að nota sjálfgefna lista yfir reiti til að búa til spálíkanið skal loka síðunni **Gagnareitir fyrir spálíkan** og síðan á síðunni **Skilgreining Finance Insights** stilla valkostinn **Virkja eiginleika** á **Já**.
        
   > [!NOTE]
   > Meira en 100 færslur undanfarna sex til níu mánuði eru gerðar vegna **Greiðsluspár viðskiptavinar**. Færslunar geta falið í sér textareikninga, sölupantanir og greiðslur til viðskiptavina. Þessi gögn verða að vera dreifð á milli **Á áætlun**, **Sein** og **Mjög seint** stillinga.    
     

    3. Tilgreinið færslutímabil „mjög seint“ til að skilgreina hvað spáramminn **Mjög seint** þýðir fyrir fyrirtækið þitt.

        Fyrir hvern opinn reikning spáir kerfið því að líkur á greiðslu í þremur römmum: **Á réttum tíma**, **Seint** og **Mjög seint**.

        - **Á tíma** - Þessi rammi inniheldur reiðslur sem áætlað er að verði greiddar á eða fyrir gjalddaga færslunnar.
        - **Seint** - Þessi rammi inniheldur greiðslur sem áætlað er að verði greiddar eftir gjalddaga færslunnar en fyrir tímabilið sem telst mjög á eftir áætlun.
        - **Mjög seint** – Þessi rammi innheldur greiðslur sem spáð er að verði borgaðar eftir upphafsdag færslutímabilsins „mjög seint“.

        > [!NOTE]
        > Þegar færslutímabilinu „mjög seint“ er breytt og **Breyta viðmiðunarmörkum fyrir seint** er valið eftir að spálíkan gervigreindar fyrir greiðslur viðkiptavinar hefur verið stofnað, er fyrirliggjandi spálíkani eytt og nýtt líkan stofnað. Nýja spálíkanið flytur færslur yfir í tímabilið „mjög seint“ miðað við stillingarnar sem voru slegnar inn til að skilgreina það.

    4. Þegar búið er að skilgreina færslutímabilið „mjög seint“ skal velja **Stofna spálíkan** til að stofna spálíkanið. Hlutinn **Spálíkan** á síðunni **Færibreytur Finance Insights** spálíkan sýnir stöðu spálíkansins.

        > [!NOTE]
        > Á meðan spálíkanið er stofnað er hægt að velja **Endurstilla stofnun spálíkans** hvenær sem er til að endurræsa ferlið.

    Eiginleikinn hefur nú verið skilgreindur og er tilbúinn til notkunar.

Þegar lokið er við að kveikja á og skilgreina eiginleikann og spálíkanið hefur verið stofnað og er í gangi sýnir hlutinn **Gerð spálíkans** á síðunni **Færibreytur Finance Insights** nákvæmni líkansins.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
