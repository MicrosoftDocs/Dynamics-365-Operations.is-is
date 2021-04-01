---
title: Stofna beiðni um notkun
description: Þetta efnisatriði lýsir ferlinu við stofnun beiðni.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b742e83cb538a0ebfe3b055ceb38fd8d1bfcf068
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211863"
---
# <a name="create-a-requisition-for-consumption"></a>Stofna beiðni um notkun

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir ferlinu við stofnun beiðni. Hún sýnir mismunandi leiðir til að leita að afurðum í innkaupavörulistanum og hvernig á að bæta við afurð sem er ekki í vörulistanum þínum. Áður en þetta ferli er hafið, verður að hafa innkaupastefna uppsetta með Notkun sem sjálfgefna gerð beiðni. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ferlið getur aðeins verið framkvæmt af forstillingu notanda sem þegar er sett upp sem starfsmaður. Þetta verk myndi venjulega framkvæmt af starfsmanni. Öryggishlutverk **Starfsmanns** gerir þér kleift að framkvæma þau verk, eða ef verið er að nota USMF er hægt að skrá sig inn sem **Alicia**.


## <a name="create-a-new-requisition"></a>Stofna nýja innkaupabeiðni
1. Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef búið til**.
2. Veljið **Nýtt**.
3. Í reitnum **Heiti** gefurðu beiðninni heiti.
4. Í reitinn **Umbeðin dagsetning** slærðu inn dagsetningu. Sjálfgefið er að umbeðin dagsetning og dagsetning reikningsskila sé afritaðar í innkaupabeiðnilínur. Hægt er að breyta þeim á línustigi. Umbeðin dagsetning er umbeðinn afhendingardagur.  
5. Í reitinn **Dagsetning reikningsskila** slærðu inn dagsetningu. Bókhaldsdagsetningin er notuð til að skrá bókhaldsfærsluna í fjárhag og staðfesta að fjármagn sé tiltækt.  
6. Veljið **Í lagi**.
7. Í reitnum **Ástæða** velurðu valkost úr fellivalmyndinni. Sjálfgefið er að sú réttlæting viðskipta sem þú velja birtast fyrir innkaupabeiðnilínur, en hægt er að breyta því á línustigi.  
8. Veljið ástæðu.
9. Í reitinn **Upplýsingar** skal slá inn meira lýsandi réttlætingu fyrir beiðninni.

## <a name="add-a-line-to-the-requisition"></a>Bæta línu við í innkaupabeiðni
1. Veldu **Bæta við línu**. Til eru tvær leiðir á að bæta línum við innkaupabeiðnina. Ef þegar vitað afurðarnúmer eða þegar vitað að beðið er um afurð sem er ekki í vörulista, þá geturðu bæta línunni beint með **Bæta Við línu**. Hin leiðin er að nota **Bæta við afurðir** þar sem hægt er að nota leit og síun til að finna vörur í vörulista.    
2. Veldu röðina sem nýverið var stofnuð.
    - Umsækjandinn er starfsmaður sem hefur beðið um beiðnina.   
    - Sjálfgefið er að einstaklingurinn sem sér um undirbúning innkaupabeiðni er starfsmaður sem hefur beðið um hana. Það þarf að veita heimild til að útbúa innkaupabeiðnilínu fyrir hönd annars starfsmanns. Ef slíkar heimildir eru til staðar munu hinir starfsmenn birtast í þessari uppflettingu.  
3. Í reitnum **Vörunúmer** skal slá inn gildi. Vörur sem eru tiltækar til að velja takmarkast við aðgangsreglur tegundarinnar og innkaupavörulistann fyrir innkaupalögaðilanum.   
4. Í reitnum **Magn** slærðu inn tölu.

## <a name="add-more-products-to-the-requisition"></a>Bæta fleiri afurðum við innkaupabeiðnina
1. Veldu **Bæta afurðum við**. Þetta er valkosturinn þar sem hægt er að leita að afurðir í vörulistanum.    
2. Í reitnum **Finna hnút innkaupategundar** slærðu inn fyrri hluti heitis flokksins sem þú leitar að og velur síðan **Enter**. Til dæmis er slegið inn `comput`.  
3. Notaðu flýtivísunina **InvokeDefaultButton**.
4. Nota **Síu** til að sía lista yfir vörur í völdu tegundinni.
5. Veldu vöruspjaldið sem á að bæta við innkaupabeiðnina.
6. Veldu **Bæta við línum**.
7. Í reitnum **Magn** slærðu inn tölu.
8. Í reitnum **Finna hnút innkaupategundar** ritarðu fyrri hluti heitis flokksins sem þú leitar að og velur síðan **Enter**. Til dæmis er slegið inn `High` (highlighters).  
9. Notaðu flýtivísunina **InvokeDefaultButton**.
10. Veldu **Bæta óskráðri afurð við línur** til að bæta við vöru sem er ekki skráð í innkaupavörulistann.
11. Í reitinn **Afurðarheiti** skal slá inn gildi.
12. Í reitnum **Eining** skal slá inn gildi.
13. Veljið **Í lagi**.
14. Í reitnum **Vörulýsing** bætirðu við lýsingu á afurðinni.
15. Í reitnum **Magn** slærðu inn tölu.
16. Í reitnum **Einingarverð** skal slá inn tölu. Ef þú þekkir verð fyrir tiltekna lánardrottna (sem er valin í svæðinu lánardrottnalykill) þá er hægt að færa inn verðið.   
17. Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina. Lánardrottna sem eru tiltækar í þessu svæði eru háð innkaupareglur og stöðu sem lánardrottinn hefur fyrir gildandi innkaupategundina. Auk þess að velja lánardrottin hér, hægt að velja **Leggja til lánardrottinn**.    
18. Veljið lánardrottinn sem á að nota í listanum.
19. Í reitnum **Ytra vörunúmer** skal slá inn gildi. Þetta er tilvísunarnúmer fyrir afurð sem lánardrottinn þekkir. Til dæmis, gæti þetta verið vörunúmer afurðar í eigin vörulista lánardrottins .  
20. Veljið **Í lagi**.

## <a name="distribute-amounts"></a>Dreifa upphæðum
1. Veldu **Fjármál**.
2. Veldu **Dreifingarupphæðir**. Þetta ferli sýnir hvernig á að dreifa kostnaði í fyrstu línunni á milli 2 lykla. Einnig má gera það seinna þegar innkaupabeiðni er í yfirferð.  
3. Veldu **Skipta** til að stofna nýja dreifingarlínu.
4. Í svæðinu **Fjárhagslykill**, veljið fyrst kostnaðarstaður sem á að taka þátt í kostnaðinum.
5. Veljið aðra dreifingarlínuna.
6. Í fjárhagslykil svæðinu, tilgreinið hitt kostnaðarstaðinn.
7. Velja **Dreifa jafnt**.
8. Lokið síðunni.

## <a name="view-line-details"></a>Skoða línuupplýsingar
1. Víxla útvíkkun á liðnum **Línuupplýsingar**.

## <a name="submit-the-requisition"></a>Senda innkaupabeiðnina
1. Veldu **Verkflæði** til að opna felligluggann.
2. Veldu **Senda**.
3. Lokið síðunni.
4. Í svæðinu **Athugasemd**, færðu inn gerð athugasemdar fyrir samþykkjandi innkaupabeiðninnar.
5. Veldu **Senda**.
6. Lokið síðunni.
7. Endurhlaðið síðuna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]