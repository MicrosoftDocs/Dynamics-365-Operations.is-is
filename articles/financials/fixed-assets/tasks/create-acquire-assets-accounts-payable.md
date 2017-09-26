--- 
title: "Stofna og eignast eignir úr viðskiptaskuldum"
description: "Þessi leiðarvísi fyrir verk um stofnun og kaup eignar með innkaupaferlið."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Stofna og eignast eignir úr viðskiptaskuldum

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk um stofnun og kaup eignar með innkaupaferlið.  Það notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.


## <a name="set-fixed-assets-parameters"></a>Stilla færibreytur eigna
1. Fara í Eignir > Uppsetning > Færibreytur eigna.
2. Útvíkka eða draga saman hlutanum innkaupapöntun.
3. Merkja við Innkaupagátreit Leyfa eignakaup úr .
4. Merktu við gátreið Stofna eign á meðan innhreyfingarskjal afurða eða bókun reiknings.

## <a name="create-a-new-vendor-invoice"></a>Nýtt reikningur lánardrottins búið til.
1. Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.
2. Smellt er á Nýtt reikning lánardrottins.
3. Í reitnum reikningslykill skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum Númer skal slá inn gildi.
6. Dagsetning er rituð í reitinn Bókunardagssetning.
7. Smellið á „Bæta við línu“.
8. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
    * Hægt er að nota annað hvort vörur ekki á lager eða innkaupaflokkar fyrir eignakaup.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Færið inn númer í reitnum „Magn“.
    * Einnar reikningslínu stofnar einungis eina eign, óháð magni.  Svæðisgildi fyrir magns reiknings verða flutt í magn eignar.  
11. Færið inn númer í reitnum „Einingarverð“.
12. Útvíkka eða draga saman hluta upplýsingar Línu.
13. Smellið á flipann eigna.
14. Merktu við gátreit Stofna nýja eign.
15. Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.
16. Veljið eignaflokk til að nota á þegar ný eign er stofnuð, á listanum.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Smellið á „Bóka“.
    * Eign verður stofnuð og keypt þegar reikningur er bókaður.  

