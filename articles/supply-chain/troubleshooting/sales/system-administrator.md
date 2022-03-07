---
title: Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess
description: Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026626"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess

KB númer: 4614642

## <a name="symptoms"></a>Einkenni

Kerfisstjórnendur geta ekki hreinsað sölupantanir í bið nema þeir séu í því hlutverki sem er úthlutað í biðpöntunarkóðanum.

## <a name="resolution"></a>Upplausn

Aðgangur að sumum aðgerðum, svo sem að hreinsa bið sölupöntunar, er drifinn af uppsetningu viðskiptastefnu. Kerfisstjórar hafa yfirleitt ekki heimild til að framkvæma aðgerðir af þessari gerð. 

Oftar fer aðgangur að ákveðnu verkefni eftir viðskiptastefnum og einungis tilteknir aðilar í fyrirtæki eru samþykktir til að framkvæma það verkefni. Sem dæmi má nefna samþykki sem eru afleiðing vinnuflæðisamþykktar og sérstök verkefni sem eru afleiðing vinnuflæðistillingar.

Þrátt fyrir að ekkert vinnuflæði sé tengt við pöntun er aðferðin svipuð. Viðeigandi hlutverk tilnefnir þann tiltekna hóp fólks í fyrirtækjum sem hefur rétt á að hreinsa pantanir í bið. Þennan rétt ætti ekki endilega að veita öllum stjórnendum því sú nálgun brýtur í bága við skilgreinda viðskiptastefnu.
