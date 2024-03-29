---
title: Stofnað sölupantanir
description: Þessi verklýsing sýnir hvernig á að stofna sölupöntun.
author: Henrikan
ms.date: 04/06/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462f47ab5d85665ed8132e5bfb6dd945c537c1ef
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551725"
---
# <a name="create-sales-orders"></a>Stofnað sölupantanir

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna sölupöntun. Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF. Sölupantanir eru yfirleitt stofnaðar af sölupantanavinnslu. 

## <a name="enter-sales-order-header-details"></a>Færa inn upplýsingar um sölupöntunarhaus
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** velurðu fellilistahnappinn til að opna uppflettinguna.
4. Í listanum skal finna og velja færsla viðskiptavinar.
    - Í þessu dæmi skal velja númer viðskiptamanns US-004.  
5. Veljið **Í lagi**.

## <a name="enter-sales-order-line-details"></a>Færa inn upplýsingar sölupöntunarlína
    
Afurðir sem eru seldar af fyrirtækið þínu koma hugsanlega í afbrigðum sem skilið er á milli með víddir, eins og samsetning, lit, stærð og stíll. Einnig geta afurðir verið settar upp til að nota geymsluvíddir, eins og vöruhús, og bretti og rakningarvíddir, eins og runu og raðnúmer. Þegar þessar víddir er úthlutað þarf að velja gildi fyrir þessar víddir í pöntunarlínunni. Til að auka skilvirkni pöntunarfærslu, gott gæti verið að bæta viðeigandi víddarsvæði við pöntunarhnitanetið.
    
1. Undir hlutanum **Sölupöntunarlínur** velurðu **Sölupöntunarlína**.
2. Veldu **Víddir**.
    
    Í þessu dæmi skal velja víddirnar Lit, Svæði og Vöruhús. Víddir sem valdir eru hér munu birtast hnitaneti sölupöntunar. Ef óskað er eftir að valið verði varanlegt, skal stilla valkostinn **Vista uppsetningu** á Já.
    
3. Veljið **Í lagi**.
4. Í reitnum **Vörunúmer** velurðu fellilistahnappinn til að opna uppflettinguna.
5. Til dæmis, veljið vörunúmerið T0004.
    - Ef varan er hluti af söluflokk, mun vöruheiti birtast sjálfkrafa í svæðinu söluflokkur.  
    - Ef svæðin afurðarvídd innihalda þegar gildi, er þetta vegna þess að gildi var afritað úr afurðarfærslu þar sem það er skilgreint sem sjálfgefið afurðarvídd. Hægt er að breyta sjálfgildinu hvenær sem er.   
6. Í reitnum **Litur** velurðu fellilistahnappinn til að opna uppflettinguna.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í reitnum **Magn** slærðu inn tölu.
    - Ef varan er seld í öðrum einingum en þegar hún var keypt, framleidd og geymd, og mælieining sölu er stillt á afurðarfærsluna, verður þetta gildi sýnt í reitnum **Eining**. Hægt er að breyta gildinu hvenær sem er.   
    - Ef reiturinn **Svæði** inniheldur þegar gildi var gildið afritað úr pöntunarhaus eða pöntunarstillingum sem tengjast afurðinni. Hægt er að breyta gildinu hvenær sem er. Ef svæðið er autt skal velja gildi.   
    - Ef reiturinn **Einingaverð** inniheldur þegar gildi var gildið afritað úr gildum viðskiptasamningi eða úr afurðafærslunni. (Einingarverð geta komið úr sölusamning, en ferlinu fyrir að stofna sölupantanir úr sölusamninga er annan það sýnt hér.) Ef svæðið er autt skal færa inn gildi.   
    - Reiturinn **Afsláttur** inniheldur afslátt á hverja afurðaeiningu. Til að reikna út samtölu upphæðar línuafsláttar, er virði afsláttar margfölduð með línumagni. Ef reiturinn **Afsláttur** inniheldur þegar gildi var gildið afritað úr gildum viðskiptasamningi. Ef svæðið er autt og þú viltgefa viðskiptavini línuafsláttur, færið inn gildi.  
    - Reiturinn **Afsláttarprósenta** inniheldur prósentugildi sem á að lækka brúttó heildarlínuupphæðina um.  Ef reiturinn **Afsláttarprósenta** inniheldur þegar gildi var það afritað úr gildum viðskiptasamningi. Ef svæðið er autt og þú viltgefa viðskiptavini línuafsláttur, færið inn gildi. 
    - Reiturinn **Nettóupphæð** inniheldur gildi sem er reiknað samkvæmt magni og einingaverði línu leiðréttu með afslætti.  Hægt er að hnekkja útreiknað gildi í aðra.  

## <a name="review-the-order-totals"></a>Fara yfir samtölu pöntunar
1. Í **Aðgerðarúðunni** velurðu **Sölupöntun**.
2. Veldu **Samtals**.
    
    Síðan **Samtals** birtir upplýsingar um alla pöntunina. Þar á meðal upphæð millisamtala sem er summa allra nettóupphæða línu leiðrétt fyrir hugsanlega línuafslætti, heildarreikningsupphæðin, sem er upphæð millisamtölu leiðrétt fyrir hugsanlega afslætti á stigi pöntunar, gjöld og virðisaukaskatt, lánamark viðskiptavinar og fleira. Reikningsupphæð er upphæðin sem mun birtast á reikningsskjalið viðskiptavinar.  
    
3. Veldu **Í lagi**.

## <a name="sales-order-creation-performance-enhancement"></a>Afkastaaukning við stofnun sölupöntunar
Nýi eiginleikinn sem kynntur var í forritsútgáfu 10.0.26 dregur úr aukalegum færslustofnunum fyrir töflur **SourceDocumentHeader** og **SourceDocumentLine**. Árangurinn er betri og stærð geymslu minnkar vegna þess að þessar færslur eru ekki búnar til. Þessar undirliggjandi rammatöflur upprunaskjals eru ekki notaðar fyrir sölupantanir í vörunni á þessum tíma og engar tímasettar áætlanir eru um að nota þær. Að virkja þennan eiginleika er talið örugg breyting fyrir bætta frammistöðu. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
