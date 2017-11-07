---
title: "Eitt fylgiskjal og gjaldmiðilsendurmatsuppfærsla"
description: "Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Eitt fylgiskjal og gjaldmiðilsendurmatsuppfærsla

[!include[banner](../includes/banner.md)]


Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.

Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 for Operations útgáfu 1611.

1.  Áður en uppfært er í Dynamics 365 for Operations skal keyra endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur. Í reitnum **Aðferð** skal stilla á **Dagsetning reiknings**. Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli. Því eru opnar færslur metnar eftir upprunalegum bókhaldsgjaldmiðli.
2.  Uppfæra í Dynamics 365 for Operations útgáfu 1611.
3.  Keyra skal endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur aftur. Í þetta sinn skal stilla **Aðferð** á **Staðlað**. Ný endurmatsfærsla er stofnið sem byggir á gildandi gengi. Þessi færsla skráir óinnleystan hagnað/tap og réttan samantektarlykil fjárhags.





