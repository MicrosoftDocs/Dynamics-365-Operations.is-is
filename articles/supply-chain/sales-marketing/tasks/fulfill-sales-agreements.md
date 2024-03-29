---
title: Uppfylla sölusamninga
description: Þessi verklýsing sýnir hvernig uppfylla sölusamning með því að tengja sölupantanir við hana.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe26d528e42da61d47fd2448e071bf9025c08f5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573394"
---
# <a name="fulfill-sales-agreements"></a>Uppfylla sölusamninga

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]