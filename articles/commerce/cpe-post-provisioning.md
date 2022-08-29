---
title: Stilla Dynamics 365 Commerce sandkassaumhverfi
description: Þessi grein útskýrir hvernig á að stilla a Microsoft Dynamics 365 Commerce sandkassaumhverfi eftir að það hefur verið útvegað.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270373"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Stilla Dynamics 365 Commerce sandkassaumhverfi

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla a Microsoft Dynamics 365 Commerce sandkassaumhverfi eftir að það hefur verið útvegað.

Ljúktu aðeins við aðferðirnar í þessari grein eftir að Commerce sandkassaumhverfið þitt hefur verið útvegað. Fyrir upplýsingar um hvernig á að útvega Commerce sandkassaumhverfið þitt, sjá [Útvega viðskiptasandkassaumhverfi](provisioning-guide.md).

Eftir að Commerce sandkassaumhverfið þitt hefur verið útvegað enda til enda, verður að ljúka við viðbótarstillingarskref eftir úthlutun áður en þú getur byrjað að nota umhverfið. Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Áður en byrjað er

1. Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).
1. Farðu í verkefnið.
1. Veldu umhverfið á listanum.
1. Í upplýsingum um umhverfið hægra megin skal velja **Skrá inn í umhverfi**. Þér verður beint á Commerce Headquarters.
1. Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu. Þessi lögaðili hefur verið forstilltur í kynningargögnunum.
1. Fara til **Viðskiptabreytur \> Stillingarfæribreytur** og tryggja að það sé færsla fyrir **ProductSearch.UseAzureSearch** og að gildið sé stillt á **satt**. Ef þessa færslu vantar skaltu bæta henni við og stilla gildið á **satt**.
1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Frumstilla viðskiptaáætlun**. Á **Frumstilla viðskiptaáætlun** valmynd, stilltu **Eyða núverandi uppsetningu** valmöguleika til **Já**, og veldu síðan **Allt í lagi**.
1. Til að verslunar- og rafræn viðskipti virki rétt verður að bæta þeim við Commerce Scale Unit. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur**, og veldu síðan Commerce Scale Unit í vinstri glugganum. Á **Smásölurás** flýtiflipann, bættu við **AW netverslun**, **Business vefverslun**, og **Fabrikam útbreidd netverslun** rásir ef þú ætlar að nota þessar netviðskiptarásir. Valfrjálst geturðu einnig bætt við smásöluverslunum ef þú ætlar að nota sölustað (POS) (td, **Seattle**, **Fransiskó**, og/eða **San Jose**).
1. Til að tryggja að allar breytingar séu samstilltar við rásargagnagrunninn skaltu velja **Rásargagnagrunnur \> Full gagnasamstilling** fyrir verslunarkvarðaeininguna.

Við úthlutun verkþátta eftir á í Commerce Headquarters skal ganga úr skugga um að **USRT** lögaðilinn sé alltaf valinn.

## <a name="configure-the-point-of-sale"></a>Grunnstilling sölustaðar

### <a name="associate-a-worker-with-your-identity"></a>Tengdu starfsmann við kenni þitt

Til að tengja starfsmann við kennimerkið þitt skal fylgja þessum skrefum í Commerce Headquarters.

1. Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Starfsmenn \> Starfskraftar**.
1. Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**. Þessi dæmi notandi er tengdur við San Francisco verslunina sem verður notuð í næsta hluta.
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

## <a name="set-up-your-e-commerce-sites"></a>Settu upp netviðskiptasíðurnar þínar

Það eru þrjár tiltækar kynningarsíður fyrir rafræn viðskipti: Fabrikam, Adventure Works og Adventure Works Business. Fylgdu skrefunum hér að neðan til að stilla hverja kynningarsíðu.

1. Skráðu þig inn á vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).
1. Veldu síðuna (**Fabrikam**, **·**, eða **Adventure Works Business**), til að opna uppsetningargluggann fyrir vefsvæðið.
1. Veldu lénið sem þú slóst inn þegar þú frumstillir Commerce.
1. Í höfuðstöðvunum skaltu velja forstilltu netverslunarrásina (**Fabrikam útbreidd netverslun**, **netverslun**, eða **AW Business vefverslun**) sem samsvarar sjálfgefna rásinni.
1. Veldu **en-us** sem sjálfgefið tungumál.
1. Stilltu slóðareitina. Þetta getur verið autt fyrir eina síðu en þarf að stilla það ef sama lén er notað fyrir margar síður. Til dæmis ef lénið er`https://www.constoso.com`, þú getur notað auða slóð fyrir Fabrikam (`https://contoso.com`), og notaðu síðan „aw“ fyrir Adventure Works (`https://contoso.com/aw`) og „awbusiness“ fyrir Adventure Works viðskiptasíðuna (`https://contoso.com/awbusiness`).
1. Veldu **Í lagi**. Listinn yfir síður svæðisins birtist.
1. Valfrjálst, endurtaktu skref 2-7 til að stilla hinar kynningarsíðurnar eftir þörfum.

## <a name="enable-jobs"></a>Virkja vinnslur

Til að virkja vinnslur í Commerce skal fylgja þessum skrefum.

1. Skráðu þig inn í umhverfi höfuðstöðvanna.
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

Eftir að úthlutunar- og stillingarskrefum er lokið geturðu byrjað að nota sandkassaumhverfið þitt. Notið vefslóð Commerce-vefsmiðins til að fara í höfundarviðmótið. Notið vefslóð Commerce-vefsvæðis til að fara á vefviðmót viðskiptavinar smásölu.

Til að stilla valfrjálsa eiginleika fyrir Commerce sandkassaumhverfið þitt, sjá [Stilltu valfrjálsa eiginleika fyrir Commerce sandkassaumhverfi](cpe-optional-features.md).

Til að gera notendum netverslunar kleift að skrá sig inn á netverslunarsíðuna þarf viðbótarstillingar til að virkja auðkenningu vefsvæðis í gegnum Azure Active Directory fyrirtæki til neytenda (B2C). Fyrir leiðbeiningar, sjá [Settu upp B2C leigjanda í Commerce](set-up-b2c-tenant.md).

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Ráalisti vefsvæðisgerðarmanns er tómur þegar vefsvæði er stillt

Ef vefsmiður sýnir engar netverslunarrásir, tryggðu í höfuðstöðvunum að rásunum hafi verið bætt við viðskiptaskalaeininguna eins og lýst er í [Áður en þú byrjar](#before-you-start) kafla hér að ofan. Einnig, hlaupa **Frumstilla viðskiptaáætlun** með **Eyða núverandi uppsetningu** gildi stillt á **Já**.  Þegar þessum skrefum er lokið, á **Rásar gagnagrunnur** síða (**Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur**), keyra **9999** starf á verslunarsviði.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Litapróf eru ekki birt á flokkasíðunni, heldur eru þau birt á vöruupplýsingasíðunni (PDP) síðunni

Fylgdu þessum skrefum til að tryggja að lita- og stærðarsýnin séu stillt á að vera endurbætt.

1. Í höfuðstöðvunum, farðu til **Verslun og verslun \> Rásaruppsetning \> Rásarflokkar og vörueiginleikar**.
1. Í vinstri glugganum, veldu netverslunarrásina og veldu síðan **Stilltu lýsigögn eiginda**.
1. Stilltu **Sýna eiginleika á rás** valmöguleika til **Já**, stilltu **Hægt að betrumbæta** valmöguleika til **Já**, og veldu síðan **Vista**. 
1. Farðu aftur á rásarsíðu netverslunarinnar og veldu síðan **Birtu rásaruppfærslur**.
1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur** og keyra **9999** starf á verslunarsviði.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Viðskiptaeiginleikar virðast ekki vera kveiktir á AdventureWorks viðskiptasíðu

Í höfuðstöðvum skaltu ganga úr skugga um að netverslunarrásin sé stillt með **Tegund viðskiptavinar** stillt á **B2B**. Ef **Tegund viðskiptavinar** er stillt á **B2C**, nýja rás verður að búa til þar sem ekki er hægt að breyta núverandi rás. 

Kynningargögn send í Commerce útgáfu 10.0.26 og fyrr voru með villu þar sem **AW Business vefverslun** rás var rangstillt. Lausnin er að búa til nýja rás með sömu stillingum og stillingum nema fyrir **Tegund viðskiptavinar**, sem ætti að vera stillt á **B2B**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Ákvæði a Dynamics 365 Commerce sandkassa umhverfi](provisioning-guide.md)

[Stilltu valfrjálsa eiginleika fyrir a Dynamics 365 Commerce sandkassa umhverfi](cpe-optional-features.md)

[Stilltu BOPIS í a Dynamics 365 Commerce sandkassa umhverfi](cpe-bopis.md)

[Microsoft Dynamics Lifecycle Services (LSC)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
