---
title: Mynda áætlun með skorðum
description: Þetta efni útskýrir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808017"
---
# <a name="generate-a-constrained-plan"></a>Mynda áætlun með skorðum

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla. Áætlunin tryggir að framleiðslu hefst ekki fyrr en efni sé tiltækt og tilföng eru ekki yfirbókaður. 

Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir framleiðslustjóri


## <a name="set-up-a-constrained-plan"></a>Setja upp áætlun með skorðum
1. Á heimasíðunni velurðu vinnusvæðið **Aðaláætlanagerð**.
2. Veldu **Aðaláætlanagerðir** á listanum yfir tengla lengst til hægri á vinnusvæðinu.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Dæmi: **StaticPlan**  
4. Veljið **Já** í reitnum **Takmörkuð geta**.
5. Í reitnum **Tímamörk takmarkaðrar getu** skal slá inn `30`.
6. Víkka út hlutann **Tímamörk í dögum**.
7. Veljið **Já** í reitnum **Afkastageta**.
8. Í reitinn **Tímamörk áætlaðrar afkastagetu (dagar)** slá inn númer. Dæmi: `60`  
9. Veljið **Já** í reitnum **Reiknaðar seinkanir**.
10. Í reitinn **Tímamörk útreiknaðra seinkana (dagar)** skal slá inn tölu. Dæmi: `60` 
11. Útvíkkaðu hlutann **Reiknaðar seinkanir**.
12. Veldu **Já** í öllum reitum **Bæta við reiknaðri seinkun á dagsetningu þarfa**.
13. Lokið síðunni.

## <a name="create-a-constrained-plan"></a>Stofna áætlun með skorðum
1. Veljið **Keyra**.
2. Í reitinn **Aðaláætlun** slærðu inn eða velur áætlunina sem þú hefur sett upp skorður fyrir.  
3. Veljið **Í lagi**.
4. Veldu **Tillögur**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]