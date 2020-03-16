---
title: Skilgreina forskoðunarumhverfi fyrir Dynamics 365 Commerce
description: Þetta efni útskýrir hvernig á að stilla forsýningarumhverfi Microsoft Dynamics 365 Commerce eftir að það er úthlutað.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057718"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Skilgreina forskoðunarumhverfi fyrir Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að stilla forsýningarumhverfi Microsoft Dynamics 365 Commerce eftir að það er úthlutað.

## <a name="overview"></a>Yfirlit

Ljúktu verklagsreglunum í þessu efni aðeins eftir að forskoðunarumhverfi Commerce hefur verið útvegað. Fyrir upplýsingar um hvernig skuli úthluta þér forskoðunarumhverfi Commerce skal sjá [Veita forskoðunarumhverfi Commerce](provisioning-guide.md).

Eftir að forskoðunarumhverfi Commerce hefur verið úthlutað á öllum sviðum verður að ljúka eftirúthlutunarstillingarþrepunum áður en þú getur byrjað að meta umhverfið. Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Áður en byrjað er

1. Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).
1. Farðu í verkefnið.
1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið til hægri skaltu velja **Nánari upplýsingar**.
1. Veldu **Skrá inn** til að opna valmynd og veldu síðan **Skrá inn í umhverfi**.
1. Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.

## <a name="configure-the-point-of-sale-in-lcs"></a>Stilla sölustað í LCS

### <a name="associate-a-worker-with-your-identity"></a>Tengdu starfsmann við kenni þitt

Fylgdu þessum skrefum til að tengja starfsmann við kenni þitt í LCS.

1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Starfsmenn \> Starfskraftar**.
1. Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**.
1. Í aðgerðarúðunni skal velja **Retail**.
1. Veldu **Tengja fyrirliggjandi kenni**.
1. Í reitinn **Netfang** til hægri við **Leita með tölvupósti** skaltu slá inn netfangið þitt.
1. Velja **Leita**.
1. Veldu skrána með nafninu þínu.
1. Veljið **Í lagi**.
1. Veljið **Vista**.

### <a name="activate-cloud-pos"></a>Virkja sölukerfi í skýinu

Fylgdu þessum skrefum til að virkja Cloud POS í LCS.

1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið til hægri skaltu velja **Nánari upplýsingar**.
1. Veldu **Skrá inn** til að opna valmynd og veldu síðan **Skrá inn á sölustað í skýi** til að opna sölustaðinn (POS).
1. Veljið **Næst**.
1. Skráðu þig inn með Microsoft Azure Active Directory (Azure AD)-reikningnum þínum.
1. Undir **Verslunarheiti** velurðu **San Fransiskó**.
1. Veljið **Næst**.
1. Undir **Skráning og tæki** velurðu **SANFRAN-1**.
1. Veldu **Virkja**. Þú ert skráð/ur út og færð/ur á POS-innskráningarsíðuna.
1. Þú getur nú skráð þig inn á Cloud POS-reynsluna með kenni rekstraraðila **000713** og lykilorði **123**.

## <a name="set-up-your-site-in-commerce"></a>Settu upp vefsvæðið í Commerce

Fylgdu þessum skrefum til að byrja að setja upp forskoðunarsíðuna í Commerce.

1. Skráðu þig inn á stjórnunartól vefsvæðisins með því að nota slóðina sem þú skrifaðir niður þegar þú frumstilltir e-Commerce við úthlutun (sjá [Frumstilla e-Commerce](provisioning-guide.md#initialize-e-commerce)).
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
1. Ef staða vinnslunnar er **Halda eftir** skal fylgja þessum skrefum:

    1. Veldu skrána.
    1. Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.
    1. Veldu **Bíður** og síðan **Í lagi**.

### <a name="run-full-data-synchronization"></a>Keyra fulla samstillingu gagna

Fylgdu þessum skrefum til að keyra fulla samstillingu gagna í Commerce.

1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Retail Verkraðari \> Rásagagnagrunnur**.
1. Á listanum til vinstri er rásin **Sjálfgefið** valin. Veldu hina rásina sem er tiltæk. Þessi rás heitir **scXXXXXXXXX**.
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

Eftir að úthlutunar- og stillingarskrefunum er lokið ertu tilbúin/n til að meta forskoðunarumhverfið þitt. Notaðu slóðina á stjórnunartólinu Commerce til að fara í höfundarupplifunina. Notaðu slóðina á Commerce-svæðinu til að fara í svæðisreynslu smásöluviðskiptavinar.

Til að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce skal sjá [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce forsýningarumhverfi](provisioning-guide.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce forskoðunarumhverfi](cpe-optional-features.md)

[Dynamics 365 Commerce yfirlitsumhverfi algengra spurninga](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)
