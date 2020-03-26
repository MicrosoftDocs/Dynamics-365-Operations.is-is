---
title: Setja upp B2C-leigjanda í Commerce
description: Þetta efni lýsir því hvernig á að setja upp þitt Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) til að auðkenna notendasíðu í Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5fca37fb89c723273ef753b102092e2cfb26563
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096509"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Setja upp B2C-leigjanda í Commerce

[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að setja upp þitt Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) til að auðkenna notendasíðu í Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce notar Azure AD B2C til að styðja persónuskilríki notenda og staðfesting. Notandi getur skráð sig, skráð sig inn og endurstillt lykilorð sitt í gegnum þessa flæði. Azure AD B2C geymir viðkvæmar sannvottunarupplýsingar notanda, svo sem notandanafn og lykilorð. Notendaskráin í leigjanda B2C mun geyma annað hvort skrá yfir B2C staðbundna reikninga eða skrá yfir fyrirtækjasamfélag B2C. Þessar B2C skrár munu tengjast aftur viðskiptamannaskránni í Commerce-umhverfi.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Búðu til eða tengdu fyrirliggjandi AAD B2C leigjanda í Azure-gáttinni

1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
1. Úr Azure-vefsíðugáttinni velurðu **Stofna tilföng**. Athugaðu að nota áskriftina og skrána sem verða tengd Commerce-umhverfi þínu.

    ![Búðu til tilföng í Azure Portal](./media/B2CImage_1.png)

1. Farðu í **Auðkenni \> Azure Active Directory B2C**.
1. Þegar þú ert á síðunni **Stofna nýjan B2C leigjanda eða tengil á núverandi leigjanda** notarðu einn af valkostunum hér að neðan sem best hentar þörfum fyrirtækisins þíns:

    - **Stofna nýjan Azure AD B2C leigjandi**: Notaðu þennan valkost til að búa til nýjan AAD B2C leigjanda.
        1. Veldu **Stofna nýjan Azure AD B2C-leigjanda**.
        1. Undir **Heiti fyrirtækisins** slærðu inn heiti fyrirtækisins.
        1. Undir **Upphaflegt lén** slærðu inn upphaflegt lén.
        1. Fyrir **Land eða svæði** velurðu landið eða svæðið.
        1. Veldu **Stofna** til að stofna leigjanda.

     ![Stofna nýjan Azure AD-leigjanda](./media/B2CImage_2.png)

     - **Tengja fyrirliggjandi Azure AD B2C leigjandi við Azure áskriftina mína**: Notaðu þennan valkost ef þú ert þegar með Azure AD B2C leigjanda sem þú vilt tengjast.
        1. Veldu **Tengja núverandi Azure AD B2C leigjandi við Azure áskriftina mína**.
        1. Fyrir **Azure AD B2C leigjandi**, veldu viðeigandi B2C leigjanda. Ef skilaboðin „Engir hæfir B2C leigjendur fundust“ birtast í valröðinni, þá ert þú ekki með núverandi gjaldgengan B2C leigjanda og verður að búa til nýjan.
        1. Fyrir **Tilfangaflokkur**, veldu **Stofna nýtt**. Sláðu inn **Heiti** fyrir tilfangaflokkinn sem mun innihalda leigjandann, veldu **Staðsetning tilfangaflokks** og veldu síðan **Stofna**.

    ![Tengja núverandi Azure AD B2C leigjandi við Azure áskrift](./media/B2CImage_3.png)

1. Þegar nýja Azure AD B2C skráin er búin til (þetta getur tekið smá stund), tengill á nýju skráasafnið birtist á yfirlitinu. Þessi hlekkur mun vísa þér á síðuna „Velkomin/n í Azure Active Directory B2C“.

    ![Hlekkur á nýja AAD skrá](./media/B2CImage_4.png)

> [!NOTE]
> Ef þú ert með margar áskriftir á Azure reikningnum þínum eða hefur sett upp leigjanda B2C án þess að tengjast virkri áskrift mun borði með **Úrræðaleit** vísa þér til að tengja leigjanda við áskrift. Veldu úrræðaleit og fylgdu leiðbeiningunum til að leysa áskriftarmálið.

Eftirfarandi mynd sýnir dæmi um borða með Azure AD B2C **Úrræðaleit**.

![Viðvörun sem sýnir skráarsafn hefur enga virka áskrift](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>Stofna B2C forrit

Þegar B2C leigjandinn hefur verið stofnaður muntu búa til B2C forrit innan leigjandans til að hafa samskipti við aðgerðir Commerce.

Til að stofna B2C forrit skal fylgja þessum skrefum.

1. Veldu í Azure vefsíðunni **Forrit** og veldu síðan **Bæta við**.
1. Undir **Heiti** slærðu inn heiti viðeigandi AAD B2C forrits.
1. Undir **Vefforrit/Vef-API**, fyrir **Hafa vefforrit með/vef-API**, veldu **Já**.
1. Fyrir **Leyfa óbeint flæði**, veldu **Já** (sjálfgefið gildi).
1. Undir **Svarslóð**, sláðu inn sérstakar svarslóðir þínar. Sjáðu [Svarslóðir](#reply-urls) hér að neðan til að fá upplýsingar um svarslóðir og hvernig eigi að forsníða þær hér.
1. Fyrir **Hafa native-bliðara með**, veldu **Nei** (sjálfgefið gildi).
1. Velja **Stofna**.

### <a name="reply-urls"></a>Svarslóðir

Svarslóðir eru mikilvægar þar sem þær leyfa hvítlista yfir lénsskilaboð þegar vefsvæðið þitt kallar í Azure AD B2C til að sannvotta notanda. Þetta gerir kleift að skila staðfestum notanda aftur til lénsins sem þeir skrá sig inn á (lén vefsvæðisins). 

Í reitnum **Svarslóð** á skjánum **Azure AD B2c - Forrit \> Nýtt forrit** þarftu að bæta við aðskildum línum fyrir bæði lén vefsvæðisins og (þegar umhverfi þitt er útvegað) Commerce-myndaðri vefslóðinni. Þessar vefslóðir verða alltaf að nota gilt slóðarsnið og verða að vera eingöngu grunnslóðir (engin skástrik eða slóðir fyrir aftan). Strengurinn ``/_msdyn365/authresp`` þarf síðan að vera bætt aftan við grunnslóðina, eins og í eftirfarandi dæmum.

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Stofna notandaflæðisstefnu

Notendastreymi eru reglurnar sem Azure AD B2C notar til að bjóða upp á örugga innskráningu, skráningu, breyta prófíl og gleyma aðgangsorðum notenda. Dynamics 365 Commerce notar þessi flæði til að framkvæma stefnuaðgerðir til að hafa samskipti við Azure AD B2C leigjanda. Þegar notandi hefur samskipti við þessar reglur er honum vísað í Azure AD B2C-leigjanda til að framkvæma aðgerðirnar.

Azure AD B2C býður upp á þrjár gerðir af grunnflæðum notenda:
- Skráðu þig og skráðu þig inn
- Forstillingum breytt
- Aðgangsorð endurstillt

Þú getur valið að nota sjálfgefna flæði notenda frá Azure AD, sem birtir síðu sem hýst er af AAD B2C. Að öðrum kosti geturðu búið til HTML síðu til að stjórna útliti og viðmóti þessara reynsluflæði notenda. 

Til að sérsníða stefnusíður notenda fyrir Dynamics 365 Commerce, sjáðu [Setja upp sérsniðnar síður fyrir notendanafn](custom-pages-user-logins.md). Sjá frekari upplýsingar í [Sérsniðið viðmót notendaupplifana í Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Búðu til skráningu og skráðu þig inn í notendaflæðisstefnu

Til að stofna innskráningu og skrá inn notendaflæðisstefnu skal fylgja þessum skrefum.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Á flipanum **Ráðlagt**, velurðu **Skráðu þig og skráðu þig inn**.
1. Undir **Heiti** slærðu inn heiti stefnu. Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).
1. Undir **Kennisveitendur**, veldu viðeigandi gátreit.
1. Undir **Fjölþættri sannvottun**, veldu viðeigandi val fyrir þitt fyrirtæki. 
1. Undir **Eiginleikar og kröfur notanda**, veldu valkosti til að safna eiginleikum eða skila kröfum eftir því sem við á. Commerce krefst eftirfarandi sjálfgefinna valkosta:

    | **Innheimtueigind** | **Skila kröfu** |
    | ---------------------- | ----------------- |
    |                        | Netföng   |
    | Fornafn             | Fornafn        |
    |                        | Auðkennisveitandi |
    | Eftirnafn                | Eftirnafn           |
    |                        | ObjectId notanda  |

1. Velja **Stofna**.

Eftirfarandi mynd er dæmi um Azure AD B2C skráningu og innskráningu í notendaflæði.

![Stefnustillingar skráningar og innskráningar](./media/B2CImage_11.png)

Eftirfarandi mynd sýnir valkostinn **Keyra notendaflæði** í Azure AD B2C skráningu og innskráningu í notendaflæði.

![Keyra valkost notendaflæðis í stefnuflæði](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Búðu til forstillingum breytt fyrir notendaflæði

Til að stofna notendaflæðisreglu forstillingabreytinga skal fylgja þessum skrefum.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Á flipanum **Ráðlagt** velurðu **Forstillingum breytt**.
1. Undir **Heiti**, sláðu inn notendaflæði forstillingabreytingar. Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).
1. Undir **Kennisveitendur**, veldu **Innskráning á staðbundinn reikning**.
1. Undir **Eiginleikar notanda** skal velja eftirfarandi gátreiti:
    - **Netföng** (aðeins **Skilakrafa**)
    - **Fornafn** (**Innheimtueigind** og **Skila kröfu**)
    - **Kennisveitandi** (aðeins **Skilakrafa**)
    - **Eftirnafn** (**Innheimtueigind** og **Skilakrafa**)
    - **ObjectId notanda** (aðeins **Skilakrafa**)
1. Velja **Stofna**.

Eftirfarandi mynd sýnir dæmi um Azure AD B2C notendaflæði forstillingabreytingar.

![Stofna notendaflæðið Forstillingum breytt](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Stofna notendaflæðisreglu endurstillingar aðgangsorðs

Til að stofna notendaflæðisreglu endurstillingar aðgangsorðs skal fylgja þessum skrefum.

1. Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.
1. Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.
1. Á flipanum **Ráðlagt** velurðu **Aðgangsorð endurstillt**.
1. Undir **Heiti**, slærðu inn heiti fyrir notandastreymi aðgangsorðs með lykilorði.
1. Undir **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.
1. Velja **Stofna**.
1. Undir **Forritskröfur** skal velja eftirfarandi gátreiti:
    - **Tölvupóstur**
    - **Aðsetur**
    - **Fornafn**
    - **Eftirnafn**
    - **ObjectId notanda**
1. Velja **Stofna**.

Eftirfarandi mynd sýnir hvar á að stilla **Núllstilla lykilorð með póstfangi** í Azure AD B2C lykilorð endurstillir notendaflæði.

![Stilltu „Núllstilla lykilorð með póstfangi“ í stefnu um endurstillingu lykilorðs](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Bæta við kennitöluveitendum (valfrjálst)

Kennitöluveitendur leyfa notendum að nota samfélagsreikninga sína til staðfestingar. Valfrjálst er að bæta við sannvottun fyrir kennisveitanda í Dynamics 365 Commerce. 

Ef staðfesting á kennitöluveitanda er ekki bætt við er sjálfgefið að Azure AD B2C forstillingar verði aðalforstillingar fyrir notandagrunn þinn. Notendur munu velja eigið notandanafn (valin netföng) og setja lykilorð. Azure AD B2C staðfestir notendur beint. 

Ef staðfesting á kennitöluveitanda bætist við og notandi velur einn af þeim kennitöluveitendum sem eru í boði er eining samt stofnuð í Azure AD B2C leigjandi. Azure AD B2C mun síðan staðfesta persónuskilríki notandans hjá kennitöluveitanda.

> [!NOTE]
> Innskráning kennisveitanda stofnar skrá í B2C leigjandanum, en á öðru sniði en staðbundnir reikningar þar sem það mun kalla tilvísun ytri kennitöluveitanda til staðfestingar. Notandinn getur notað sama netfang á milli kennitöluveitenda, sem þýðir að notandanafn tölvupóstsins sem notað er til sannvottunar er hugsanlega ekki einkvæmt fyrir leigjanda. Azure AD B2C mun einungis framfylgja því að notendur hafi einkvæmt netfang á B2C reikningum.

Áður en þú getur bætt við kennitöluveitanda til að staðfesta, verður þú að fara í gátt kennisveitanda og setja upp umsókn um kennisveitanda samkvæmt leiðbeiningunum í Azure AD B2C skjöl. Hér fyrir neðan er listi yfir tengla á fylgiskjölin.

- [Amazon](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Stakur leigjandi)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-reikningur](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Bættu við og settu upp kennisveitanda

Fylgdu þessum skrefum til að bæta við og setja upp kennisveitanda.  

1. Farðu á Azure gáttina **Persónuaðilum**.
1. Veljið **Bæta við**. Skjárinn **Bæta við kennisveitanda** birtist.
1. Undir **Heiti**, slærðu inn nafnið sem á að birtast notendum á innskráningarskjánum.
1. Undir **Gerð auðkennisveitanda**, veldu auðkennisveitanda af listanum.
1. Veljið **Í lagi**.
1. Veldu **Setja þennan kennisveitanda upp** til að fá aðgang að skjánum **Setja upp kennisveitanda**.
1. Undir **Biðlarakenni**, sláðu inn biðlarakennið eins og það er fengið úr forritsuppsetningu kennisveitandans.
1. Undir **Leynilykill biðlara**, sláðu inn leynilykill biðlara eins og það er fengið úr forritsuppsetningu kennisveitandans.
1. Festu notendaflæði fyrir innskráningarreglur við innskráningu:
1. Fara til **Azure AD B2C - Notendastreymi (reglur) \> {innskráningarstefna þín fyrir innskráningu} \> Kennisveitendur**.
1. Til að festa notendaflæðisstefnu fyrir skráningu/innskráningu velurðu alla kennisveitendur sem þú hefur sett upp fyrir reikninginn. Til að prófa þetta velurðu **Keyra notendaflæði** fyrir hvern kennisveitanda. Nýr flipi sýnir innskráningarsíðuna sem sýnir nýjan valkassa fyrir kennisveitanda.

Eftirfarandi mynd sýnir dæmi um skjáina **Bæta við kennisveitanda** og **Setja upp kennitöluveitanda** í Azure AD B2C.

![Að bæta við kennitöluveitanda fyrir forritið](./media/B2CImage_14.png)

Eftirfarandi mynd sýnir dæmi um hvernig eigi að velja kennisveitendur á síðunni Azure AD B2C **Kennisveitendur**.

![Veldu hvern félagslegan auðkennisaðila til að gera kleift að nota fyrir stefnu þína](./media/B2CImage_16.png)

Eftirfarandi mynd sýnir dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan.

![Dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Uppfærðu höfuðstöðvar verslunar með nýju Azure AD B2C upplýsingum

Þegar Azure AD B2C úthlutunarskrefum hér að ofan er lokið verður Azure AD B2C umsókn að vera skráð á þitt Dynamics 365 Commerce umhverfi.

Til að uppfæra höfuðstöðvar með nýjum Azure AD B2C upplýsingum, fylgdu þessum skrefum.

1. Farðu í **Samnýttar færibreytur Commerce** og veldu **Kennisveitendur** í vinstri valmyndinni.
1. Undir **Kennisveitendur** gerirðu eftirfarandi:
    1. Í reitinn **Útgefandi** slærðu inn vefslóð útgefanda kennisveitanda. Til að finna slóð útgefanda skal sjá [Fá slóð útgefanda](#obtain-issuer-url) hér að neðan.
    1. Í reitinn **Heiti** skal færa inn heiti fyrir útgefendaskrána.
    1. Í reitnum **Gerð** slærðu inn **Azure AD B2C (id_token)**.
1. Undir **Treystandi aðilar**, með valinn hlut B2C kennisveitanda hér að ofan, gerðu eftirfarandi:
    1. Í reitinn **ClientID** slærðu inn B2C forritsauðkenni þitt. Þú getur fundið þetta í reitnum **Kenni forrits** á eiginleikasíðu B2C forritsins.
    1. Í reitnum **Gerð** slærðu inn **Opinbert**.
    1. Í reitnum **Notandagerð** slærðu inn **Viðskiptavinur**.
1. Í aðgerðaglugganum velurðu **Vista.**
1. Leitaðu að í leitarreitnum fyrir viðskipti **Númeraraðir** (Fyrirtækisstjórnun > Númeraraðir).
1. Í aðgerðarglugganum velurðu **Breyta** undir **Viðhalda**.
1. Á flýtiflipanum **Almennt** velurðu **Nei** fyrir **Handbók**.
1. Í aðgerðaglugganum velurðu **Vista.** 
1. Í leitarreit Commerce leitarðu að **Dreifingaráætlun**
1. Í vinstri valmyndinni á síðunni **Dreifingaráætlanir** velurðu vinnsluna **1110 altæk stilling**.
1. Í aðgerðarúðunni skal velja **Keyra núna**.

### <a name="obtain-issuer-url"></a>Fá slóð útgefanda

Fylgdu þessum skrefum til að fá vefslóð útgefanda kennisveitanda.

1. Búðu til veffang lýsigagna á eftirfarandi sniði með B2C leigjanda þínum og stefnu: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Dæmi: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Sláðu inn veffang lýsigagna í veffangastiku vafrans.
1. Í lýsigögnum, afritarðu veffang útgefanda kennisveitanda (gildið fyrir **"útgefandi"**).
    - Dæmi: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði

Þegar uppsetningu á Azure AD B2C leigjandi er lokið, þú verður að stilla B2C leigjanda í vefsvæðishönnuði Commerce. Stillingarþrepin fela í sér að safna upplýsingum um B2C umsóknir úr Azure-gáttinni, færa þær B2C forritaupplýsingar inn í vefsvæðishönnuð og tengja síðan B2C forritið við vefsvæðið og rás.

### <a name="collect-the-required-application-information"></a>Safnaðu nauðsynlegum upplýsingum um forritið

Fylgdu þessum skrefum til að safna nauðsynlegum forritsupplýsingum.

1. Í Azure gáttinni ferðu í **Heim \> Azure AD B2C - Forrit**.
1. Veldu forritið þitt og veldu síðan í vinstri glugganum **Eiginleikar** til að fá upplýsingar um forritið.
1. Úr reitnum **Kenni forrits**, safnaðu forritskenni B2C forritsins sem búið var til í B2C leigjanda þínum. Þetta verður síðar fært inn sem **GUID biðlara** í vefsvæðishönnuði.
1. Undir **Svarslóðinni**, safnarðu svarslóðum.
1. Farðu í **Heim \> Azure AD B2C - Notendastreymi (reglur)**, og safnaðu síðan nöfnum hverrar notendastreymisstefnu.

Eftirfarandi mynd sýnir dæmi um síðuna **Azure AD B2C - Forrit**.

![Farðu í B2C forritið í leigjanda þínum](./media/B2CImage_19.png)

Eftirfarandi mynd sýnir dæmi um forritasíðuna **Eiginleikar** í Azure AD B2C. 

![Afritaðu auðkenni forritsins úr eiginleikum B2C forritsins](./media/B2CImage_21.png)

Eftirfarandi mynd sýnir dæmi um reglur notendaflæðis á síðunni **Azure AD B2C - Notendastreymi (reglur)**.

![Safnaðu heitum á hverju B2C stefnuflæði](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>Sláðu inn forritsupplýsingar AAD B2C leigjanda inn í Commerce

Þú verður að slá inn upplýsingar um Azure AD B2C leigjandi í vefsvæðishönnuð Commerce áður en B2C leigjandi er tengdur við vefsvæðin þín.

Fylgdu þessum skrefum til að bæta forritsupplýsingum um AAD B2C leigjanda í Commerce.

1. Skráðu þig inn sem stjórnandi í vefsvæðishönnuði Commerce fyrir umhverfi þitt.
1. Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.
1. Undir **Leigjandastillingar** velurðu **B2C stillinngar**. 
1. Í aðalglugganum við hliðina á **B2C forrit**, veldu **Stjórna**. (Ef leigjandi þinn birtist í B2C forritalistanum var kerfisstjórinn þegar búinn að bæta honum við. Staðfestu að hlutirnir í skrefi 6 hér að neðan samsvari B2C forritinu þínu.)
1. Veljið **Bæta við B2C forriti**.
1. Sláðu inn eftirfarandi nauðsynlega hluti í glugganum sem birtist, með gildum úr B2C leigjanda þínum og forriti. Reitir sem ekki er krafist (þeir sem eru án stjörnu) kunna að vera auðir.

    - **Heiti forrits**: Heiti B2C forritsins, til dæmis „Fabrikam B2C“.
    - **Heiti leigjanda**: Heiti B2C leigjanda, til dæmis „Fabrikam“.
    - **Gleymdu auðkenni lykilorðsstefnu**: Notandastraumur fyrir gleymt lykilorð notendastreymis, til dæmis „B2C_1_PasswordReset“.
    - **Auðkenni kennsluskilríkja við innskráningu**: Auðkenni skráningar og innskráningarflæði notendastreymis, til dæmis „B2C_1_signup_signin“.
    - **GUID biðlara**: Auðkenni B2C forritsins, til dæmis „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.
    - **Breyta auðkenni prófílstefnu**: Auðkenni sniðs sem breytir notendastreymi, til dæmis „B2C_1A_ProfileEdit“.

1. Veljið **Í lagi**. Þú ættir nú að sjá nafn B2C forritsins þíns birtast á listanum.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Tengdu B2C forritið við síðuna þína og rás

> [!WARNING]
> Ef vefsvæðið þitt er nú þegar tengt B2C forriti, með því að breyta í annað B2C forrit, verður að fjarlægja núverandi tilvísanir sem settar hafa verið upp fyrir notendur sem þegar hafa skráð sig í þessu umhverfi. Ef það hefur breyst verða engin skilríki sem eru tengd B2C forritinu sem nú er úthlutað tiltæk fyrir notendur. 
> 
> Uppfærðu aðeins B2C forritið ef þú ert að setja upp B2C forrit rásarinnar í fyrsta skipti eða ef þú ætlar að láta notendur skrá sig með nýjum skilríkjum á þessa rás með nýju B2C forritinu. Gætið varúðar þegar rásir eru tengdar við B2C forrit og nafnið forrit greinilega. Ef rás er ekki tengd B2C forriti í skrefunum hér að neðan verða notendur sem skrá sig inn á þá rás fyrir síðuna þína færðir inn í B2C forritið sem birtist sem **sjálfgefið** í listanum **Leigjandastillingar \> B2C stillingar** yfir B2C forrit.

Til að tengja B2C forritið við síðuna þína og rás skaltu fylgja þessum skrefum.

1. Farðu á vefsvæðið í vefsvæðishönnuði Commerce.
1. Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.
1. Undir **Vefsvæðisstillingar** velurðu **Rásir**.
1. Í aðalglugganum undir **Rásir** velurðu rásina þína.
1. Veldu rásina fyrir rásina til hægri, veldu nafn B2C forritsins úr fellivalmyndinni **Velja B2C forrit**.
1. Veldu **Loka** og veldu síðan **Vista og birta**.

## <a name="additional-b2c-information"></a>Frekari B2C upplýsingar

### <a name="customer-migration"></a>Flutningur viðskiptavina

Ef þú ert að íhuga að flytja skrár viðskiptavina frá fyrri vettvangi fyrir persónuskilaboð, vinsamlegast vinndu með Dynamics 365 Commerce teymi til að fara yfir fólksflutningaþörf þína.

Fyrir aukaleg Azure AD B2C skjöl um flutning viðskiptavina, sjá [Flytja notendur til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Sérsniðnar stefnur

Fyrir frekari upplýsingar um sérsníða Azure AD B2C samskipti og stefnuflæði umfram það sem boðið er upp á við B2C stöðluðu stefnur, sjá [Sérsniðnar stefnur í Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Annar stjórnandi

Hægt er að bæta við valfrjálsum aukaforritareikningi í hlutanum **Notendur** af B2C leigjanda þínum. Þetta getur verið beinn reikningur eða almennur reikningur. Ef þú þarft að deila reikningi þvert á teymi, þá er einnig hægt að stofna sameiginlegan reikning. Vegna næmni gagnanna sem geymd eru í Azure AD B2C, ætti að fylgjast náið með sameiginlegum reikningi samkvæmt öryggisvenjum fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum slóðartilvísunum í einu](upload-bulk-redirects.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
