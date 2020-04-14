---
title: Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð
description: Þessi ferli sýnir hvernig á að stofna nýja lífferlisstöðu afurðar sem útilokar vörur úr aðaláætlanagerð og úrreikningi á uppskriftarstigi.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62de37b5a84a1771b77ef2566942b7ffe8895f16
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149942"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð

[!include [banner](../../includes/banner.md)]

Þessi ferli sýnir hvernig á að stofna nýja lífferlisstöðu afurðar sem útilokar vörur úr aðaláætlanagerð og úrreikningi á uppskriftarstigi.


## <a name="create-an-obsolete-state"></a>Stofna úrelda stöðu
1. Fara í Upplýsingastjórnun afurðar > Uppsetning > Lífferilsstaða afurðar.
2. Smellið á „Nýtt“.
3. Í reitinn Staða skal slá inn gildi.
4. Velja skal Nei í reitinum Er virk fyrir áætlunargerð.
5. Sláið inn gildi í reitnum „Lýsing“.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Tengja úrelta stöðu á útgefina afurð
1. Lokið síðunni.
2. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
3. Nota flýtiafmörkun til að finna færslur Til dæmis skal sía svæðið Leitarheiti með gildinu „M00“.
4. Smellið á „Breyta“.
5. Í listanum skal merkja valda línu.
6. Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.

