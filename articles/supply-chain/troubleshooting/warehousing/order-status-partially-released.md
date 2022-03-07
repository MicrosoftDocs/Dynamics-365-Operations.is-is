---
title: Staða pöntunar er áfram losuð að hluta eftir reikningsfærslu hennar
description: Í sumum tilvikum er staða sölupöntunar áfram að hluta til losuð, jafnvel eftir að pöntunin hefur verið reikningsfærð. Á þessari síðu er útskýrt hvers vegna og möguleg hjáleið sýnd.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476670"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Staða pöntunar er áfram „Losuð að hluta“ eftir að sölupöntunin hefur verið reikningsfærð

## <a name="symptoms"></a>Einkenni

Sölupöntun er afhendingarpöntun en ein eða fleiri vörur á henni hafa annan flutningsmáta. Þegar pöntunin hefur verið reikningsfærð er hún enn með útgáfustöðu *Losað að hluta*.

Til dæmis er sölupöntun með tvær vörur: eina fyrir afhendingu og eina fyrir tiltekt. Bæði afhendingum og tiltekt hefur verið lokið. Báðar línur hafa verið reikningsfærðar. Útgáfustaðan er hins vegar enn sýnd sem *Losað að hluta*, sem er villandi.

## <a name="workaround"></a>Hjáleið

Losunarstaðan á aðeins við um pöntunarlínur þar sem vörurnar eru virkjaðar fyrir vöruhúsastjórnun. Þess vegna er útgáfustaðan enn *Losað að hluta* í þessum aðstæðum. Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Hægt er að bæta við viðbót sem hluta af fylgiseðli og reikningsfærsluferli til að uppfæra útgáfustöðu.
