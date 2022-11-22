---
title: Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði
description: Þessi grein lýsir því hvernig á að stilla leigjanda fyrirtækis til neytenda (B2C) í Microsoft Dynamics 365 Commerce vefsmiður.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785819"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla leigjanda fyrirtækis til neytenda (B2C) í Microsoft Dynamics 365 Commerce vefsmiður.

Þegar uppsetningu á Azure AD B2C leigjandi er lokið, þú verður að stilla B2C leigjanda í vefsvæðishönnuði Commerce. Stillingarþrepin fela í sér að safna upplýsingum um B2C umsóknir úr Azure-gáttinni, færa þær B2C forritaupplýsingar inn í vefsvæðishönnuð og tengja síðan B2C forritið við vefsvæðið og rás.

### <a name="collect-the-required-application-information"></a>Safnaðu nauðsynlegum upplýsingum um forritið

Fylgdu þessum skrefum til að safna nauðsynlegum forritsupplýsingum.

1. Í Azure gáttinni, farðu til **Heim \>Azure AD B2C - App skráningar**.
1. Veldu forritið þitt og veldu síðan í vinstri yfirlitsrúðunni **Yfirlit** til að fá upplýsingar um umsóknina.
1. Frá **Auðkenni umsóknar (viðskiptavinar).** tilvísun, safnaðu auðkenni umsóknar B2C forritsins sem búið var til í B2C leigjanda þínum. Þetta verður síðar fært inn sem **GUID biðlara** í vefsvæðishönnuði.
1. Veldu **Tilvísun URI** og safnaðu svarslóðinni sem sýnd er fyrir síðuna þína (svarslóðin sem færð var inn við uppsetningu).
1. Fara til **Heim \>Azure AD B2C – Notendaflæði**, og safnaðu síðan fullum nöfnum hverrar notendaflæðisstefnu.

Eftirfarandi mynd sýnir dæmi um **Azure AD B2C - App skráningar** yfirlitssíðu.

![Azure AD B2C - Yfirlitssíða forritaskráningar með auðkenni umsóknar (viðskiptavinar) auðkennt](./media/ClientGUID_Application_AzurePortal.png)

Eftirfarandi mynd sýnir dæmi um reglur notendaflæðis á síðunni **Azure AD B2C - Notendastreymi (reglur)**.

![Safnaðu heitum fyrir hvert flæði B2C-reglu.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Sláðu inn þinn Azure AD B2C umsóknarupplýsingar leigjanda í Commerce

Þú verður að slá inn upplýsingar um Azure AD B2C leigjandi í vefsvæðishönnuð Commerce áður en B2C leigjandi er tengdur við vefsvæðin þín.

Til að bæta við þínu Azure AD B2C umsóknarupplýsingar leigjanda til Commerce, fylgdu þessum skrefum.

1. Skráðu þig inn sem stjórnandi í vefsvæðishönnuði Commerce fyrir umhverfi þitt.
1. Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.
1. Undir **Stillingar leigjanda**, veldu **Auðkenningaruppsetning vefsvæðis**. 
1. Í aðalglugganum við hliðina á **Staðfestingarprófílar**, veldu **Stjórna**. (Ef leigjandi þinn birtist á lista yfir auðkenningarprófíla, þá var honum þegar bætt við af stjórnanda. Gakktu úr skugga um að atriðin í skrefi 6 hér að neðan passa við þau fyrir fyrirhugaða B2C uppsetningu. Einnig er hægt að búa til nýtt snið með því að nota svipað Azure AD B2C leigjendur eða forrit til að gera grein fyrir minniháttar mun, svo sem mismunandi notendastefnuauðkenni).
1. Veldu **Bættu við auðkenningarprófíl vefsvæðis**.
1. Sláðu inn eftirfarandi nauðsynlega hluti í glugganum sem birtist, með gildum úr B2C leigjanda þínum og forriti. Reitir sem ekki er krafist (þeir sem eru án stjörnu) kunna að vera auðir.

    - **Heiti forrits**: Heiti B2C forritsins, til dæmis „Fabrikam B2C“.
    - **Nafn leigjanda**: Heiti B2C leigjanda (til dæmis er notað „fabrikam“ ef lénið birtist sem „fabrikam.onmicrosoft.com“ fyrir B2C leigjandann). 
    - **Gleymdu auðkenni lykilorðsstefnu**: Notandastraumur fyrir gleymt lykilorð notendastreymis, til dæmis „B2C_1_PasswordReset“.
    - **Auðkenni innskráningarstefnu** : Innskráningar- og innskráningarauðkenni notendaflæðisstefnu, til dæmis „B2C_1_signup_signin“.
    - **GUID biðlara**: Auðkenni B2C forritsins, til dæmis „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.
    - **Breyta auðkenni prófílstefnu**: Auðkenni sniðs sem breytir notendastreymi, til dæmis „B2C_1A_ProfileEdit“.

1. Veljið **Í lagi**. Þú ættir nú að sjá nafn B2C forritsins þíns birtast á listanum.
1. Veldu **Vista** til að vista breytingarnar.

Hið valfrjálsa **Skráðu inn sérsniðið lén** reitinn ætti aðeins að nota ef þú ert að setja upp sérsniðið lén fyrir Azure AD B2C leigjandi. Fyrir frekari upplýsingar og íhuganir varðandi notkun á **Skráðu inn sérsniðið lén** sviði, sjá [Viðbótarupplýsingar B2C](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Tengdu B2C forritið við síðuna þína og rás

> [!WARNING]
> - Ef vefsvæðið þitt er nú þegar tengt B2C forriti, með því að breyta í annað B2C forrit, verður að fjarlægja núverandi tilvísanir sem settar hafa verið upp fyrir notendur sem þegar hafa skráð sig í þessu umhverfi. Ef það hefur breyst verða engin skilríki sem eru tengd B2C forritinu sem nú er úthlutað tiltæk fyrir notendur. 
> - Uppfærðu B2C forritið aðeins ef þú ert að setja upp B2C forrit rásarinnar í fyrsta skipti eða ef þú ætlar að láta notendur skrá sig aftur með nýjum skilríkjum á þessa rás með nýja B2C forritinu. Gætið varúðar þegar rásir eru tengdar við B2C forrit og nafnið forrit greinilega. Ef rás er ekki tengd B2C forriti í skrefunum hér að neðan verða notendur sem skrá sig inn á þá rás fyrir síðuna þína færðir inn í B2C forritið sem birtist sem **sjálfgefið** í listanum **Leigjandastillingar \> B2C stillingar** yfir B2C forrit.

Til að tengja B2C forritið við síðuna þína og rás skaltu fylgja þessum skrefum.

1. Farðu á vefsvæðið í vefsvæðishönnuði Commerce.
1. Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.
1. Undir **Vefsvæðisstillingar** velurðu **Rásir**.
1. Í aðalglugganum undir **Rásir** velurðu rásina þína.
1. Í rásareiginleikarúðunni til hægri skaltu velja B2C forritsheitið þitt úr **Veldu B2C forrit** fellivalmynd.
1. Veldu **Loka** og veldu síðan **Vista og birta**.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Viðbótarupplýsingar B2C](additional-b2c-info.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
