---
title: Taka til elstu runu í fartæki
description: Þetta efnisatriði lýsir uppsetningu og notkun á valmöguleikum til að taka til elstu runu úr fartæki.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430213"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="a8ecc-103">Taka til elstu runu í fartæki</span><span class="sxs-lookup"><span data-stu-id="a8ecc-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8ecc-104">Hægt er að komast í skilgreininguna **Taka til elstu runu** í gegnum valmynd í fartæki og hún gerir þér kleift að þvinga eða láta starfsmenn í vöruhúsi vita að þeir eigi að taka til elstu rununa í núverandi staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="a8ecc-105">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="a8ecc-105">Where it applies</span></span>
<span data-ttu-id="a8ecc-106">Taka til elstu runu er skilgreint í valmyndaratriðum fartækis og orsakar tiltekt á neðangreindum runum vara.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="a8ecc-107">Hvernig á að setja upp skilgreiningu á Taka til elstu runu</span><span class="sxs-lookup"><span data-stu-id="a8ecc-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="a8ecc-108">Fyrir vörur sem eru stilltar þannig að þær notist við fyrirliggjandi verk er hægt að stilla **Tína elstu runu** á **Engin**, **Aðvara** eða **Þvinga** úr valmynd fartækis.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="a8ecc-109">**Engin**: Starfsmenn fá engin skilaboð og þeim er heimilt að taka til hvaða runu sem er í staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="a8ecc-110">**Aðvara** og **Þvinga**: Listi yfir elstu runu(r) með elsta lokadeginum birtist fyrir ofan runustjórnun þegar starfsmaður velur runu.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="a8ecc-111">Ef staðsetningu er stýrt af númeraplötu birtist listi yfir númeraplötur sem hafa elstu rununa fyrir ofan númeraplötustjórnun.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="a8ecc-112">**Aðvara**: Ef starfsmaður velur númeraplötu eða runu sem ekki birtist á listanum er stjórnunin auð og aðvörun birtist um að það sé eldri runa sem þarf að velja.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="a8ecc-113">Til að geta haldið áfram vinnu getur starfsmaður valið sömu númeraplötu eða runu aftur.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="a8ecc-114">**Þvinga**: Starfsmenn munu áfram fá skilaboðin um að það sé eldri runa sem á að taka til.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>
