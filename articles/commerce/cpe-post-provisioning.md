---
title: Skilgreina Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9738700ca495d54c91ad91aa9c5a3d32c95a5a5
ms.sourcegitcommit: 4a973ac0e7af0176270a8070a96a52293567dfbf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2022
ms.locfileid: "8747638"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Skilgreina Dynamics 365 Commerce matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.

Ljúktu aðeins við aðgerðirnar í þessu efnisatriði eftir að forskoðunarumhverfi fyrir Commerce hefur verið úthlutað. Frekari upplýsingar um hvernig á að úthluta matsumhverfinu í Commerce er að finna í [Úthlutun Commerce-matsumhverfis](provisioning-guide.md).

Eftir að Commerce-umhverfismatinu hefur verið úthlutað í heild sinni, þarf að ljúka nokkrum grunnstillingarskrefum eftir úthlutun áður en hægt er að leggja mat á umhverfið. Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Áður en byrjað er

1. Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).
1. Farðu í verkefnið.
1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið hægra megin skal velja **Skrá inn í umhverfi**. Þér verður beint á Commerce Headquarters.
1. Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.
1. Fara til **Viðskiptabreytur \> Stillingarfæribreytur** og tryggja að það sé færsla fyrir **ProductSearch.UseAzureSearch** og að gildið sé stillt á **satt**. Ef þessa færslu vantar geturðu bætt henni við, stillt gildið á **satt**, og veldu síðan **Rásargagnagrunnur \> Full gagnasamstilling** fyrir Commerce Scale Unit sem tengist netverslunarvefsíðunni þinni.
1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Frumstilla viðskiptaáætlun**. Á **Frumstilla viðskiptaáætlun** valmynd, stilltu **Eyða núverandi uppsetningu** valmöguleika til **Já**, og veldu síðan **Allt í lagi**.
1. Til að bæta rásum við Commerce Scale Unit, farðu á **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur**, og veldu síðan Commerce Scale Unit í vinstri glugganum. Á **Smásölurás** Flýtiflipi, bættu við **AW netverslun**, **Business vefverslun**, og **Fabrikam útbreidd netverslun** rásir. Valfrjálst geturðu líka bætt við smásöluverslunum ef þú ætlar að nota POS (td, **Seattle**, **Fransiskó**, og **San Jose**).

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
1. Veldu **Í lagi**. Listinn yfir síður svæðisins birtist.
1. Endurtaktu skref 2-7 fyrir **AdventureWorks** síða (sem kortleggst á **AW netverslun** rás) og **AdventureWorks Viðskipti** síða (sem kortleggst á **AW Business vefverslun** rás). Ef **Leið** reiturinn fyrir Fabrikam síðuna er tómur, þá verður þú að bæta við slóðum fyrir þær tvær AdventureWorks síður (td „aw“ og „awbusiness“).

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

1. Ef staða starfsins er **Haldið eftir**, fylgdu þessum skrefum:

    1. Veldu skrána.
    1. Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.
    1. Veldu **Bíður** og síðan **Í lagi**.

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
- **Gildistími:** 10/30
- **Sannprófunargildi korts (CVV)-kóði:** 737

> [!IMPORTANT]
> Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.

## <a name="next-steps"></a>Næstu skref

Þegar úthlutunar- og grunnstillingarskrefum er lokið er hægt að byrja að nota matsumhverfið. Notið vefslóð Commerce-vefsmiðins til að fara í höfundarviðmótið. Notið vefslóð Commerce-vefsvæðis til að fara á vefviðmót viðskiptavinar smásölu.

Til að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið skal skoða [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).

> [!NOTE]
> Matsumhverfi Commerce koma með forhlöðnum Azure Active Directory (Azure AD) B2C-leigjanda fyrir sýnikennslu. Ekki er krafist þess að skilgreina eigin Azure AD B2C-leigjanda fyrir matsumhverfi. Ef þú ert hinsvegar að skilgreina matsumhverfið til að nota þinn eigin Azure AD B2C-leigjanda skaltu ganga úr skugga um að bæta við ``https://login.commerce.dynamics.com/_msdyn365/authresp`` sem svörunarvefslóð í Azure AD B2C-forritinu gegnum Azure -gáttina.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Ráalisti vefsvæðisgerðarmanns er tómur þegar vefsvæði er stillt

Ef vefsmiður sýnir engar netverslunarrásir, tryggðu í höfuðstöðvunum að rásunum hafi verið bætt við viðskiptaskalaeininguna eins og lýst er í [Áður en þú byrjar](#before-you-start) kafla hér að ofan. Einnig, hlaupa **Frumstilla viðskiptaáætlun** með **Eyða núverandi uppsetningu** gildi stillt á **Já**.  Þegar þessum skrefum er lokið, á **Rásar gagnagrunnur** síða (**Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur**), keyra **9999** starf á verslunarsviði.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Litapróf eru ekki birt á flokkasíðunni, heldur eru þau birt á vöruupplýsingasíðunni (PDP) síðunni

Fylgdu þessum skrefum til að tryggja að lita- og stærðarsýnin séu stillt á að vera endurbætt.

1. Í höfuðstöðvunum, farðu til **Verslun og verslun \> Rásaruppsetning \> Rásarflokkar og vörueiginleikar**.
1. Í vinstri glugganum, veldu netverslunarrásina og veldu síðan **Stilltu lýsigögn eiginda**.
1. Stilltu **Sýna eigind á rás** valmöguleika til **Já**, stilltu **Hægt að betrumbæta** valmöguleika til **Já**, og veldu síðan **Vista**. 
1. Farðu aftur á rásarsíðu netverslunarinnar og veldu síðan **Birtu rásaruppfærslur**.
1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur** og keyra **9999** starf á verslunarsviði.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Viðskiptaeiginleikar virðast ekki vera kveiktir á AdventureWorks viðskiptasíðu

Í höfuðstöðvum skaltu ganga úr skugga um að netverslunarrásin sé stillt með **Tegund viðskiptavinar** stillt á **B2B**. Ef **Tegund viðskiptavinar** er stillt á **B2C**, nýja rás verður að búa til þar sem ekki er hægt að breyta núverandi rás. 

Kynningargögn send í Commerce útgáfu 10.0.26 og fyrr voru með villu þar sem **AW Business vefverslun** rás var rangstillt. Lausnin er að búa til nýja rás með sömu stillingum og stillingum nema fyrir **Tegund viðskiptavinar**, sem ætti að vera stillt á **B2B**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Úthluta Dynamics 365 Commerce matsumhverfi](provisioning-guide.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi](cpe-optional-features.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[algengar spurningar um Dynamics 365 Commerce matsumhverfi](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
