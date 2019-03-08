---
title: " Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum"
description: Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33e0b1da5d16372b8a3c4cd153f451166af6003f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "360487"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="bc467-103"> Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum</span><span class="sxs-lookup"><span data-stu-id="bc467-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bc467-104">Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="bc467-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="bc467-105">Þetta ferli ekki taka með aðrar tengdar skref, s.s. að stofna víddarsamstæður og lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="bc467-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="bc467-106">Þessum verkefnum er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="bc467-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="bc467-107">Þessi skráning notar sýnigögn USRT fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="bc467-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="bc467-108">Fara í fjárhag > Línurit yfir lykla > Víddir > Fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="bc467-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="bc467-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bc467-109">Click New.</span></span>
3. <span data-ttu-id="bc467-110">Veljið í svæðinu Nota gildi frá,veldu valkostur'.</span><span class="sxs-lookup"><span data-stu-id="bc467-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="bc467-111">Í reitinn Heiti víddar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bc467-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="bc467-112">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="bc467-112">Click Activate.</span></span>
6. <span data-ttu-id="bc467-113">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="bc467-113">Click Close.</span></span>
7. <span data-ttu-id="bc467-114">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="bc467-114">Click Activate.</span></span>
8. <span data-ttu-id="bc467-115">Smellt er á víddargildi.</span><span class="sxs-lookup"><span data-stu-id="bc467-115">Click Dimension values.</span></span>
9. <span data-ttu-id="bc467-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bc467-116">Close the page.</span></span>
10. <span data-ttu-id="bc467-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="bc467-117">Click Save.</span></span>
11. <span data-ttu-id="bc467-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bc467-118">Close the page.</span></span>
12. <span data-ttu-id="bc467-119">Fara í Smásala og viðskipti > Uppsetning rásar > Uppsetning smásölustaðar >Skrár.</span><span class="sxs-lookup"><span data-stu-id="bc467-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="bc467-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="bc467-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bc467-121">Víxla útvíkkun á liðnum fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="bc467-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="bc467-122">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="bc467-122">Click Edit.</span></span>
16. <span data-ttu-id="bc467-123">Í reitnum afgreiðslustöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bc467-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="bc467-124">Á listanum, Finna og velja víddargildi fyrir afgreiðslukassi sem verið er að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="bc467-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="bc467-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="bc467-125">Click Save.</span></span>

