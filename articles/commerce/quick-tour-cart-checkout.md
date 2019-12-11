---
title: Yfirlit yfir síður körfu og greiðsluferlis
description: Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 347db3af36521e11dc70d5188dcc54b07efa1fbe
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697843"
---
# <a name="overview-of-cart-and-checkout-pages"></a>Yfirlit yfir síður körfu og greiðsluferlis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Körfusíðan á vef netverslunar sýnir alla hluti sem viðskiptavinur hefur bætt við körfuna. Körfusíðan er smíðuð með því að nota körfueininguna. Körfueiningin er gámur sem er hýsir allar einingar sem þarf til að sýna hluti sem eru í körfunni. Körfueiningin getur einnig notað aðrar einingar til að sýna pöntunaryfirlitið og alla kynningarkóða sem hefur verið beitt á pöntun viðskiptavinarins.

Greiðslusíðan á vefsíðu netverslunar sýnir skref fyrir skref sem viðskiptavinir fylgja til að færa inn allar upplýsingar sem þarf til að setja inn pöntun. Greiðsluferliseining getur innihaldið einingar sem sjá um póstfang, sendingaraðferðir, innheimtuupplýsingar, pöntunaryfirlit og aðrar upplýsingar sem tengjast pantanir viðskiptavina.

## <a name="cart-page"></a>Körfusíða

Körfusíðan virkar sem innkaupapokinn og inniheldur alla hluti sem hafa verið settir í körfuna.

Eftirfarandi mynd sýnir dæmi um körfusíðu sem var smíðuð með því að nota byrjunarbúnaðinn á netinu og „Fabrikam“ þemað.

![Dæmi um körfusíðu](./media/cart2.PNG)

Meginhlutinn af körfusíðunni sýnir hluti sem viðskiptavinur hefur bætt við körfuna. Allur viðeigandi afsláttur er sýndur. Þessir afslættir innihalda flókna afslátt. Sem dæmi má nefna „Kauptu 3 hluti og fáðu 10% afslátt“ eða „Kauptu flösku og bakpoka til að fá 10% afslátt.“ Pöntunarsamantektareiningin sýnir upphæðina sem er gjaldfærð eftir að afslætti, flutningum, sköttum og svo framvegis hefur verið beitt. Það er einnig til kynningarkóðaeining sem gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.

Viðskiptavinur getur verslað nafnlaust eða sem innskráður notandi. Ef viðskiptavinur er skráður inn eru hlutir í körfunni varðveittir milli seta. Á þennan hátt getur viðskiptavinurinn haldið áfram að versla úr mörgum tækjum.

Úr körfunni getur viðskiptavinurinn haldið áfram í greiðsluferli. Viðskiptavinur getur hafið greiðsluferli sem gestanotandi eða sem innskráður notandi.

Sjá upplýsingar um hvernig á að skrifa körfusíðu [Bæta körfueiningu við síðu](add-cart-module.md).

## <a name="checkout-page"></a>Greiðslusíða

Greiðslusíðan er þar sem viðskiptavinir slá inn upplýsingarnar sem þarf til að setja pöntun.

Eftirfarandi mynd sýnir dæmi um greiðslusíðu sem var smíðuð með því að nota byrjunarbúnaðinn á netinu.

![Dæmi um greiðslusíðu](./media/Checkout.PNG)

Meginhluti greiðslusíðunnar er þar sem öllum pöntunarupplýsingum er safnað. Þessar upplýsingar fela í sér póstfang, afhendingarmöguleika og greiðsluupplýsingar. Kassi hefur skref fyrir skref flæði, vegna þess að upplýsingarnar verða að vera færðar í ákveðna röð til að vinna úr. Til dæmis verður að færa inn flutningsfangið áður en hægt er að reikna út flutningskostnaðinn og heimila greiðsluna.

### <a name="shipping-address"></a>Aðsetur sendingar

Sendingar heimilisfang er krafist ef hlutir verða að vera sendir. Hægt er að stilla snið sendingarföngs fyrir hvert land í Dynamics 365 Retail. Til dæmis, ef hlutirnir verða fluttir til Bandaríkjanna, verður flutningsfangið að innihalda götuheiti, ástand og póstnúmer. Nokkur grunninntaksprófun er gerð fyrir sendingarfangareiti, svo sem staðfestingu á stafrófsröddum, hámarkslengd og tölur. Þótt réttmæti heimilisfangsins sjálfs sé ekki staðfest, er hægt að gera þessa staðfestingu með því að nota sérsniðna þjónustu þriðja aðila.

Póstfangið er notað á alla hluti í körfunni sem „skipið“ er valinn fyrir. Ef þú notar stöðvunarrennslið sem er að finna í byrjunarbúnaðinum á netinu er ekki hægt að senda einstaka körfuhluti á mismunandi netföng. Ef þú þarft þessa hæfileika er hægt að útfæra hana með því að aðlaga kassaeiningarnar.

Eftir að sendingarfangið hefur verið gefið upp eru sendingaraðferðir sem fáanlegar eru frá Dynamics 365 Commerce netverslun er sýnd. Hægt er að stilla sendingaraðferðirnar og netföngin sem þeir styðja í smásölu.

### <a name="payment"></a>Greiðsla

Næsta skref í greiðsluflæðinu er greiðsla. Í rafrænum viðskiptum er hægt að nota margar greiðslumáta til að setja inn pantanir, svo sem kreditkort, gjafakort og vildarpunkta. Einnig er hægt að nota sambland af þessum greiðslumátum. Það fer eftir greiðslumáta sem notaður er, viðbótarupplýsingar gætu verið nauðsynlegar. Til dæmis krefst greiðslu með kreditkorti greiðslu heimilisfang. Greiðslur með kreditkortum eru unnar með því að nota Adyen Payment Connector.

#### <a name="loyalty-points"></a>Vildarpunktar

Í greiðsluferlisflæðinu getur viðskiptavinur sem er meðlimur í vildarforriti og hefur safnað vildarpunkta innleyst þá vildarpunkta fyrir pöntun. Vildarpunktaeiningin er aðeins sýnd ef viðskiptavinurinn er með núverandi vildaraðild. Fyrir notendur sem ekki eru meðlimir og gestir er þessi eining falin.

#### <a name="gift-cards"></a>Gjafakort

Byrjunareiningin á netinu gerir kleift að hægt sé að innleysa alþjóðleg gjafakort fyrir pöntun. Til að nota innra gjafakort verður viðskiptavinurinn að vera skráður inn. Til að auka öryggi mælum við með því að þú sérsniðir flæðið með því að nota persónuauðkenni fyrir innri gjafakort.

### <a name="signed-in-and-guest-users"></a>Innskráðir og gestir notendur

Viðskiptavinur getur lokið greiðsluferli sem gestanotandi eða sem innskráður notandi. Ef viðskiptavinurinn skráir sig inn eru reikningsupplýsingar eins og vistaðar sendingarföng og vistaðar kreditkortaupplýsingar sjálfkrafa sóttar.

### <a name="order-summary"></a>Samantekt pöntunar

Afgreiðsla sýnir yfirlit yfir línuritin í körfunni, svo að viðskiptavinurinn geti staðfest pöntunina áður en hann eða hún leggur hana fram. Ekki er hægt að breyta línum atriðunum meðan á greiðsluferlinu stendur. Hins vegar er tengill á körfuna til staðar ef notandinn vill fara til baka og breyta línuliðum.

Eftir að viðskiptavinurinn hefur sent frá sér sendingar- og innheimtuupplýsingar endurspeglar pöntunaryfirlitið þá upphæð sem er gjaldfærð eftir að vildarpunkta, gjafakort og aðrar greiðslur hefur verið beitt.

### <a name="order-confirmation-and-email"></a>Pöntunarstaðfesting og tölvupóstur

Þegar viðskiptavinurinn leggur inn pöntun er staðfestingarnúmer gefið upp. Á þessum tímapunkti hefur greiðslan verið heimiluð en ekki gjaldfærð. Greiðslan verður aðeins gjaldfærð þegar pöntuninni er fullnægt (það er að segja þegar hún er annaðhvort send eða sótt).

Eftir að pöntun er búin til, er tölvupóstur til staðfestingar pöntunar sendur til viðskiptavinarins.

Nánari upplýsingar um hvernig á að skrifa greiðsluferlissíðu er að finna á [Bæta greiðsluferliseiningu við síðu](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir heimasíðuna](quick-tour-home-page.md)

[Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu](category-search-page-overview.md)

[Yfirlit yfir upplýsingasíður afurðar](quick-tour-pdp.md)

[Yfirlit yfir síður reikningastjórnunar](quick-tour-account-management.md)
