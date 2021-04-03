---
title: Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli
description: Þetta efni lýsir því hvernig eigi að uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli.
author: ShylaThompson
manager: AnnBe
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
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559522"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="e8c6d-103">Uppfæra færslubækur með eitt fylgiskjal og endurmat á gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="e8c6d-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8c6d-104">Sum fyrirtæki nota færslubækur sem innihalda eitt fylgiskjal sem hefur fleiri en einn viðskiptavin eða lánardrottinn og keyra einnig endurmat á erlendum gjaldmiðli fyrir Viðskiptakröfur eða Viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="e8c6d-105">Þetta efnisatriði lýsir skrefunum sem þessi fyrirtæki ættu að fylgja þegar þau uppfæra í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="e8c6d-106">Fylgið eftirfarandi skrefum þegar uppfært er í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="e8c6d-107">Áður en uppfært er í Finance and Operations skal keyra endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="e8c6d-108">Í reitnum **Aðferð** skal stilla á **Dagsetning reiknings**.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="e8c6d-109">Endurmatsfærsla er stofnuð sem bakfærir síðasta endurmat á erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="e8c6d-110">Því eru opnar færslur metnar eftir upprunalegum bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="e8c6d-111">Uppfærðu í útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="e8c6d-112">Keyra skal endurmat á erlendum gjaldmiðli fyrir viðskiptaskuldir og viðskiptakröfur aftur.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="e8c6d-113">Í þetta sinn skal stilla **Aðferð** á **Staðlað**.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="e8c6d-114">Ný endurmatsfærsla er stofnið sem byggir á gildandi gengi.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="e8c6d-115">Þessi færsla skráir óinnleystan hagnað/tap og réttan samantektarlykil fjárhags.</span><span class="sxs-lookup"><span data-stu-id="e8c6d-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]