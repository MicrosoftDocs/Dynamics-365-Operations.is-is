---
title: Raða framleiðsluvinnslum fyrir framleiðsluferli
description: Þessi ferli notar málningu afurðir sem dæmi til að sýna hvernig raða á áætlaðar pantanir eftir forgang lit og stærð pakka.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e064f55ed451d44f58e60ba0aa722166981c129
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "312256"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Raða framleiðsluvinnslum fyrir framleiðsluferli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli notar málningu afurðir sem dæmi til að sýna hvernig raða á áætlaðar pantanir eftir forgang lit og stærð pakka. Sýnigögn fyrirtækisins til að stofna þetta ferli er USPI. Þetta ferli er ætluð fyrir framleiðslustjóri


## <a name="run-master-planning-for-uspi"></a>Keyra áætlanagerð fyrir USPI
1. Fara í Áætlanagerð > Áætlunargerðar > Keyra > áætlunargerðar.
2. Í aðaláætlunarreitnum skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið MasterPlan.  
4. Smellið á „Í lagi“.
    * Þetta hefur Áætlanagerð, þar á meðal ferli röð. Þetta ferli getur tekið nokkrar mínútur.  

## <a name="view-planned-orders-for-the-paint-products"></a>Skoða áætlaðar pantanir fyrir málningu afurðir
1. Fara í Áætlanagerð > Áætlunargerðar > Áætluð pöntun.
2. Útvíkka upplýsingareit vöruupplýsinga
3. Útvíkka upplýsingareit upplýsingar um áætlun
4. Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið MasterPlan.  
6. Í listanum skal smella á tengilinn í valinni línu.
7. Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P300“.
    * Aflæstu til að skruna til hægri til að sjá pöntunardagsetningu og afhendingardagur. Athugaðu að þessar vörur eru með pöntunardagsetningu dagsins í dag og afhendingardagar fyrir áætlaðar pantanir eru ekki raðaðar samkvæmt forgangi litar og pakkningastærðar, eins og sýnt er í vöruheiti. Hægt er að halda bendlinum yfir vörunúmeri til að sjá afurðarheiti og forgang.  

## <a name="sequence-planned-orders-for-paint"></a>Raða áætluðum pöntunum fyrir málningu
1. Lokið síðunni.
2. Fara í Áætlanagerð > Áætlunargerð > Raðaðar áætlaðar pantanir.
3. Útvíkka upplýsingareit vöruupplýsinga
4. Útvíkka upplýsingareit upplýsingar um áætlun
    * Athugasemd: Hér sést Upphafsdagsetning /-tími fyrir áætlaðar pantanir eru raðaðar eftir lit og pakka stærð innan tímarramma 28 daga. Þessar tímabil eru skilgreindar með númeri á svæði Herferðar. Röðuð áætluð pöntun skjámynd hagar eins og skjámynd dæmigert áætlaða pöntun og framleiðslustjórinn getur staðfesta áætlaðar pantanir hér.  
5. Merkja allar línur
6. Smellið á Samþykkja.
    * Þannig verður unnt að uppfærsla áætluð pöntun með valinni röðunaraðgerð sem er annað hvort Fresta eða Flýta.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Staðfesta röð áætlaðar pantanir
1. Lokið síðunni.
2. Fara í Áætlanagerð > Áætlunargerðar > Áætluð pöntun.
3. Útvíkka upplýsingareit vöruupplýsinga
4. Útvíkka upplýsingareit upplýsingar um áætlun
5. Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið MasterPlan.  
7. Í listanum skal smella á tengilinn í valinni línu.
8. Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P300“.
    * Athugið pantanirnar eru nú raðað eftir forgangi lit og stærð og áætlaðar pantanir byrja á fyrstu pöntunardagsetningu og afhendingardagsetningu. Villuleita dálknum pöntunardagsetningu eða upphafsdagsetning upplýsingum um Áætlun upplýsingareit.  

