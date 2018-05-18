--- 
title: "Uppfylla sölusamninga"
description: "Þessi verklýsing sýnir hvernig uppfylla sölusamning með því að tengja sölupantanir við hana."
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
ms.openlocfilehash: f0894bf962c139c2e9e4c9f8d1589fd933afcedb
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="fulfill-sales-agreements"></a>Uppfylla sölusamninga

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig uppfylla sölusamning með því að tengja sölupantanir við hana. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Áður en þessari handbók er ræst, ganga úr skugga um þú sért með virkan sölusamnings af gerðinni "skuldbinding um gildi afurðar". Einnig er hægt að keyra leiðarvísi fyrir verk kallast "Stofna sölusamninga".  




## <a name="release-a-sales-order-from-the-agreement"></a>Losa sölupöntun úr samninginn
1. Fara í Sölu og markaðssetningu > Sölusamningar > Sölusamninga.
2. Opna samning sem á að losa pöntunina gagnvart á listanum.
3. Á Aðgerðasvæðinu skal smellt á sölusamningur.
4. Smellt er á úttektarpöntun.
    * Eins og texti yfir Stofna úttektarpöntun bendir á, eru upplýsingar sem þarf fyrir sölupöntunarlínur verður mismunandi eftir því hvort samningurinn er byggður á magni eða virði.  
    * Samningurinn í þessari handbók er af gerðinni "skuldbinding um gildi afurðar". Þetta er ástæðan fyrir því að línuhluti þessarar síðu er auður. Ef skuldbindingin var byggð á magni myndu upplýsingar línunnar vera afritaðar úr samningnum.  
5. Smellið á „Stofna“.
    * Skilaboðin tilkynnir sölupöntun hefur verið stofnuð. Þar sem pöntunin inniheldur engar línur þarf að bæta við upplýsingum um pöntunarlínu til að ljúka útgáfuferlinu.   
6. Lokið síðunni.
7. Lokið síðunni.
8. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
9. Finna og opna pöntun var stofnuð í kjölfar þess að pöntunina var losa í fyrra verki á listanum.
10. Smella á bæta Við línu.
11. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
12. Í svæðinu vörunúmer, Færa inn eða velja vöru sem er tilgreind í tengdum sölusamningnum.
13. Færið inn númer í reitnum „Magn“.
    * Gangið úr skugga um að færa inn magn sem knýr nettóupphæð undir gildi tengt sölusamning.  
    * Athugið þar sem sölupöntunin er tengd við samning, er umsamin afsláttarprósenta beitt í pöntunarlínuna.  
14. Smellið á „Uppfæra línu“.
15. Smellið á „Viðhengi“.
    * Tengdar síða samnings sýnir Kenni og skilmálum samningsins þaðan sem línan er losuð frá.  
16. Lokið síðunni.
17. Smellið á „Almennt“ á aðgerðarúðunni.
18. Smelltu á tengdur Sölusamningar
19. Víkkið út hlutann „Upplýsingar um línu“.
20. Smelltu á uppfyllingarflipann.
    * Uppfyllingarflipi sýnir yfirlit yfir allar sölupöntunarlínur sem eru tengdar við skuldbindingu, og stöðu uppfyllingar þeirra, sem og upphæð eða magn sem enn hefur ekki verið losuð.   
21. Lokið síðunni.
22. Lokið síðunni.
23. Lokið síðunni.

## <a name="apply-sales-agreement-in-the-order-process"></a>Jafna sölusamninga í pöntunarferli
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Finna og velja viðskiptavinar sem tilgreindur er í sölusamningnum á listanum.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Útvíkka eða draga saman hlutann Almennt.
7. Í reitnum kenni sölusamningur skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smella á Já.
10. Smellið á „Í lagi“.
11. Í listanum skal merkja valda línu.
12. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
13. Í svæðinu vörunúmer, Færa inn eða velja vöru sem er tilgreind í tengdum sölusamningnum.
14. Í listanum skal smella á tengilinn í valinni línu.
15. Smelltu á Vista.
16. Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.
17. Smellið á „Bóka fylgiseðil“.
18. Víkkið út færibreytuhlutann.
19. Velja skal Já í reitnum Bókun.
20. Smellið á „Í lagi“.
21. Smellið á „Í lagi“.
22. Smellið á „Almennt“ á aðgerðarúðunni.
23. Smelltu á tengdur Sölusamningar
24. Smelltu á uppfyllingarflipann.


