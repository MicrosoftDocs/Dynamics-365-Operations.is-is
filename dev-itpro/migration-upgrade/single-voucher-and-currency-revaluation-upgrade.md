---
title: "Eitt fylgiskjal og gjaldmiðilsendurmatið gagnauppfærslu fyrir Microsoft Dynamics 365 Aðgerðir útgáfu 1611"
description: "Sum fyrirtæki inn færslubækur sem innihalda eitt fylgiskjal hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra þau einnig Viðskiptakröfur eða Lykla viðskiptaskulda erlendum gjaldmiðli endurmat ferli. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki á að fylgja þegar þeir uppfærslu Microsoft Dynamics 365 Aðgerðir útgáfu 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Eitt fylgiskjal og gjaldmiðilsendurmatið gagnauppfærslu fyrir Microsoft Dynamics 365 Aðgerðir útgáfu 1611

Sum fyrirtæki inn færslubækur sem innihalda eitt fylgiskjal hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra þau einnig Viðskiptakröfur eða Lykla viðskiptaskulda erlendum gjaldmiðli endurmat ferli. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki á að fylgja þegar þeir uppfærslu Microsoft Dynamics 365 Aðgerðir útgáfu 1611.

Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 Aðgerðir útgáfu 1611.

1.  Keyra ferli endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur og Viðskiptaskuldir áður en uppfært er í Dynamics 365 fyrir Aðgerðir. Setja skal **Aðferð** á **Reikningsdagsetningar**. Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli. Því opnar færslur eru metnar þeirra upprunalegu bókhaldsgjaldmiðli.
2.  Uppfæra í Dynamics 365 Aðgerðir útgáfu 1611.
3.  Keyra Viðskiptakröfur og Lykla lánardrottna erlendum gjaldmiðli endurmat ferli aftur. Þessi tími er sett í **Aðferðina** svæðinu **Staðlaða**. Ný endurmatsfærsla er stofnað sem byggir á gildandi gengi. Þessi færsla færslur óinnleystur hagnaður/tap og rétt samantektarlykil fjárhags.



