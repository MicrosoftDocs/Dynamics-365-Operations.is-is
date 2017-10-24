--- 
title: "Greiðsluyfirlit lánardrottins"
description: "Þessi leiðarvísir fyrir verk fer í gegnum ýmsar aðferðir sem eru notuð til að stofna greiðslur lánardrottna, þar á meðal hvernig á að nota greiðslutillögu eða færa handvirkt inn eingreiðslu."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 020d147744df24b2065e66e5fc68ed5d5479127b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="vendor-payment-overview"></a>Greiðsluyfirlit lánardrottins

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísir fyrir verk fer í gegnum ýmsar aðferðir sem eru notuð til að stofna greiðslur lánardrottna, þar á meðal hvernig á að nota greiðslutillögu eða færa handvirkt inn eingreiðslu. Þessi aðferð notar sýnigögn USMF fyrirtækisins.

1. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Veljið greiðslubók þar sem á að vista greiðslur lánardrottna. 
4. Veljið færslubók eða færa það handvirkt inn.
5. Smellið á „Línur“.
6. Smellt er á Greiðslutillögur
7. Smellt er á Stofna greiðslutillögu
    * Greiðslutillaga er fyrirspurn notuð til að velja reikninga til greiðslu. Hægt er að breyta lista yfir reikninga til greiðslu áður en þú stofnar eða myndar greiðslur lánardrottins.  
8. Velja reikninga til greiðslu samkvæmt gjalddaga, staðgreiðsluafslátt, eða bæði. 
9. Færið inn dagsetningu til að bera saman við gjalddaga eða staðgreiðsluafslátt. 
10. Valfrjálst: Færið Inn greiðsludagsetningu sem er notað fyrir allar greiðslur.
    * Dagsetningin sem færð er inn hér verður greiðsludagur fyrir allar greiðslur sem eru stofnaðar, óháð gjalddaga eða dagsetning staðgreiðsluafsláttar.  
11. Valfrjálst: Slá Inn lágmarks greiðsludag sem má nota sem greiðsludag.
    * Lágmarks greiðsludagur verður fyrstu mögulegu dagsetningu sem er notaður þegar greiðslur eru stofnaðar. Til dæmis, ef reikningur er á gjalddaga eftir lágmarks greiðsludag, mun gjalddaga verða greiðsludagsetningu í stað lágmarks greiðsludags til að greiða reikninginn á síðustu mögulegu dagsetningu.  
12. Færa inn viðbótarskilyrði fyrirspurnarinnar undir Færslur að hafa með.
    * Síunni er oft notað til að takmarka þá reikninga sem eru valdar fyrir greiðslu eftir lánardrottnaflokki eða greiðsluhætti. Til dæmis er hægt að bæta við síu til að greiða einungis reikninga með ávísun í þessari launakeyrslu.  
13. Færa inn viðbótarskilyrði fyrirspurnarinnar eða sjálfgildi greiðslu. 
    * Viðbótar færibreytur er hægt að nota til að skilgreina greiðslugjaldmiðli eða til að virkja miðstýrðar greiðslur fyrir þessa launakeyrslu.  
14. Smellið á „Í lagi“.
    * Niðurstöður fyrirspurnarinnar mun birtast þegar smellt er á í lagi. Ef ekki á að forskoða lista yfir reikninga sem eru valdir til greiðslu er hægt að fara aftur í flýtiflipann Færibreytur og breyta stillingunum Stofna greiðslur án forskoðunar á reikningi = Já.  
15. Velja hnappinn Sýna greiðsluyfirlit til að skoða þær greiðslur sem verður stofnaðar fyrir lánardrottinn á völdum reikningi.
16. Velja hnappinn Fela greiðsluyfirlit til fela greiðslur. 
17. Smellt er á Stofna greiðslur.
    * Áður en valið er að stofna greiðslur er hægt að hægri-smella í hnitanetinu og flytja út lista af reikningum í Excel. Hnappurinn til að Stofna greiðslur stofnar lánadrottnagreiðslur í greiðslubók.  
18. Skanna greiðslum og gangið úr skugga um að greiðsluaðferð er skilgreind fyrir allar greiðslur. 
    * Ef þú myndar greiðslurnar, eins og ávísun er prentuð eða stofnar rafræna greiðslu, verður að skilgreina greiðslumáta. Greiðsluháttur mun einnig falla í vanskil á bankareiknngnum frá því að greiðslan er gerð.  
19. Smella á Nýtt til að stofna eingreiðslu.
    * Hægt er að bæta eingreiðslu í greiðslubók hvenær sem er fyrir bókun. Þetta er gert með því að smella á hnappinn Nýtt og bæta upplýsingar um greiðslu handvirkt, frekar en að nota greiðslutillöguna.  
20. Veljið lánardrottinn sem greiðslan fer til.
21. Ef reikningur er til greiðslu, skal að velja Jafna færslur til að velja reikning til greiðslu.
    * Ef þetta er fyrirframgreiðsla er þetta þrep valfrjálst. Hægt er að stofna greiðslu án þess að velja neinn reikning.  
22. Merkja allar reikninga sem verða greiddir.
    * Ef verið er að Jafna færslur er notuð til að velja reikninga til greiðslu er greiðsluupphæðin sjálfkrafa reiknuð út á samkvæmt þeim reikningum sem á að merkja til greiðslu og hvaða upphæð er færð inn í Upphæð til jöfnunar.  
23. Smellið á „Í lagi“.
24. Ef óskað er að eyða greiðslu skal merkja línuna.
25. Smellið á Eyða.
    * Eyðing greiðslu mun aðeins eyða greiðslunni. Allir reikningar merktir til greiðslu verða enn tiltækir til greiðslu með annarri greiðslu.  
26. Smella á Já.
27. Velja Mynda greiðslu til að prenta ávísanir eða stofna rafræna greiðsluskrá.
28. Velja greiðsluhátt sem á að mynda.
    * Greiðslubók getur innihaldið greiðslur fyrir bæði ávísanir og rafrænar greiðslur, en einungis er hægt að mynda eina greiðslugerð í einu.  
29. Velja bankareikninginn þaðan sem á að búa til greiðslur.
30. Smellið á „Í lagi“.
    * Greiðslur verða aðeins myndaðar fyrir greiðslur sem samsvara þeim greiðsluhætti og bankareikningi sem var valinn.  
31. Ef verið er að mynda ávísanir, veljið Skjal til að tryggja að réttur prentara sé notaður fyrir ávísanirnar.
32. Smellið á „Í lagi“.
33. Smellt er á Í lagi til að búa til greiðslur.
34. Smellt er á Bóka ef allar greiðslur eru samþykktar og myndaðar. 


