--- 
title: "Bæta skorðu á segð við afbrigðalíkan afurðar"
description: "Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Bæta skorðu á segð við afbrigðalíkan afurðar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig hægt er að bæta nýjum skorðusegð við afbrigðalíkani afurðar. Hún sýnir hvernig er hægt að gefa fyrirmæli sem um að hornvörn verður að nota í hátalara ef notandinn hefur valið sé framgrill í málmi. Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.


## <a name="create-an-expression-constraint"></a>Stofna segð töfluskorðu
1. Smellið á Skilgreining afurðarafbrigðislíkans
2. Smella á Afbrigðalíkan afurðar
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Þetta dæmi nota hágæða hátalara líkanið.  
4. Í listanum skal smella á tengilinn í valinni línu.
5. Stækka skorðuhluti.
6. Smelltu á Bæta við.
7. Smellið á „Stofna“.
8. Í reitinn Heiti skal slá inn gildi.

## <a name="enter-expression"></a>Færa inn segð
1. Smella á Breyta segð.
    * Ef notendaviðmótinu í verkinu á skráningu á þessu stigi er aflæsa, má nota IntelliSense og lista yfir tákn til að byggja skorðusegð.  
2. Færið inn í svæðið ConstraintBody 'Implies [FrontGrill == "Metal", CornerProtection] '.
    * Rökhugsun á bakvið þessa segð segir: Ef Framgrill er úr málmi, þá verður að velja valkostinn hornvörn.  
3. Smella á Villuleita.
    * Villuleita aðgerð keyrir gegnum skorðusegð og athugar málskipanarvilla.  
4. Smellið á „Loka“.
5. Smellið á „Í lagi“.


