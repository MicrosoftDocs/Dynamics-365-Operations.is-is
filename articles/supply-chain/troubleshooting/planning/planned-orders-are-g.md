---
title: Aðaláætlanagerð býr til áætlaðar pantanir fyrir skuggaafurðir
description: Áætlaðar pantanir eru stofnaðar fyrir skuggaafurðir eftir að aðaláætlanagerð er keyrð.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026616"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="7866f-103">Aðaláætlanagerð býr til áætlaðar pantanir fyrir skuggaafurðir</span><span class="sxs-lookup"><span data-stu-id="7866f-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="7866f-104">KB númer: 4614729</span><span class="sxs-lookup"><span data-stu-id="7866f-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="7866f-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="7866f-105">Symptoms</span></span>

<span data-ttu-id="7866f-106">Áætlaðar pantanir eru stofnaðar fyrir skuggaafurðir eftir að aðaláætlanagerð er keyrð.</span><span class="sxs-lookup"><span data-stu-id="7866f-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="7866f-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="7866f-107">Resolution</span></span>

<span data-ttu-id="7866f-108">Stilling **Phantom** valkostsins fyrir útgefnar vörur ákvarðar sjálfgefna línutegund á uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="7866f-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="7866f-109">Þegar valkosturinn **Skuggi** er stilltur á *Já* mun kerfið enn búa til áætlaðar pantanir fyrir atriðið en valkosturinn **Beint afleidd þörf** fyrir hverja skipulagða pöntun verður stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="7866f-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="7866f-110">Því er ekki hægt að staðfesta áætlaða framleiðslupöntun eina og sér.</span><span class="sxs-lookup"><span data-stu-id="7866f-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="7866f-111">Þess í stað verður hann alltaf sjálfvirkt innifalinn þegar yfirframleiðslupöntun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="7866f-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="7866f-112">Að auki verða styttri línur fyrirhugaðrar skuggapöntunar teknar með í uppskrift yfirframleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="7866f-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
