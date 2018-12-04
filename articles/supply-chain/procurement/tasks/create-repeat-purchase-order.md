--- 
title: "Stofna endurtekna innkaupapöntun"
description: "Þessi verklýsing sýnir hvernig á að stofna endurtaka innkaupapöntunina (PO) með því að afrita línur úr eldri innkaupapöntunarskjalinu í nýja Innkaupapöntun eða fyrirliggjandi Innkaupapantana."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Stofna endurtekna innkaupapöntun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna endurtaka innkaupapöntunina (PO) með því að afrita línur úr eldri innkaupapöntunarskjalinu í nýja Innkaupapöntun eða fyrirliggjandi Innkaupapantana. Það eru tvær aðferðir til þess að stofna endurtakar pantanir. Hægt er að nota aðgerðirnar sem eru tiltækar á stigi skjalsins úr Aðgerðarúðunni, eða hægt er að nota aðgerðir línuupplýsingar. Aðgerðir á skjalastigi eru aðallega ætlaðar til að stofna nýja innkaupapöntun með því að bæta upplýsingum úr haus og línum úr annarri pöntun, meðan aðgerð línuupplýsinga er aðallega til að bæta línum við fyrirliggjandi pöntun. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.


## <a name="create-a-new-repeat-purchase-order"></a>Stofna nýja endurtekna innkaupapöntun
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
    * Fyrst reynum við valkostinn að afrita upplýsinga á nýju pöntun.  
2. Smellið á „Nýtt“.
3. Í svæðinu Lánardrottnalykill skal slá inn 'US-101'.
4. Smellið á „Í lagi“.
5. Í aðgerðasvæðinu er smellt á innkaupapöntun.
6. Smella á úr öllu
    * Þetta er síðuna þaðan sem hægt er að afrita úr fyrirliggjandi pantanir yfir í þína pöntun. Mismunandi valmöguleikar eru til staðar hvernig línur eru afritaðar, og mismunandi gerðir af skjölum sem hægt er að afrita úr. Við skoðum valkosti fyrir því hvernig línur eru afritaðar fyrst.   
7. Víkkið út færibreytuhlutann.
    * Svæðið magnstuðull er gagnleg ef nauðsynlegt er að nota magn sem er annað en það sem er í pöntuninni sem verið er að afrita úr. Til dæmis, ef óskað er að panta tvöfalt magnið sem er á línunum sem verið er að afrita úr væri fært inn ' 2' í þessu svæði og kerfið bæta við línur þar sem hefur upphaflegt magn hefur verið tvöfaldað.  
    * Reiturinn Snúa Við formerki styður líka við breytingu á pöntuðu magni með því að breyta formerki magns fyrir pöntunarlínur sem er bætt við. Þetta gæti verið gagnleg ef nauðsynlegt er að bakfæra færsluna, með því að stofna pöntunarlínur sem ógilda færsluna. Þessi valkostur er valinn sjálfvirkt þegar síðan er opnað úr aðgerðina Stofna kreditnótu.  
    * Afrita gjöld valkostur leyfir þér að afrita gjöld yfir í nýja pöntunina úr skjalinu þaðan sem verið er að afrita pöntunarlínur.  
    * Valkosturinn Endurreikna verð notar gildandi verðum og afsláttum frekar en að afrita þær úr skjalinu sem verið er að afrita aðrar upplýsingar úr.  
    * Valkosturinn Afrita nákvæmlega stofnar nákvæmt afrit af gildum í öllum svæðum í haus og línur á pöntunarskjalinu. Sé þessi kostur er ekki valinn eru sjálfgildi notaðar fyrir mörg svæði sem tengjast lánardrottinn og afurðir, rétt eins og ef verið væri að stofna nýtt pöntun handvirkt. Til dæmis, ef pöntun sem verið er að afrita úr hefur hnekkt sjálfgefna reikningslykill fyrir lánardrottinn, yrði sami reikningslykill afritaður í pöntunina þína. Ef þú valdir ekki valkosturinn Afrita nákvæmlega, yrði sjálfgefinn reikningslykill fyrir lánardrottinn notuð í þína pöntun í staðinn.  
    * Valkosturinn eyða innkaupalínum eyðir öllum innkaupapantanalínur sem þegar eru til staðar á innkaupapöntuninni sem verið er að afrita til, áður en nýju línurnar eru notaðar. Notið þennan valkost varlega, þar sem hann eyðir öllum fyrirliggjandi línum án frekari viðvörun .  
    * Ef þú notar valkostinn Afrita pöntunarhaus, þarft ekki að stofna handvirkt hausupplýsingar á nýju pöntunina. Athugið að þessi valkostur veldur því að notuð eru sjálfgefnum gildum fyrir svæðin sem eru tengdar við lánardrottinn. Ef skjalið sem verið er að afrita úr hefur ósjálfgefin gildi sem á að afrita, skal nota valkostinn Afrita nákvæmlega líka.  
8. Draga saman hlutann Færibreytur.
    * Til eru mismunandi upprunar skjala sem hægt er að afrita úr, og hver hefur sérstakan hluta á þessari síðu. Til dæmis, hlutanum innkaupapantanir leyfir þér að afrita úr fyrirliggjandi innkaupapantanir.  
9. Smelltu á línuna fyrir innkaupapöntun sem er með kennið 00015. 
10. Velja línuna með því að smella á gátreit
11. Hreinsið gátreitinn fyrir línu þannig að hún er ekki afrituð í pöntunina.
    * Nú hafa verið valdar 4 línur til að afrita yfir í þína innkaupapöntun. Mögulegt er að velja frekari innkaupapöntunarlínur úr öðrum innkaupapöntunum og afrita þær í pöntunina þína líka. Einnig er hægt að bæta við línur úr annars konar innkaupaskjölum. Næstu skref skoða mismunandi valkostir.  
12. Draga saman hlutanum innkaupapöntun.
13. Víkkið út hlutann staðfesting.
    * Hér er hægt að velja staðfestingar á innkaupapöntunum til að afrita úr. Staðfestingar á innkaupapöntunum eru auðkenndar með viðkomandi innkaupabókarkenni eða kenni innkaupapöntunar.  
14. Stækka eða fella saman hlutann staðfesting.
15. Víkka út hlutann innhreyfingarskjal afurða.
    * Hér er hægt að velja færslubækur innhreyfingarskjala til að afrita úr. Færslubækur innhreyfingarskjala eru auðkenndar með fylgiskjali innhreyfingarskjala eða kenni innkaupapöntunar.   
16. Draga saman út hlutann innhreyfingarskjal afurða.
17. Víkkið út hlutann reikningar.
    * Hér er hægt reikningur lánardrottins sem afrita á úr. Reikningarnir eru auðkenndar með fylgiskjali reikningsins eða kenni innkaupapöntunar.   
18. Fella saman hlutann reikningar.
19. Víkkið út hlutann Valdar línur eða haus til afritunar
    * Þetta yfirlit sýnir samantekt yfir öll skjöl og línur sem hafa verið valdar til afritunar í þína pöntunina.   
20. Fellið saman hlutann Valdar línur eða haus til afritunar
21. Smellið á „Í lagi“.
    * 4 línur sem þú valdir hafa verið afritaðar í nýju innkaupapöntun þína.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Afrita línur í fyrirliggjandi innkaupapöntun
    * Frekar en að Afrita heila pöntun, er algengara að stofna nýja Innkaupapöntun og klára upplýsingarnar í haus Innkaupapöntunar, og afrita einstakar línur úr fyrirliggjandi pantanir.  
1. Smellt er á Innkaup Innkaupapöntunarlína
2. Smella á úr öllu
    * Síða sem opnast er sú sama og var opin áður, en mismunandi valkostir eru valdir þegar hún er opnuð úr yfirliti pöntunarlína. Endurskoðum nú færibreyturnar.   
3. Víkkið út færibreytuhlutann.
    * Valkosturinn eyða innkaupalínum er ekki valinn. Þetta þýðir að hægt er að afrita nýjar línur í pöntunina án þess að fjarlægja fyrirliggjandi línur.   
    * Valkosturinn Afrita pöntunarhaus er einnig ekki valin, þar sem aðeins er verið að bæta fleiri línur í pöntun.   
4. Draga saman hlutann Færibreytur.
    * Í þessu dæmi munum við afrita línur úr fyrirliggjandi innkaupapöntun.   
5. Smelltu á línuna fyrir innkaupapöntun sem er með kennið 00034. 
6. Velja línuna með því að smella á gátreit
    * Athugið að einni pöntunarlínu sem er í þetta Innkaupapöntun er einnig valinn.  
7. Smellið á „Í lagi“.
    * Viðbótar pöntunarlínan hefur verið bætt við innkaupapöntun.  


