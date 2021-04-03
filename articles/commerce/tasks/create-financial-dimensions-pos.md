---
title: Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum
description: Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4042fb9da0fe38de50ad7e0c8e64b98925ea1188
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265960"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="dac0f-103">Stofna fjárhagsvíddir fyrir afgreiðslukassa og skilgreina víddagildi í afgreiðslukössum</span><span class="sxs-lookup"><span data-stu-id="dac0f-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dac0f-104">Þetta ferli fer í gegnum stofnun fjárhagslegar víddir fyrir afgreiðslukassa á sölustað og sýnir hvernig skal skilgreina gildi fjárhagsvídda á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="dac0f-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="dac0f-105">Þetta ferli tekur ekki til annarra tengdra skrefa, s.s. að stofna víddarsamstæður og lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="dac0f-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="dac0f-106">Þessum verkefnum er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="dac0f-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="dac0f-107">Þessi skráning notar sýnigögn USRT fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="dac0f-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="dac0f-108">Fara í fjárhag > Línurit yfir lykla > Víddir > Fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="dac0f-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="dac0f-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dac0f-109">Click New.</span></span>
3. <span data-ttu-id="dac0f-110">Veljið í svæðinu Nota gildi frá,veldu valkostur'.</span><span class="sxs-lookup"><span data-stu-id="dac0f-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="dac0f-111">Í reitinn Heiti víddar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dac0f-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="dac0f-112">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="dac0f-112">Click Activate.</span></span>
6. <span data-ttu-id="dac0f-113">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="dac0f-113">Click Close.</span></span>
7. <span data-ttu-id="dac0f-114">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="dac0f-114">Click Activate.</span></span>
8. <span data-ttu-id="dac0f-115">Smellt er á víddargildi.</span><span class="sxs-lookup"><span data-stu-id="dac0f-115">Click Dimension values.</span></span>
9. <span data-ttu-id="dac0f-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dac0f-116">Close the page.</span></span>
10. <span data-ttu-id="dac0f-117">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="dac0f-117">Click Save.</span></span>
11. <span data-ttu-id="dac0f-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dac0f-118">Close the page.</span></span>
12. <span data-ttu-id="dac0f-119">Fara í Retail og Commerce > Uppsetning rásar > Uppsetning smásölustaðar > Afgreiðslukassar.</span><span class="sxs-lookup"><span data-stu-id="dac0f-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="dac0f-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dac0f-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="dac0f-121">Víxla útvíkkun á liðnum fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="dac0f-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="dac0f-122">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="dac0f-122">Click Edit.</span></span>
16. <span data-ttu-id="dac0f-123">Í reitnum afgreiðslustöð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dac0f-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="dac0f-124">Á listanum, Finna og velja víddargildi fyrir afgreiðslukassi sem verið er að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="dac0f-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="dac0f-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dac0f-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]