---
title: Notkun Microsoft Power Apps-vefgátta með gagnalíkani aðila
description: Þetta efnisatriði lýsir breytingum á vefhlutverkum fyrir Microsoft Power Apps-gáttir vegna gagnalíkans aðilans í tvöfaldri skráningu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: eee4076c5f16d9655bde3ee4943f79732598199f286d14aa542c167497d83262
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726212"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Notkun Microsoft Power Apps-vefgátta með gagnalíkani aðila

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Útgáfa tvöfaldrar skráningar niðurröðunarþjónustu, útgáfa 2.0.999.0 og nýrri, inniheldur breytingar gagnalíkans á aðila- og altækri tengiliðaskrá fyrir reikninginn og tengiliðatöflur. Breytingarnar gera tengls við marga möguleg sem styðja ítarleg viðskiptaumhverfi. Þessar breytingar eru ekki studdar af vefhlutverkum vefgáttar, þar á meðal viðskiptavinagátt, sem eru sendar eins og þær eru eða sem voru til staðar í umhverfinu áður en sett var upp tvöföld skráning. Til að vefhlutverkin virki sem skyldi er nauðsynlegt að búa til ný vefhlutverk með nýja gagnalíkaninu. 

Með öðrum orðum hafa töflurnar breyst en töfluheimildir í viðskiptavinagáttinni hafa ekki breyst. Þetta efnisatriði útskýrir hvernig á að búa til nýtt vefhlutverk sem virka með nýja ítarlega gagnalíkaninu.

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
