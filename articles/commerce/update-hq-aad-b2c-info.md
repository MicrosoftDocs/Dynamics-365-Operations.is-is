---
title: Uppfærðu höfuðstöðvar verslunar með nýju Azure AD B2C upplýsingum
description: Þessi grein lýsir því hvernig á að uppfæra Microsoft Dynamics 365 Commerce höfuðstöðvar með nýjum Azure Active Directory (Azure AD) upplýsingar frá fyrirtæki til neytenda (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785822"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Uppfærðu höfuðstöðvar verslunar með nýju Azure AD B2C upplýsingum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að uppfæra Microsoft Dynamics 365 Commerce höfuðstöðvar með nýjum Azure Active Directory (Azure AD) upplýsingar frá fyrirtæki til neytenda (B2C).

Þegar Azure AD B2C úthlutunarskrefum hér að ofan er lokið verður Azure AD B2C umsókn að vera skráð á þitt Dynamics 365 Commerce umhverfi.

Til að uppfæra höfuðstöðvar með nýjum Azure AD B2C upplýsingum, fylgdu þessum skrefum.

1. Farðu í **Samnýttar færibreytur Commerce** og veldu **Kennisveitendur** í vinstri valmyndinni.
1. Undir **Kennisveitendur** gerirðu eftirfarandi:
    1. Í **Útgefandi** reit, sláðu inn útgefandastreng auðkennisveitunnar. Sjáðu til að finna útgefandastrenginn þinn [Fáðu útgefandastreng fyrir uppsetningu höfuðstöðva](#obtain-issuer-string-for-headquarters-setup) hér að neðan.
    1. Í reitinn **Heiti** skal færa inn heiti fyrir útgefendaskrána.
    1. Í reitnum **Gerð** slærðu inn **Azure AD B2C (id_token)**.
1. Undir **Treystandi aðilar**, með valinn hlut B2C kennisveitanda hér að ofan, gerðu eftirfarandi:
    1. Í **Auðkenni viðskiptavinar** reit, sláðu inn B2C forritaauðkenni þitt, sem þú getur fundið í **Auðkenni umsóknar** kassi á eiginleikasíðu B2C forritsins þíns.
    1. Í reitnum **Gerð** slærðu inn **Opinbert**.
    1. Í reitnum **Notandagerð** slærðu inn **Viðskiptavinur**.
1. Í aðgerðaglugganum velurðu **Vista.**
1. Í leitarreit Commerce leitarðu að **Dreifingaráætlun**
1. Í vinstri valmyndinni á síðunni **Dreifingaráætlanir** velurðu vinnsluna **1110 altæk stilling**.
1. Í aðgerðarúðunni skal velja **Keyra núna**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Fáðu útgefandastreng fyrir uppsetningu höfuðstöðva

Fylgdu þessum skrefum til að fá útgefandastreng auðkennisveitunnar þinnar.

1. Á Azure AD B2C síðu Azure-gáttarinnar skal fara í **Nýskrá og innskrá** notandaflæði.
1. Veljið **Síðuútlit** í vinstri yfirlitsvalmyndinni, undir **Heiti útlits** skal velja **Samræmd síða nýskráningar og innskráningar** og veljið því næst **Keyra notandaflæði**.
1. Gakktu úr skugga um að forritið þitt sé stillt á það sem þú ætlaðir þér Azure AD B2C forrit búið til hér að ofan, og veldu síðan notendaflæðistengilinn sem birtist undir **Keyra notendaflæði** haus sem inniheldur ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Ekki velja **Keyra notendaflæði** .) Nýr flipi opnast sem sýnir lýsigögn fyrir stefnuna til að safna útgefandastrengnum.
1. Á lýsigagnasíðunni sem birtist á vafraflipanum skaltu afrita útgefandastreng auðkennisveitunnar (gildið fyrir **útgefanda** byrjar á "https:// " og endar á "/v2.0/") sem lítur svipað út og eftirfarandi dæmi.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**EÐA** : Til að setja saman sömu slóð lýsigagna handvirkt skal fara í gegnum eftirfarandi skref.

1. Búðu til veffang lýsigagna á eftirfarandi sniði með B2C leigjanda þínum og stefnu: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Dæmi: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Sláðu inn veffang lýsigagna í veffangastiku vafrans.
1. Í lýsigögnum, afritarðu veffang útgefanda kennisveitanda (gildið fyrir **"útgefandi"**).
    - Dæmi: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Stilltu B2C leigjanda þinn í Commerce site builder](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
