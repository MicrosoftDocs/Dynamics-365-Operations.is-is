--- 
title: "Stofnað sölupantanir"
description: "Þessi verklýsing sýnir hvernig á að stofna sölupöntun."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4ccd2c4ace41f07dce14498031e3cc29ecb61b1c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-orders"></a>Stofnað sölupantanir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna sölupöntun. Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF. Sölupantanir eru yfirleitt stofnaðar af sölupantanavinnslu. 




## <a name="enter-sales-order-header-details"></a>Færa inn upplýsingar um sölupöntunarhaus
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja færsla viðskiptavinar.
    * Í þessu dæmi skal velja númer viðskiptamanns US-004.  
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Í lagi“.

## <a name="enter-sales-order-line-details"></a>Færa inn upplýsingar sölupöntunarlína
    * Afurðir sem eru seldar af fyrirtækið þínu koma hugsanlega í afbrigðum sem skilið er á milli með víddir, eins og samsetning, lit, stærð og stíll. Einnig geta afurðir verið settar upp til að nota geymsluvíddir, eins og vöruhús, og bretti og rekkavíddir, eins og runu og raðnúmer. Þegar þessar víddir er úthlutað þarf að velja gildi fyrir þessar víddir í pöntunarlínunni. Til að auka skilvirkni pöntunarfærslu, gott gæti verið að bæta viðeigandi víddarsvæði við pöntunarhnitanetið.  
1. Smellið á „Sölupöntunarlína“.
2. Smellt er á Víddir.
    * Í þessu dæmi skal velja víddirnar Lit, Svæði og Vöruhús. Víddir sem valdir eru hér munu birtast hnitaneti sölupöntunar. Ef óskað er eftir að valið verði varanlegt, skal setja  Já á valkostinn Vista uppsetningu.   
3. Smellið á „Í lagi“.
4. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
5. Til dæmis, veljið vörunúmerið T0004.
6. Í listanum skal smella á tengilinn í valinni línu.
    * Ef varan er hluti af söluflokk, mun vöruheiti birtast sjálfkrafa í svæðinu söluflokkur.  
    * Ef svæðin afurðarvídd innihalda þegar gildi, er þetta vegna þess að gildi var afritað úr afurðarfærslu þar sem það er skilgreint sem sjálfgefið afurðarvídd. Hægt er að breyta sjálfgildinu hvenær sem er.   
7. Í reitnum Litur skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Færið inn númer í reitnum „Magn“.
    * Ef varan er seld í öðrum einingum en þegar hún hefur verið keypt, framleitt og geymt, og mælieining sölu er stillt á afurðarfærsluna, verður þetta gildi sýnd í reitinn Eining. Hægt er að breyta gildinu hvenær sem er.   
    * Ef þetta svæði þegar inniheldur gildi, gildi var afrituð úr pöntunarhaus eða pöntunarstillingar sem tengjast vörunni. Hægt er að breyta gildinu hvenær sem er. Ef svæðið er autt skal velja gildi.   
    * Ef svæðið einingarverð inniheldur gildi var gildi afritað frá gildum viðskiptasamningi eða úr afurðarfærslu. (Einingarverð geta komið úr sölusamning, en ferlinu fyrir að stofna sölupantanir úr sölusamninga er annan það sýnt hér.) Ef svæðið er autt skal færa inn gildi.   
    * Svæðið Afsláttur inniheldur afsláttarupphæð eftir einingu afurðar. Til að reikna út samtölu upphæðar línuafsláttar, er virði afsláttar margfölduð með línumagni.    Ef svæðið afsláttur inniheldur gildi var gildi afritað úr gildum verðsamningi. Ef svæðið er autt og þú viltgefa viðskiptavini línuafsláttur, færið inn gildi.  
    * Svæðið Afsláttarprósenta inniheldur gildi prósentuafsláttar sem brúttó heildarlínuupphæðin er minnkað um.  Ef svæðið afsláttarprósenta inniheldur gildi var það afritað úr gildum verðsamningi. Ef svæðið er autt og þú viltgefa viðskiptavini línuafsláttur, færið inn gildi.  
    * Svæðið Nettóupphæð inniheldur gildi sem er reiknaður á grundvelli magni línunnar og einingarverði leiðréttu með afslætti.  Hægt er að hnekkja útreiknað gildi í aðra.  

## <a name="review-the-order-totals"></a>Fara yfir samtölu pöntunar
1. Smellið á „Sölupöntun“ á aðgerðarúðunni.
2. Smellið á „Samtölur“.
    * Samtölur síðan birtir upplýsingar um alla pöntunina. Þar á meðal upphæð millisamtala sem er summa allra nettóupphæða línu leiðrétt fyrir hugsanlega línuafslætti, heildarreikningsupphæðin, sem er upphæð millisamtölu leiðrétt fyrir hugsanlega afslætti á stigi pöntunar, gjöld og virðisaukaskatt, lánamark viðskiptavinar og fleira.  Reikningsupphæð er upphæðin sem mun birtast á reikningsskjalið viðskiptavinar.  
3. Smellið á „Í lagi“.


