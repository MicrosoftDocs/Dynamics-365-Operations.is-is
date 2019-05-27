---
title: Stilla skjá eldri keyrsla innan vöruhúss á fartæki
description: Þetta efnisatriði lýsir því hvernig eigi að setja upp fartæki svo það birti lista yfir staðsetningar með eldri runum en núverandi staðsetning á vinnulínu.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569429"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="98a63-103">Stilla skjá eldri keyrsla innan vöruhúss á fartæki</span><span class="sxs-lookup"><span data-stu-id="98a63-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a63-104">Skilgreiningin **Birta eldri runur innan vöruhússins** gefur kost á að birta lista yfir staðsetningar með eldri runum en núverandi staðsetning á vinnulínunni.</span><span class="sxs-lookup"><span data-stu-id="98a63-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="98a63-105">Listinn yfir staðsetningar sem eru birtar inniheldur upplýsingar um eldri runur á staðsetningunni með lokatíma og efnislegum birgðum hverrar runu.</span><span class="sxs-lookup"><span data-stu-id="98a63-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="98a63-106">Hægt er að velja tiltekt frá nýrri staðsetningu eða að halda áfram tiltekt frá gildandi staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="98a63-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="98a63-107">Tiltekt frá nýrri staðsetningu - Ef valin er ný staðsetning fyrir tiltekt verður núverandi vinnulína uppfærð til að nota nýju staðsetninguna og vinna heldur áfram sem fyrr með nýju staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="98a63-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="98a63-108">Svo nýja staðsetningin sé gild verður hún að hafa nægt tiltækt magn fyrir alla vinnulínuna.</span><span class="sxs-lookup"><span data-stu-id="98a63-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="98a63-109">Ef nauðsynlegt magn er ekki tiltækt verður vinnulínan ekki uppfærð og listinn birtist.</span><span class="sxs-lookup"><span data-stu-id="98a63-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="98a63-110">Halda áfram tiltekt frá núverandi staðsetningu - Ef haldið er áfram með gildandi staðsetningu vinnulínu heldur tiltekt á magni fyrir vinnulínuna áfram frá upphaflegri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="98a63-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="98a63-111">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="98a63-111">Where it applies</span></span>
<span data-ttu-id="98a63-112">Birta eldri runur innan vöruhússins er grunnstillt í valmyndaratriðum fartækis og hefur áhrif á tiltekt á neðangreindum runum vara.</span><span class="sxs-lookup"><span data-stu-id="98a63-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="98a63-113">Setja upp Birta eldri runur innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="98a63-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="98a63-114">Stillingin **Birta eldri runur innan vöruhússins** er í boði í valmyndaratriðum fartækja þegar valkosturinn **Tína elstu runu** er stilltur á **Vara við**.</span><span class="sxs-lookup"><span data-stu-id="98a63-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="98a63-115">Undir **Vöruhúsastjórnun** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis** stillirðu **Nota fyrirliggjandi verk** á **Já** fyrir valmyndaratriðið, og velur **Vara við** í reitnum **Tína elsta runu**.</span><span class="sxs-lookup"><span data-stu-id="98a63-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

