---
title: Setja upp sérsniðnar síður fyrir innskráningu notenda
description: Þessi grein lýsir því hvernig á að byggja sérsniðnar síður inn Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur á Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c610866b896ef7648d2596e17b51d1935a78dee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880341"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Setja upp sérsniðnar síður fyrir innskráningu notenda

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að byggja sérsniðnar síður inn Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur á Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).

Til að nota sérsniðnar síður sem eru gerðar í Dynamics 365 Commerce til að takast á við innskráningarflæði notenda verður þú að setja upp Azure AD stefnu sem vísað verður til í viðskiptaumhverfi. Þú getur stillt „Skráning og innskráning“, „Forstillingum breytt“ og „Aðgangsorð endurstillt“ Azure AD B2C stefnur með því að nota Azure AD B2C forrit. Síðan er hægt að vísa til Azure AD B2C leigjanda og stefnuheita við útvegunarferlið sem er gert fyrir viðskiptaumhverfið með því að nota Microsoft Dynamics Lifecycle Services (LCS).

Hægt er að smíða sérsniðnar viðskiptasíður með því að nota innskráningu, skráningu, breytingu reikningssniðs, endurstillingu lykilorðs eða almennar AAD-einingar. Síðan ætti að vísa í vefslóðir síðunnar sem eru birtar fyrir þessar sérsniðnu síður Azure AD B2C stefnuskilgreiningar í Azure gáttinni.

> [!WARNING] 
> Azure AD B2C mun hætta í gamla (eldra) notandaflæði frá 1. ágúst, 2021. Því ætti að áforma að yfirfæra notandaflæðin í nýju ráðlögðu útgáfuna. Nýja útgáfan býður upp á jafngilda eiginleika og nýja eiginleika.. Frekari upplýsingar eru í [Notandaflæði í Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).

>Einingasafnið fyrir Commerce-útgáfu 10.0.15 eða nýrri ætti að nota með ráðlögðum B2C-notandaflæðum. Einnig er hægt að nota sjálfgefnar síður um notandareglur sem boðið er upp á í Azure AD B2C og leyfa auknar breytingar á bakgrunnsmynd, lógói og bakgrunnslit sem tengjast vörumerki fyrirtækis. Þótt hönnunarmöguleikarnir séu takmarkaðri bjóða sjálfgefnar síður um notandareglur upp á regluvirkni Azure AD B2C án þess að búa til eða skilgreina sérstakar sérstilltar síður. 

## <a name="set-up-b2c-policies"></a>Setja upp B2C reglur

Eftir að þú hefur sett upp þinn Azure AD B2C leigjanda og tengt hann við viðskiptaumhverfi þitt ferðu á síðuna **Azure AD B2C** í Azure gáttinni og síðan á valmyndinni undir **Stefnur** velurðu **Notendastreymi (reglur)**.

![Skipunin Notandaflæði (stefna) í valmyndinni.](./media/B2C_CustomPage_PoliciesMenu.png)

Þú getur nú stillt innskráninguna "Skráðu þig inn og skráðu þig inn", "Prófíklippingu" og "Lykilorð endurstillt" innskráningarflæði notenda.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Stilla stefnuna „Skráning og innskráning“

Fylgdu þessum skrefum til að stilla stefnuna „Skráning og innskráning“.

1. Veldu **Nýtt notendaflæði** og síðan í flipanum **Skráning og innskráning** velurðu flipann **Ráðlagt** og síðan **Stofna**.
1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_SignInSignUp**).
1. Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna. Að lágmarki verður **Innskráning í gegnum tölvupóst** að vera valin.
1. Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netfang**, **Fornafn** og **Eftirnafn**.
1. Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.

    ![Eigindir og kröfur valdar.](./media/B2C_SignInSignUp_Attributes.png)

1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

    ![Eiginleikasíða fyrir nýju regluna.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Vísað verður að fullu til heitis reglunnar í viðskiptaumhverfi. (Forskeytið **B2C\_1\_** verður með í tilvísuninni.) Ekki er hægt að endurnefna reglur eftir að þær eru búnar til. Ef þú ert að skipta út núverandi reglu fyrir viðskiptaumhverfi þitt geturðu eytt upprunalegu reglunni og byggt upp nýja reglu með sama heiti. Að öðrum kosti, ef umhverfið hefur þegar verið útvegað, geturðu sent nýja regluheitið í gegnum þjónustubeiðni.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

### <a name="configure-the-profile-editing-policy"></a>Stilla regluna „Forstillingum breytt“

Til að skilgreina regluna „Forstillingum breytt“ skal fylgja þessum skrefum.

1. Veldu **Nýtt notendaflæði** og síðan í flipanum **Breyting prófíls** skaltu velja flipann **Ráðlagt** og síðan velja **Stofna**.
1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_EditProfile**).
1. Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna. Að lágmarki verður **Innskráning á staðbundin reikning** að vera valin.
1. Í dálknum **Innheimtueigind** skaltu velja gátreitina fyrir **Fornafn** og **Eftirnafn**.
1. Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.
1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

### <a name="configure-the-password-reset-policy"></a>Stilltu regluna „Núllstilla lykilorð“

Til að skilgreina regluna „Aðgangsorð endurstillt“ skal fylgja þessum skrefum.

1. Veldu **Nýtt notendaflæði** og því næst valkostinn **Endurstilling aðgangsorðs** og veldu flipann **Ráðlagt** og smelltu á **Stofna**.
1. Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_ForgetPassword**).
1. Í hlutanum **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.
1. Í dálknum **Skilakrafa** velurðu gátreitina fyrir **Netföng**, **Fornafn**, **Eftirnafn** og **Hlutakenni notanda**.
1. Velja skal **Í lagi** til að stofna regluna.
1. Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.
1. Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.

Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður. Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.

## <a name="build-the-custom-pages"></a>Smíða sérsniðnar síður

Sérstakar Azure AD einingar eru innifaldar í Commerce til að smíða sérstilltar síður fyrir notandareglur Azure AD B2C. Hægt er að smíða síður sérstaklega fyrir hvert útlit af síðu yfir notandareglur með því að nota aðaleiningar Azure AD B2C sem lýst er hér að neðan. Einnig er hægt að nota eininguna **AAD almennt** fyrir öllu síðuútlit og reglur í Azure AD B2C (jafnvel fyrir valkosti síðuútlits innan reglna sem ekki eru gefnar upp hér að neðan). 

- Síðubundnar Azure AD einingar eru bundnar við atriði gagnainnsláttar sem sett eru fram af Azure AD B2C. Þessar einingar veita notendum meiri stjórn á því hvar hægt að staðsetja einingar á síðunum þeirra. Hins vegar kann að þurfa að smíða fleiri síður og viðbætur eininga til að gera grein fyrir frávikum sem eru utan við sjálfgefnu stillingarnar sem lýst er hér að neðan.
- Einingin **AAD almennt** býr til „div“-eininguna fyrir Azure AD B2C til að setja fram allar einingar í útliti á síðu fyrir notandareglur, sem gefur B2C-aðgerðum á síðunni aukinn sveigjanleika en minni stjórnun á staðsetningu og stílmótun (þótt hægt sé að nota CSS til að passa við útlit og yfirbragð svæðisins).

Þú getur búið til eina síðu með einingunni **AAD almennt** og notað hana fyrir allar síður yfir notandareglur eða hægt er að smíða ákveðnar síður með því að nota stakar Azure AD einingar fyrir innskráningu, skráningu, breytingu á prófíl, endurstillingu aðgangsorðs og staðfestingu á endurstillingu aðgangsorðs. Einni er hægt að nota blöndu af bæði, nota tilteknu Azure AD síðurnar fyrir síðuútlitin sem minnst er á hér að neðan og almennu AAD-einingasíðuna fyrir eftirstandandi síðuútlit innan þessara eða annarra síða fyrir notandareglur.

Frekari upplýsingar um Azure AD einingarnar sem fylgja einingasafninu er að finna í [Síður og einingar fyrir auðkennisstjórnun](identity-mgmt-modules.md).

Til að smíða sérstilltar síður með ákveðnum auðkenniseiningum til að sjá innskráningar notenda skal fylgja þessum skrefum.

1. Opnaðu síðuna þína á svæðissmið Commerce.
1. Búðu til eftirfarandi fimm sniðmát og síður (ef þau eru ekki þegar til staðar á vefsvæðinu þínu):
    - Sniðmát og síðu **Innskráningar** sem nota innskráningareininguna.
    - Sniðmát og síðu **Nýskráningar** sem nota nýskráningareininguna.
    - Sniðmátið **Aðgangsorð endurstillt** og síðu sem notar eininguna aðgangsorð endurstillt.
    - Sniðmátið **Staðfesting á endurstillingu aðgangsorðs** og síðu sem notar eininguna staðfesting á endurstillingu aðgangsorðs.
    - Sniðmátið **Forstillingum breytt** og síðu sem notar eininguna lykilforstillingum breytt.

Fylgdu þessum leiðbeiningum þegar þú smíðar síðurnar:

- Notaðu útlit og stíl fyrir hverja síðu eða einingu sem hentar best viðskiptaþörfum þínum.
- Birtu allar síður og vefslóðir sem þarf að nota í uppsetningu Azure AD B2C.
- Eftir að síðurnar og vefslóðirnar eru birtar safnarðu vefslóðum sem verður að nota fyrir regluskilgreiningar Azure AD B2C. Viðskeytinu **?preloadscripts=true** verður bætt við hverja vefslóð þegar það er notað.

> [!IMPORTANT]
> Síður sem eru smíðaðar til að vera vísað á í Azure AD B2C eru þjónustaðar beint úr léni leigjanda Azure AD B2C. Ekki endurnýta altæka síðuhausa og síðufætur sem eru með afstæða tengla. Vegna þess að þessar síður verða hýstar í Azure AD B2C lén þegar þau eru notuð, aðeins hreinar vefslóðir ættu að nota fyrir alla tengla. Mælt er með því að búa til ákveðinn síðuhaus og síðufót með nákvæmum slóðum fyrir sérstilltar síður sem tengjast Azure AD með einhverjum einingum sem tengjast Commerce sem krefjast þess að tenging við Retail Server verði fjarlægð. Til dæmis ættu einingar fyrir eftirlæti, leitarstiku, innskráningartengil og körfu ekki að vera hafðar með á síðum sem verða notaðar í notandaflæði Azure AD B2C.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Stilla Azure AD B2C reglur með sérsniðnum síðuupplýsingum 

Farðu aftur í Azure gáttina á síðuna **Azure AD B2C** og síðan, á valmyndinni undir **Reglur**, velurðu **Notendastreymi (reglur)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Uppfærðu regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Skráning og innskráning** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Samræmd skráningar- eða innskráningarsíða**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla innskráningarslóðina. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits** skal velja útgáfu **2.1.0** eða nýrri (krefst einingasafns fyrir Commerce-útgáfu 10.0.15 eða nýrri).
1. Veljið **Vista**.
1. Veldu útlitið **Skráningarsíða staðbundins reiknings**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla skráningarslóðina. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits** skal velja útgáfu **2.1.0** eða nýrri (krefst einingasafns fyrir Commerce-útgáfu 10.0.15 eða nýrri).
1. Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:
    1. Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.
    1. Fyrir eigindina **Netfang** er mælt með að halda sjálfgefna gildinu **Já** völdu í dálknum **Krefst staðfestingar**. Þessi valkostur tryggir að notendur sem skrá sig með tilteknu netfangi staðfesta að þeir eigi netfangið.
    1. Fyrir eigindirnar **Netfang**, **Fornafn** og **Eftirnafn** skaltu velja **Nei** í dálknum **Valfrjálst**.
1. Veldu **Vista**.

    ![Stillingar reglu fyrir skráningarsíðu staðbundinna reikninga.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Uppfærðu regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Forstillingum breytt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Síða forstillingabreytingar** (gæti þurft að fletta niður og framhjá öðrum útlitsmöguleikum, fer eftir skjánum).
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að breyta forstillingum. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Fyrir **Útgáfa síðuútlits** skal velja útgáfu **2.1.0** eða nýrri (krefst einingasafns fyrir Commerce-útgáfu 10.0.15 eða nýrri).
1. Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:
    1. Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í dálknum **Valfrjálst**.
    1. Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.
1. Veljið **Vista**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Uppfærðu regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum

Til að uppfæra regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.

1. Í reglunni **Aðgangsorð endurstillt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.
1. Veldu útlitið **Síða gleymds aðgangsorðs**.
1. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
1. Í reitinn **Sérsniðin URI** slærðu inn alla stafestingarslóðina fyrir endurstillt aðgangsorð. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Í reitnum **Útgáfa síðuútlits** skal velja útgáfu **2.1.0** eða nýrri (krefst einingasafns fyrir Commerce-útgáfu 10.0.15 eða nýrri).
2. Veljið **Vista**.
3. Veldu útlitið **Síða fyrir breytt aðgangsorð**.
4. Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.
5. Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að endurstilla aðgangsorð. Hafðu viðskeytið **?preloadscripts=true** með. Til dæmis er slegið inn ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Í reitnum **Útgáfa síðuútlits** skal velja útgáfu **2.1.0** eða nýrri (krefst einingasafns fyrir Commerce-útgáfu 10.0.15 eða nýrri).
7. Veljið **Vista**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Sérsníða sjálfgefna textastrengi fyrir merki og lýsingar

Í einingasafninu eru innskráningareiningar forfylltar með sjálfgefnum textastrengjum fyrir merki og lýsingu. Hægt er að sérstilla strengina í eiginleikaglugga einingarinnar sem unnið er í. Fleiri strengir á síðunni (eins og textinn **Gleymdirðu aðgangsorðinu?** fyrir tengil eða textinn **Stofna reikning** sem kallar eftir aðgerð) krefjast þess að hugbúnaðarþróunarsett Commerce (SDK) verði notað og gildin í global.json-skránni verði uppfært fyrir innskráningareininguna.

Til dæmis er sjálfgefinn texti fyrir tengilinn sem gleymdist lykilorð **Gleymt lykilorð?**. Eftirfarandi sýnir þennan sjálfgefna texta á innskráningarsíðunni.

![Sjálfgefinn texti fyrir tengilinn við gleymt lykilorð á innskráningarsíðunni.](./media/B2C_SignUp_ModuleFace.png)

Í global.json skrá fyrir innskráningareiningu einingasafnsins er hægt að breyta textanum í **Manstu ekki aðgangsorðið?** eins og sýnt er á eftirfarandi teikningu.

![Uppfærður tenglatexti í global.json skránni í einingunni.](./media/B2C_CustomizingStringsForModule.png)

Þegar búið er að uppfæra global.json-skrá og birta breytingarnar birtist nýr tengill í innskráningareiningunni í bæði verslun og á innskráningarsíðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]