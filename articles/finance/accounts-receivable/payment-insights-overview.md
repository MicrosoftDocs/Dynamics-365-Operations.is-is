---
title: Innsýn í greiðslu viðskiptavinar (forútgáfa)
description: Í þessu efnisatriði er lýsing á greiðsluinnsýn sem getur aukið skilning á dæmigerðri greiðsluhegðun einstakra viðskiptavina. Þessi eiginleiki getur hjálpað til við að auðkenna aðstæður sem réttlæta innheimtuferli fyrr en annars hefði verið.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 82b301b4b8ba61375a53a8fe6220628500f6cf3d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359318"
---
# <a name="customer-payment-insights-preview"></a>Innsýn í greiðslu viðskiptavinar (forútgáfa)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er lýsing á greiðsluinnsýn sem getur aukið skilning á dæmigerðri greiðsluhegðun einstakra viðskiptavina. Þessi eiginleiki getur hjálpað til við að auðkenna aðstæður sem réttlæta innheimtuferli fyrr en annars hefði verið. 

## <a name="overview"></a>Yfirlit

Það getur verið erfitt að spá fyrir um hvenær viðskiptavinir munu greiða reikninga sína. Þessi skortur á innsæi leiðir til ónákvæmari spáa um sjóðstreymi, innheimtuferla sem hefjast of seint og pantana sem gefnar eru út til viðskiptavina sem kunna að standa ekki í skilum með greiðslu. Innsýn í greiðslur viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur. Þessar upplýsingar geta hjálpað fyrirtækjum að búa til innheimtuaðferðir sem auka líkurnar á því að fá greitt á réttum tíma. 

## <a name="predictions"></a>Spár

Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sín með því að hjálpa þeim að greina auðveldlega þá reikninga sem líklega verða greiddir seint og gera viðeigandi ráðstafanir sem bæta möguleika þeirra á að fá greitt á réttum tíma.

Með því að nota vélanámslíkan, sem nýtir sögulega reikninga, greiðslur og gögn viðskiptavina, spáir innsýn í greiðslu viðskiptavinar (forskoðun) nákvæmar hvenær viðskiptavinur muni greiða útistandandi reikning.

Fyrir hvern opinn reikning getur innsýn spáð í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:

-   Líkur á að greiðsla fari fram á réttum tíma 
-   Líkur á að greiðsla fari seint fram
-   Líkur á að greiðsla fari fram eftir gjalddaga

Innsýn í greiðslur viðskiptavinar (forskoðun) veitir einnig samandregið yfirlit yfir áætlaðar greiðslur sem geta hjálpað fyrirtækjum að skilja heildargreiðsluupphæðina sem þeir geta búist við að viðskiptavinur greiði í einum af þremur römmum; á réttum tíma, seint og mjög seint.

[![Samanlögð sýn á spá um greiðslur.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Einnig er hverjum reikningi úthlutað líkum á greiðslu á réttum tíma. Ef líkurnar á greiðslu á réttum tíma eru undir 50% eru reikningarnir merktir með rauðum hring til að gefa til kynna að þessir reikningar geti þurft innheimtuathygli. 

[![Listi yfir greiðslulíkur.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Innsýn greiðslu viðskiptavina (forskoðun) veitir einnig samhengisupplýsingar til að skýra spána, svo sem helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavina. Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsverkþáttur; innheimtu ferlið hefst ekki fyrr en innheimtuseðlar koma til gjalddaga. 

Með greiðslu innsýn viðskiptavina (forskoðun), geta fyrirtæki verið meira fyrirbyggjandi varðandi innheimtu. Þau þurfa ekki lengur að bíða eftir að færslur komi á gjalddaga til að hefja innheimtuferli. Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á að fá greitt á réttum tíma. Greiðsluspá veitir fyrirtækjum einnig þær upplýsingar sem þarf til að réttlæta að hefja innheimtuferlið snemma.

## <a name="methodology"></a>Aðferð

Erfitt er að þróa og dreifa AI lausn. Fjöldi gagnasérfræðinga, sérfræðinga á viðkomandi sviði og verkfræðinga þarf að vinna lengi að mótun, þróun, uppsetningu og viðhaldi nothæfrar AI-lausnar. Við erum að auðvelda að dreifingu og notkun á AI lausnum í Finance. Við erum að forpakka AI lausnum í Finance sem eru byggðar ofan á Microsoft AI Builder. Með einum smelli á hnapp getur notandi beitt AI lausninni og byrjað að nýta ávinninginn af snjallspám. Ef fyrirtæki er ekki ánægt með nákvæmni spáa getur yfirnotandi, aftur með einum smelli, farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár. Þegar þeir eru tilbúnir geta þeir þjálfað og birt breytingarnar og nýþjálfaða líkanið verður sjálfkrafa sótt fyrir spár í Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)

Sendið tölvupóst til [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er fyrir því að prófa „Innsýn í greiðslur viðskiptavinar (forskoðun)“.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) geta mögulega notað minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]