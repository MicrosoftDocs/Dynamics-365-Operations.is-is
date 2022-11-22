---
title: Öryggisstillingarhugtök fyrir sýndartöflusamþættingar
description: Þessi grein útskýrir arkitektúr til að byggja upp samþættingu milli Microsoft Dynamics 365 Human Resources og önnur kerfi.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759728"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Öryggisstillingarhugtök fyrir sýndartöflusamþættingar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir arkitektúr til að nota [Microsoft Dataverse sýndarborð (einingar)](/dev-itpro/power-platform/virtual-entities-overview) að byggja upp samþættingu á milli Dynamics 365 Human Resources og þriðja aðila kerfi. Áherslan í greininni er á öryggisstillingar og á auðkenningar- og heimildaþætti sem þarf á milli kerfismarka til að byggja upp virkt, öruggt kerfi.

## <a name="prerequisite-reference-articles"></a>Forkröfur tilvísunargreinar

Eftirfarandi greinar veita frekari upplýsingar um hugtökin í þessari grein:

- [Yfirlit sýndareininga](/dev-itpro/power-platform/virtual-entities-overview)
- [Byrjaðu með sýndarborðum (einingum)](/developer/data-platform/virtual-entities/get-started-ve)
- [Notaðu auðkenningu netþjóns til miðlara með mörgum leigjendum (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Notaðu OAuth auðkenningu með Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0 biðlaraskilríki streyma á Microsoft auðkennisvettvangi](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Sannvottun og heimild](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Högun 

Eftirfarandi byggingarskýringarmynd sýnir helstu hugtökin sem taka þátt í samþættingu sem notar sýndartöflur (einingar).

![Sýndartöflubundin samþætting.](./media/Hosts.jpg)

Hér er útskýring á sumum þáttunum í skýringarmyndinni á undan:

- **Microsoft** – Microsoft hýsir og rekur mismunandi Dynamics 365 vörur fyrir hönd viðskiptavina.

    - **Azure Active Directory(Azure AD) leigjandi C** — An Azure AD leigjanda sem er í eigu Microsoft. Það er leigjandinn sem Dynamics 365 forritin eru skráð í.

- **Samþættandi félagi**

    - **Samþættingarkerfi** – Kerfið sem verið er að samþætta Dynamics 365. Það gæti verið launakerfi eða hvaða kerfi sem er sem byggir á gögnum sem eru geymd í Dynamics 365.
    - **Millistykki** – Hugbúnaðurinn eða þjónustan sem ber ábyrgð á samskiptum við bæði Dynamics 365 og samþættingarkerfið.

        > [!NOTE]
        > Ef millistykki er ætlað að vera notað af mörgum Dynamics 365 viðskiptavinum er búist við að það verði skráð sem fjölleigjandi forrit í Azure AD.

    - **Azure AD leigjandi A** — An Azure AD leigjanda sem er í eigu samþættingaraðilans. Það er leigjandinn sem forritakenni millistykkisins er skráð á.

- **Gagnkvæmur viðskiptavinur** – Viðskiptavinur sem útfærir Dynamics 365 Human Resources og lausn samþættingaraðilans.

    - **Dynamics 365 Finance eða Human Resources** – Viðskiptasértækt tilvik Dynamics 365 Finance eða Human Resources sem inniheldur gögn viðskiptavina sem samþættingarkerfið krefst.
    - **Dataverse**– Viðskiptavinurinn Dataverse umhverfi sem er tengt annað hvort fjármálum eða mannauði. Dataverse býður upp á vefforritaskil fyrir samskipti við Dynamics 365 gögn.
    - **Azure AD leigjandi B** — viðskiptavinarins Azure AD leigjanda. Það virkar sem auðkennisveitandi (heimildarþjónn) og gefur út tákn sem heimila þeim sem hringja til að hringja í viðskiptavininn.Dataverse dæmi.

## <a name="basic-request-flow"></a>Grunnbeiðnaflæði

Þessi hluti lýsir grunnflæði dæmigerðrar beiðni sem tekur þátt í samþættingu. Það vísar til byggingarmyndarinnar fyrr í þessari grein.

Dæmigerð beiðni krefst þess að millistykkið biðji um Dynamics 365 eftir gögnum og visti síðan og samstillir þau gögn við samþættingarkerfið.

1. Millistykkið kallar á Dataverse Web API til að spyrjast fyrir um viðeigandi gögn.

    > [!NOTE]
    > Auðkenning er forsenda og öflun tákna er stór hluti af ferlinu. Auðkenningu verður lýst í [Auðkenning og heimild á kerfismörkum](#authentication-and-authorization-at-system-boundaries) kafla.

    Þetta ákall er beint gegn Dataverse Web API til að spyrjast fyrir um forritsgögn sem eru afhjúpuð í gegnum sýndartöflu. (Sjá „2. Upphafleg samstilling" og "3. Delta Sync" á skýringarmyndinni.)

2. Dataverse sér um beiðnina með því að spyrjast fyrir um sýndartöfluna í gegnum Virtual entity plugin ("Virtual Table Proxy" á skýringarmyndinni). The Dataverse beiðni er send til fjármála- eða mannauðsþjónustu sýndaraðila til að spyrjast fyrir um gögnin sem eru geymd líkamlega í gagnagrunni fjármála eða mannauðs.
3. Fjármála- eða mannauðsþjónusta sýndaraðila þýðir beiðnina gegn sýndaraðilanum yfir í fyrirspurn gegn fjármála- eða mannauðsaðilanum sem styður Dataverse sýndareining. Gögnin eru sótt úr gagnagrunninum, þýdd aftur í Dataverse framsetning aðila og skilað til þess sem hringir.
4. Millistykkið lýkur öllum nauðsynlegum kortlagningu og gagnaþýðingu og hringir í samþættingarkerfið til að halda gögnunum áfram í samþættingarkerfisgagnagrunninum. (Sjá „4. Vista gögn" á skýringarmyndinni.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Auðkenning og heimild á kerfismörkum

*Auðkenning* staðfestir að auðkenni notanda eða forrits hafi verið sannað og staðfestir að notandinn eða forritið sé sá sem þeir segjast vera. *Heimild* veitir notandanum eða forritinu rétt til að fá aðgang að sérstökum heimildum á forritastigi. Fyrir frekari upplýsingar, sjá [Auðkenning vs heimild](/azure/active-directory/develop/authentication-vs-authorization).

Flest krosskerfissímtöl í byggingarskýrslunni fyrr í þessari grein fela í sér millistykkið. Millistykkið verður að auðkenna sig til að hringja í eftirfarandi símtöl:

- Símtalið til Dataverse
- Símtalið til samþættingarkerfisins

Horfðu á kerfismörkin á skýringarmyndinni. Sérhver vefbeiðni milli kerfa verður að vera auðkennd og leyfispróf á forritastigi verða að standast áður en gögnum er skilað til þess sem hringir. Fyrir beiðni gegn Dynamics 365 sýndartöflu sem er studd af fjármálum eða mannauði, er auðkenningar- og heimildathugunum framfylgt við eftirfarandi kerfismörk:

- Símtalið milli millistykkisins og Dataverse Web API (OData) endapunktur
- Símtalið milli Dataverse Sýndareiningaviðbót og fjármála- eða mannauðsþjónusta sýndaraðila

Í báðum tilvikum eru auðkenningarathuganir gerðar fyrst. Síðan eru leyfisathuganir á forritastigi gerðar til að tryggja að auðkenndur notandi eða forrit hafi rétt forritsréttindi til að sækja umbeðin gögn.

Auðkenning til að hringja Dataverse er meðhöndlað í gegnum burðartákn sem verður að vera með sem HTTP haus í vefbeiðninni til Dataverse. Millistykkið verður að fá tákn frá leigjanda B Azure AD dæmi. (Sjá „1. Get Token" á skýringarmyndinni.)Azure AD virkar sem auðkennisveitandi í auðkenningarflæðinu.

Millistykkið sannvotir með því að gefa upp auðkenni forritsins (ekki leyndarmál, eins og það er skráð í Azure AD leigjanda A) og umsóknarleyndarmál eða vottorð sem aðeins millistykkisforritið hefur.

Eftir að notandi eða forrit hefur verið auðkennt til að hringja til Dataverse, hinn Dataverse -Leyfiprófanir eru gerðar gegn hverri beiðni. Þessar athuganir ganga úr skugga um að sá sem hringir (auðkenni millistykkisins, sem er merkt "\<guid A\> " á skýringarmyndinni) hefur viðeigandi forritsheimildir. Heimild á umsóknarstigi er stjórnað í Dataverse í gegnum forritanotanda sem táknar forritakenni millistykkisins. Heimildum á umsóknarstigi er stjórnað með því að veita aðgang að sérstökum Dataverse -skilgreint umsóknarhlutverk. Þessi hlutverk veita umsókninni nákvæm réttindi.

Fyrir ítarlegri leiðbeiningar, sjá [Notaðu auðkenningu frá miðlara til miðlara með mörgum leigjendum](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Ef Dataverse Athuganir á leyfisveitingu forrita á stigi eru samþykktar, Virtual entity plugin hringir í Virtual entity þjónustu endapunktinn í Finance eða Human Resources umhverfinu. Auðkenning netþjóns til netþjóns (S2S) er notuð til að hringja þetta símtal. Það notar auðkenni og leyndarmál sem eru stillt í stillingarskránni Finance and Operations sýndargagnagjafa.

![Finance and Operations stillingarskrá sýndargagnagjafa í sandkassaumhverfinu.](./media/sandbox.jpg)

Fyrir frekari upplýsingar, sjá [Stilla Dataverse sýndareiningar](/dev-itpro/power-platform/admin-reference).

Símtalið frá Dataverse Sýndareiningaviðbót við Finance eða Human Resources inniheldur millistykkisauðkenni upprunalega símtalsins til Dataverse frá millistykkinu (auðkennið sem er tilgreint "\<guid A\> " í byggingarmyndinni). Ef sýndareiningargagnagjafinn er rétt stilltur og S2S auðkenningarprófanir eru staðnar, mun sýndaraðilaþjónustan í Finance eða Human Resources keyra fyrirspurnina í samhengi við upphaflega hringjandann (millistykkið,\<guid A\>). Forritsheimildaathuganir (heimild) á fjármála- eða mannauðsstigi verða gerðar til að tryggja að millistykkið hafi þau réttindi sem þarf til að fá aðgang að gagnaeiningunum sem beðið er um í gegnum fyrirspurnina.

Fjármála- og mannauðsöryggi er stýrt á eftirfarandi hátt:

1. Með því að kortleggja auðkenni millistykkisins (\<guid A\>) til tiltekins fjármála- eða mannauðsnotanda. Þessi kortlagning er gerð á **Azure active directory forrit** síðu. Fyrir frekari upplýsingar, sjá [Skráðu ytri umsókn þína](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Með því að veita fjármála- eða mannauðsnotandanum viðeigandi hlutverk, skyldur og réttindi á forritastigi. Fyrir frekari upplýsingar, sjá [Hlutverkamiðað öryggi](/dev-itpro/sysadmin/role-based-security).

Ef millistykkisforritið (\<guid A\>) er veitt þau réttindi sem nauðsynleg eru til að fá aðgang að umbeðnum gögnum, eiga sér stað eftirfarandi atburðir:

1. Fyrirspurnin er keyrð.
2. Gögnin eru þýdd aftur til þess Dataverse aðila síðu.
3. Gögnin eru skilað til millistykkisins.

> [!IMPORTANT]
> Meðan á þróun stendur er hægt að keyra millistykkið með því að nota Finance eða Human Resources notanda sem hefur stjórnandahlutverkið. Hins vegar, í framleiðsluumhverfi, ætti millistykkið aldrei að vera keyrt með stjórnandaréttindi.

## <a name="key-takeaways"></a>Helstu veitingar

Hér eru nokkrar mikilvægar afleiðingar sýndarborðsins eða einingaarkitektúrsins:

- Öryggisstillingu fyrir sýndartöflur sem eru studdar af Human Resources er stjórnað í Human Resources.
- Viðskiptavinurinn ("Gagnkvæmur viðskiptavinur" í byggingarskýrslunni fyrr í þessari grein) hefur fulla stjórn á því hvaða forréttindi eru veitt samþættingarauðkenni millistykkisins (tilnefnd "\<guid A\> " á skýringarmyndinni).
- Viðskiptavinurinn ber ábyrgð á réttri öryggisuppsetningu á mannauðsumhverfi sínu. Samþættingaraðilinn sem býr til millistykkið verður að veita leiðbeiningar um þau réttindi sem millistykkið krefst.
