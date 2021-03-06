---
title: Leitaryfirlit í skýinu
description: Þetta efnisatriði sýnir yfirlit yfir leit í skýinu í Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b5182df9d45a3b5d2572a5b6b391c924ef23bf9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800422"
---
# <a name="cloud-powered-search-overview"></a>Leitaryfirlit í skýinu

[!include [banner](includes/banner.md)]

Þetta efnisatriði sýnir yfirlit yfir leit í skýinu í Microsoft Dynamics 365 Commerce.

Vöruuppgötvun hjálpar til við að tryggja að viðskiptavinir geti fundið vörur fljótt og auðveldlega með því að vafra um flokka, leita og sía. Smásalar líta á vöruuppgötvun sem aðalverkfæri til að hafa samskipti við viðskiptavini á öllum rásum.

Viðskiptavinir eru vanir nánast samstundis svartímum vefleitarvéla, háþróuðum netverslunarsíðum, félagslegum forritum, sjálfvirkum uppástungum sem birtast þegar þeir slá inn leitarskilyrði, hliðarleiðsögn og auðkenningu. Ef viðskiptavinir geta ekki fundið vöruna sem þeir eru að leita að nógu fljótt í einni verslun með netverslun, munu þeir ekki hika við að fara í aðra netverslun.

Uppgötvun skýjavöru afurðar í Dynamics 365 Commerce hjálpar smásöluaðilum að halda áfram að auka varðveislu neytenda og viðskiptahlutfall á öllum rásum, bæði rásir í netverslun og sölustaði (POS).

Leitarreynslan Dynamics 365 Commerce hefur bætt getu til að hjálpa smásöluaðilum að öðlast betri uppgötvun vöru. Á sama tíma skilar þessi geta sveigjanleika og afköstum sem eru nauðsynleg fyrir umferð í netverslun.

## <a name="browse-and-search"></a>Vafra og leita

Samsvörun leitar og afköst eru lykilatriði í alhliða upplifun, því uppgötvun vöru byggir fyrst og fremst á leitareiginleikum til að sækja upplýsingar og fletta í gegnum efni. Skilvirk leit og leitareynsla hjálpar til við að auka umreikning.

Eftirfarandi mynd sýnir dæmi um dæmigerða virkni vafra og leitar.

![Leita á lendingasíðu](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Hliðarflakk og yfirlit yfir val 

Hliðarflakk auðveldar viðskiptavinum að leita að efni með því að láta þá sía á hreinsara sem tengjast hugtökum í hugtakasetti. Eftir að viðskiptavinur hefur valið og beitt hreinsurum er yfirlit yfir valið sýnt. 

Með því að nota hliðarleiðsögn er hægt að stilla mismunandi hreinsara fyrir mismunandi hugtök í hugtakasetti, án þess að þurfa að búa til viðbótarsíður. 

Eftirfarandi mynd sýnir dæmi þar sem hliðarleiðsögn er notuð við leit.

![Yfirlit yfir val](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Heildstæð sjálfvirkni

Núverandi virkni sjálfvirkrar mælingar sýnir bara lykilorð sem kalla fram leit að samsvarandi leitarorði. Vegna nýrra endurbóta í Dynamics 365 Commerce geta viðskiptavinir oft uppgötvað hlekki á vörur áður en þeir hafa lokið við að slá inn.

Dynamics 365 Commerce styður einnig virkni fyrir samsvörun leitarorða í ýmsum flokkum. Þessa virkni skulum viðskiptavinir sjá fjölda samsvarandi leitarorða milli flokka og kalla fram leit að leitarorði í öðrum flokkum.

Eftirfarandi mynd sýnir dæmi þar sem verið er að nota heildstæða sjálfvirkni.

![heildstæð sjálfvirkni](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Raða

Aukin flokkun í Dynamics 365 Commerce gerir viðskiptavinum kleift að flokka, leita og fletta í leitarniðurstöðum og betrumbæta þær eftir forsendum eins og verði, vöruheiti og vörunúmeri. Viðskiptavinir geta einnig flokkað niðurstöður út frá því hvort vara er ný, mest seld eða nýlega bætt við.

>[!NOTE]
>Þessir leitareiginleikar í skýi eru tiltækir frá útgáfu 10.0.8. Gangið úr skugga um að undir **Viðskiptafæribreytur > Skilgreiningarfæribreytur** sé færsla fyrir „ProductSearch.UseAzureSearch stillt á true“. 
![Færibreytur skilgreininga fyrir leit í skýinu](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
