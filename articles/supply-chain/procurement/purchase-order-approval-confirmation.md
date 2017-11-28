---
title: "Staðfesta og samþykkja innkaupantanir"
description: "Þessi skrá lýsir stöðum sem innkaupapöntunina (PO) fer í gegnum þegar hún hefur verið stofnuð og áhrif þess virkja breytingastjórnun á innkaupapöntunum."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1c7209c91f3821a77e9b127d767c78df403ff6cc
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="approve-and-confirm-purchase-orders"></a>Staðfesta og samþykkja innkaupantanir

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Þessi skrá lýsir stöðum sem innkaupapöntunina (PO) fer í gegnum þegar hún hefur verið stofnuð og áhrif þess virkja breytingastjórnun á innkaupapöntunum.

Eftir að innkaupapöntunina (PO) hefur verið stofnuð, gæti það þurft að fara í gegnum samþykktarferli. Eftir að lánardrottinn hefur samþykkt pöntun, er Innkaupapöntunin stillt á stöðuna **Staðfest**.

## <a name="approval-of-purchase-orders"></a>Samþykki innkaupapantana
Innkaupapantanir sem ekki nota breytingastjórnun hafa stöðuna **Samþykkt** um leið og þær eru stofnaðar, á meðan innaupapantanir sem nota breytingastjórnun hafa stöðuna **Drög** þegar þau eru stofnuð. Innkaupapöntun sem hefur verið stofnuð með staðfestingu áætlaðrar pöntunar úr aðaláætlanagerð er alltaf stillt á stöðuna **Samþykkt**, óháð stillingum breytingastjórnunar. Innkaupapöntun Stofnar birgðafærslur þegar hún er komin í **Samþykkt** stöðu. Þess vegna birtist sú birgðir ekki eins og þær séu til staðar til frátektar erða merkingar  fyrr en pöntun er samþykkt.  

Þú virkja breytingastjórnun fyrir innkaupapantanir með uppsetningu **Virkja breytingastjórnun** valkostinn á á **færibreytur innkaupa og aðfanga** síðu. Þegar breytingastjórnun er virkjuð verða innkaupapantanir að fara gegnum samþykktarverkflæði eftir að þær hafa verið lokið. Microsoft Dynamics 365 for Finance and Operations er með verkflæðisritil þar sem hægt er að skilgreina verkflæði til að tákna samþykktarferli. Þetta verkflæði getur falið í sér reglur fyrir sjálfvirkt samþykki, reglum sem ákvarða hverjum verður úthlutað til að samþykkja tilteknar innkaupapantanir, og reglur fyrir stigmanga verkflæði sem hefur beðið eftir samþykki í lengri tíma. Hægt er að virkja breytingastjórnunarferlið fyrir alla lánardrottna eða fyrir tiltekna lánardrottna. einnig Er hægt að setja upp ferlið þannig að hægt er að hnekkja því fyrir einstakar innkaupapantanir.  

Þegar breytingastjórnun er virkjuð færast innkaupapantanir í gegnum sex samþykktarstaða, úr **Drög** að **lokið**. Eftir að pöntun hefur verið samþykkt, verða notendur sem vilja breyta því að nota **Breytingabeiðni** aðgerð.

| Staða samþykkis | Lýsing                                                                      | beiðni um breytingu er virkjuð |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Drög           | Innkaupapöntunin er drög og hefur ekki verið send til samþykkis í verkflæði Innkaupapöntunar.     | Nei                        |
| Í skoðun       | Innkaupapöntunin var send til samþykkis í verkflæði Innkaupapöntunar. Bíður samþykkis       | Nei                        |
| Hafnað        | Innkaupapöntunin var hafnað meðan á samþykktarferlinu stendur.                                 | Nei                        |
| Samþykkt        | Innkaupapöntunin var samþykkt.                                                             | Já                       |
| Staðfest       | Innkaupapöntunin var samþykkt. Ekki er hægt að staðfesta Innkaupapöntun þar til hún hefur verið samþykkt.        | Já                       |
| Lokið       | Innkaupapöntunin var gerð endanleg. Hún er nú fjárhagslega lokuð og ekki lengur hægt að breyta. | Nei                        |

## <a name="confirming-purchase-orders"></a>Staðfesta innkaupapantanir
Innkaupapantanir með stöðu samþykkis **Samþykkt** geta fara gegnum viðbótarskref áður en þær eru staðfestar. Til dæmis gæti þurft að senda fyrirspurn um innkaup til lánardrottins til að spyrjast fyrir um verð, afslættir eða afhendingardagsetningar. Í þessu tilfelli er hægt að stilla Innkaupapöntun á **í ytri yfirferð** stöðu með því að nota í **Innkaupafyrirspurn** aðgerð.  

Lánardrottna sem eru sett upp til að geta nota gátt Lánardrottins getur að endurskoða pantanir í gátt og samþykkja eða hafna þeim. Á meðan þetta endurskoðunarferli fer fram hefur Innkaupapöntunin stöðuna **í ytri yfirferð**. Mögulegt er að skilgreina gátt lánardrottins þannig að staðfesting frá lánardrottni staðfesti sjálfkrafa pöntun í Finance and Operations. Einnig er hægt handvirkt að staðfesta Innkaupapöntun eftir að staðfesting berst frá lánardrottni. Ef lánardrottinn hafnar Innkaupapöntun, er  höfnuninni móttekin ásamt ástæðan fyrir höfnun og tillögur fyrir breytingum. Í þessu tilfelli, helst stöðu Innkaupapöntunin **í ytri yfirferð**.  

Einnig er kostur að mynda bráðabirgða staðfesting fyrir pöntun áður en raunveruleg staðfesting hefur verið unnin. Þessi valkostur stofnar einfaldlega skýrslu sem er hægt að deila með lánardrottins. Það stofna ekki neinar færslubókarupplýsingar.  

Eftir að lánardrottinn hefur samþykkt pöntunina, er næsta skref að skrá Innkaupapöntun sem skuldbundna. Hægt er að ljúka þessu skrefi með því að nota annað hvort **Staðfestingu** aðgerð eða **Staðfesta** aðgerð. Báðar þessar aðgerðir stilla samþykktarstaða pöntunar á  **Staðfest**. Staðfesting pöntunar setur í gang tvö aukaleg ferli:

-   Færslubók er stofnuð til að geyma nákvæmt afrit af því hvað var staðfest í kerfinu. Stundum krefjast pantanir breytinga, og fleiri færslubækur eru stofnaðar eftir að uppfærð pöntunin er staðfest. Þessar færslubækur leyfa þér að skoða sögu mismunandi útgáfa af pöntuninni sem voru staðfest.
-   Dreifingar á fjárhagsupphæð stofnaðar og athuganir á pöntunum og fjárhagsáætlun fara fram ef þessi aðgerð hefur verið virkjuð. Ef annað hvort athugun virkar ekki, berast villuskilaboð sem tilgreinir að verður að gera breytingar á Innkaupapöntun áður en hægt er að staðfesta hana aftur.

Lánardrottinn gæti beðið um einhver trygging væri lögð fram fyrir greiðslu kaupa Það eru mismunandi aðferðir veita þessa tryggingu innan viðskiptaskuldaferla. Til dæmis tekur aðgerðina **Fyrirframgreiðslu** frá fjármagn fyrir Innkaupapöntunina og þessari fyrirframgreiðslu er skráð á Innkaupapöntunina.

## <a name="changing-purchase-orders"></a>Breyting innkaupapantana
Í sumum tilvikum, þarf hugsanlega að breyta Innkaupapöntun eftir að hún hefur náð samþykktarstaða **Samþykkt** eða **Staðfest**.  

Ef Innkaupapöntunin var stofnuð með því að nota ferli breytingastjórnunar, er hægt að gera breytingar með því að kalla aftur fram pöntun eða, ef pöntunin hefur þegar verið samþykkt, með því að nota **Breytingabeiðni** aðgerð. Í þessu tilfelli er samþykktarstaðan breytt aftur í **Drög**, og síðan er hægt að breyta pöntuninni. Eftir að lokið hefur verið við breytingarnar, gæti þurft að senda innkaupapöntunina til samþykktar aftur. Hægt er að skilgreina gerðir breytinga sem krefjast endursamþykktar með því að nota í **endursamþykktarregla fyrir innkaupapantanir** stefnureglu á **Innkaupareglur** síðuna.  

Ef hluti af pöntuðu magni fyrir línu Innkaupapöntunar hefur verið afhent, er ekki hægt að breyta pantaða magninu. Hins vegar er hægt að breyta **Eftirstöðvar afhendingar** magninu á línunni. Síðan er hægt að nota **Ljúka** aðgerð til að hætta við línur og koma í veg fyrir frekari vinnslu. 

Eftir að pöntun hefur verið staðfest getur þú ekki lengur eytt henni. Hins vegar er hægt að hætta við heildarmagn eða eftirstöðvum magns í pöntun, svo lengi sem ekki hefur verið móttekið magnið eða reikningsfært magnið.

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir innkaupapöntun](purchase-order-overview.md)

[Stofnun innkaupapöntunar](purchase-order-creation.md)

[innhreyfingarskjal afurða gagnvart innkaupapantanir](product-receipt-against-purchase-orders.md)

[Yfirlit yfir lánardrottnareikninga](../../financials/accounts-payable/vendor-invoices-overview.md)




