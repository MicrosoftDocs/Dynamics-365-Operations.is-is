---
title: Innkaup
description: Þetta efni skýrir innkaup í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875712"
---
# <a name="procurement"></a>Innkaup


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Í eignastjórnun geturðu fengið yfirlit yfir innkaupabeiðnir og innkaupapantanir sem tengjast verkbeiðnum. Það er líka mögulegt að búa til innkaupapöntun eða innkaupabeiðni úr verkbeiðni.

Í listanum **Innkaupabeiðni um verkbeiðni** (**Eignastjórnun** > **Sameiginlegt** > **Innkaup** > **Innkaupabeiðni um verkbeiðni**), sérðu lista yfir innkaupabeiðnir sem tengjast verkbeiðnum.

- Veldu verkbeiðniverk í listanum **Innkaupabeiðni um verkbeiðni** og smelltu á **Kaupbeiðni** til að opna tengda innkaupabeiðni.  
- Veldu verkbeiðniverk í listanum **Innkaupabeiðni um verkbeiðni** og smelltu á **Verkbeiðni** til að opna tengda verkbeiðni.  
- Veldu verkbeiðniverk í listanum **Innkaupabeiðni um verkbeiðni** og smelltu á hnappinn **Notkunarstaður vöru** ef þú vilt fá yfirlit yfir hvar vara í valinni línu er notuð í eignastjórnun í tengslum við eignir, tegundasjálfgildi viðhaldsverka, varahluti og verkbeiðnir. 

![Mynd 1](media/08-work-orders.png)


Í listanum **Innkaupabeiðni um verkbeiðni** (**Eignastjórnun Enterprise** > **Sameiginlegt** > **Innkaup** > **Innkaupabeiðni um verkbeiðni**), er hægt að sjá lista yfir innkaupabeiðnir sem tengjast verkbeiðnum.

- Veldu verkbeiðniverk í listanum **Innkaupabeiðni um verkbeiðni** og smelltu á **Innkaupabeiðni** til að opna tengda innkaupabeiðni.  
- Veldu verkbeiðniverk í listanum **Innkaupabeiðni um verkbeiðni** og smelltu á **Verkbeiðni** til að opna tengda verkbeiðni.  
- Veldu verkbeiðniverk í innkaupalistanum **Verkbeiðni** og smelltu á hnappinn **Notkunarstaður vöru** ef þú vilt fá yfirlit yfir hvar vara í valinni línu er notuð í eignastjórnun í tengslum við eignir, tegundasjálfgildi viðhaldsverka, varahluti og verkbeiðnir. 

![Mynd 2](media/09-work-orders.png)


Á listunum hér að ofan er tákn varðandi stjórnun á afhendingardegi komið til hægri á hverri línu. Ef táknið sýnir upphrópunarmerki í rauðum hring þýðir það að afhending á tengdri innkaupabeiðni eða innkaupapöntun getur tafist.

Í innkaupabeiðni er dagsetningin sem notuð er til að reikna mögulega seinkun að finna í skjámyndinni **Innkaupabeiðnir** > flýtiflipanum **Haus innkaupabeiðni** > reitnum **Umbeðin dagsetning**. Sú dagsetning er borin saman við fyrirliggjandi dagsetningu í verkbeiðni eða verkbeiðniverkum á sama hátt og dagsetningu innkaupapöntunar.

Á innkaupapöntun er dagsetningin sem notuð er til að reikna út mögulega seinkun dagsetningin sem tengist innkaupapöntunarlínunni, sem sýnd er í skjámyndinni **Innkaupapöntun** > veldu innkaupapöntunarlínu > flýtiflipann **Línuupplýsingar** > flipann **Uppsetning** > reitinn **Staðfestur afhendingardagur**. Ef þessi reitur er ekki fylltur út er dagsetningin í reitnum **Afhendingardagur** á flýtiflipanum **Haus innkaupapöntunar** notuð. Ein af þessum dagsetningum er borin saman við fyrirliggjandi dagsetningu í verkbeiðni eða verkbeiðniverkum í eftirfarandi röð:

- Raunverulegur upphafsdagur verkbeiðni, eða  

- Áætlaður upphafsdagur á tengdu verkbeiðniverki, eða  

- Áætlaður upphafsdagur verkbeiðni, eða  

- Væntur upphafsdagur verkbeiðni, eða  


## <a name="create-purchase-order-from-a-work-order"></a>Stofna innkaupapöntun úr verkbeiðni

Í **Öllum verkbeiðnum** velurðu verkbeiðniverk og stofnar tengda innkaupapöntun eða innkaupabeiðni. Þetta er gert til að tryggja samskipti verkefna milli innkaupapöntunar eða innkaupabeiðni og verkbeiðni.

1. Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.

2. Í listanum **Allar verkbeiðnir** eða **Virkar verkbeiðnir** skaltu velja verkbeiðnina sem þú vilt búa til innkaupapöntun fyrir og smella á **Breyta**.

3. Í skjámyndinni **Verkbeiðni** > flýtiflipanum **Viðhaldsverk verkbeiðni** skaltu velja verkbeiðniverkið sem þú vilt búa til innkaupapöntunina fyrir.

4. Smelltu á **Vöruliðir** > **Innkaupapöntun úr verkbeiðniverki**.

5. Í listasíðuna **Innkaupapantanir verks** smellirðu á **Nýtt**.

6. Stofnaðu innkaupapöntunina.

>[!NOTE]
>Að búa til innkaupabeiðni er nánast eins og að búa til innkaupapöntun. Eini munurinn er að í ofangreindri aðferð smellirðu á **Vöruliði** > **Innkaupabeiðni úr verkbeiðniverkinu** í 2. þrepi.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Verkefnatengsl milli verkbeiðni og innkaupapöntunar eða innkaupabeiðni

Innkaupapöntunarlína eða innkaupabeiðnilína er tengd verkbeiðniverkum í gegnum verkbeiðniverkið og tengda verkþáttanúmerið. Þegar þú býrð til innkaupapöntun eða innkaupabeiðni úr verkbeiðniverki er tengt verkþáttanúmer skylda. Verkþáttanúmerið er sjálfkrafa sett inn í innkaupapöntun eða innkaupabeiðni ef tengd verkbeiðni inniheldur verkbeiðniverk sem öll nota sömu gerð viðhaldsverka. Ef verkbeiðniverkin innihalda mismunandi gerðir viðhaldsverka verður að setja verkþáttanúmer inn á handvirkan hátt.

Til að sjá eða setja inn verkþáttanúmer tengt innkaupapöntunarlínu opnarðu **Verkbeiðnikaup** > veldu innkaupapöntunarskrá > smelltu á innkaupapöntunina í dálknum **Innkaupapöntun** > flýtiflipanum **Línuupplýsingar** > flipanum **Verk** > reitnum **Verkþáttur**.


![Mynd 3](media/10-work-orders.png)


Sömuleiðis, til að sjá eða setja inn verkþáttanúmer tengt innkaupabeiðnilínu verkbeiðni opnarðu **Innkaupabeiðni verkbeiðni** > veldu innkaupabeiðniskrá > smelltu á innkaupabeiðnina í dálknum **Innkaupabeiðni** > flýtiflipanum **Línuupplýsingar** > flipanum **Verk** > reitnum **Verkþáttur**.

