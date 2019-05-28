---
title: Innhreyfingarskjal jafnað við innkaupapantanir
description: Þetta efnisatriði lýsir ýmsum valkostum til að skrá afurðir sem mótteknar.
author: FrankDahl
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fea28da19c0aa1e9083091d0693404e0d8cb173c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554344"
---
# <a name="product-receipt-against-purchase-orders"></a>Innhreyfingarskjal jafnað við innkaupapantanir

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Þetta efnisatriði lýsir ýmsum valkostum til að skrá afurðir sem mótteknar.

Innhreyfingarskjal afurða er ferli við að skrá afurðir sem hafa verið pantaðar,svo hægt sé að vinna innkaupapöntunarlínur (PO) fyrir reikningsfærslu. Í sumum tilvikum, fara afurðir í gegnum forskráningu, þar sem viðbótarupplýsingar frá birgi er skráð áður en afurðirnar eru mótteknar. Þegar afurðirnar berast, eru þær fyrstu merkt **Skráð**. Afurðir gæti síðan fara gegnum fleiri ferli, eins og gæðastjórnun, áður en þeir eru að lokum merkt **Móttekið**.

## <a name="preregistration-asn"></a>Forskráning (ASN)
Birgjar gæti verið að deila upplýsingum um afurðir sem verður send. Í þessu tilfelli er hægt að forskrá afurðir til að skrá þessar upplýsingar áður en afurðirnar eru mótteknar. með því að Forskrá afurðir er dregið úr magn vinnunnar sem er krafist við skráningu vara og móttöku. Birgjar getur veitt vöruupplýsingar rafrænt gegnum fyrirframtilkynningu um sendingu (ASN) sem er þá sjálfvirkt skráð í kerfið. Upplýsingarnar í á ASN inniheldur magn afurða sem verður sent og dagsetningu þegar þeir verða sendar. Á ASN gætu einnig innihaldið upplýsingar eins og rununúmer eða raðnúmer. Skráning á ASN fer fram í á **flutningsstjórnun** kerfiseiningu.

## <a name="registration"></a>Skráning
Skráning innhreyfingarskjala á sér oft stað við innhlið í vöruhúsi. Það er framkvæmd með því að nota annaðhvort handbært tæki eða gegnum komubækur. Einnig er hægt að skrá handvirkt innhreyfingarskjal afurða með því að nota **Skráningu** aðgerð á **Innkaupapöntun** síðu. Í báðum tilvikum eru afurðir merktar sem **Skráð**. Athugið að afurðir sem ekki enn merkt sem **Móttekið**.  

Afurðir sem eru mótteknar í vöruhús gæti fara í gegnum gæðaskoðun áður en gengið er frá þeim í birgðir. Bæði Gæðapantanir eða biðgeymslupantanir má nota til að framkvæma gæðaeftirlit. Ef gæðapantanir eru notaðar, er hægt að skilgreina ferli til að læsa tímabundið vörur með frátekning meðan þær eru skoðaðar. Ef biðgeymslupantanir eru notaðar, eru afurðir fluttar í annað vöruhús til skoðunar. Vöruhúsið er þekkt sem biðgeymsluvöruhús. Í báðum gæðaskoðunarferlunum, gætu sumar vörur rýrnað, annað hvort þar sem þeir ekki samræmist gæðakröfum eða af því gæðaeftirlit felur í sér eyðileggingarprófun á sýnishorn afurðarinnar.

## <a name="product-receipt"></a>Innhreyfingarskjal afurðar
Oftast er aðgerðin **Innhreyfingarskjal afurða** á **Innkaupapantanir** síða notuð til að merkja vörur sem **Móttekið** á Innkaupapöntunina. **Bókun innhreyfingarskjals afurða** síðuna hefur mismunandi valkostir fyrir það magn sem er bókfært sem móttekið. Til dæmis er hægt að stilla **Magn** reitinn á **Pantað magn** eða **Magn sem móttaka á nú**. Einnig, ef komuferli vöruhúss hefur verið notuð, stillirðu þetta svæði oft á **Skráð magn**. Hægt er að breyta magni á hverri pöntunarlínu sem verður merkt sem **Móttekið**, til að gera grein fyrir hvers kyns misræmi svo sem umframafhendingu og undirafhendingu. Við móttöku afurða, verður að tilgreina kennimerki innhreyfingarskjals afurðar, sem yfirleitt er tilvísun í fylgiseðils frá birgi. Þetta kennimerki er krafist í bókhaldi þar sem hún gerir athuganir eða úttektir á fylgiseðlum birgis gagnvart þess sem hefur verið móttökuð mögulegar, og reikningsfærðar birgðir eða kostnaðar.  

Hægt er að stofna innkaupapantanir fyrir afurðir sem ekki eru ætlaðar að vera birgðir en skoðast sem útgjöld. Þessi tegund inniheldur pöntunarlínur þar sem afurðir eru merktar sem **Ekki í birgðum** samkvæmt birgðalíkanaflokki þeirra, og líka línur sem nota innkaupaflokka. Í þessu tilfelli fara vörur hugsanlega ekki í gegnum komuskráningu og móttöku í vöruhúsi. Í staðinn er **Innhreyfingarskjal afurða** aðgerð notuð til að skrá á innhreyfingu beint á Innkaupapöntuninni, og móttöku er grundvölluð á pantaðs magns, ekki skráð magn.  

Hægt er að stofna innkaupapöntunarlínur þar sem **Nýja eign** valkosturinn er virkjaður. Þessi valkostur gefur til kynna að innkaupin skuli teljast eign frekar en birgðir. Í þessu tilfelli ákvarða ákvörðunarreglur eigna sem hafa verið skilgreindir hvort innkaupin afurða eða flokks fer yfir tiltekin þröskulda,og þarf því að gera grein fyrir sem eign og fara í gegnum eignastýringu Einnig er hægt að gera innkaup sem beinast í átt að eign. Í þessu tilfelli er upphæð leiðrétt eins og við á.  

Hægt er að velja margar pantanir og vinna úr móttöku á öllum þeim pöntunum saman. Þessi nálgun er ekki notuð mjög oft, en þú vilt kannski nota hana ef birgir hefur sameinað sendingar fyrir þíg í einn stakan farm. Við móttöku afurða vegna innkaupanna, er aðgerði til að framkvæma safnuppfærslur. Safnuppfærsla gera þér kleift að bóka stakan fylgiseðil frá birgi fyrir meira en eina innkaupapöntun.  

Innkaupapantanir gætu verið stofnaðar úr sölupöntun þar sem **Beina afhendingu** valkostur var valinn. Þegar notuð er bein afhending, eru afurðir aldrei mótteknar í vöruhúsinu þínu heldur eru sendar beint frá birgi til viðskiptavinar. Í þessu tilfelli er móttakan yfirleitt skráðar beint á Innkaupapöntunina. Innhreyfingu er hægt að gera sjálfkrafa, eins og með innþættingu á rafrænum gagnaskiptum (EDI) við birgi. Einnig, ef Innkaupapöntunin er Innkaupapöntun innan samstæðu gerir Microsoft Dynamics 365 for Finance and Operations móttökuna á sjálfvirkan hátt á sölupöntun innan samstæðu þegar sendingin á sér stað. Þegar notuð er bein afhending, eru afurðir enn bókaðar sem birgðir, jafnvel þótt efnislega berist þær ekki í vöruhús. Þess vegna þegar innhreyfingarskjal afurða er skráður á Innkaupapöntun, er sölupöntun sjálfkrafa uppfært með fylgiseðill, þannig að heildarbreytingin í birgðir er 0 (núll). Í aðstæðum beinnar afhendingar ætti ekki að krefjast forskráningar. Ef verið er að nota vöruhús sem eru virkjaðar fyrir vöruhúsakerfi, er hægt komast hjá kröfunni um skráningu númeraplötu með því að tilgreina sýndarvöruhús í staðinn. Þú Tilgreina þetta vöruhús í á **vöruhús Beinnar afhendingar** reitnum á afurðinni. 

Eftir að innhreyfingarskjal afurða hefur verið unnið á Innkaupapöntunin, er staða Innkaupapantana stillt á **Móttekið** til að tilgreina a' hægt er að vinna reikningur fyrir pöntunina. Hægt er að skoða upplýsingar um afurðir sem hafa þegar verið móttekin með **færslubækur innhreyfingarskjals Afurða** síðu.  

Hægt er að opna þessa síðu úr á **Innhreyfing** aðgerðaflokk á **Innkaupapöntun** síðu. Upplýsingarnar í færslubækurnar inniheldur upplýsingar um magn, dagsetningar og víddir.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit yfir innkaupapöntun](purchase-order-overview.md)

[Stofnun innkaupapöntunar](purchase-order-creation.md)

[Staðfesting innkaupapöntunar og samþykki](purchase-order-approval-confirmation.md)

[Yfirlit yfir lánardrottnareikninga](../../financials/accounts-payable/vendor-invoices-overview.md)



