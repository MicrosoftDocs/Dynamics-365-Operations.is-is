---
title: Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli
description: Þetta efni lýsir því hvernig eigi að uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b66b969d13cff7f1f39fb644f459aa92bea198f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743922"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli

[!include [banner](../includes/banner.md)]

Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir. Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.

Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 for Operations útgáfu 1611.

1.  Áður en uppfært er í Finance and Operations skal keyra endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur. Í reitnum **Aðferð** skal stilla á **Dagsetning reiknings**. Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli. Því eru opnar færslur metnar eftir upprunalegum bókhaldsgjaldmiðli.
2.  Uppfærðu í útgáfu 1611.
3.  Keyra skal endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur aftur. Í þetta sinn skal stilla **Aðferð** á **Staðlað**. Ný endurmatsfærsla er stofnið sem byggir á gildandi gengi. Þessi færsla skráir óinnleystan hagnað/tap og réttan samantektarlykil fjárhags.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]