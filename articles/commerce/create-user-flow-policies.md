---
title: Stofna notandaflæðisstefnu
description: Þessi grein lýsir því hvernig á að búa til notendaflæðisreglur í Microsoft Azure gátt.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785818"
---
# <a name="create-user-flow-policies"></a>Stofna notandaflæðisstefnu

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til notendaflæðisreglur í Microsoft Azure gátt.

Notendaflæði eru stefnurnar Azure Active Directory (Azure AD) fyrirtæki til neytenda (B2C) notar til að veita örugga innskráningu, skrá sig, breyta prófílnum og gleyma notendaupplifunum með lykilorði. Dynamics 365 Commerce notar þessi flæði til að framkvæma stefnuaðgerðir til að hafa samskipti við Azure AD B2C leigjanda. Þegar notandi hefur samskipti við þessar reglur er þeim vísað til Azure AD B2C leigjandi til að framkvæma aðgerðirnar.

Azure AD B2C býður upp á þrjár gerðir af grunnflæðum notenda:
- Skráðu þig og skráðu þig inn
- Forstillingum breytt
- Aðgangsorð endurstillt

Þú getur valið að nota sjálfgefið notendaflæði sem veitt er af Azure AD, sem mun birta síðu sem hýst er af Azure AD B2C. Að öðrum kosti geturðu búið til HTML síðu til að stjórna útliti og viðmóti þessara reynsluflæði notenda. 

Til að sérsníða stefnusíður notenda með síðum smíðuðum í Dynamics 365 Commerce skal skoða [Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md). Fyrir frekari upplýsingar, sjá [Sérsníddu viðmót notendaupplifunar í Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Búðu til notendaflæðisstefnu fyrir skráningu og innskráningu

Fylgdu þessum skrefum til að búa til notendaflæðisstefnu fyrir skráningu og innskráningu.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Veljið regluna **Nýskrá og innskrá** og því næst velja **Ráðlagða** útgáfu.
1. Undir **Heiti** slærðu inn heiti stefnu. Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).
1. Undir **Auðkennisveitendur**, í **Staðbundnir reikningar** kafla, veldu **Skráning í tölvupósti**. Tölvupóstsvottun er notuð í flestum algengum tilfellum fyrir verslun. Ef þú ert líka að nota auðkenningarveitu fyrir félagslega auðkenni geturðu líka valið þá á þessum tíma.
1. Undir **Fjölþættri sannvottun**, veldu viðeigandi val fyrir þitt fyrirtæki. 
1. Undir **Eiginleikar og kröfur notanda**, veldu valkosti til að safna eiginleikum eða skila kröfum eftir því sem við á. Veldu **Sýndu meira...** til að fá allan lista yfir eiginleika og kröfumöguleika. Commerce krefst eftirfarandi sjálfgefinna valkosta:

    | **Innheimtueigind** | **Skila kröfu** |
    | ---------------------- | ----------------- |
    | Tölvupóstfang          | Netföng   |
    | Fornafn             | Fornafn        |
    |                        | Auðkennisveitandi |
    | Eftirnafn                | Eftirnafn           |
    |                        | ObjectId notanda  |

1. Velja **Stofna**.

Eftirfarandi mynd er dæmi um Azure AD B2C skráning og innskráningarflæði notenda.

![Stefnustillingar skráningar og innskráningar.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Búðu til forstillingum breytt fyrir notendaflæði

Til að stofna notendaflæðisreglu forstillingabreytinga skal fylgja þessum skrefum.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Veljið **Forstillingum breytt** og því næst veljið **Ráðlagða** útgáfu.
1. Undir **Heiti**, sláðu inn notendaflæði forstillingabreytingar. Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).
1. Undir **Auðkennisveitendur**, í **Staðbundnir reikningar** kafla, veldu **Innskráning í tölvupósti**.
1. Undir **Eiginleikar notanda** skal velja eftirfarandi gátreiti:
    
    | **Innheimtueigind** | **Skila kröfu** |
    | ---------------------- | ----------------- |
    |                        | Netföng   |
    | Fornafn             | Fornafn        |
    |                        | Auðkennisveitandi |
    | Eftirnafn                | Eftirnafn           |
    |                        | ObjectId notanda  |
    
1. Velja **Stofna**.

Eftirfarandi mynd sýnir dæmi um Azure AD B2C notendaflæði forstillingabreytingar.

![Dæmi um Azure AD B2C prófíl breyta notendaflæði](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Stofna notendaflæðisreglu endurstillingar aðgangsorðs

Til að stofna notendaflæðisreglu endurstillingar aðgangsorðs skal fylgja þessum skrefum.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Veljið **Endurstilling aðgangsorðs** og því næst veljið **Ráðlagða** útgáfu.
1. Undir **Heiti**, slærðu inn heiti fyrir notandastreymi aðgangsorðs með lykilorði.
1. Undir **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.
1. Velja **Stofna**.
1. Undir **Forritskröfur** skal velja eftirfarandi gátreiti:
    - **Netföng**
    - **Fornafn**
    - **Eftirnafn**
    - **ObjectId notanda**
1. Velja **Stofna**.

Eftirfarandi mynd sýnir hvar á að stilla **Núllstilla lykilorð með póstfangi** í Azure AD B2C lykilorð endurstillir notendaflæði.

![Stilltu „Núllstilla lykilorð með póstfangi“ í stefnu um endurstillingu lykilorðs](./media/B2CImage_13.png)

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Bættu við samfélagsmiðlum](add-social-identity-providers.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
