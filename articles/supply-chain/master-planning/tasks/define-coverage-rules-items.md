---
title: Skilgreina þekjureglur fyrir vörur
description: Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru. Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3947c8a51facfb02012cc8e9a3ffd5887073bd9
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860614"
---
# <a name="define-coverage-rules-for-items"></a>Skilgreina þekjureglur fyrir vörur

[!include [banner](../../includes/banner.md)]

Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru. Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.

## <a name="create-a-coverage-group"></a>Stofna þekjuflokk

Stofnaðu þekjuflokk með því að gera eftirfarandi:

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Þekjuflokkar**.
1. Veljið **Nýtt**.
1. Í reitnum **Þekjuflokkur** slærðu inn gildi.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í reitinn **Dagatal** skal slá inn gildi. Velja dagatalið sem aðaláætlanagerð notar til að stofna tillögur um áfyllingu fyrir vörur í þessum flokki.  
1. Í reitnum **Þekjukóði** velurðu valkost. Veldu „Þarfir“ fyrir þetta ferli.  
1. Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚90‘. Fyrir vörur í þessum flokki, mun aðaláætlanagerð stofna tillögur að áfyllingu fyrir upp að 90 daga til framtíðar.  
1. Í reitinn **Neikvæðir dagar** færirðu inn „1“.
1. Í reitinn **Jákvæðir dagar** færirðu inn „1“.
1. Stækka eða fella saman hlutann **Annað**.
1. Undir hlutanum **Öryggismörk á dögum**, í reitinn **Mörk innhreyfinga bætt við dagsetningu þarfa**, slærðu inn '1'. Til dæmis, ef mörk innhreyfinga eru stillt á 1 dag og innkaupapöntunarlína er áætluð til móttöku þann 15. maí reikna mörk innhreyfinga móttökudagsetningu sem 16. maí.
1. Í reitnum **Mörk úthreyfinga dregin af dagsetningu þarfa** skal færa inn 1. Til dæmis, ef öryggismörk eru stillt á 1 dag og sölupöntunarlína er áætluð til afhendingar þann 15. maí reiknar röðun leiðrétta móttökudagsetningu sem 14. maí.  
1. Í svæðinu **Endurpöntunarmagni bætt við afhendingartíma vöru** skal færa inn 1.
1. Veldu **Vista**.

## <a name="create-a-new-product"></a>Stofna nýja afurð

Stofna nýja afurð með því að gera eftirfarandi:

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.
1. Veljið **Nýtt**.
1. Í reitnum **Afurðarnúmer** skal slá inn gildi.
1. Í reitinn **Afurðarheiti** skal slá inn gildi.
1. Í reitnum **Vörulíkanaflokkur** velurðu fellilistahnappinn til að opna leitina.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í listanum skal velja tengilinn í valinni línu.
1. Í reitnum **Vöruflokkur** velurðu fellilistahnappinn til að opna leitina.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í listanum skal velja tengilinn í valinni línu.
1. Í reitnum **Geymsluvíddarflokkur** velurðu fellilistahnappinn til að opna leitina.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í listanum skal velja tengilinn í valinni línu.
1. Í reitnum **Rakningarvíddarflokkur** velurðu fellilistahnappinn til að opna leitina.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í listanum skal velja tengilinn í valinni línu.
1. Veldu **Í lagi**.

## <a name="set-up-default-order-settings"></a>Setja upp sjálfgefnar pöntunarstillingar

Settu upp sjálfgefnar pöntunarstillingar með því að gera eftirfarandi:

1. Á **Aðgerðarsvæðinu** skal velja **Áætlun**.
1. Undir **Pöntunarstillingar** skal velja **Sjálfgefnar pöntunarstillingar**.
1. Undir **Innkaupapöntun**, í reitnum **Sjálfgefið svæði** færirðu inn svæðið sem er notað sem sjálfgefið þegar innkaupapantanir eru stofnaðar.
1. Í reitnum **Sjálfgefið vöruhús** skal slá inn staðinn þar sem varan er geymd.
1. Stækka eða fella saman hlutann **Birgðir**.
1. Í reitinn **Margfeldi** skal slá inn „10“.
1. Í reitinn **Lágmarksmagn í pöntun** slærðu inn '10'.
1. Í reitinn **Hámarksmagn í pöntun** slærðu inn '100'.
1. Í reitinn **Staðlað magn í pöntun** slærðu inn '10'.
1. Í reitinn **Afhendingartími innkaupa** skal slá inn tölu.
1. Velja skal eða hreinsa gátreitinn **Vinnudagar**.
1. Veldu **Vista**.
1. Í reitnum **Sjálfgefin gerð pöntunar** velurðu „Innkaupapantanir“.
1. Veldu **Vista**.
1. Lokið síðunni. Lokaðu skjámyndinni Sjálfgefnar pöntunarstillingar.  

## <a name="add-an-item-to-a-coverage-group"></a>Bæta vöru við þekjuflokk

Bættu vöru við þekjuflokk með því að gera eftirfarandi:

1. Stækka eða fella saman hlutann **Áætlun**.
1. Í reitnum **Þekjuflokkur** skal velja fellilistahnappinn til að opna leitina.
1. Í listanum finnurðu **Þekjuflokk** sem hefur verið stofnaður.
1. Í listanum skal velja tengilinn í valinni línu.

## <a name="create-item-coverage-rules"></a>Stofna þekjureglur vöru

Stofnaðu þekjureglur vöru með því að gera eftirfarandi:

1. Á **Aðgerðarsvæðinu** skal velja **Áætlun**.
1. Undir **Þekju** skal velja **Vöruþekja**.
1. Veljið **Nýtt**.
1. Veldu flipann **Almennt**.
1. Merkið við gátreitinn í hausnum í stillingunum **Hnekking þekjuflokks**.
1. Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚60‘. Jafnvel þótt vörur í þekjuflokki Þarfir séu áætlaðar 90 daga fram í tímann, verður varan áætluð 60 daga fram í tímann.  
1. Í reitinn **Neikvæðir dagar** færirðu inn „2“.
1. Í reitinn **Jákvæðir dagar** færirðu inn „2“.
1. Veldu flipann **Afhendingartími**.
1. Merktu í reitinn í haus **Innkaupa**.
1. Í reitnum **Innkaupatími** skal slá inn ‚5‘.
1. Veldu **Vista**.

> [!NOTE]
> Fyrir framleidda hluti, **Framleiðslutími** er notað ef engin leið er fyrir hlutinn. Ef virk leið hefur verið tengd vörunni mun aðalskipulag tímasetja pöntunina og reikna út dagsetningar hennar í samræmi við leiðartíma og getu tilfönganna (ef við á).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
