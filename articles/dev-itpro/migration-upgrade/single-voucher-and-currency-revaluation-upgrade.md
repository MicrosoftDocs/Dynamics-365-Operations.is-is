---
title: Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli
description: Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b76354d0b8bb89e09e861e013a0c680c36b6537d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851682"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli

[!include [banner](../includes/banner.md)]

Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.

Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 for Operations útgáfu 1611.

1.  Áður en uppfært er í Dynamics 365 for Operations skal keyra endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur. Í reitnum **Aðferð** skal stilla á **Dagsetning reiknings**. Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli. Því eru opnar færslur metnar eftir upprunalegum bókhaldsgjaldmiðli.
2.  Uppfærðu í Dynamics 365 for Operations útgáfu 1611.
3.  Keyra skal endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur aftur. Í þetta sinn skal stilla **Aðferð** á **Staðlað**. Ný endurmatsfærsla er stofnið sem byggir á gildandi gengi. Þessi færsla skráir óinnleystan hagnað/tap og réttan samantektarlykil fjárhags.




