---
title: Innsýn í greiðslu viðskiptavinar (forútgáfa)
description: Þetta efni lýsir getu greiðsluinnsýna sem hjálpar til við að bæta skilning á dæmigerðum greiðsluaðferðum einstakra viðskiptavina og geta greint aðstæður sem réttlæta að hefja innheimtuferli fyrr en þú hefur gert annars.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773978"
---
# <a name="customer-payment-insights-preview"></a>Innsýn í greiðslu viðskiptavinar (forútgáfa)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efni lýsir getu greiðsluinnsýna sem hjálpar til við að bæta skilning á dæmigerðum greiðsluaðferðum einstakra viðskiptavina og geta greint aðstæður sem réttlæta að hefja innheimtuferli fyrr en þú gætir hafa annars gert. 

## <a name="overview"></a>Yfirlit

Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinir greiða reikninga sína. Þessi skortur á innsæi leiðir til ónákvæmari spáa um sjóðstreymi, innheimtuferla sem hefjast of seint og pantana sem gefnar eru út til viðskiptavina sem kunna að standa ekki í skilum með greiðslu. Innsýn í greiðslu viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur, sem auðveldar fyrirtækjum að stofna innheimtustefnur sem auka líkurnar á því að greitt sé á réttum tíma. 

## <a name="predictions"></a>Spár

Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sín með því að hjálpa þeim að greina auðveldlega þá reikninga sem líklega verða greiddir seint og gera viðeigandi ráðstafanir sem bæta möguleika þeirra á að fá greitt á réttum tíma.

Með því að nota vélanámslíkan, sem nýtir sögulega reikninga, greiðslur og gögn viðskiptavina, spáir innsýn í greiðslu viðskiptavinar (forskoðun) nákvæmar hvenær viðskiptavinur muni greiða útistandandi reikning.

Fyrir hvern opinn reikning spáir innsýn í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:

-   Líkur á að greiðsla fari fram á réttum tíma 
-   Líkur á að greiðsla fari seint fram
-   Líkur á að greiðsla fari fram eftir gjalddaga

Til að hjálpa fyrirtækjum að skilja heildargreiðslufjárhæðina sem þeir geta búist við frá viðskiptavini í einu af þremur fötunum, á réttum tíma, seint og mjög seint, veitir greiðsla innsýn viðskiptavina (foskoðun) samansafn af væntanlegum greiðslum.

[![Samanlögð sýn á spá um greiðslur](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Einnig er hverjum reikningi úthlutað líkum á greiðslu á réttum tíma. Ef líkurnar á greiðslu á réttum tíma eru undir 50% eru reikningarnir merktir með rauðum hring til að gefa til kynna að þessir reikningar geti þurft innheimtuathygli. 

[![Listi yfir greiðslulíkur](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Innsýn greiðslu viðskiptavina (forskoðun) veitir einnig samhengisupplýsingar til að skýra spána, svo sem helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavina. Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsverkþáttur; innheimtu ferlið hefst ekki fyrr en innheimtuseðlar koma til gjalddaga. 

Með greiðslu innsýn viðskiptavina (forskoðun), geta fyrirtæki verið meira fyrirbyggjandi varðandi innheimtu. Þau þurfa ekki lengur að bíða eftir að færslur komi á gjalddaga til að hefja innheimtuferli. Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á að fá greitt á réttum tíma. Greiðsluspá veitir fyrirtækjum einnig þær upplýsingar sem þarf til að réttlæta að hefja innheimtuferlið snemma.

## <a name="methodology"></a>Aðferð

Erfitt er að þróa og dreifa AI lausn. Það þarf hóp gagnafræðinga, fagaðila og verkfræðinga sem vinna í langan tíma til að móta, þróa, dreifa og viðhalda nothæfri AI lausn. Við erum að auðvelda að dreifingu og notkun á AI lausnum í Finance. Við erum að forpakka AI lausnum í Finance sem eru byggðar ofan á Microsoft AI Builder. Með einum smelli á hnapp getur notandi beitt AI lausninni og byrjað að nýta ávinninginn af snjallspám. Ef fyrirtæki er ekki ánægt með nákvæmni spáa getur yfirnotandi, aftur með einum smelli, farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár. Þegar þeir eru tilbúnir geta þeir þjálfað og birt breytingarnar og nýþjálfaða líkanið verður sjálfkrafa sótt fyrir spár í Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)

Vinsamlegast sendu tölvupóst til [Innsýn í greiðslu viðskiptavinar (forútgáfa)](mailto:fiap@microsoft.com) ef þú hefur áhuga á að prófa innsýn í greiðslu viðskiptavinar (forútgáfu).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) geta mögulega notað minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


