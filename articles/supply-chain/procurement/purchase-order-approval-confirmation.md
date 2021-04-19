---
title: Samþykkt og staðfesting innkaupapanta
description: Þetta efnisatriði lýsir stöðum sem innkaupapöntunin fer í gegnum þegar hún hefur verið stofnuð og áhrif þess að virkja breytingastjórnun á innkaupapöntunum.
author: kamaybac
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f1f6971e645a0aae8679c94a4bbd4cba946dc3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825423"
---
# <a name="approve-and-confirm-purchase-orders"></a>Samþykkt og staðfesting innkaupapanta

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir stöðum sem innkaupapöntunin fer í gegnum þegar hún hefur verið stofnuð og áhrif þess að virkja breytingastjórnun á innkaupapöntunum.

Eftir að innkaupapöntunina (PO) hefur verið stofnuð, gæti það þurft að fara í gegnum samþykktarferli. Eftir að lánardrottinn hefur samþykkt pöntun, er Innkaupapöntunin stillt á stöðuna **Staðfest**.

## <a name="approval-of-purchase-orders"></a>Samþykki innkaupapantana
Innkaupapantanir sem ekki nota breytingastjórnun hafa stöðuna **Samþykkt** um leið og þær eru stofnaðar, á meðan innaupapantanir sem nota breytingastjórnun hafa stöðuna **Drög** þegar þau eru stofnuð. Innkaupapöntun sem hefur verið stofnuð með staðfestingu áætlaðrar pöntunar úr aðaláætlanagerð er alltaf stillt á stöðuna **Samþykkt**, óháð stillingum breytingastjórnunar. Innkaupapöntun Stofnar birgðafærslur þegar hún er komin í **Samþykkt** stöðu. Þess vegna birtist þær birgðir ekki eins og þær séu til staðar til frátektar erða merkingar fyrr en pöntun er samþykkt.

Þú virkja breytingastjórnun fyrir innkaupapantanir með uppsetningu **Virkja breytingastjórnun** valkostinn á á **færibreytur innkaupa og aðfanga** síðu. Þegar breytingastjórnun er virkjuð verða innkaupapantanir að fara gegnum samþykktarverkflæði eftir að þær hafa verið lokið. Supply Chain Management er með verkflæðisritil þar sem hægt er að skilgreina verkflæði til að tákna samþykktarferli. Þetta verkflæði getur falið í sér reglur fyrir sjálfvirkt samþykki, reglum sem ákvarða hverjum verður úthlutað til að samþykkja tilteknar innkaupapantanir, og reglur fyrir stigmanga verkflæði sem hefur beðið eftir samþykki í lengri tíma. Hægt er að virkja breytingastjórnunarferlið fyrir alla lánardrottna eða fyrir tiltekna lánardrottna. einnig Er hægt að setja upp ferlið þannig að hægt er að hnekkja því fyrir einstakar innkaupapantanir.

Þegar breytingastjórnun er virkjuð færast innkaupapantanir í gegnum sex samþykktarstaða, úr **Drög** að **lokið**. Eftir að pöntun hefur verið samþykkt, verða notendur sem vilja breyta því að nota **Breytingabeiðni** aðgerð.

| Staða samþykkis | Lýsing                                                                      | beiðni um breytingu er virkjuð |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Drög           | Innkaupapöntunin er drög og hefur ekki verið send til samþykkis í verkflæði Innkaupapöntunar.     | Nr                        |
| Í skoðun       | Innkaupapöntunin var send til samþykkis í verkflæði Innkaupapöntunar. Bíður samþykkis       | Nei                        |
| Hafnað        | Innkaupapöntunin var hafnað meðan á samþykktarferlinu stendur.                                 | Nei                        |
| Samþykkt        | Innkaupapöntunin var samþykkt.                                                             | Já                       |
| Staðfest       | Innkaupapöntunin var samþykkt. Ekki er hægt að staðfesta Innkaupapöntun fyrr en hún hefur verið samþykkt.        | Já                       |
| Lokið       | Innkaupapöntunin var gerð endanleg. Hún er nú fjárhagslega lokuð og ekki lengur hægt að breyta. | Nr                        |

## <a name="confirming-purchase-orders"></a>Staðfesta innkaupapantanir
Innkaupapantanir með stöðu samþykkis **Samþykkt** geta fara gegnum viðbótarskref áður en þær eru staðfestar. Til dæmis gæti þurft að senda fyrirspurn um innkaup til lánardrottins til að spyrjast fyrir um verð, afslættir eða afhendingardagsetningar. Í þessu tilfelli er hægt að stilla Innkaupapöntun á **í ytri yfirferð** stöðu með því að nota í **Innkaupafyrirspurn** aðgerð.

Lánardrottna sem eru sett upp til að geta nota gátt Lánardrottins getur að endurskoða pantanir í gátt og samþykkja eða hafna þeim. Á meðan þetta endurskoðunarferli fer fram hefur Innkaupapöntunin stöðuna **í ytri yfirferð**. Mögulegt er að skilgreina gátt lánardrottins þannig að staðfesting frá lánardrottni staðfesti sjálfkrafa pöntun í Supply Chain Management. Einnig er hægt handvirkt að staðfesta Innkaupapöntun eftir að staðfesting berst frá lánardrottni. Ef lánardrottinn hafnar Innkaupapöntun, er höfnunin móttekin ásamt ástæðan fyrir höfnun og tillögur fyrir breytingum. Í þessu tilfelli, helst stöðu Innkaupapöntunin **í ytri yfirferð**.

Einnig er kostur að mynda bráðabirgða staðfesting fyrir pöntun áður en raunveruleg staðfesting hefur verið unnin. Þessi valkostur stofnar einfaldlega skýrslu sem er hægt að deila með lánardrottins. Hann stofnar ekki neinar færslubókarupplýsingar.

Eftir að lánardrottinn hefur samþykkt pöntunina, er næsta skref að skrá Innkaupapöntun sem skuldbundna. Hægt er að ljúka þessu skrefi með því að nota annað hvort **Staðfestingu** aðgerð eða **Staðfesta** aðgerð. Báðar þessar aðgerðir stilla samþykktarstaða pöntunar á **Staðfest**. Staðfesting pöntunar setur í gang tvö aukaleg ferli:

-   Færslubók er stofnuð til að geyma nákvæmt afrit af því hvað var staðfest í kerfinu. Stundum krefjast pantanir breytinga, og fleiri færslubækur eru stofnaðar eftir að uppfærð pöntunin er staðfest. Þessar færslubækur leyfa þér að skoða sögu mismunandi útgáfa af pöntuninni sem voru staðfest.
-   Dreifingar á fjárhagsupphæð stofnaðar og athuganir á pöntunum og fjárhagsáætlun fara fram ef þessi aðgerð hefur verið virkjuð. Ef annað hvort athugun virkar ekki, berast villuskilaboð sem tilgreinir að verður að gera breytingar á Innkaupapöntun áður en hægt er að staðfesta hana aftur.

Lánardrottinn gæti beðið um einhver trygging væri lögð fram fyrir greiðslu kaupa Það eru mismunandi aðferðir veita þessa tryggingu innan viðskiptaskuldaferla. Til dæmis tekur aðgerðina **Fyrirframgreiðslu** frá fjármagn fyrir Innkaupapöntunina og þessari fyrirframgreiðslu er skráð á Innkaupapöntunina.

## <a name="changing-purchase-orders"></a>Breyting innkaupapantana
Í sumum tilvikum, þarf hugsanlega að breyta Innkaupapöntun eftir að hún hefur náð samþykktarstaða **Samþykkt** eða **Staðfest**.

Ef Innkaupapöntunin var stofnuð með því að nota ferli breytingastjórnunar, er hægt að gera breytingar með því að kalla aftur fram pöntun eða, ef pöntunin hefur þegar verið samþykkt, með því að nota **Breytingabeiðni** aðgerð. Í þessu tilfelli er samþykktarstaðan breytt aftur í **Drög**, og síðan er hægt að breyta pöntuninni. Eftir að lokið hefur verið við breytingarnar, gæti þurft að senda innkaupapöntunina til samþykktar aftur. Hægt er að skilgreina gerðir breytinga sem krefjast endursamþykktar með því að nota í **endursamþykktarregla fyrir innkaupapantanir** stefnureglu á **Innkaupareglur** síðuna.

Ef hluti af pöntuðu magni fyrir línu Innkaupapöntunar hefur verið afhentu, er ekki hægt að breyta pantaða magninu þegar innkaupapöntunin er **Drög**. Hins vegar getur þú breytt magninu **Eftirstöðvar afhendingar** á línunni fyrir innkaupapöntunina sem er í stöðunni **Drög**.

Eftir að pöntun hefur verið staðfest getur þú ekki lengur eytt henni. Hins vegar er hægt að hætta við heildarmagn eða eftirstöðvum magns í pöntun, svo lengi sem ekki hefur verið móttekið magnið eða reikningsfært magnið. Síðan er hægt að nota **Ljúka** aðgerð til að koma í veg fyrir frekari vinnslu. 


## <a name="canceling-purchase-orders"></a>Hætt við innkaupapantanir

Hægt er að hætta við innkaupapöntun með því að nota aðgerðina **Hætta við** á hausnum.

Ef magnið hefur verið skráð, móttekið eða reiknað að hluta, er aðeins hægt að hætta við það magn sem ekki hefur verið skráð, fengið eða fengið reikning. Pöntunarmagnið er síðan minnkað í samræmi við það. Þegar magnið á línunni er uppfært er staða línunnar einnig uppfærð. Til dæmis er upphaflega magnið á línunni 5 og magnið 3 er móttekið. Í þessu tilfelli er aðeins hægt að hætta við tvo. Línan er síðan uppfærð í stöðuna **Móttekið**.

Ef afhendingarafgangi er bætt við pöntunarlínuna og það fer yfir magnið á pöntunarlínunni, þá afturkallar aðgerðin **Hætta við** ekki umframmagnið. Í staðinn er línan áfram í stöðunni **Opin pöntun**, vegna þess að hún er með eftirstandandi magn. Til dæmis er upphaflega magnið á línunni 5 og eftirstöðvar afhendingar eru 7. Ef pöntuninni er aflýst, eru fimm felld niður og 2 verður eftir í magni, eins og þú sérð í birgðafærslunum.

Til að hætta við allt magn á innkaupalínu ættir þú að hætta við magn eftir afhendingu á línunni. Línan verður síðan uppfærð í stöðuna **Hætt við**.

Ef innkaupapöntun er undir breytingastjórnun verður að leggja fram allar breytingar, svo sem afturköllun á pöntun eða eftirstöðvar afhendingar, til verkflæðiskerfisins og samþykkja áður en hægt er að ljúka ferlinu og hægt er að uppfæra birgðafærslurnar sem felldar niður.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit yfir innkaupapöntun](purchase-order-overview.md)

[Stofna innkaupapantanir](purchase-order-creation.md)

[Innhreyfingarskjal jafnað við innkaupapantanir](product-receipt-against-purchase-orders.md)

[Yfirlit yfir reikninga lánardrottna](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]