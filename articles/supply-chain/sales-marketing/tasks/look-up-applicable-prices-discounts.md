--- 
title: "Fletta upp gildandi verði og afslætti"
description: "Þessi ferli sýnir hvernig á að finna verð og/eða afsláttur fyrir afurð sem er gild fyrir ákveðinn viðskiptavin, án þess að stofna sölupöntun."
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
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 7ef63151f352b3664bccd7a59e7417dfddc7470b
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a>Fletta upp gildandi verði og afslætti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli sýnir hvernig á að finna verð og/eða afsláttur fyrir afurð sem er gild fyrir ákveðinn viðskiptavin, án þess að stofna sölupöntun. Ferlið fer í gegnum tiltekið dæmi og þú þarft að fylgja dæminu sem notar USMF sýnigögn fyrirtæki til að velja nauðsynleg gildi.


## <a name="find-the-applicable-price"></a>Finna viðeigandi verð
1. Fara í Sölu og markaðssetningu > Verð og afslætti > Finna verð.
2. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
3. Á listanum finna og velja viðskiptavin US-001.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Sláið inn „T0004“ á svæðinu „Vörunúmer“.
    * Að sjálfgefnu er svæðið Magn er stillt á 1. Hins vegar ef vitað er um stærð pöntunarinnar sem viðskiptavinurinn ætlar að panta fyrir viðkomandi afurð, færið þá þetta gildi í staðinn. Þessar upplýsingar skipta máli ef verðsamninga við viðskiptavininn hefur hlé í magni, það er, verð afurðarinnar er háð lágmarksmagni sem keypt er.  
6. Í svæði Dagsetningar, Færið inn dagsetningu þegar viðskiptavinurinn reiknar með að panta 
    * Dagsetningin getur verið dagurinn í dag eða hvaða dagsetningu í framtíðinni.  
    * Nú skilar kerfið verði sem er gild fyrir valda afurð þegar hún er keypt af valinn viðskiptavinur á valinni dagsetningu með tilgreindu magni. Í þessu dæmi, ef viðskiptavinur US-001 keypti 1 einingu af afurð T0004 í dag væri hann rukkaður um 350 CAD á einingu. Verðið kemur úr fyrirliggjandi og virkum viðskiptasamningi við viðskiptavininn.      Önnur svæði á síðunni veita frekari upplýsingar um afurðarverð og -kostnað (ef sett er upp á afurðarsniðmáti), og arðsemi er reiknuð út.  
    * Ef valkosturinn Sýna tengda afurðarafbrigði er valinn, merkir það að til eru viðbótar verðsamninga fyrir afurðarafbrigðin.  
7. smellt á Sýna tengd afurðarafbrigði gátreitinn.
    * Listi yfir afurðarafbrigði er sýndur, með upplýsingum um víddir þeirra.  
8. Merkja línuna sem táknar Hvítan lit, á listanum.
    * Athugið að vöruverðið er nú annað en það sem hefur áður verið birt þegar það var ekki tilgreint eftir vídd.  
9. Smellt er á Skoða söluverð.
    * Síðan Verð (sala) birtir alla verðsamninga sem gilda um afurð, þ.m.t. afbrigði hennar.  
10. Lokið síðunni.

## <a name="find-the-applicable-discount"></a>Finna viðeigandi afsláttur
    * Gangið úr skugga um að svæðið viðskiptavinalykill innihaldi númer viðskiptavinar US-001    
1. Sláið inn „T0012“ á svæðinu „Vörunúmer“.
    * Gangið úr skugga um að svæðið Magn er stillt á 1.  
    * Eftirfarandi verðupplýsingum sem sýnd eru fyrir afurð T0012 koma úr einni eða fleiri verðsamninga: einingarverð er 1.000 CAD og afsláttarprósentan er 5.  
2. Stillið magn á „20“.
    * Aukinn pöntunarmagn veldur línuafslátt sem er boðið viðskiptavini til að breyta úr 5 til 7 prósent.  
    * Nettó upphæð er reiknuð á grundvelli á einingaverðs, afslætti og heildarmagni.  
3. Smellt er á Skoða línuafslátt.
    * Það eru tvær línuafsláttarsamninga fyrir afurða T0012, sem tilgreina 5 prósent afslátt í fyrir pöntunarmagn línu frá 1 til 10, og 7 prósent afsláttur fyrir magn yfir 10. Athugaðu að afslættir gilda um hóp afurða, í þessu dæmi, flokkskóði 01 sem afurðin T0012 tilheyrir.  
4. Lokið síðunni.


