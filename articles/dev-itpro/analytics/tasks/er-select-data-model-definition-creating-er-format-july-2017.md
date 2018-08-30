--- 
title: "Velja skilgreiningar gagnalíkans þegar snið er búið til"
description: "Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Velja skilgreiningar gagnalíkans þegar snið er búið til

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka. 

Þetta ferli sýnir hvernig rótaratriði líkans getu verið valið sem skilgreining gagnalíkans fyrir innsetningu Rafræn skýrslugerð (ER) grunnstilling sniðs sem er hönnuð til að búa til rafræn skjöl. Í þessu dæmi muntu bæta við nýrri Rafræn skýrslugerð grunnstilling sniðs fyrir sýnifyrirtækið, Litware, Inc. 

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota öll gagnasöfn.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, Stofna skilgreiningarveitu og merkja hana sem virka.  
2. Smelltu á Grunnstillingar skýrslugerðar

## <a name="add-a-new-er-data-model-configuration"></a>Bæta við nýrri grunnstillingu gagnalíkans í Rafræn skýrslugerð
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
    * Við bætum við nýju Rafræn skýrslugerð grunnstillingarlíkani sem inniheldur gagnalíkan sem er hannað til notkunar sem gagnaveita fyrir tilbúning skýrslna Rafræn skýrslugerð  
2. Í reitnum Heiti skal færa inn „Greiðslulíkan (ímyndað).
    * Greiðslulíkan (ímyndað)  
3. Smelltu á Stofna skilgreiningu.
4. Smellið á Hönnuður.
    * Opna hönnuður Rafræn skýrslugerð til að tilgreina skipan gagnalíkans þessarar grunnstillingar.  
    * Gera ráð fyrir að við hönnum gagnalíkan fyrir greiðslur viðskiptalén til stuðnings 2 greiðsluaðferðum – kreditfærslum og beingreiðslum.  
5. Smellt er á Nýtt til að opna felligluggann.
6. Í svæðið Heiti, færðu inn „Greiðslur – kreditfærsla“.
    * Greiðslur – kreditfærsla  
7. Smelltu á Bæta við.
8. Smellt er á Nýtt til að opna felligluggann.
9. Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.
10. Í reitnum Heiti skal færa inn „Greiðslur – beingreiðsla“.
    * Greiðslur - beingreiðsla  
11. Smelltu á Bæta við.
12. Smellið á „Vista“.
13. Lokið síðunni.
14. Smellið á „Breyta stöðu“.
    * Ljúka við drög útgáfu af líkaninu til að gera það tiltækt í nýjum líkan vörpunum og sniðum.  
15. Smelltu á Ljúka.
16. Smellið á „Í lagi“.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Byrja að færa inn nýja grunnstillingu sniðs í Rafræn skýrslugerð
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani Greiðslulíkan (ímyndað)“.
3. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
    * Athugið að öll rótaratriði hins valda gagnalíkans eru nú tiltæk í valmöguleikum sem skilgreining gagnalíkans. Þú getur haldið áfram að hanna eigið snið með með því að nota eitthvað af þeim rótaratriðum gagnalíkans sem er krafist. Það að vörpun líkans fyrir valið rótaratriði vanti mun ekki hindra þig í að halda áfram.  
4. Lokið síðunni.

## <a name="add-a-new-er-model-mapping-configuration"></a>Bæta við nýrri grunnstillingu líkan vörpun í Rafræn skýrslugerð
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæði Nýtt skal slá inn „Vörpun líkans byggir á gagnalíkani Greiðslulíkan (ímyndað)“.
3. Í reitnum Heiti skal færa inn „Vörpun greiðslulíkans (ímyndað)“.
    * Varpanir greiðslulíkans (ímynduð)  
4. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
5. Smelltu á Stofna skilgreiningu.

## <a name="design-er-model-mappings"></a>Hanna Vörpun líkans í Rafræn skýrslugerð
1. Smellið á Hönnuður.
    * Nota hönnuður Rafræn skýrslugerð til að tilgreina líkan varpanir fyrir þau atriði rótar sem er krafist.  
2. Smellið á Hönnuður.
    * Herma eftir stillingum valinna líkan varpanir fyrir valin rótaratriði líkans.  
3. Í trénu skal velja „Dynamics 365 for Operations\Tafla færslur“.
4. Smella á bæta Við rót.
5. Í svæðið Heiti, færðu inn „Fjárhagur“.
6. Í reitnum Tafla skal færa inn ‚LedgerJournalTrans‘.
    * LedgerJournalTrans  
7. Smellið á „Í lagi“.
8. Smellið á „Vista“.
9. Lokið síðunni.
10. Lokið síðunni.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Byrja að færa inn aðra nýja grunnstillingu sniðs í Rafræn skýrslugerð
1. Í trénu skal velja „Greiðslulíkan (ímyndað)“.
2. Smellt er á stofna skilgreiningu til að opna fellilistanum.
3. Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani Greiðslulíkan (ímyndað)“.
4. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
    * Athugið að aðeins eitt rótaratriði er tiltækt til vörpunar yfir í gagnaveitu forritsins. Þegar að minnsta kosti ein vörpun líkans er lögð fram, er aðeins hægt að velja þau rótaratriði líkansins sem er varpað yfir í gagnaveitu forritsins, sem skilgreiningu líkans um leið og sniði Rafræn skýrslugerð er bætt við.   
5. Lokið síðunni.


