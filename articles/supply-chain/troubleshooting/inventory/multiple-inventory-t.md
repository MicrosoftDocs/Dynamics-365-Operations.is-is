---
title: Margar birgðafærslur fyrir rununúmer þegar slökkt er á „Við efnislega uppfærslu“
description: Fjölmargar birgðafærslur eru stofnaðar eftir að þú stillir innkaupapöntunarlínu fyrir vörur þar sem valkosturinn „Við efnislega uppfærslu“ fyrir lotunúmerahópinn er stilltur á Nei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026623"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="70b0b-103">Margar birgðafærslur fyrir rununúmer þegar slökkt er á „Við efnislega uppfærslu“</span><span class="sxs-lookup"><span data-stu-id="70b0b-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="70b0b-104">KB númer: 4613390</span><span class="sxs-lookup"><span data-stu-id="70b0b-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="70b0b-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="70b0b-105">Symptoms</span></span>

<span data-ttu-id="70b0b-106">Fjölmargar birgðafærslur eru stofnaðar eftir að þú stillir innkaupapöntunarlínu fyrir vörur þar sem valkosturinn **Við efnislega uppfærslu** fyrir lotunúmerahópinn er stilltur á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="70b0b-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="70b0b-107">Þegar búið er að stofna vöru þar sem valkosturinn **Við efnislega uppfærslu** í lotunúmeraflokknum er stilltur á *Nei* stofnar kerfið sjálfkrafa nýtt lotunúmer ef breyta á innkaupalínumagni og vista síðuna fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="70b0b-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="70b0b-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="70b0b-108">Resolution</span></span>

<span data-ttu-id="70b0b-109">Stillingin **Við efnislega uppfærslu** fyrir lotunúmerahópa virkar með eftirfarandi hætti:</span><span class="sxs-lookup"><span data-stu-id="70b0b-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="70b0b-110">Þegar valkosturinn er stilltur á *Já* eru ný lotunúmer aðeins búin til eftir efnislegar uppfærslur (til dæmis þegar atriði eru send eða móttekin).</span><span class="sxs-lookup"><span data-stu-id="70b0b-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="70b0b-111">Þegar valkosturinn er stilltur á *Nei* er nýtt lotunúmer stofnað í hvert sinn sem viðeigandi uppfærsla á sér stað (til dæmis þegar nýju magni er bætt við innkaupapöntun).</span><span class="sxs-lookup"><span data-stu-id="70b0b-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
