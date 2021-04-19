---
title: Staðfesting lotu og númeraplötu
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp og nota staðfestingu runu og númeraplötu úr fartæki.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837538"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="618de-103">Staðfesting lotu og númeraplötu</span><span class="sxs-lookup"><span data-stu-id="618de-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="618de-104">Staðfesting runu gerir kleift að staðfesta að rétt runa sé valin úr fartækinu.</span><span class="sxs-lookup"><span data-stu-id="618de-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="618de-105">Í fyrstu tiltekt á vinnustöð fyrir vörur með *Runa fyrir ofan\[staðsetningu\]* eingöngu, þar sem runa fyrir ofan gefur til kynna að runa sem er hærri en staðsetningin í leitarstigveldinu, verður að staðfesta að runan sem er valin sé sú sama og er í tiltektarlínu.</span><span class="sxs-lookup"><span data-stu-id="618de-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="618de-106">Staðfesting númeraplötu gerir kleift að staðfesta að rétt númeraplata sé tekin til úr fartækinu</span><span class="sxs-lookup"><span data-stu-id="618de-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="618de-107">Þegar tiltektarvinna á sér stað úr stigstaðsetningu verður að staðfesta að númeraplatan sem er tekin til sé sú sama og sú sem tengist verkinu.</span><span class="sxs-lookup"><span data-stu-id="618de-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="618de-108">Ef vinna er hafin með því að skanna númeraplötu er þessu staðfestingarskrefi sleppt.</span><span class="sxs-lookup"><span data-stu-id="618de-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="618de-109">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="618de-109">Where it applies</span></span>

<span data-ttu-id="618de-110">Staðfesting á við við eftirfarandi kringumstæður:</span><span class="sxs-lookup"><span data-stu-id="618de-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="618de-111">Runustaðfesting á við um tiltekt í upphafi á vörum með runu yfir.</span><span class="sxs-lookup"><span data-stu-id="618de-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="618de-112">Staðfesting á númeraplötu á við um tiltekt úr stigstaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="618de-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="618de-113">Áfylling er ekki studd fyrir staðfestingu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="618de-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="618de-114">Engin staðfestingarskref númeraplötu eru stofnuð þegar verið er að framkvæma áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="618de-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="618de-115">Uppsetning staðfestingar á runu og númeraplötu</span><span class="sxs-lookup"><span data-stu-id="618de-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="618de-116">Hægt er að stilla staðfestingu á runu og númeraplötu úr valmynd í fartæki.</span><span class="sxs-lookup"><span data-stu-id="618de-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="618de-117">Færið inn uppsetningu á verkstaðfestingu í valmynd fartækisins.</span><span class="sxs-lookup"><span data-stu-id="618de-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="618de-118">Veljið valmöguleikann fyrir staðfestingu á annaðhvort runu eða númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="618de-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="618de-119">Báðir valmöguleikar eru í boði fyrir tiltektarvinnu þar sem sjálfkrafa staðfesting er ekki virkjuð.</span><span class="sxs-lookup"><span data-stu-id="618de-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
