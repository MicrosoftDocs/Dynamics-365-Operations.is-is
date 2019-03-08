---
title: Búa til færslusniðmát til að greiða fyrir skráningu gagna
description: Þetta ferli sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "315982"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="eaa63-103">Búa til færslusniðmát til að greiða fyrir skráningu gagna</span><span class="sxs-lookup"><span data-stu-id="eaa63-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eaa63-104">Þetta ferli sýnir hvernig stofna færslusniðmát til að gildi í svæði sem oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.</span><span class="sxs-lookup"><span data-stu-id="eaa63-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="eaa63-105">Í þessu ferli er stofnað ný færsla fyrir nýjar fartölvur sem ætti að bæta við þínar eignir.</span><span class="sxs-lookup"><span data-stu-id="eaa63-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="eaa63-106">Þetta ferli notar USMF sýnifyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="eaa63-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="eaa63-107">Fara í Eignir > Eignir > Eignir.</span><span class="sxs-lookup"><span data-stu-id="eaa63-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="eaa63-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-108">Click New.</span></span>
3. <span data-ttu-id="eaa63-109">Færa inn eða veljið gildi í svæðinu eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="eaa63-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="eaa63-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eaa63-111">Til dæmis, slá inn „fartölva yfirmanns“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="eaa63-112">Í svæði Leita að nafni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="eaa63-113">Til dæmis slá inn „fartölva“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="eaa63-114">Víkka út hlutann Tæknilegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="eaa63-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="eaa63-115">Í svæðinu Tegund, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="eaa63-116">Í svæði Reitur, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="eaa63-117">Í svæðinu Árgerð, slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="eaa63-118">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="eaa63-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="eaa63-119">Smellt er á Upplýsingar um færslu.</span><span class="sxs-lookup"><span data-stu-id="eaa63-119">Click Record info.</span></span>
12. <span data-ttu-id="eaa63-120">Smellt er á Notandasniðmát.</span><span class="sxs-lookup"><span data-stu-id="eaa63-120">Click User template.</span></span>
13. <span data-ttu-id="eaa63-121">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eaa63-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eaa63-122">Til dæmis, slá inn „fartölva fyrirtækis“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="eaa63-123">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="eaa63-124">Til dæmis, slá inn „fartölva fyrirtækis“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="eaa63-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-125">Click OK.</span></span>
16. <span data-ttu-id="eaa63-126">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="eaa63-126">Click Close.</span></span>

