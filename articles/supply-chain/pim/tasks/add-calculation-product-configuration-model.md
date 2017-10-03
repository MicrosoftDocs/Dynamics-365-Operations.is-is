--- 
title: "Bæta útreikningi við afbrigðalíkan afurðar"
description: "Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Bæta útreikningi við afbrigðalíkan afurðar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar. Hún sýnir hvernig hægt er að stofna röksegð með notkun "Ef" virknitákn til að setja hæð hátalara til 10 fyrir hvítum hátalara og 15 fyrir allar aðrar frágang húss. Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.


## <a name="add-a-calculation"></a>Bæta við útreikningum

## <a name="create-calculation-expression"></a>Stofna segð útreiknings
1. Smella á Breyta segð.
2. Færið inn í svæðið ConstraintBody ‚If[CabinetFinish == „white", 10, 15]'.
3. Smella á Villuleita.
4. Smellið á „Loka“.
5. Smellið á „Í lagi“.


