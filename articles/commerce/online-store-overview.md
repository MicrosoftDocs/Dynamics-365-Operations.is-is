---
title: Yfirlit yfir svæði fyrir rafræn viðskipti
description: Þetta efnisatriði veitir yfirlit yfir stuðning fyrir svæði fyrir rafræn viðskipti í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a5ced6311f32405e544e66d18c912ce40deb177f
ms.sourcegitcommit: 33a746e41cd6f7b6b056b19b550a84f6a1b905d4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/12/2020
ms.locfileid: "4512918"
---
# <a name="e-commerce-site-overview"></a>Yfirlit yfir svæði fyrir rafræn viðskipti

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir stuðning fyrir svæði fyrir rafræn viðskipti í Microsoft Dynamics 365 Commerce. Þar eru upplýsingar um það hvernig netverslanir eru frumstilltar og meðhöndlaðar í Dynamics 365 Commerce. Þar er einnig að finna tengla á frekari upplýsingar um netverslanir og um hvernig á að setja upp og grunnstilla svæði fyrir rafræn viðskipti. Þetta efnisatriði nær yfir mörg grunnatriði en fjallar ekki um öll áskilin atriði varðandi uppsetningu svæðis fyrir rafræn viðskipti. Ítarlegri efnisatriði má finna í fylgiskjölum Dynamics 365 Commerce.

## <a name="online-store-channel"></a>Rás netverslunar

Áður en hægt er að búa til svæði í Dynamics 365 Commerce þarf að setja upp að minnsta kosti eina netverslunarrás. Frekari upplýsingar er að finna í [Setja upp netrás](channel-setup-online.md). 

Í Dynamics 365 Commerce notar þú netverslunarrás til að koma á fót afurðum, verðlagningu, tungumálum, greiðslumátum, afhendingarmátum, uppfyllingavinnustöðvar og öðrum þáttum í netversluninni sem ættu að vera aðgengilegir viðskiptavinum.

Aðeins er hægt að setja upp eina netverslunarrás áður en hafist er handa við Dynamics 365 Commerce. Hins vegar getur eitt svæði fyrir rafræn viðskipti sýnt margar netverslanir. Ef margar netverslanir eru til dæmis settar upp til að styðja við ólík landsvæði er hægt að nota eitt sett af síðum fyrir rafræn viðskipti til að veita upplifanir sem eru skilgreindar með hverri verslun fyrir sig. Nánari upplýsingar um hvernig á að stilla vefsíðu til að styðja margar netverslanir er að finna í [Tengja netsvæði við rás](associate-site-online-store.md).

Eftir að netverslun hefur verið sett upp er hægt að tengja hana við Dynamics 365 Commerce-vefsvæði sem mun þjóna sem netverslun þín. Nánari upplýsingar um netverslanir og hvernig á að setja þær upp er að finna í [Setja upp netverslanir](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Uppsetning á nýjum leigjanda rafrænna viðskipta

Við ræsingu á svæði fyrir rafræn viðskipti er beðið um lénsheiti. Frekari upplýsingar um lén í Commerce er að finna í [Skilgreina lénsheiti](configure-your-domain-name.md) og [Lén í Dynamics 365 Commerce](domains-commerce.md). Þegar setja á upp nýjan leigjanda rafrænna viðskipta með [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) skal fylgja skrefunum í [Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md). Þegar lokið er við að setja upp nýjan leigjanda rafrænna viðskipta, verður tengill útvegaður á Commerce Site Builder. Síðan er hægt að nota Commerce Site Builder til að frumstilla og grunnstilla svæði fyrir rafræn viðskipti.

## <a name="initialize-your-e-commerce-site"></a>Ræsa svæðið þitt fyrir rafræn viðskipti

Þegar þú ræsir Commerce Site Builder í LCS birtist vefsíðan **Svæði** um leið. Á þessari síðu birtast tvö forstillt vefsvæði, **sjálfgefið** og **Fabrikam** eins og sýnt er í dæminu á skýringarmyndinni hér á eftir.

![Svæðasíða í Commerce Site Builder](media/e-commerce-site-01.png)

Þegar eitt af þessum svæðum er valið er beðið um að velja lénsheiti, sjálfgefna netverslunarrás, studd tungumál fyrir valda rás og vefslóð. Hægt er að hafa vefslóðina auða ef aðeins ein rás er notuð. Hægt er að skilgreina fleiri netverslunarrásir eða tungumál síðar í Commerce Site Builder. Hver viðbótarleið eða tungumál mun krefjast einkvæmrar slóðar. Til dæmis eru netrásir tengdar við eitt svæði og lénsheitið fyrir svæðið er `www.fabrikam.com`. Í slíku tilviki getur vefslóð einnar rásarinnar verið sjálfgefna gildið sem hefur enga vefslóð (`https://www.fabrikam.com`) og seinni rásina er hægt að stilla á nýja vefslóð eins og **site2** með vefslóðina `https://www.fabrikam.com/site2`. Á eftirfarandi skýringarmynd er sýnt dæmi um svarglugga ræsingar vefsvæðis í Commerce Site Builder.

![Svargluggi ræsingar vefsvæðis í Commerce Site Builder.](media/e-commerce-site-02.png)

Síðan **Svæði** inniheldur einnig hnappinn **Nýtt vefsvæði**. Svarglugginn sem birtist þegar þessi hnappur er valinn líkjast svarglugga fyrir frumstillingu vefsvæðis, en hann er notaður til að búa til nýtt svæði. Nýjar síður eru auðar. Þær innihalda ekki sömu sjálfgefnu sniðmátin, brotin, síðurnar og myndirnar sem fylgja **sjálfgefnu** og **Fabrikam** svæðunum. Hins vegar getur þú opnað þjónustubeiðni eftir þörfum til að óska eftir viðbót af afriti sjálfgefins efnis við nýtt autt svæði. Frekari upplýsingar eru í [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md).

Eftir að nýtt svæði er frumstillt opnast **Heimasíða** Commerce Page Builder. Þessi síða innheldur tengla á algengar aðgerðir og leiðbeiningar eins og kemur fram í dæminu á skýringarmyndinni hér á eftir.

![Tenglar á heimasíðu í Commerce Site Builder](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Breyta netverslunarrásum eða bæta netverslunarrásum við vefsvæði í e-Commerce

Þegar búið er að stofna svæði fyrir rafræn viðskipti er hægt að breyta rásinni sem henni tengist með því að fylgja eftirfarandi skrefum í [Tengja svæði rafrænna viðskipta við netrás](associate-site-online-store.md). Dæmið sem kemur fram á skýringarmyndinni hér á eftir sýnir hvernig hægt er að breyta númeri sjálfgefinnar rásar rekstrareiningar (OUN) á síðunni **Rás** (**Stillingar vefsvæðis \> Rásir**). Þegar búið er að gera breytingu skal ganga úr skugga um að velja **Vista og birta**. Á þennan hátt er tryggt að breytingin birtist.

![Rásarsíða í Commerce Site Builder](media/e-commerce-site-04.png)

Hægt er að bæta við nýjum rásum með því að velja **Bæta við rás**. Til að bæta nýjum tungumálum við rásina skal velja rásina og síðan velja **Bæta við stað** í svarglugganum sem birtist. Áður en staðir geta birst í svarglugganum verða þeir að vera forskilgreindir fyrir netverslunarrásina í Commerce Headquarters.

![Svargluggi rásar í Commerce Site Builder](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Setja upp Azure B2C-leigjanda

Dynamics 365 Commerce notar Azure Active Directory (Azure AD) fyrirtæki-til-neytenda (B2C) til að styðja notandaskilríki og sannvottunarflæði. Frekari upplýsingar um hvernig á að setja upp Azure B2C leigjandann er að finna í [Setja upp B2C leigjanda í Commerce](set-up-b2c-tenant.md), [Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md) og [Skilgreina marga B2C leigjendur í Commerce-umhverfi](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Yfirlit yfir sjálfgefnar síður

Bæði **sjálfgefnu** og **Fabrikam** svæðin innihalda forstillt sniðmát, brot og síður til að hjálpa þér við að hefjast handa. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Yfirlit heimasíðu](quick-tour-home-page.md)
- [Yfirlit upplýsingasíðu afurða](quick-tour-pdp.md)
- [Yfirlit yfir síður körfu og greiðsluferlis](quick-tour-cart-checkout.md)
- [Yfirlit yfir síður fyrir stjórnun reikninga](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Stjórna stillingum svæðis

Nánari upplýsingar um hvernig á að stjórna stillingum svæðis er að finna í eftirfarandi efnisatriðum:

- [Stjórna notendum og hlutverkum rafrænna viðskipta](manage-ecommerce-users-roles.md)
- [Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt](/search-engine-optimization-considerations.md)
- [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md)
- [Velja þema svæðis](select-site-theme.md)

## <a name="manage-site-content"></a>Stjórna efni svæðis

Nánari upplýsingar um hvernig á að stjórna efni svæðis er að finna í eftirfarandi efnisatriðum:

- [Orðalisti síðulíkans](page-elements-overview.md)
- [Staða og líftími skjala](document-states-overview.md)
- [Sniðmát og útlit](templates-layouts-overview.md)
- [Vinna með brot](work-with-fragments.md)
- [Vinna með einingar](work-with-modules.md)
- [Yfirlit stjórnunar stafrænna eigna](dam-overview.md)
- [Yfirlit einingasafns](starter-kit-overview.md)

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)
