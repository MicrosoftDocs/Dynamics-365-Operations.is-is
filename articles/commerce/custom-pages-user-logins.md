---
title: Setja upp sérsniðnar síður fyrir innskráningu notenda
description: Þetta efni lýsir því hvernig á að smíða sérsniðnar síður í Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b54bf6234dcb87c84b21259c30ca5c321869adf
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817307"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Setja upp sérsniðnar síður fyrir innskráningu notenda


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að smíða sérsniðnar síður í Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).

## <a name="overview"></a>Yfirlit

Til að nota sérsniðnar síður sem eru gerðar í Dynamics 365 Commerce til að takast á við innskráningarflæði notenda verður þú að setja upp Azure AD stefnu sem vísað verður til í viðskiptaumhverfi. Þú getur stillt „Skráning og innskráning“, „Forstillingum breytt“ og „Aðgangsorð endurstillt“ Azure AD B2C stefnur með því að nota Azure AD B2C forrit. Síðan er hægt að vísa til Azure AD B2C leigjanda og stefnuheita við útvegunarferlið sem er gert fyrir viðskiptaumhverfið með því að nota Microsoft Dynamics Lifecycle Services (LCS).

Hægt er að smíða sérsniðnar viðskiptasíður með því að nota innskráningu, skráningu, breytingu reikningssniðs eða endurstillingu lykilorðs. Síðan ætti að vísa í vefslóðir síðunnar sem eru birtar fyrir þessar sérsniðnu síður Azure AD B2C stefnuskilgreiningar í Azure gáttinni.

## <a name="set-up-b2c-policies"></a>Setja upp B2C reglur

Eftir að þú hefur sett upp þinn Azure AD B2C leigjanda og tengt hann við viðskiptaumhverfi þitt ferðu á síðuna **Azure AD B2C** í Azure gáttinni og síðan á valmyndinni undir **Stefnur** velurðu **Notendastreymi (reglur)**.

![Skipunin Notandaflæði (stefna) í valmyndinni](./media/B2C_CustomPage_PoliciesMenu.png)

Þú getur nú stillt innskráninguna "Skráðu þig inn og skráðu þig inn", "Prófíklippingu" og "Lykilorð endurstillt" innskráningarflæði notenda.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Stilla stefnuna „Skráning og innskráning“

Fylgdu þessum skrefum til að stilla stefnuna „Skráning og innskráning“.

1. Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Skráning og innskráning**.
1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_SignInSignUp**).
1. Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna. Að lágmarki verður **Innskráning í gegnum tölvupóst** að vera valin.
1. Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netfang**, **Fornafn** og **Eftirnafn**.
1. Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.

    ![Eiginleikar og kröfur valdar](./media/B2C_SignInSignUp_Attributes.png)

1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

    ![Eiginleikasíða fyrir nýju regluna](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Vísað verður að fullu til heitis reglunnar í viðskiptaumhverfi. (Forskeytið **B2C\_1\_** verður með í tilvísuninni.) Ekki er hægt að endurnefna reglur eftir að þær eru búnar til. Ef þú ert að skipta út núverandi reglu fyrir viðskiptaumhverfi þitt geturðu eytt upprunalegu reglunni og byggt upp nýja reglu með sama heiti. Að öðrum kosti, ef umhverfið hefur þegar verið útvegað, geturðu sent nýja regluheitið í gegnum þjónustubeiðni.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

### <a name="configure-the-profile-editing-policy"></a>Stilla regluna „Forstillingum breytt“

Til að skilgreina regluna „Forstillingum breytt“ skal fylgja þessum skrefum.

1. Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Forstillingum breytt**.
1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_EditProfile**).
1. Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna. Að lágmarki verður **Innskráning á staðbundin reikning** að vera valin.
1. Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netföng** og **Eftirnafn**.
1. Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.
1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

### <a name="configure-the-password-reset-policy"></a>Stilltu regluna „Núllstilla lykilorð“

Til að skilgreina regluna „Aðgangsorð endurstillt“ skal fylgja þessum skrefum.

1. Veldu **Nýtt notendaflæði** og síðan á flipanum **Forskoða** velurðu regluna **Aðgangsorð endurstill v1.1**.

    ![V1.1 reglan fyrir endurstillingu aðgangsorðs valin á flipanum Forskoða](./media/B2C_ForgetPassword_Menu.png)

1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_ForgetPassword**).
1. Í hlutanum **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.
1. Í dálknum **Skilakrafa** velurðu gátreitina fyrir **Netföng**, **Fornafn**, **Eftirnafn** og **Hlutakenni notanda**.

    ![Valdar kröfur](./media/B2C_ForgetPassword_Attributes.png)

1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

## <a name="build-the-custom-pages"></a>Smíða sérsniðnar síður

Fylgdu þessum skrefum til að búa til sérsniðnar síður til að meðhöndla innskráningu notenda.

1. Farðu á síðuna þína í höfundatólum verslunarinnar.
1. Búðu til eftirfarandi fimm sniðmát og fimm blaðsíður:

    - Sniðmátið **Innskráning** og síðu sem notar innskráningareininguna.
    - Sniðmátið **Skráning** og síðu sem notar skráningareininguna.
    - Sniðmátið **Aðgangsorð endurstillt** og síðu sem notar eininguna aðgangsorð endurstillt.
    - Sniðmátið **Staðfesting á endurstillingu aðgangsorðs** og síðu sem notar eininguna staðfesting á endurstillingu aðgangsorðs.
    - Sniðmátið **Forstillingum breytt** og síðu sem notar eininguna lykilforstillingum breytt

Fylgdu þessum leiðbeiningum þegar þú smíðar síðurnar:

- Notaðu útlit og stíl fyrir hverja síðu eða einingu sem hentar best viðskiptaþörfum þínum.
- Birtu allar síður og vefslóðir sem þarf að nota í uppsetningu Azure AD B2C.
- Eftir að síðurnar og vefslóðirnar eru birtar safnarðu vefslóðum sem verður að nota fyrir regluskilgreiningar Azure AD B2C. Viðskeytinu **?preloadscripts=true** verður bætt við hverja vefslóð þegar það er notað.

> [!IMPORTANT]
> Ekki endurnýta altækan hausa og síðufætur sem hafa tengda tengla. Vegna þess að þessar síður verða hýstar í Azure AD B2C lén þegar þau eru notuð, aðeins hreinar vefslóðir ættu að nota fyrir alla tengla.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Stilla Azure AD B2C reglur með sérsniðnum síðuupplýsingum 

Farðu aftur í Azure gáttina á síðuna **Azure AD B2C** og síðan, á valmyndinni undir **Reglur**, velurðu **Notendastreymi (reglur)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Uppfærðu regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Skráning og innskráning** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Samræmd skráningar- eða innskráningarsíða**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla innskráningarslóðina. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.
1. Veldu útlitið **Skráningarsíða staðbundins reiknings**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla skráningarslóðina. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.
1. Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:

    1. Fyrir eigindirnar **Netfang**, **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.
    1. Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.

    ![Stillingar reglu fyrir skráningarsíðu staðbundinna reikninga](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Uppfærðu regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Forstillingum breytt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Síðan Breyta forstillingum**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að breyta forstillingum. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.
1. Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:

    1. Fyrir eigindirnar **Netfang**, **Fornafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.
    1. Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Uppfærðu regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Aðgangsorð endurstillt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Ný aðgangsorðasíða**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að endurstilla aðgangsorð. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.
1. Veldu útlitið **Síðan Staðfesting á reikningi**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla stafestingarslóðina fyrir endurstillt aðgangsorð. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Sérsníða sjálfgefna textastrengi fyrir merki og lýsingar

Í einingasafninu eru innskráningareiningar forfylltar með sjálfgefnum textastrengjum fyrir merki og lýsingu. Þú getur sérsniðið þessa strengi í hugbúnaðarþróunarbúnaðinum (SDK) með því að uppfæra gildin í global.json skránni fyrir innskráningarhlutann.

Til dæmis er sjálfgefinn texti fyrir tengilinn sem gleymdist lykilorð **Gleymt lykilorð?**. Eftirfarandi sýnir þennan sjálfgefna texta á innskráningarsíðunni.

![Sjálfgefinn texti fyrir tengilinn við gleymt lykilorð á innskráningarsíðunni](./media/B2C_SignUp_ModuleFace.png)

Í global.json skrá fyrir innskráningareiningu einingasafnsins er hægt að breyta textanum í **Manstu ekki aðgangsorðið?** eins og sýnt er á eftirfarandi teikningu.

![Uppfærður tenglatexti í global.json skránni í einingunni](./media/B2C_CustomizingStringsForModule.png)

Þegar búið er að uppfæra global.json-skrá og birta breytingarnar birtist nýr tengill í innskráningareiningunni í bæði verslun og á innskráningarsíðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum slóðartilvísunum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
