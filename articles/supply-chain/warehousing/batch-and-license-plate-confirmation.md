---
title: "Staðfesting lotu og númeraplötu"
description: "Í þessu efnisatriði er lýst hvernig eigi að setja upp og nota staðfestingu runu og númeraplötu úr fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="6c6d2-103">Staðfesting lotu og númeraplötu</span><span class="sxs-lookup"><span data-stu-id="6c6d2-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6c6d2-104">Staðfesting runu gerir kleift að staðfesta að rétt runa sé valin úr fartækinu.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="6c6d2-105">Í fyrstu tiltekt á vinnustöð fyrir vörur með „runu yfir“ eingöngu, þar sem runa yfir gefur til kynna runusvið sem er hærra en staðsetningin í leitarstigveldinu verður að staðfesta að runan sem er valin sé sú sama og er í tiltektarlínu.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="6c6d2-106">Staðfesting númeraplötu gerir kleift að staðfesta að rétt númeraplata sé tekin til úr fartækinu</span><span class="sxs-lookup"><span data-stu-id="6c6d2-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="6c6d2-107">Þegar tiltektarvinna á sér stað úr stigstaðsetningu verður að staðfesta að númeraplatan sem er tekin til sé sú sama og sú sem tengist verkinu.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="6c6d2-108">Ef vinna er hafin með því að skanna númeraplötu er þessu staðfestingarskrefi sleppt.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6c6d2-109">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="6c6d2-109">Where it applies</span></span>
<span data-ttu-id="6c6d2-110">Staðfesting á við við eftirfarandi kringumstæður:</span><span class="sxs-lookup"><span data-stu-id="6c6d2-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="6c6d2-111">Runustaðfesting á við um tiltekt í upphafi á vörum með runu yfir.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="6c6d2-112">Staðfesting á númeraplötu á við um tiltekt úr stigstaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="6c6d2-113">Uppsetning staðfestingar á runu og númeraplötu</span><span class="sxs-lookup"><span data-stu-id="6c6d2-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="6c6d2-114">Hægt er að stilla staðfestingu á runu og númeraplötu úr valmynd í fartæki.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="6c6d2-115">Færið inn uppsetningu á verkstaðfestingu í valmynd fartækisins.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="6c6d2-116">Veljið valmöguleikann fyrir staðfestingu á annaðhvort runu eða númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="6c6d2-117">Báðir valmöguleikar eru í boði fyrir tiltektarvinnu þar sem sjálfkrafa staðfesting er ekki virkjuð.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

