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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756752"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Ekki er hægt að reikningsfæra sölupöntun sem snýr að viðskiptavini

KB númer: 4611793

## <a name="symptoms"></a>Einkenni

Þú getur ekki lengur reikningsfært upprunalegu sölupöntunina og upphaflegu innkaupapöntunina fyrir beina afhendingu eftir að þú hefur virkjað **Bóka reikning sjálfvirkt** á síðunni **Innan samstæðu** fyrir lánardrottinn.

## <a name="resolution"></a>Upplausn

Samstillingarhegðun fyrir samstæðureikninga og reikninga fyrir beina afgreiðslu er stjórnað og þvingað af færibreytum sem lýst er í [Setja upp færibreytur til að bóka samstæðupöntun](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Eftir að þessar færibreytur hafa verið stilltar þarf fyrst að reikningsfæra samstæðusölupöntunina. Upprunalegar sölupantanir og innkaupapantanir verða síðan samstilltar.
