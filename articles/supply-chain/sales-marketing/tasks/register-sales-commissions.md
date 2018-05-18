--- 
title: "Skrá söluþóknun"
description: "Þessi verklýsing sýnir hvernig sölulaun eru reiknuð og skráð."
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
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Skrá söluþóknun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig sölulaun eru reiknuð og skráð. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Áður en þessari handbók er ræst þarf að keyra leiðbeiningar sem kallast "Setja upp reglur um söluþóknun" til að tryggja að allar nauðsynlegar uppsetningar á útreikningi sölulauna séu til staðar.

Athugið þær tölur viðskiptavina og vara sem voru valdar fyrir sölulaunaferlið og notið þær þegar beðið er um að stofna sölupöntun í þessari handbók.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Reikningsfæra sölupöntun sem uppfyllir skilyrði sölumanns fyrir þóknun
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Í lagi“.
7. Í aðgerðasvæðinu er smellt á valkostir.
8. Smellið á skoða Breytingu.
9. Smellið á skoða Haus.
10. Víkka út hlutann Uppsetning.
    * Gildið í reitnum Söluflokkur stendur fyrir flokk með einn eða fleiri sölumenn sem úthlutað. Fólk innan flokksins eru þau sem fá sölulaun þegar pöntunin er reikningsfærð, samkvæmt fyrirframskilgreindum taxta og dreifingu.   Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.  Söluflokkurinn er einnig afritaður í sölupöntunarlínu. Hægt er að breyta þannig að hún sé önnur en sú sem er í haus og/eða á milli lína.  
    * Gildið í svæðinu Sölulaunaflokkur stendur fyrir flokk sem var stofnaður fyrir einn eða fleiri vegna rakningar á sölulaunum.   Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.   
11. Í aðgerðasvæðinu er smellt á valkostir.
12. Smellið á skoða Breytingu.
13. Smellið á Línuyfirlit.
14. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
15. Á listanum, skal velja vöru sem er uppsett fyrir þóknanir. 
16. Færið inn númer í reitnum „Magn“.
    * Athugið nettóupphæð línunnar. Hún stendur fyrir sölutekjur sem í þessu dæmi eru grunnurinn fyrir útreikning þóknunar.  
17. Smellið á „Vista“.
18. Smellið á „Reikningur“ á aðgerðarúðunni.
19. Smellið á „Reikningur“.
20. Víkkið út færibreytuhlutann.
21. Veljið „Allt“ á svæðinu „Magn“.
22. Velja skal Já í reitnum Bókun.
23. Smellið á „Í lagi“.
24. Smellið á „Í lagi“.
    * Það gæti tekið um það bil mínútu að bóka færsluna. Heimila vinnslu að ljúka og ekki loka síðunni.  

## <a name="review-the-registered-sales-commissions"></a>Fara yfir skráðar söluþóknanir
1. Smellið á „Reikningur“ á aðgerðarúðunni.
2. Smellið á „Reikningur“.
3. Smellið á „Reikningur“ á aðgerðarúðunni.
4. Smelltu á Þóknunarfærslur.
    * Yfirlitsflipinn birtir línur sem sýna upphæðir sölulauna sem greiða á sölufulltrúum sem eru tengdir reikningsfærðu sölupöntuninni. Endurskoðum nú upplýsingarnar.     
    * Ef handbókin "Setja upp reglur sölu þóknun" var notuð til að setja upp sölulaunaflokk eru tveir sölumenn til að móttaka sölulaun og sölulaununum er skipt skipt jafnt á milli þeirra.  
    * Í þessu dæmi er heildarupphæð þóknun reiknuð sem hlutfall sölutekna (nettóupphæð pöntunarlínu).   
5. Lokið síðunni.
6. Smellt er á Fylgiskjalið.
    * Hægt er að skoða færslur fylgiskjala fyrir upphæðir sölulauna sem hafa verið bókaðar í forskilgreindu þóknunarkostnaður og þóknun lykla lánardrottna.  


