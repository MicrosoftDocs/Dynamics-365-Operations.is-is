---
title: Stilla marga B2C leigjendur í viðskiptaumhverfi
description: Þetta efni lýsir því hvenær og hvernig á að setja upp margar á rás Microsoft Azure Active Directory (Azure AD) viðskipti til neytenda (B2C) leigjendur fyrir auðkenningu notenda í sérhæfðu umhverfi Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6ca48badbe15b7e1bf543716a9b0e3da31477a20
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096510"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Stilla marga B2C leigjendur í viðskiptaumhverfi

[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvenær og hvernig á að setja upp margar á rás Microsoft Azure Active Directory (Azure AD) viðskipti til neytenda (B2C) leigjendur fyrir auðkenningu notenda í sérhæfðu umhverfi Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce notar Azure AD B2C skýjaeiningarþjónusta til að styðja skilríki notenda og auðkenningarflæði. Notendur geta notað auðkenningarflæðin til að skrá sig, skrá sig inn og endurstilla lykilorð sitt. Azure AD B2C geymir viðkvæmar sannvottunarupplýsingar notanda, svo sem notandanafn og lykilorð. Notendaskráin er einstök fyrir hvern B2C leigjanda og hún notar annað hvort notendanafn (netfang) eða persónuskilríki.

Í flestum tilvikum einn Azure AD B2C leigjandi er notaður í viðskiptaumhverfi. Viðskiptavinir geta síðan búið til og birt margar síður í sama viðskiptaumhverfi og sömu persónuskilríki viðskiptavina verða notuð á þessum vefsvæðum. Ef hins vegar ætti að meðhöndla vefsvæðin í umhverfinu sem mismunandi tegundir og birtast notendum sem aðskild fyrirtæki, er hægt að stilla B2C leigjanda fyrir rásina sem er notuð við aðskilnað vefsins/vörumerkisins.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Til athugunar þegar margir B2C leigjendur eru settir upp á hverja rás

Oft, þegar hver rás eða síða er meðhöndluð sem sérstök viðskipti, er besti kosturinn varðandi auðkenningu notenda í viðskiptum að nota aðskilda lögaðila. Hins vegar, ef þú vilt halda hverri rás/vefsvæði í sama umhverfi og lögaðilum, en vilt hafa sérstaka auðkenningu notenda fyrir hverja síðu, þá er það mikilvægt að þú lítur á eftirfarandi atriði áður en þú heldur áfram:

- Notendur munu hafa sín sérstöku persónuskilríki fyrir hverja rás/vefsíðu.

    Sami einstaklingur getur haft tvo aðskilda reikninga á hverri rás/vefsvæði, vegna þess að hver reikningur verður einstök færsla í sérstakan B2C leigjanda.

- Í umhverfi Microsoft Dynamics verður aðskildum viðskiptamannaskrám skilað fyrir altæka skráaleit.

    Ef notandi notar sama netfang á rásir/vefsvæði mun altæk leit viðskiptavina skila niðurstöðum fyrir hverja rás/síðu. (Rásavísir verður sýndur.)

- Hægt er að nota veffangaskrána til að hjálpa hópnotendum, svo hægt sé að rekja þá á hverri rás.
- Fjöldi skráningar viðskiptavina á hverja rás gæti aukist og þessi aukning gæti haft áhrif á árangur altækrar leitar viðskiptavina.
- Leigja verður B2C leigjendur að rás til að koma í veg fyrir aðstæður þar sem viðskiptavinir skrá sig í rangan leigjanda. Annars geta rugl eða rekja vandamál komið upp.

Eftirfarandi mynd sýnir marga B2C leigjendur í viðskiptaumhverfi.

![Margir B2C leigjendur í viðskiptaumhverfi](media/MultiB2C_In_Environment.png)

Ef þú ákveður að fyrirtæki þitt þurfi sérstaka B2C leigjendur á hverja rás í sama viðskiptaumhverfi skaltu ljúka verklagsreglunum í eftirfarandi hlutum til að biðja um þennan eiginleika.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Biðja um að B2C á hverja rás verði virkt í umhverfi þínu

Eins og er, ef þú vilt að sérstakir B2C leigjendur á hvern rás séu tiltækir í sama viðskiptaumhverfi, verður þú að leggja fram beiðni til Dynamics 365 Commerce. Fyrir frekari upplýsingar, sjá [Fáðu stuðning við Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), eða ræddu þetta mál með tengiliðnum þínum um viðskiptalausnir.

## <a name="configure-b2c-tenants-in-your-environment"></a>Stilla B2C leigjendur í umhverfi þínu

Til að stilla B2C leigjendur í umhverfi þínu skaltu ljúka viðeigandi verklagsreglum í þessum kafla.

### <a name="add-an-azure-ad-b2c-tenant"></a>Bættu við Azure AD B2C leigjanda

Til að bæta við Azure AD B2C leigjanda að umhverfi þínu, fylgdu þessum skrefum.

1. Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.
1. Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.
1. Smellið á **B2C-stillingar** og veljið síðan **Stjórna**.
1. Velja skal **Bæta við B2C-forriti** og færið síðan inn eftirfarandi upplýsingar:

    - **Heiti umsóknar**: Sláðu inn nafnið sem ætti að nota fyrir forritið í tengslum við stjórnun þess í verslun. Við mælum með að þú notir heiti forritsins sem þú valdir þegar þú settir upp Azure AD B2C forrit í Azure vefsíðunni. Á þennan hátt getur þú hjálpað til við að draga úr rugli þegar þú stjórnar B2C leigjendum í verslun.
    - **Nafn leigjanda**: Sláðu inn B2C leigjanda nafn eins og það birtist í Azure vefsíðunni.
    - **Gleymdu auðkenni lykilorðsstefnu**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).
    - **Reglukenni skráningar og innskráningar**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).
    - **GUID biðlara**: Sláðu inn Azure AD B2C leigjandaauðkenni eins og það birtist í Azure vefsíðunni (ekki forritsauðkenni B2C leigjanda).
    - **Breyta auðkenni forstillingarreglu**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).

1. Þegar þú hefur lokið við að slá inn þessar upplýsingar skaltu velja **Í lagi** til að vista breytingarnar.

> [!NOTE]
> Þú ættir að hafa reiti eins og **Umfang**, **Ógagnvirk reglukenni**, **Ógagnvirk biðlarakenni**, **Sérstillt lén innskráninga** og **Reglukenni skráningar** auða nema teymi Dynamics 365 Commerce leiðbeini þér að stilla þá.
Nýi Azure AD B2C-leigjandinn ætti nú að birtast á listanum undir **Stjórna B2C forritum**.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Hafa umsjón með eða eyða Azure AD B2C-leigjanda

1. Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.
1. Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.
1. Smellið á **B2C-stillingar** og veljið síðan **Stjórna**.
1. Veldu blýantstáknið við hliðina til að breyta B2C leigjanda. Til að eyða B2C leigjanda skaltu velja ruslatunnutáknið við hliðina.
1. Veldu **Vista** og veldu síðan **Birta** til að virkja breytingarnar þínar.

> [!WARNING]
> Þegar leigjandi B2C er stilltur fyrir lifandi/birta síðu gætu notendur skráð sig með því að nota reikninga sem eru til staðar á leigjandanum. Ef þú eyðir stillta leigjanda í valmyndinni **Leigjanda stillingar \> B2C leigjandi**, fjarlægir þú félag þess B2C leigjanda frá vefsvæðum sem tengjast einhverjum farvegi leigjanda. Í þessu tilfelli gætu notendur þínir ekki lengur getað skráð sig inn á reikninga sína. Því skal gæta fyllstu varúðar þegar þú eyðir stilltum leigjanda.
>
> Þegar uppsettum leigjanda er eytt verður B2C leigjanda og gögnum haldið áfram, en viðskiptakerfisstillingu viðkomandi leigjanda verður breytt eða fjarlægt. Notendur sem reyna að skrá sig eða skrá sig inn á vefinn munu búa til nýja reikningsskrá í sjálfgefna eða nýlega tengda B2C leigjanda sem er stilltur fyrir rás vefsins.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Stilla rásina þína með B2C leigjanda

1. Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.
1. Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.
1. Veldu **Rásir** og veldu síðan rásina sem á að stilla.
1. Í eignarrúðunni til hægri, í reitnum **Velja B2C forrit**, veldu stillan Azure AD B2C leigjandi til að nota fyrir þessa rás.
1. Veldu á skipanastikunni **Vista og birta** til að festa nýja eða uppfærða stillingu.

> [!WARNING]
> Ef þú breytir B2C forritinu sem er úthlutað á rásina fjarlægir þú núverandi tilvísanir sem hafa verið settar upp fyrir alla notendur sem þegar hafa skráð sig í umhverfið. Í þessu tilfelli eru öll skilríki sem eru tengd B2C forritinu sem nú er úthlutað ekki tiltæk fyrir notendur. Þess vegna skaltu breyta rás Azure AD B2C stillingar aðeins ef þú ert að setja upp rásina í fyrsta skipti og engir notendur hafa getað skráð sig. Annars gætu notendur þurft að skrá sig aftur til að koma upp met í nýju Azure AD B2C leigjandi.
## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum slóðartilvísunum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
