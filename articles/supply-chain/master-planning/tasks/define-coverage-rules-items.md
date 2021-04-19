---
title: Skilgreina þekjureglur fyrir vörur
description: Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.
author: ShylaThompson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff2d83a01f366517502bfc5c885b6f963bd945ca
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829714"
---
# <a name="define-coverage-rules-for-items"></a>Skilgreina þekjureglur fyrir vörur

[!include [banner](../../includes/banner.md)]

Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru. Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.


## <a name="create-a-coverage-group"></a>Stofna þekjuflokk
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Þekjuflokkar**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Þekjuflokkur** slærðu inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Dagatal** skal slá inn gildi. Velja dagatalið sem aðaláætlanagerð notar til að stofna tillögur um áfyllingu fyrir vörur í þessum flokki.  
6. Í reitnum **Þekjukóði** velurðu valkost. Veldu „Þarfir“ fyrir þetta ferli.  
7. Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚90‘. Fyrir vörur í þessum flokki, mun aðaláætlanagerð stofna tillögur að áfyllingu fyrir upp að 90 daga til framtíðar.  
8. Í reitinn **Neikvæðir dagar** færirðu inn „1“.
9. Í reitinn **Jákvæðir dagar** færirðu inn „1“.
10. Stækka eða fella saman hlutann **Annað**.
11. Undir hlutanum **Öryggismörk á dögum**, í reitinn **Mörk innhreyfinga bætt við dagsetningu þarfa**, slærðu inn '1'. Til dæmis, ef mörk innhreyfinga eru stillt á 1 dag og innkaupapöntunarlína er áætluð til móttöku þann 15. maí reikna mörk innhreyfinga móttökudagsetningu sem 16. maí.  
12. Í reitnum **Mörk úthreyfinga dregin af dagsetningu þarfa** skal færa inn 1. Til dæmis, ef öryggismörk eru stillt á 1 dag og sölupöntunarlína er áætluð til afhendingar þann 15. maí reiknar röðun leiðrétta móttökudagsetningu sem 14. maí.  
13. Í svæðinu **Endurpöntunarmagni bætt við afhendingartíma vöru** skal færa inn 1.
14. Smellt er á **Vista**.

## <a name="create-a-new-product"></a>Stofna nýja afurð
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Afurðarnúmer** skal slá inn gildi.
4. Í reitinn **Afurðarheiti** skal slá inn gildi.
5. Í reitnum **Vörulíkanaflokkur** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum **Vöruflokkur** skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Í reitnum **Geymsluvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.
12. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
13. Í listanum skal smella á tengilinn í valinni línu.
14. Í reitnum **Rakningarvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Í listanum skal smella á tengilinn í valinni línu.
17. Smellt er á **OK**.

## <a name="setup-default-order-settings"></a>Setja upp sjálfgefnar pöntunarstillingar
1. Í **Aðgerðarrúðunni** er smellt á **Áætlun**.
2. Undir **Panta stillingar** smellirðu á **Sjálfgefnar pöntunarstillingar**.
3. Undir **Innkaupapöntun**, í reitnum **Sjálfgefið svæði** færirðu inn svæðið sem er notað sem sjálfgefið þegar innkaupapantanir eru stofnaðar.
4. Í reitnum **Sjálfgefið vöruhús** skal slá inn staðinn þar sem varan er geymd.
5. Stækka eða fella saman hlutann **Birgðir**.
6. Í reitinn **Margfeldi** skal slá inn „10“.
7. Í reitinn **Lágmarksmagn í pöntun** slærðu inn '10'.
8. Í reitinn **Hámarksmagn í pöntun** slærðu inn '100'.
9. Í reitinn **Staðlað magn í pöntun** slærðu inn '10'.
10. Í reitinn **Afhendingartími innkaupa** skal slá inn tölu.
11. Velja skal eða hreinsa gátreitinn **Vinnudagar**.
12. Smellt er á **Vista**.
13. Í reitnum **Sjálfgefin gerð pöntunar** velurðu „Innkaupapantanir“.
14. Smellt er á **Vista**.
15. Lokið síðunni. Lokaðu skjámyndinni Sjálfgefnar pöntunarstillingar.  

## <a name="add-an-item-to-a-coverage-group"></a>Bæta vöru við þekjuflokk
1. Stækka eða fella saman hlutann **Áætlun**.
2. Í reitnum **Þekjuflokkur** skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum finnurðu **Þekjuflokk** sem hefur verið stofnaður.
4. Í listanum skal smella á tengilinn í valinni línu.

## <a name="create-item-coverage-rules"></a>Stofna þekjureglur vöru
1. Í **Aðgerðarrúðunni** er smellt á **Áætlun**.
2. Undir **Þekja** smellirðu á **Vöruþekju**.
3. Smellt er á **Nýtt**.
4. Smelltu á flipann **Almennt**.
5. Merkið við gátreitinn í hausnum í stillingunum **Hnekking þekjuflokks**.
6. Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚60‘. Jafnvel þótt vörur í þekjuflokki Þarfir séu áætlaðar 90 daga fram í tímann, verður varan áætluð 60 daga fram í tímann.  
7. Í reitinn **Neikvæðir dagar** færirðu inn „2“.
8. Í reitinn **Jákvæðir dagar** færirðu inn „2“.
9. Smellt er á flipann **Afhendingartími**.
10. Merktu í reitinn í haus **Innkaupa**.
11. Í reitnum **Innkaupatími** skal slá inn ‚5‘.
12. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]