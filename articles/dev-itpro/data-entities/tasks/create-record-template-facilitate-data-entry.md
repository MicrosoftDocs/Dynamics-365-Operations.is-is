--- 
title: "Búa til færslusniðmát til að greiða fyrir skráningu gagna"
description: "Þetta ferli sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla."
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="6d7a1-103">Búa til færslusniðmát til að greiða fyrir skráningu gagna</span><span class="sxs-lookup"><span data-stu-id="6d7a1-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d7a1-104">Þetta ferli sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="6d7a1-105">Í þessu ferli er stofnað ný færsla fyrir nýjar fartölvur sem ætti að bæta við þínar eignir.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="6d7a1-106">Þetta ferli notar USMF sýnifyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="6d7a1-107">Fara í Eignir > Eignir > Eignir.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="6d7a1-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-108">Click New.</span></span>
3. <span data-ttu-id="6d7a1-109">Færa inn eða veljið gildi í svæðinu eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="6d7a1-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6d7a1-111">Til dæmis, slá inn „fartölva yfirmanns“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="6d7a1-112">Í svæði Leita að nafni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="6d7a1-113">Til dæmis slá inn „fartölva“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="6d7a1-114">Víkka út hlutann Tæknilegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="6d7a1-115">Í svæðinu Tegund, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="6d7a1-116">Í svæði Reitur, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="6d7a1-117">Í svæðinu Árgerð, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="6d7a1-118">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="6d7a1-119">Smellt er á Upplýsingar um færslu.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-119">Click Record info.</span></span>
12. <span data-ttu-id="6d7a1-120">Smellt er á Notandasniðmát.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-120">Click User template.</span></span>
13. <span data-ttu-id="6d7a1-121">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6d7a1-122">Til dæmis, slá inn „fartölva fyrirtækis“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="6d7a1-123">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6d7a1-124">Til dæmis, slá inn „fartölva fyrirtækis“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="6d7a1-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-125">Click OK.</span></span>
16. <span data-ttu-id="6d7a1-126">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="6d7a1-126">Click Close.</span></span>


