---
title: Yfirlit yfir síður körfu og greiðsluferlis
description: Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a9b7fe1722c366eb504882c61a337a95500c92ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000510"
---
# <a name="cart-and-checkout-pages-overview"></a>Yfirlit yfir síður körfu og greiðsluferlis

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Körfusíðan á vef netverslunar sýnir alla hluti sem viðskiptavinur hefur bætt við körfuna. Körfusíðan er smíðuð með því að nota körfueininguna. Körfueiningin er gámur sem er hýsir allar einingar sem þarf til að sýna hluti sem eru í körfunni. Körfueiningin getur einnig notað aðrar einingar til að sýna pöntunaryfirlitið og alla kynningarkóða sem hefur verið beitt á pöntun viðskiptavinarins.

Greiðslusíðan á vefsíðu netverslunar sýnir skref fyrir skref sem viðskiptavinir fylgja til að færa inn allar upplýsingar sem þarf til að setja inn pöntun. Greiðsluferliseining getur innihaldið einingar sem sjá um póstfang, sendingaraðferðir, innheimtuupplýsingar, pöntunaryfirlit og aðrar upplýsingar sem tengjast pantanir viðskiptavina.

## <a name="cart-page"></a>Körfusíða

Körfusíðan virkar sem innkaupapokinn og inniheldur alla hluti sem hafa verið settir í körfuna.

Eftirfarandi mynd sýnir dæmi um körfusíðu sem var byggð með einingarsafninu og „Fabrikam“ þema.

![Dæmi um körfusíðu](./media/cart2.PNG)

Meginhlutinn af körfusíðunni sýnir hluti sem viðskiptavinur hefur bætt við körfuna. Allur viðeigandi afsláttur er sýndur. Þessir afslættir innihalda flókna afslátt. Sem dæmi má nefna „Kauptu 3 hluti og fáðu 10% afslátt“ eða „Kauptu flösku og bakpoka til að fá 10% afslátt.“ Pöntunarsamantektareiningin sýnir upphæðina sem er gjaldfærð eftir að afslætti, flutningum, sköttum og svo framvegis hefur verið beitt. Það er einnig til kynningarkóðaeining sem gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.

Viðskiptavinur getur verslað nafnlaust eða sem innskráður notandi. Ef viðskiptavinur er skráður inn eru hlutir í körfunni varðveittir milli seta. Á þennan hátt getur viðskiptavinurinn haldið áfram að versla úr mörgum tækjum.

Úr körfunni getur viðskiptavinurinn haldið áfram í greiðsluferli. Viðskiptavinur getur hafið greiðsluferli sem gestanotandi eða sem innskráður notandi.

Sjá upplýsingar um hvernig á að skrifa körfusíðu [Bæta körfueiningu við síðu](add-cart-module.md).

## <a name="checkout-page"></a>Greiðslusíða

Greiðslusíðan er þar sem viðskiptavinir slá inn upplýsingarnar sem þarf til að setja pöntun.

Eftirfarandi mynd sýnir dæmi um útskráningarsíðu sem var byggð með einingasafni.

![Dæmi um greiðslusíðu](./media/Checkout.PNG)

Meginhluti greiðslusíðunnar er þar sem öllum pöntunarupplýsingum er safnað. Þessar upplýsingar fela í sér póstfang, afhendingarmöguleika og greiðsluupplýsingar. Kassi hefur skref fyrir skref flæði, vegna þess að upplýsingarnar verða að vera færðar í ákveðna röð til að vinna úr. Til dæmis verður að færa inn flutningsfangið áður en hægt er að reikna út flutningskostnaðinn og heimila greiðsluna.

### <a name="shipping-address"></a>Aðsetur sendingar

Sendingar heimilisfang er krafist ef hlutir verða að vera sendir. Hægt er að stilla snið sendingarföngs fyrir hvert land í Dynamics 365 Commerce. Til dæmis, ef hlutirnir verða fluttir til Bandaríkjanna, verður flutningsfangið að innihalda götuheiti, ástand og póstnúmer. Nokkur grunninntaksprófun er gerð fyrir sendingarfangareiti, svo sem staðfestingu á stafrófsröddum, hámarkslengd og tölur. Þótt réttmæti heimilisfangsins sjálfs sé ekki staðfest, er hægt að gera þessa staðfestingu með því að nota sérsniðna þjónustu þriðja aðila.

Póstfangið er notað á alla hluti í körfunni sem „skipið“ er valinn fyrir. Ef verið er að nota greiðsluferli sem er veitt í einingarsafni er ekki hægt að senda staka hluti í körfu á önnur aðsetur. Ef þú þarft þessa hæfileika er hægt að útfæra hana með því að aðlaga kassaeiningarnar.

Eftir að sendingarfangið hefur verið gefið upp eru sendingaraðferðir sem fáanlegar eru frá Dynamics 365 Commerce netverslun er sýnd. Hægt er að stilla sendingaraðferðirnar og netföngin sem þeir styðja í Commerce.

### <a name="payment"></a>Greiðsla

Næsta skref í greiðsluflæðinu er greiðsla. Í rafrænum viðskiptum er hægt að nota margar greiðslumáta til að setja inn pantanir, svo sem kreditkort, gjafakort og vildarpunkta. Einnig er hægt að nota sambland af þessum greiðslumátum. Það fer eftir greiðslumáta sem notaður er, viðbótarupplýsingar gætu verið nauðsynlegar. Til dæmis krefst greiðslu með kreditkorti greiðslu heimilisfang. Greiðslur með kreditkortum eru unnar með því að nota Adyen Payment Connector.

#### <a name="loyalty-points"></a>Vildarpunktar

Í greiðsluferlisflæðinu getur viðskiptavinur sem er meðlimur í vildarforriti og hefur safnað vildarpunkta innleyst þá vildarpunkta fyrir pöntun. Vildarpunktaeiningin er aðeins sýnd ef viðskiptavinurinn er með núverandi vildaraðild. Fyrir notendur sem ekki eru meðlimir og gestir er þessi eining falin.

#### <a name="gift-cards"></a>Gjafakort

Einingasafnið gerir kleift að nota innri gjafakort fyrir pöntun. Til að nota innra gjafakort verður viðskiptavinurinn að vera skráður inn. Til að auka öryggi mælum við með því að þú sérsniðir flæðið með því að nota persónuauðkenni fyrir innri gjafakort.

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

[Yfirlit heimasíðu](quick-tour-home-page.md)

[Yfirlýt upplýsingasíðu afurða](quick-tour-pdp.md)

[Yfirlit yfir síður fyrir stjórnun reikninga](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]