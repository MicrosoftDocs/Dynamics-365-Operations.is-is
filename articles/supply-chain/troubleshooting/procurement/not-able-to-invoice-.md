---
title: Ekki er hægt að reikningsfæra sölupöntun sem snýr að viðskiptavini
description: Þú getur ekki lengur reikningsfært upphaflegu sölupöntunina og upphaflega innkaupapöntunina með beinni afhendingu eftir að þú hefur virkjað sjálfkrafa bókun reiknings.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026605"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Ekki er hægt að reikningsfæra sölupöntun sem snýr að viðskiptavini

KB númer: 4611793

## <a name="symptoms"></a>Einkenni

Þú getur ekki lengur reikningsfært upprunalegu sölupöntunina og upphaflegu innkaupapöntunina fyrir beina afhendingu eftir að þú hefur virkjað **Bóka reikning sjálfvirkt** á síðunni **Innan samstæðu** fyrir lánardrottinn.

## <a name="resolution"></a>Upplausn

Samstillingarhegðun fyrir samstæðureikninga og reikninga fyrir beina afgreiðslu er stjórnað og þvingað af færibreytum sem lýst er í [Setja upp færibreytur til að bóka samstæðupöntun](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Eftir að þessar færibreytur hafa verið stilltar þarf fyrst að reikningsfæra samstæðusölupöntunina. Upprunalegar sölupantanir og innkaupapantanir verða síðan samstilltar.
