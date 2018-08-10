--- 
title: "Stofna beiðni um tilboð"
description: "Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-request-for-quotation"></a>Stofna beiðni um tilboð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð. Þetta verk myndi yfirleitt gert af innkaupaaðila. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þú Þarft að hafa sett upp beiðnigerðir áður en byrjað er. Þegar þessu verki hefur verið lokið og stofnuð og send hefur verið beiðni um TILBOÐ, er hægt að færa svör fyrir hvern lánardrottinn, gera samanburð á þeim og veita samninga.


## <a name="prepare-a-new-rfq"></a>Útbúa skal nýja beiðni um tilboð
1. Fara í innkaup og aðföng  > Beiðnir um tilboð  > Allar beiðnir um tilboð.
2. Smellið á „Nýtt“.
    * Eftirfarandi gerðir innkaupa eru tiltækar: Innkaupapöntun (það er sjálfgefið): skjal sem staðfestir tilboð um að kaupa afurðir, eða samþykki tilboðs um að selja afurðir in skiptum fyrir greiðslu. Innkaupabeiðni – Þessi gerð er sjálfkrafa valin ef stofna á tilboðsbeiðni beint úr innkaupabeiðni. Ef þessi valkostur er valinn handvirk kemur upp villa. Innkaupasamningur - samningur um að kaupa ákveðið magn eða virði vöru yfir tíma. Ef þessi valkostur er valinn verður að velja dagsetningabilið sem á við innkaupasamninginn.  
3. Í reitinn Titill skjals skal slá inn gildi.
4. Færa inn eða veljið gildi í svæðinu beiðnigerð.
    * Ef stigagjafaraðferð er tengd gerð beiðni verður hún sjálfgefin gerð beðini fyrir tilboð sem verið er að stofna. Þá er mögulegt að breyta aðferð við stigagjöf seinna.  
    * Dagsetning er rituð í reitinn afhendingardagur.  
    * Velja skal þá dagsetningu þegar á að taka á móti afurðunum.  
    * Færa inn dagsetningu og tíma í reitnum fyrir lokadag og gildistíma.  
    * Tilgreina skal dagsetninguna og tímann innan hvers lánardrottnar verða svara beiðni um tilboð.  
5. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Afhendingaraðsetur mun vera sjálfgefið aðsetur vöruhússins.  
6. Smellið á „Í lagi“.

## <a name="add-lines"></a>Bæta við línum
    * Eftir að þú hefur tilgreint grunnupplýsingar um tilboðsbeiðnir þínar, þú að tilgreina vörur eða þjónustu sem þú vilt að lánardrottnar geri tilboð í. Þetta er sjálfgefin línugerð.   
1. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Ef verið er að nota USMF er hægt að velja 'T0020'.  
2. Færið inn númer í reitnum „Magn“.
3. Smellið á „Bæta við línu“.
4. Veljið Flokkur í reitnum Gerð línu.
    * Hægt er að nota línugerðina Tegund til að stofna Tilboðsbeiðnir fyrir vörur eða þjónustu sem eru ekki hluti af birgðum. Svo þarf að velja gerð af vörur eða þjónustu úr stigveldi innkaupaflokka.  
5. Slá inn eða velja gildi í reitnum innkaupategund.
6. Í reitinn Afurðarheiti skal slá inn gildi.
7. Færið inn númer í reitnum „Magn“.
8. Í reitinn eining skal slá inn eða velja gildi.

## <a name="add-vendors"></a>Bæta við lánardrottnum
1. Smellt er á Hausnum til að breyta úr línuyfirliti í hausyfirlit. 
2. Stækka hlutann Lánardrottinn.
3. Smellt er á Bæta lánardrottnum sjálfkrafa við.
    * Þú getur bæta lánardrottnum á beiðni um tilboð sjálfkrafa samkvæmt innkaupategund umbeðnu varanna. Ef það eru engir lánardrottnar samþykkt fyrir tegundum í línum er hægt að bæta lánardrottnum við handvirkt.  
4. Smelltu á Bæta við.
5. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
6. Smelltu á Bæta við.
7. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
    * Þegar lánardrottinn var valinn, er staða Stofnuð. Upplýsingar lánardrottinsins hafa samkvæmt þessu verið vistaðar í beiðninni um tilboð, en notandi hefur ekki sent beiðni um tilboð til lánardrottins. Hægt er að bæta lánardrottni við tilboðsbeiðni óháð stöðu lánardrottins.  

## <a name="send-the-rfq-to-vendors"></a>Senda beiðni um tilboð til lánardrottna
1. Smellt er á Senda.
    * Í síðunni senda beiðni um tilboð skal gengið úr skugga um að lánardrottnar í listanum séu þeir sem á að senda tilboðsbeiðni til.  
2. Smelltu á Prenta.
    * Þessi svargluggi gerir notanda kleift að prenta beiðni um tilboð. Ef kosið er að prenta svarblað er innihald þessa skilgreint í færibreytum innkaupa og aðfanga. Til að velja hvernig á að prenta svarblöð, þegar búið er að opna prentglugga, smella á Ítarlegir prentunarvalkostir. Ein beiðni um tilboð verður prentuð fyrir hvern lánardrottinn sem inniheldur línur sem hafa stöðuna Stofnað eða Sent. Línur sem hætt var við og línur með skráðum svörum verða ekki prentaðar.   
3. Smellið á Hætta við.
4. Smellið á „Í lagi“.
5. Lokið síðunni.
6. Lokið síðunni.

## <a name="view-the-rfq-journal"></a>Skoða færslubók tilboðsbeiðna
1. Fara í innkaup og aðföng > Beiðnir um tilboð > eftirfylgni við Beiðni um tilboð > Færslubækur beiðna um tilboð.
2. Smellt er á Forskoða/prenta.
3. Smellt er á forskoðunina Upprunalegt.
4. Lokið síðunni.
5. Lokið síðunni.


