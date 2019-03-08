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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "328149"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="7fdd1-104">Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="7fdd1-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fdd1-105">Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="7fdd1-106">Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="7fdd1-107">Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="7fdd1-108">Áður en uppfært er í Dynamics 365 for Operations skal keyra endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="7fdd1-109">Í reitnum **Aðferð** skal stilla á **Dagsetning reiknings**.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="7fdd1-110">Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="7fdd1-111">Því eru opnar færslur metnar eftir upprunalegum bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="7fdd1-112">Uppfærðu í Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="7fdd1-113">Keyra skal endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur aftur.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="7fdd1-114">Í þetta sinn skal stilla **Aðferð** á **Staðlað**.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="7fdd1-115">Ný endurmatsfærsla er stofnið sem byggir á gildandi gengi.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="7fdd1-116">Þessi færsla skráir óinnleystan hagnað/tap og réttan samantektarlykil fjárhags.</span><span class="sxs-lookup"><span data-stu-id="7fdd1-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




