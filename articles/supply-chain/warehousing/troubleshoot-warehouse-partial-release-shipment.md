---
title: Úrræðaleit fyrir losun að hluta og hlutaafhendingar
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með hlutalosanir og hlutaafhendingar í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828155"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Úrræðaleit fyrir losun að hluta og hlutaafhendingar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með hlutalosanir og hlutaafhendingar í Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Losunarstaða sölupöntunar er áfram Losuð að hluta eftir að sölupöntunin hefur verið reikningsfærð.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Sölupöntun er afhendingarpöntun en ein eða fleiri vörur á henni hafa annan flutningsmáta. Þegar pöntunin hefur verið reikningsfærð er hún enn með útgáfustöðu *Losað að hluta*.

Til dæmis er sölupöntun með tvær vörur: eina fyrir afhendingu og eina fyrir tiltekt. Bæði afhendingum og tiltekt hefur verið lokið. Báðar línur hafa verið reikningsfærðar. Útgáfustaðan er hins vegar enn sýnd sem *Losað að hluta*, sem er villandi.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Losunarstaðan á aðeins við um pöntunarlínur þar sem vörurnar eru virkjaðar fyrir vöruhúsastjórnun. Þess vegna er útgáfustaðan enn *Losað að hluta* í þessum aðstæðum. Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Hægt er að bæta við viðbót sem hluta af fylgiseðli og reikningsfærsluferli til að uppfæra útgáfustöðu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]