---
title: Stofna vaxtakóða með sviði
description: Hægt er að setja upp vaxtakóða til að reikna vexti á mismunandi upphæðir samkvæmt svið gilda.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d684eedd5b40ee9775ab779c243d05cdc6e01f58
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842978"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="6f24d-103">Stofna vaxtakóða með sviði</span><span class="sxs-lookup"><span data-stu-id="6f24d-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f24d-104">Hægt er að setja upp vaxtakóða til að reikna vexti á mismunandi upphæðir samkvæmt svið gilda.</span><span class="sxs-lookup"><span data-stu-id="6f24d-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="6f24d-105">Þetta ferli sýnir hvernig á að bæta vaxtakóða og bæta afmörkun við hana.</span><span class="sxs-lookup"><span data-stu-id="6f24d-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="6f24d-106">Fara í Skuldir og innheimta > Vextir > Setja upp vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="6f24d-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="6f24d-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6f24d-107">Click New.</span></span>
3. <span data-ttu-id="6f24d-108">Í svæðinu vaxtakóði, færðu inn heiti vaxtakóða</span><span class="sxs-lookup"><span data-stu-id="6f24d-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="6f24d-109">Í reitnum Lýsing færirðu inn lýsingu á vaxtakóði.</span><span class="sxs-lookup"><span data-stu-id="6f24d-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="6f24d-110">Velja Mánuð.</span><span class="sxs-lookup"><span data-stu-id="6f24d-110">Select Month.</span></span>
6. <span data-ttu-id="6f24d-111">Víkkið út hlutann tekjur.</span><span class="sxs-lookup"><span data-stu-id="6f24d-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="6f24d-112">Útvíkka hlutann tekjur eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="6f24d-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="6f24d-113">Í Fjárhagsbókunarlykli svæðinu, tilgreinið gildin sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6f24d-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="6f24d-114">Í svæðinu Vextir eftir sviði, velja "Mánuðir".</span><span class="sxs-lookup"><span data-stu-id="6f24d-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="6f24d-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6f24d-115">Click Add.</span></span>
11. <span data-ttu-id="6f24d-116">Færið inn lýsingu fyrir þessa gjaldmiðil og svið í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="6f24d-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="6f24d-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6f24d-117">Click Save.</span></span>
13. <span data-ttu-id="6f24d-118">Smellt er á svið.</span><span class="sxs-lookup"><span data-stu-id="6f24d-118">Click Ranges.</span></span>
14. <span data-ttu-id="6f24d-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6f24d-119">Click New.</span></span>
15. <span data-ttu-id="6f24d-120">Færið inn Frá gildið sem 0 og færið svo vexti í prósentum á mánuði sem verður notað til að reikna vexti.</span><span class="sxs-lookup"><span data-stu-id="6f24d-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="6f24d-121">Til dæmis okkar er 1,5.</span><span class="sxs-lookup"><span data-stu-id="6f24d-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="6f24d-122">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6f24d-122">Click New.</span></span>
17. <span data-ttu-id="6f24d-123">Færið inn næsta gildi Frá sem 4, sem er í fyrsta mánuðinum sem þú verður að reikna út nýja vaxtaupphæð.</span><span class="sxs-lookup"><span data-stu-id="6f24d-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="6f24d-124">Færa skal inn vexti í prósentum á mánuði sem verður notað til að reikna vexti frá og með mánuði 4.</span><span class="sxs-lookup"><span data-stu-id="6f24d-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="6f24d-125">Í þessu dæmi er það 2,0.</span><span class="sxs-lookup"><span data-stu-id="6f24d-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="6f24d-126">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6f24d-126">Click New.</span></span>
20. <span data-ttu-id="6f24d-127">Færið inn næsta gildi Frá sem 7 sem er næsta mánuð sem þú verður að reikna út nýja vaxtaupphæð.</span><span class="sxs-lookup"><span data-stu-id="6f24d-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="6f24d-128">Færa skal inn vexti í prósentum á mánuði sem verður notað til að reikna vexti frá og með mánuði 7.</span><span class="sxs-lookup"><span data-stu-id="6f24d-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="6f24d-129">Í þessu dæmi er það 2,5.</span><span class="sxs-lookup"><span data-stu-id="6f24d-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="6f24d-130">Smellið á Loka Til að ljúka uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="6f24d-130">Click Close to complete the setup.</span></span>

