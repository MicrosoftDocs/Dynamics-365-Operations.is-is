---
title: Virkja greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222587"
---
# <a name="enable-customer-payment-predictions-preview"></a>Virkja greiðsluspár viðskiptavinar (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn. Kveikt er á aðgerðinni á vinnusvæðinu **Eiginleikastjórnun** og skilgreiningarstillingar eru slegnar inn á síðunni **Færibreytur fjármálainnsýnar**. Þetta efnisatriði inniheldur einnig upplýsingar sem geta aðstoðað þig við að nota eiginleikann á skilvirkan hátt.

> [!NOTE]
> Áður en eftirfarandi skrefum er lokið skal ganga úr skugga um að ljúka undirbúningsskrefunum í efnisatriðinu [Skilgreining fyrir fjármál](configure-for-fin-insites.md).

1. Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi. Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa. (Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > Sleppið þessu skrefi ef notuð er útgáfa 10.0.20 eða nýrri eða ef notuð er uppsetning Service Fabric. Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig. Ef þú sérð ekki eiginleikann á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á honum skal hafa samband við <fiap@microsoft.com>. 

2. Kveikja á innsýnareiginleika greiðslu viðskiptavinar:

    1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
    2. Leitaðu að eiginleikanum sem heitir **Innsýn í greiðslu viðskiptavinar (forskoðun)**.
    3. Veldu **Virkja núna**.

    Kveikt er á eiginleikanum innsýn í greiðslu viðskiptavinar og hann er tilbúin til skilgreiningar.

3. Skilgreina innsýnareiginleika greiðslu viðskiptavinar:

    1. Opnaðu **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**.

        [![Síða færibreyta fjármálainnsýnar áður en eiginleikinn er skilgreindur](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Á síðunni **Færibreytur fjármálainnsýnar** á flipanum **Innsýn í greiðslu viðskiptavinar** skal velja tengilinn **Skoða gagnareitina sem eru notaðir í spálíkaninu** til að opna síðuna **Gagnareitir fyrir spálíkan**. Þar er hægt að skoða sjálfgefinn lista yfir svæði sem eru notuð til að stofna spálíkan gervigreindar (AI) fyrir greiðsluspár viðskiptavinar.

        Til að nota sjálfgefna lista yfir reiti til að búa til spálíkanið skal loka síðunni **Gagnareitir fyrir spálíkan** og síðan á síðunni **Færibreytur fjármálainnsýnar** stilla valkostinn **Virkja eiginleika** á **Já**.

    3. Tilgreinið færslutímabil „mjög seint“ til að skilgreina hvað spáramminn **Mjög seint** þýðir fyrir fyrirtækið þitt.

        Fyrir hvern opinn reikning spáir kerfið því að líkur á greiðslu í þremur römmum: **Á réttum tíma**, **Seint** og **Mjög seint**.

        - **Á tíma** - Þessi rammi inniheldur reiðslur sem áætlað er að verði greiddar á eða fyrir gjalddaga færslunnar.
        - **Seint** - Þessi rammi inniheldur greiðslur sem áætlað er að verði greiddar eftir gjalddaga færslunnar en fyrir tímabilið sem telst mjög á eftir áætlun.
        - **Mjög seint** – Þessi rammi innheldur greiðslur sem spáð er að verði borgaðar eftir upphafsdag færslutímabilsins „mjög seint“.

        > [!NOTE]
        > Þegar færslutímabilinu „mjög seint“ er breytt og **Breyta viðmiðunarmörkum fyrir seint** er valið eftir að spálíkan gervigreindar fyrir greiðslur viðkiptavinar hefur verið stofnað, er fyrirliggjandi spálíkani eytt og nýtt líkan stofnað. Nýja spálíkanið flytur færslur yfir í tímabilið „mjög seint“ miðað við stillingarnar sem voru slegnar inn til að skilgreina það.

    4. Þegar búið er að skilgreina færslutímabilið „mjög seint“ skal velja **Stofna spálíkan** til að stofna spálíkanið. Hlutinn **Spálíkan** á síðunni **Færibreytur fjármálainnsýnar** sýnir stöðu spálíkansins.

        > [!NOTE]
        > Á meðan spálíkanið er stofnað er hægt að velja **Endurstilla stofnun spálíkans** hvenær sem er til að endurræsa ferlið.

    Eiginleikinn hefur nú verið skilgreindur og er tilbúinn til notkunar.

Þegar lokið er við að kveikja á og skilgreina eiginleikann og spálíkanið hefur verið stofnað og er í gangi sýnir hlutinn **Gerð spálíkans** á síðunni **Færibreytur fjármálainnsýnar** nákvæmni líkansins, eins og sýnt er á eftirfarandi skýringarmynd.

[![Nákvæmni spálíkans á síðunni Færibreytur fjármálainnsýnar](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Upplýsingar um losun

Almenn forskoðun Fjármálainnsýnar er í boði til prufuuppsetningar í Bandaríkjunum, Evrópu og Bretlandi. Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.

Aðeins er hægt og aðeins skal kveikja á eiginleikum almennrar forskoðunar í tveggja laga sandkassaumhverfi. Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi. Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
