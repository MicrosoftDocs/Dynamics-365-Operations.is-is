---
title: Leitaryfirlit í skýinu
description: Þessi grein gefur yfirlit yfir skýknúna leit í Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273667"
---
# <a name="cloud-powered-search-overview"></a>Leitaryfirlit í skýinu

[!include [banner](includes/banner.md)]

Þessi grein gefur yfirlit yfir skýknúna leit í Microsoft Dynamics 365 Commerce.

Vöruuppgötvun hjálpar til við að tryggja að viðskiptavinir geti fundið vörur fljótt og auðveldlega með því að vafra um flokka, leita og sía. Söluaðilar líta á vöruuppgötvun sem aðalverkfæri fyrir samskipti viðskiptavina þvert á rásir knúnar af Cloud Scale Unit (CSU), svo sem rafræn viðskipti og sölustað (POS).

Viðskiptavinir eru vanir nánast samstundis svartímum vefleitarvéla, háþróuðum netverslunarsíðum, félagslegum forritum, sjálfvirkum uppástungum sem birtast þegar þeir slá inn leitarskilyrði, hliðarleiðsögn og auðkenningu. Ef viðskiptavinir geta ekki fundið vöruna sem þeir eru að leita að á fljótlegan hátt í einni netverslun munu þeir ekki hika við að fara í aðra netverslun.

Skýknúna vöruuppgötvunin í Commerce hjálpar smásöluaðilum að halda áfram að auka neytendahald og viðskiptahlutfall á milli rása sem knúnar eru af CSU.

Commerce leitarupplifunin hefur bætt möguleika til að hjálpa smásöluaðilum að ná betri uppgötvun vöru. Á sama tíma skila þessir eiginleikar þeim sveigjanleika og afköstum sem krafist er fyrir rafræn viðskipti.

## <a name="browse-and-search"></a>Vafra og leita

Samsvörun leitar og afköst eru lykilatriði í alhliða upplifun, því uppgötvun vöru byggir fyrst og fremst á leitareiginleikum til að sækja upplýsingar og fletta í gegnum efni. Skilvirk leit og leitareynsla hjálpar til við að auka umreikning.

Eftirfarandi mynd sýnir dæmi um dæmigerða virkni vafra og leitar.

![Leita á lendingasíðu.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Hliðarflakk og yfirlit yfir val 

Hliðarflakk auðveldar viðskiptavinum að leita að efni með því að láta þá sía á hreinsara sem tengjast hugtökum í hugtakasetti. Eftir að viðskiptavinur hefur valið og beitt hreinsurum er yfirlit yfir valið sýnt. 

Með því að nota hliðarleiðsögn er hægt að stilla mismunandi hreinsara fyrir mismunandi hugtök í hugtakasetti, án þess að þurfa að búa til viðbótarsíður. 

Eftirfarandi mynd sýnir dæmi þar sem hliðarleiðsögn er notuð við leit.

![Yfirlit yfir val.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Heildstæð sjálfvirkni

Núverandi virkni sjálfvirkrar uppástungu sýnir leitarorð sem kalla fram leit að samsvarandi leitarorði. Vegna nýrra endurbóta í Commerce geta viðskiptavinir oft uppgötvað tengla á vörur áður en þeir hafa lokið við að slá inn.

Viðskipti styður einnig virkni fyrir leitarorðasamsvörun í ýmsum flokkum. Þessa virkni skulum viðskiptavinir sjá fjölda samsvarandi leitarorða milli flokka og kalla fram leit að leitarorði í öðrum flokkum.

Eftirfarandi mynd sýnir dæmi þar sem verið er að nota heildstæða sjálfvirkni.

![heildstæð sjálfvirk tillaga.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Raða

Flokkunarvirkni gerir viðskiptavinum kleift að flokka, leita og fletta í niðurstöðum flokka og betrumbæta þær eftir viðmiðum eins og verði, vöruheiti og vörunúmeri. Ef þú virkjar [Vararáðleggingar](product-recommendations.md) í þínu umhverfi geta viðskiptavinir einnig flokkað niðurstöður út frá háþróuðum flokkunarviðmiðum eins og nýjum, söluhæstu og vinsælum.


> [!NOTE]
> Þessir leitareiginleikar í skýi eru tiltækir frá útgáfu 10.0.8. Gakktu úr skugga um að það sé færsla fyrir „ProductSearch.UseAzureSearch“ stillt á „true“ í **Viðskiptafæribreytur > Stillingarfæribreytur**. 
![Færibreytur skilgreininga fyrir leit í skýinu.](./media/CloudPoweredSearchConfigurationParameters.png)
>Ítarlegir flokkunarvalkostir eins og nýir, söluhæstu og vinsælir eru fáanlegir með Commerce SSK útgáfu af 9.35+ og Dynamics 365 Commerce 10.0.20 útgáfa.  


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
