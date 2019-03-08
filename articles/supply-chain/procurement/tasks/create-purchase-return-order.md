---
title: Stofna innkaupaskilapöntun
description: Þessi verklýsing sýnir hvernig á að stofna vöruskilapöntun innkaupa, með því að nota aðgerðina kreditnótu til að afrita línur úr reikningsskjal lánardrottins í nýja Innkaupapöntun.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e080252006d889e2f27db2bccb7b541f3ee4cf9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "354139"
---
# <a name="create-a-purchase-return-order"></a>Stofna innkaupaskilapöntun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna vöruskilapöntun innkaupa, með því að nota aðgerðina kreditnótu til að afrita línur úr reikningsskjal lánardrottins í nýja Innkaupapöntun. Hún sýnir líka hvernig á að staðfesta sendingu og vinna sendingu afurðanna aftur til lánardrottins. Dæmi sem eru sýndar í þessu ferli er hægt að nota sýnigögn USMF-fyrirtækisins. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.


## <a name="create-a-new-purchase-return-order"></a>Búa til nýja vöruskilapöntun innkaupa.
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
    * Fyrsta skrefið er að stofna nýja innkaupapöntun sem verður notuð sem vöruskilapöntun innkaupa.  
2. Smellið á „Nýtt“.
3. Í svæðinu Lánardrottnalykill skal slá inn 'US-102'.
4. Smellið á „Í lagi“.
5. Smellið á „Innkaup“ á aðgerðarúðunni.
6. Smellt er á kreditnótu.
    * Þetta er síðuna þaðan sem hægt er að afrita úr fyrirliggjandi reikningur lánardrottins yfir í þína skilapöntun. Þetta er sama síða og er notuð fyrir aðrar afritunaraðgerðir. En þar sem við höfum opnuð það úr aðgerð kreditnótu , er síðan skilgreind til að styðja við stofnun skilapöntunar sem mótbókar reikninga lánardrottins.  
7. Víkkið út færibreytuhlutann.
    * Valkosturinn viðsnúið formerki er sjálfvirkt valinn og er ekki hægt að breyta. Þetta tryggir að merkið er breytt fyrir magn, og að pöntunarlínur sem bætt verður við verða mótfærð gagnvart reikningi lánardrottins.  
    * Valkosturinn afrita gjöld er sjálfkrafa valinn, og ekki er hægt að breyta því. Þetta þýðir að gjöld úr reikningi lánardrottins er bætt við innkaupaskilapöntun til að mótbóka upprunalega gjaldið. Mögulegt er að breyta breytingunum á hausnum og línunum síðar.  
    * Valkosturinn afrita nákvæmlega er sjálfkrafa valinn, og ekki er hægt að breyta því. Þetta tryggir að nákvæmt afrit er gerð á gildum í öllum reitum á reikningshaus lánardrottins og línum. Þetta þýðir að vöruskilapöntun innkaupa er stofnuð með gildum sem samsvara öllum skilmálum sem eru notuð með reikningsskjali lánardrottins.  
    * Valkosturinn eyða innkaupalínum eyðir sérhverjum innkaupapantanalínur sem þegar eru til staðar á innkaupapöntuninni áður en bætt er við nýju línurnar. Í þessu dæmi höfum við ekki bætt við neinum línum við vöruskilapöntun innkaupa, svo áhrifin yrðu engin. Notið þennan valkost varlega, þar sem hann eyðir öllum fyrirliggjandi línum án frekari viðvörun .  
    * Valkosturinn afrita pöntunarhaus er sjálfkrafa valinn, og ekki er hægt að breyta því. Þetta tryggir að upplýsingar eru afritaðar úr reikningi lánardrottins og notaður í haus vöruskilapöntunar innkaupa. Þetta er gagnlegt þar sem það er hjálpar til að tryggja að vöruskilapöntun innkaupa mótbókar reikninginn með því að nota svipaða afhendingarskilmála.  
8. Draga saman hlutann Færibreytur.
9. Víkkið út hlutann reikningar.
    * Síðan hefur verið opnuð úr aðgerðinni kreditnóta, svo að eini valkosturinn sem er tiltækt er að afrita upplýsingar úr reikningum lánardrottins. Þessi flipi sýnir öll tiltæk reikningum fyrir lánadrottinslykilinn sem er tilgreint í vöruskilapöntun innkaupa sem þú stofnaðir áður.   Reikningarnir eru auðkenndar með fylgiskjali reikningsins eða kenni innkaupapöntunar.  
10. Finna reikningur lánardrottins auðkennt af reikningsnúmeri AP-0006 og auðkenna línuna með því að smella á hvaða svæði í þá línu.
11. Velja línuna með því að smella á gátreit fyrir línuna. 
    * Athugið að tiltækar línur í reikningur lánardrottins eru sjálfkrafa valin ásamt pöntunarinnar. Þessi tiltekna reikningur lánardrottins hefur 2 pöntunarlínur. Fyrir þetta dæmi munum við skila hluta af magninu úr annarri línu.  
12. Auðkennið næstu línu (það sem er með vöru M0006) með því að smella á hvaða svæði í þá línu.
13. Magninu er breytt í 10 í reitnum Magn. Þetta er magnið sem verður að skila til lánardrottins. 
14. Auðkennið fyrstu línu (það sem er með vöru M0005) með því að smella á hvaða svæði í þá línu.
15. Hreinsa gátreitinn fyrir línuna.
    * Aðeins línur sem þú hefur valið verður afrituð á pöntunina þína.  
16. Fella saman hlutann reikningar.
17. Víkkið út hlutann Valdar línur eða haus til afritunar
    * Þetta yfirlit sýnir samantekt yfir öll skjöl og línur sem hafa verið valdar til afritunar í þína pöntunina.  
18. Fellið saman hlutann Valdar línur eða haus til afritunar
19. Smellið á „Í lagi“.
    * Línan sem þú valdir hefur nú verið afrituð í vöruskilapöntun innkaupa. Reiturinn Magnið sýnir -10.   
20. Smellið á birgðir.
21. Smellið á Merking
    * Pöntunarlína sem var stofnuð er merkt gagnvart birgðafærslu úr reikningi lánardrottins. Þetta tryggir að birgðum sem er skilað til lánardrottins er sú sama og birgðir sem barst frá þeim fyrr. Það eru einhverjar aðstæður þar sem merking á sér ekki stað, til dæmis, ef birgða hefur þegar verið merkt sem Notað, eða ef varan er vara sem ekki notar merkingu.  
22. Smellið á „Í lagi“.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Staðfesta og skrá sendingar á vörum
1. Smellið á „Staðfesta“.
2. Smellið á „Móttaka“ á aðgerðarúðunni.
3. Smellið á „Innhreyfingarskjal“.
    * Þessi síða er notuð til að skrá innhreyfingarskjal afurða fyrir innkaupapantanir og einnig vinna skil á vörurnar aftur til lánardrottins. Línur með neikvæðu magni þýða að vörum á að skila til lánardrottins og skjal sem má mynda á þessari síðu er hægt að nota sem fylgiseðil í þessum tilgangi.   
    * Í svæðinu magn, skal velja pantað magn fyrir þetta dæmi.   Þetta tryggir að sendingin verða unnin fyrir allt pantað magn sem pöntunarlínurnar voru stofnaðar með.   
4. Í reitinn innhreyfingarskjal afurða skal slá inn gildi.
    * Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.  
5. Smellið á „Í lagi“.
    * Vörurnar hafa nú verið skráð sem sendar á vöruskilapöntun innkaupa, og búið er að stofna færslubók fyrir innhreyfingarskjal afurða. Hægt er að nota aðgerðina innhreyfing afurðar til að fara yfir færslubækur sem stofnaðar eru með innkaupapöntuninni og sjá hvað var móttekið eða skilað, og hvenær.  

