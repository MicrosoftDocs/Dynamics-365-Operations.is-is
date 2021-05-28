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
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="c9742-103">Ekki er hægt að reikningsfæra sölupöntun sem snýr að viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="c9742-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="c9742-104">KB númer: 4611793</span><span class="sxs-lookup"><span data-stu-id="c9742-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="c9742-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="c9742-105">Symptoms</span></span>

<span data-ttu-id="c9742-106">Þú getur ekki lengur reikningsfært upprunalegu sölupöntunina og upphaflegu innkaupapöntunina fyrir beina afhendingu eftir að þú hefur virkjað **Bóka reikning sjálfvirkt** á síðunni **Innan samstæðu** fyrir lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="c9742-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="c9742-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="c9742-107">Resolution</span></span>

<span data-ttu-id="c9742-108">Samstillingarhegðun fyrir samstæðureikninga og reikninga fyrir beina afgreiðslu er stjórnað og þvingað af færibreytum sem lýst er í [Setja upp færibreytur til að bóka samstæðupöntun](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="c9742-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="c9742-109">Eftir að þessar færibreytur hafa verið stilltar þarf fyrst að reikningsfæra samstæðusölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="c9742-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="c9742-110">Upprunalegar sölupantanir og innkaupapantanir verða síðan samstilltar.</span><span class="sxs-lookup"><span data-stu-id="c9742-110">The original sales orders and purchase orders will then be synchronized.</span></span>
