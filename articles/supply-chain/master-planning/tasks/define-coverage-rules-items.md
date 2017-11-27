--- 
title: "Skilgreina þekjureglur fyrir vörur"
description: "Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: fe92393cc264df68f084db6974f7d4607d37d3ab
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="define-coverage-rules-for-items"></a>Skilgreina þekjureglur fyrir vörur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru. Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.


## <a name="create-a-coverage-group"></a>Stofna þekjuflokk
1. Fara í þekjuflokka.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu Þekjuflokkur.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Dagatal skal slá inn gildi.
    * Velja dagatalið sem aðaláætlanagerð notar til að stofna tillögur um áfyllingu fyrir vörur í þessum flokki.  
6. Veljið valkost í svæðinu Þekjukóði.
    * Veljið Þarfir fyrir þessa færslu.  
7. Í reitnum Tímamörk tryggingar (dagar) skal slá inn ‚90‘.
    * Fyrir vörur í þessum flokki, mun aðaláætlanagerð stofna tillögur að áfyllingu fyrir upp að 90 daga til framtíðar.  
8. Fært er inn 1 í reitinn Neikvætt Dagar.
9. Fært er inn 1 í reitinn Jákvætt Dagar.
10. Stækka eða fella saman hlutann Annað.
11. Í svæðinu Mörk innhreyfinga bætt við dagsetningu þarfa, færðu inn 1.
    * Til dæmis, ef mörk innhreyfinga eru stillt á 1 dag og innkaupapöntunarlína er áætluð til móttöku þann 15. maí reikna mörk innhreyfinga móttökudagsetningu sem 16. maí.  
12. Í svæðinu Mörk úthreyfinga dregin af dagsetningu þarfa skal færa inn 1.
    * Til dæmis, ef öryggismörk eru stillt á 1 dag og sölupöntunarlína er áætluð til afhendingar þann 15. maí reiknar röðun leiðrétta móttökudagsetningu sem 14. maí.  
13. Í svæðinu Endurpöntunarmagni bætt við afhendingartíma vöru skal færa inn 1.
14. Smellið á „Vista“.

## <a name="create-a-new-product"></a>Stofna nýja afurð
1. Farðu í Losaðar afurðir.
2. Smellið á „Nýtt“.
3. Í reitinn Afurðarnúmer skal slá inn gildi.
4. Sláið inn gildi í reitinn Afurðarheiti.
5. Í reitnum Vörulíkanaflokkur skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum Vöruflokkur skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Í reitnum Geymsluvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.
12. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
13. Í listanum skal smella á tengilinn í valinni línu.
14. Í reitnum Rakningarvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Í listanum skal smella á tengilinn í valinni línu.
17. Smellið á „Í lagi“.

## <a name="setup-default-order-settings"></a>Setja upp sjálfgefnar pöntunarstillingar
1. Smellið á „Áætlun“ á aðgerðarúðunni.
2. Smellt er á sjálfgefnar pöntunarstillingar.
3. Í svæðinu innkaupasvæði, færðu inn svæðið sem er notað sem sjálfgefið þegar innkaupapantanir eru stofnaðar.
4. Í reitnum Birgðasvæði skal slá inn staðinn þar sem varan er geymd.
5. Stækka eða fella saman hlutann Birgðir.
6. Margir er stillt á '10'.
7. Setja lágm. pöntunarmagn á ‚10‘.
8. Setja Hám. pöntunarmagn á ‚100‘.
9. Stilltu staðlað pöntunarmagn á ‚10‘.
10. Í reitinn Afhendingartími innkaupa skal slá inn númer.
11. Velja skal eða hreinsa gátreitinn Vinnudagar.
12. Smellið á „Vista“.
13. Í reitnum sjálfgefin gerð pöntunar velurðu „Innkaupapantanir“.
14. Smellið á „Vista“.
15. Lokið síðunni.
    * Lokaðu skjámyndinni Sjálfgefnar pöntunarstillingar.  

## <a name="add-an-item-to-a-coverage-group"></a>Bæta vöru við þekjuflokk
1. Stækka eða fella saman hlutann Áætlun.
2. Í reitnum Þekjuflokkur skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum, Finna þekjuflokk sem hafa verið stofnaðar.
4. Í listanum skal smella á tengilinn í valinni línu.

## <a name="create-item-coverage-rules"></a>Stofna þekjureglur vöru
1. Smellið á „Áætlun“ á aðgerðarúðunni.
2. Smellt er á vöruþekju.
3. Smellið á „Nýtt“.
4. Smellið á flipann „Almennt“.
5. Merkið við gátreitinn á haus Hnekking þekjuflokks.
6. Í reitnum Tímamörk tryggingar (dagar) skal slá inn ‚60‘.
    * Jafnvel þótt vörur í þekjuflokki Þarfir séu áætlaðar 90 daga fram í tímann, verður varan áætluð 60 daga fram í tímann.  
7. Fært er inn 2 í reitinn Neikvætt Dagar.
8. Fært er inn 2 í reitinn Jákvætt Dagar.
9. Smellt er á flipanum afhendingartími.
10. Merktu í reitinn í haus Innkaupa.
11. Í reitnum Innkaupatími skal slá inn ‚5‘.
12. Smellið á „Vista“.


