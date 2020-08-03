---
title: Stilla Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599725"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Stilla Dynamics 365 Commerce matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.

## <a name="overview"></a>Yfirlit

Ljúktu aðeins við aðgerðirnar í þessu efnisatriði eftir að forskoðunarumhverfi fyrir Commerce hefur verið úthlutað. Frekari upplýsingar um hvernig á að úthluta matsumhverfinu í Commerce er að finna í [Úthlutun Commerce-matsumhverfis](provisioning-guide.md).

Eftir að Commerce-umhverfismatinu hefur verið úthlutað í heild sinni, þarf að ljúka nokkrum grunnstillingarskrefum eftir úthlutun áður en hægt er að leggja mat á umhverfið. Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Áður en byrjað er

1. Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).
1. Farðu í verkefnið.
1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið hægra megin skal velja **Skrá inn í umhverfi**. Þér verður beint á Commerce Headquarters.
1. Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.

Við úthlutun verkþátta eftir á í Commerce Headquarters skal ganga úr skugga um að **USRT** lögaðilinn sé alltaf valinn.

## <a name="configure-the-point-of-sale"></a>Grunnstilling sölustaðar

### <a name="associate-a-worker-with-your-identity"></a>Tengdu starfsmann við kenni þitt

Til að tengja starfsmann við kennimerkið þitt skal fylgja þessum skrefum í Commerce Headquarters.

1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Starfsmenn \> Starfskraftar**.
1. Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**.
1. Á aðgerðasvæðinu skal velja **Commerce**.
1. Veldu **Tengja fyrirliggjandi kenni**.
1. Í reitinn **Netfang** til hægri við **Leita með tölvupósti** skaltu slá inn netfangið þitt.
1. Velja **Leita**.
1. Veldu skrána með nafninu þínu.
1. Veljið **Í lagi**.
1. Veljið **Vista**.

### <a name="activate-cloud-pos"></a>Virkja sölukerfi í skýinu

Til að virkja sölukerfi í skýinu skal fylgja þessum skrefum í LCS.

1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið hægra megin skal velja **Skrá sig inn í sölukerfi í skýinu**.
1. Veljið **Næst** til að opna svargluggann **Áður en þú hefst handa**.
1. Skiljið **Vefslóð þjóns** eftir eins og hann er. Veljið **Næst**.
1. Skráðu þig inn með Microsoft Azure Active Directory (Azure AD)-reikningnum þínum.
1. Undir **Heiti verslunar** skal velja **San Francisco** og síðan velja **Næst**.
1. Undir **Skráning og tæki** velurðu **SANFRAN-1**.
1. Veldu **Virkja**. Þú ert skráð/ur út og færð/ur á POS-innskráningarsíðuna.
1. Þú getur nú skráð þig inn á Cloud POS-reynsluna með kenni rekstraraðila **000713** og lykilorði **123**.

## <a name="set-up-your-site-in-commerce"></a>Settu upp vefsvæðið í Commerce

Til að hefja uppsetningu á matssvæðinu þínu í Commerce skal fylgja þessum skrefum.

1. Skráðu þig inn á vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).
1. Veldu svæðið **Fabrikam** til að opna uppsetningarglugga svæðisins.
1. Veldu lénið sem þú slóst inn þegar þú frumstilltir e-Commerce.
1. Veldu **Fabrikam útvíkkuð netverslun** sem sjálfgefna rás. (Gakktu úr skugga um að þú veljir **framlengda** netverslun.)
1. Veldu **en-us** sem sjálfgefið tungumál.
1. Hafðu gildið í reitnum **Slóð** eins og það er.
1. Veljið **Í lagi**. Listinn yfir síður svæðisins birtist.

## <a name="enable-jobs"></a>Virkja vinnslur

Til að virkja vinnslur í Commerce skal fylgja þessum skrefum.

1. Skráðu þig inn í umhverfið (HQ).
1. Notaðu valmyndina til vinstri til að fara í **Retail og Commerce \> Fyrirspurnir og skýrslur \> Runuvinnslur**.

    Hinum skrefum þessa ferlis verður að vera lokið fyrir sérhverja af eftirfarandi vinnslum:

    * Vinna úr tilkynningartölvupósti smásölupöntunar
    * Tiltækar afurðir
    * P-0001
    * Samstilla pantanavinnslu

1. Notaðu hraðsíuna til að leita að vinnslunni eftir heiti.
1. Ef staða vinnslunnar er **Í gangi** skal fylgja þessum skrefum:

    1. Veldu skrána.
    1. Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.
    1. Velja skal **Hætta við** og svo **Í lagi**.

Einnig er hægt að stilla endurtekningartímabil á eina (1) mínútu fyrir eftirfarandi störf:

* Vinna úr vinnslu vegna tilkynningar á smásölupöntun í tölvupósti
* P-0001 starf
* Samstilla pantanavinnslu

### <a name="run-full-data-synchronization"></a>Keyra fulla samstillingu gagna

Til að keyra heildarsamstillingu gagna í Commerce skal fylgja þessum skrefum í Commerce Headquarters.

1. Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnur rásar**.
1. Veldu rásina sem kallast **scXXXXXXXXX**.
1. Í aðgerðaglugganum velurðu **Samstilling allra gagna**.
1. Skráðu **9999** sem dreifingaráætlun.
1. Veljið **Í lagi**.
1. Veljið **Í lagi**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Prófaðu kreditkortaupplýsingar til að gera prufukaup

Til að framkvæma prófunarviðskipti á vefnum geturðu notað eftirfarandi prufukreditkortaupplýsingar:

- **Kortanúmer:** 4111-1111-1111-1111
- **Gildistími:** 10/20
- **Sannprófunargildi korts (CVV)-kóði:** 737

> [!IMPORTANT]
> Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.

## <a name="next-steps"></a>Næstu skref

Þegar úthlutunar- og grunnstillingarskrefum er lokið er hægt að byrja að nota matsumhverfið. Notið vefslóð Commerce-vefsmiðins til að fara í höfundarviðmótið. Notið vefslóð Commerce-vefsvæðis til að fara á vefviðmót viðskiptavinar smásölu.

Til að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið skal skoða [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce matsumhverfi](provisioning-guide.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi](cpe-optional-features.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[algengar spurningar um Dynamics 365 Commerce matsumhverfi](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)
