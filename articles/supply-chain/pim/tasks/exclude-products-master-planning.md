---
title: Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð
description: Þessi ferli sýnir hvernig á að stofna nýja lífferlisstöðu afurðar sem útilokar vörur úr aðaláætlanagerð og úrreikningi á uppskriftarstigi.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264699"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]