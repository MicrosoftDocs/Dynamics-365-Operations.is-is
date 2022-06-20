---
title: Notkun Microsoft Power Apps-vefgátta með gagnalíkani aðila
description: Þessi grein lýsir breytingunum á vefhlutverkunum fyrir Microsoft Power Apps gáttir vegna aðilagagnalíkans í tvískrifa.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: c2e9d0f47ef90167bf84bb5b20e6a7ad2d58ffd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898947"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Notkun Microsoft Power Apps-vefgátta með gagnalíkani aðila

[!INCLUDE[banner](../../includes/banner.md)]



Útgáfa tvöfaldrar skráningar niðurröðunarþjónustu, útgáfa 2.0.999.0 og nýrri, inniheldur breytingar gagnalíkans á aðila- og altækri tengiliðaskrá fyrir reikninginn og tengiliðatöflur. Breytingarnar gera tengls við marga möguleg sem styðja ítarleg viðskiptaumhverfi. Þessar breytingar eru ekki studdar af vefhlutverkum vefgáttar, þar á meðal viðskiptavinagátt, sem eru sendar eins og þær eru eða sem voru til staðar í umhverfinu áður en sett var upp tvöföld skráning. Til að vefhlutverkin virki sem skyldi er nauðsynlegt að búa til ný vefhlutverk með nýja gagnalíkaninu. 

Með öðrum orðum hafa töflurnar breyst en töfluheimildir í viðskiptavinagáttinni hafa ekki breyst. Þessi grein útskýrir hvernig á að búa til ný vefhlutverk sem vinna með nýja háþróaða gagnalíkaninu.

Þessi skýringarmynd sýnir töflutengslin **án** gagnalíkans aðila- og altækrar aðsetursbókar:

   ![án aðilalíkans.](media/without-party-model.PNG)

Þessi skýringarmynd sýnir töflutengslin **með** gagnalíkani aðila- og altækrar aðsetursbók:

   ![með aðilalíkani.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Stofna nýja töfluheimild

Fylgið þessum skrefum til að búa til þessar nýju töfluheimildir:

1. Skráðu þig inn á [Power Apps](https://make.powerapps.com), og farðu í forritin þín.
2. Veljið forritið fyrir gáttarumsjón.
3. Í hliðarstikunni skal velja **Öryggi > Töfluheimildir**.

    Búa þarft til þrjár nýjar heimildir:

    + **Tengiliður** í töflutengingu **Aðila**
    + **Aðili** í töflutengingu **Lykils**
    + **Lykill** í töflutengingu **Pöntunar**

4. Búa til og vista nýja heimild fyrir tengingu tengiliðs við aðila og stilla þessar færibreytur:

    + **Heiti**: **Aðili** í töflutengingu **Lykils** (eða eigið val)
    + **Töfluheiti**: msdyn_contactforparty
    + **Vefsvæði**: Gátt viðskiptavinar
    + **Umfang**: Tengiliður
    + **Réttindi**: Velja allt
    + **Vefhlutverk**: Sannvottaðir notendur, fulltrúi viðskiptavinar (eða eigið val)

5. Búa til og vista nýja heimild fyrir tengingu aðila að reikningi og stilla þessar færibreytur:

    + **Heiti**: Tenging aðila að reikningi (eða eigið val)
    + **Töfluheiti**: reikningur
    + **Vefsvæði**: Gátt viðskiptavinar
    + **Umfang**: Yfireining
    + **Réttindi**: Velja allt
    + **Heimild yfirtöflu**: Tenging tengiliðs við aðilia

6. Búa til og vista nýja heimild fyrir Reikningur til að panta tengingu, stilla þessar færibreytur:

    + **Heiti**: Tenging reiknings við pöntun (eða eigið val)
    + **Töfluheiti**: salesorder
    + **Vefsvæði**: Gátt viðskiptavinar
    + **Umfang**: Yfireining
    + **Réttindi**: Velja allt
    + **Heimild yfirtöflu**: Tenging aðila að reikningi

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
