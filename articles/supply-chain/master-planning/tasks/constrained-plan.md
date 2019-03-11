---
title: Mynda áætlun með skorðum
description: Þessi verklýsing sýnir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "336038"
---
# <a name="generate-a-constrained-plan"></a>Mynda áætlun með skorðum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla. Áætlunin tryggir að framleiðslu hefst ekki fyrr en efni sé tiltækt og tilföng eru ekki yfirbókaður. 

Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir framleiðslustjóri


## <a name="set-up-a-constrained-plan"></a>Setja upp áætlun með skorðum
1. Smellt er á aðaláætlanagerð.
2. Smellt er á aðaláætlanir.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Dæmi: StaticPlan  
4. Veljið Já í svæðinu takmörkuð Afkastageta.
5. Í reitnum Tímamörk takmarkað afkastaveita skal slá inn ‚30‘.
6. Víkka út hlutann tímamörk í dögum.
7. Veljið Já í svæðinu Afkastageta.
8. Í reitinn Tímamörk áætlaðrar afkastagetu slá inn númer.
    * Dæmi: 60  
9. Veljið Já í Reiknaðar seinkanir reitnum.
10. Í reitinn Tímamörk útreiknaðra seinkana (dagar) skal slá inn númer.
    * Dæmi: 60  
11. Útvíkka hlutann Reiknuð seinkanir.
12. Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa
13. Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa
14. Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa
15. Lokið síðunni.

## <a name="create-a-constrained-plan"></a>Stofna áætlun með skorðum
1. Smellið á „Keyra“.
2. Færa inn eða veljið gildi í svæðinu Aðaláætlun.
    * Velja áætlunina sem settar voru upp skorður fyrir.  
3. Smellið á „Í lagi“.
    * Þetta gæti tekið nokkra stund.  
4. Smellt er á Áætlaðar pantanir.

