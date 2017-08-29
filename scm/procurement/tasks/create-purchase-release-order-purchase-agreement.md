--- 
title: "Stofna úttektarpöntun innkaupa úr innkaupasamningi"
description: "Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð."
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ee4bec20fa2449aaa961ab19891a002702174446
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Stofna úttektarpöntun innkaupa úr innkaupasamningi

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð. Innkaupasamnings verður að nota þegar innkaupapöntun er stofnuð þar almennir skilmálar sem á að afrita í haus innkaupapöntunar. Þetta verk myndi venjulega framkvæmt af innkaupaaðila. Nauðsynleg frumforsenda þessari handbók, þú verður að hafa gildan innkaupasamning með í ráðstöfun afurðarmagns fyrir lánardrottinn og vörur. Hægt er að nota sömu aðferð ef þú ert með  innkaupasamning með aðrar gerðir af ráðstafanir. Hægt er að keyra þessari handbók sýnigögn fyrirtækisins USMF. Ef verið er að nota USMF er hægt að keyra "Stofna innkaupasamning" leiðarvísi fyrst til að setja upp nauðsynlegt frumskilyrði fyrir þessari handbók.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Opna undirbúningssvæði innkaupapöntunar.
2. Smellt er á Ný innkaupapöntun.
3. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Víxla útvíkkun á liðnum Almennt.
7. Í reitnum innkaupasamningur skal smella á fellilistahnappinn til að opna leitina.
    * Allar tiltækar samninga lánardrottins eru taldar upp hér. Finna gildan samning sem þú vilt nota.  
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smella á Já.
10. Smellið á „Í lagi“.

## <a name="add-a-line"></a>Bæta við línu
1. Í reitnum Vörunúmer skal slá inn gildi.
    * Ef tilteknar víddir staðsetningar eða birgða eru á ráðstöfun verður þú að færa inn sama gildi í innkaupapöntunarlínu til að geta notað samningnum.  
2. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
    * Svæðið er hugsanlega útfyllt þegar með sjálfgefnu gildi úr pöntuninni, eða frá lánardrottni. Ef svo er er hægt að sleppa þessu þrepi.  
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Færið inn númer í reitnum „Magn“.
    * Villuleita að verð er afritað úr ráðstöfun.  

## <a name="look-up-the-commitment"></a>Fletta upp á ráðstöfun
1. Smellið á „Uppfæra línu“.
2. Smellið á „Viðhengi“.
    * Hér er hægt að fá upplýsingar fyrir innkaupasamning. Til dæmis er hægt að sjá verð og hvort verð og afsláttur er fastur, sem þýðir að ef þú breytir verði eða afslætti á innkaupapöntun í annað gildi en á ráðstöfun, mun kerfið fjarlægja tengil svo innkaupapöntunarlínan uppfyllir ekki á ráðstöfun. Er einnig hægt að sjá hvort valkosturinn Hámark er notað er valinn, sem þýðir að magn á ráðstöfun má ekki fara fram úr með samlagningu allra innkaupa sem uppfylla ráðstöfun.  
3. Lokið síðunni.

## <a name="look-up-the-purchase-agreement"></a>Fletta upp á innkaupasamningur
1. Smellið á „Almennt“ á aðgerðarúðunni.
2. Smellt er á Innkaupasamningur.
3. Lokið síðunni.
4. Lokið síðunni.


