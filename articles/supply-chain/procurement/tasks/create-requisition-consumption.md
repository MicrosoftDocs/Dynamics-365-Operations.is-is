--- 
title: "Stofna beiðni um notkun"
description: "Þetta ferli fer í gegnum ferlið fyrir myndun á innkaupabeiðni."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 55ef4b1757a6f3c28c8575412d66488fda8608a5
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-requisition-for-consumption"></a>Stofna beiðni um notkun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum ferlið fyrir myndun á innkaupabeiðni. Hún sýnir mismunandi leiðir til að leita að afurðum í þínu innkaupavörulista og hvernig á að bæta við afurð sem er ekki í vörulistanum þínum. Áður en þetta ferli er hafið, verður að hafa innkaupastefna uppsetta með Notkun sem sjálfgefna gerð beiðni. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ferlið getur aðeins verið framkvæmt af forstillingu notanda sem þegar er sett upp sem starfsmaður.  Þetta verk myndi venjulega framkvæmt af starfsmanni. öryggishlutverk Starfsmanns gerir þér kleift að framkvæma þau verk, eða ef verið er að nota USMF er hægt að skrá sig inn sem Alicia.


## <a name="create-a-new-requisition"></a>Stofna nýja innkaupabeiðni
1. Fara í Innkaup og uppruni > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef.
2. Smellið á „Nýtt“.
3. Í svæðið Heiti skal nefna beiðnina.
4. Dagsetning er rituð í reitinn umbeðin dagsetning:.
    * Sjálfgefið er að umbeðin dagsetning og dagsetning reikningsskila sé afritaðar í innkaupabeiðnilínur. Hægt er að breyta þeim á línustigi. Umbeðin dagsetning er umbeðinn afhendingardagur.  
5. Dagsetning er rituð í reitinn dagsetning reikningsskila.
    * Bókhaldsdagsetningin er notuð til að skrá bókhaldsfærsluna í fjárhag og staðfesta að fjármagn sé tiltækt.  
6. Smellið á „Í lagi“.
7. Í reitnum Ástæða skal smella á fellilistahnappinn til að opna leitina.
    * Sjálfgefið er að sú réttlæting viðskipta sem þú velja birtast fyrir innkaupabeiðnilínur, en hægt er að breyta því á línustigi.    
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Veljið ástæðu
10. Í reitinn Upplýsingar skal slá inn meira lýsandi réttlætingu fyrir beiðninni.

## <a name="add-a-line-to-the-requisition"></a>Bæta línu við í innkaupabeiðni
1. Smellið á „Bæta við línu“.
    * Til eru tvær leiðir á að bæta línum við innkaupabeiðnina. Ef þegar vitað afurðarnúmer eða þegar vitað að beðið er um afurð sem er ekki í vörulista, þá geturðu bæta línunni beint með "Bæta Við línu". Hin leiðin er að nota "Bæta við afurðir" þar sem hægt er að nota leit og síun til að finna vörur í vörulista.    
2. Smellt er á línunni sem nýverið var stofnuð.
    * Umsækjandinn er starfsmaður sem hefur beðið um beiðnina.   
    * Sjálfgefið er að einstaklingurinn sem sér um undirbúning innkaupabeiðni er starfsmaður sem hefur beðið um hana. Það þarf að veita heimild til að útbúa innkaupabeiðnilínu fyrir hönd annars starfsmanns. Ef slíkar heimildir eru til staðar munu hinir starfsmenn birtast í þessari uppflettingu.  
3. Í reitnum Vörunúmer skal slá inn gildi.
    * Vörur sem eru tiltækar til að velja takmarkast við aðgangsreglur tegundarinnar og innkaupavörulistann fyrir innkaupalögaðilanum.   
4. Færið inn númer í reitnum „Magn“.

## <a name="add-more-products-to-the-requisition"></a>Bæta fleiri afurðum við innkaupabeiðnina
1. Smella á Bæta við afurðum.
    * Þetta er valkosturinn þar sem hægt er að leita að afurðir í vörulistanum.    
2. Í reitnum Finna innkaupa tegund hnúts, Sláðu inn fyrri hluti heitis tegundar þú leitar, og smellið síðan á Enter.
    * Til dæmis, skráið tölva.  
3. Nota InvokeDefaultButton flýtivísunina.
4. Nota Síu til að sía lista yfir vörur í völdu tegundinni.
5. Veldu vöruspjaldið sem á að bæta við innkaupabeiðnina.
6. Smellt er á Bæta við línum.
7. Í reitinn magn skal slá inn númer.
8. Í reitnum Finna innkaupa tegund hnúts, Sláðu inn fyrri hluti heitis tegundar þú leitar, og smellið síðan á Enter.
    * Til dæmis skráið Há (highlighters).  
9. Nota InvokeDefaultButton flýtivísunina.
10. Smella á bæta Við óskráðum afurðar á línur til að bæta við vöru sem er ekki skráður í innkaupavörulista.
11. Sláið inn gildi í reitinn Afurðarheiti.
12. Í reitnum Eining skal slá inn gildi.
13. Smellt er á Í lagi.
14. Bæta við lýsingu á afurðina í lýsingarsvæði Vöru.
15. Færið inn númer í reitnum „Magn“.
16. Færið inn númer í reitnum „Einingarverð“.
    * Ef þú þekkir verð fyrir tiltekna lánardrottna (sem er valin í svæðinu lánardrottnalykill) þá er hægt að færa inn verðið.   
17. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
    * Lánardrottna sem eru tiltækar í þessu svæði eru háð innkaupareglur og stöðu sem lánardrottinn hefur fyrir gildandi innkaupategundina. Auk þess að velja lánardrottin hér, hægt að smella á hnappinn Leggja til lánardrottinn.    
18. Veljið lánardrottinn sem á að nota í listanum.
19. Í reitnum ytra vörunúmer skal slá inn gildi.
    * Þetta er tilvísunarnúmer fyrir afurð sem lánardrottinn þekkir. Til dæmis, gæti þetta verið vörunúmer afurðar í eigin vörulista lánardrottins .  
20. Smellið á „Í lagi“.

## <a name="distribute-amounts"></a>Dreifa upphæðum
1. Smelltu á Fjárhagur.
2. Smellt er á Dreifa upphæðum.
    * Þetta ferli sýnir hvernig á að dreifa kostnaði í fyrstu línunni á milli 2 lykla. Einnig má gera það seinna þegar innkaupabeiðni er í yfirferð.  
3. Smellt er á Skipta til að stofna nýja dreifingarlínu.
4. Í svæðinu fjárhagslykill, veljið fyrst kostnaðarstaður sem á að taka hluta af kostnaðinum.
5. Veljið aðra dreifingarlínuna.
6. Í fjárhagslykil svæðinu, tilgreinið hitt kostnaðarstaðinn.
7. Smellt er á Dreifa jafnt.
8. Lokið síðunni.

## <a name="view-line-details"></a>Skoða línuupplýsingar
1. Víxla útvíkkun á liðnum línuupplýsingar.

## <a name="submit-the-requisition"></a>Senda innkaupabeiðnina
1. Smellt er á Verkflæði til að opna felligluggann.
2. Smelltu á Senda.
3. Lokið síðunni.
4. Í svæðinu Athugasemd, færðu inn gerð athugasemdar fyrir samþykkjandi innkaupabeiðninnar.
5. Smelltu á Senda.
6. Lokið síðunni.
7. Endurhlaðið síðuna.


