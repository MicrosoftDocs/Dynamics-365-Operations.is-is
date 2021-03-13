---
title: Verkbeiðnir og eignir
description: Þetta efni útskýrir verkbeiðnir og eignir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4eadbdc452a5b7d28adfa0f102a9a727faad3c07
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016704"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="1d8dd-103">Verkbeiðnir og eignir</span><span class="sxs-lookup"><span data-stu-id="1d8dd-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1d8dd-104">Í eignastýringu geta eignir verið tengdar fastafjármunum og þú getur búið til verkbeiðnir fyrir þessar eignir.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="1d8dd-105">Ef þú notar þessa virkni geturðu fengið fullkomið yfirlit yfir fastafjármuni, tengd fjárfestingarverkefni og kostnaðinn sem skráður er á fjárfestingarverkefnin í einingunum **Verkefnisstjórnun og bókhald** og **Fastafjármunir** í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="1d8dd-106">Reiturinn **Númer eignar** í vinnslu verkbeiðni er aðeins stilltur ef **Fjárfesting** er valin sem verkgerð í verkbeiðnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="1d8dd-107">Myndin hér að neðan sýnir tengsl fjárfestingarverkefnis í einingunni **Verkefnisstjórnun og bókhald** og vinnuverkefni vinnuverkefni.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Mynd 1](media/24-work-orders.png)

<span data-ttu-id="1d8dd-109">Eftirfarandi aðferð lýsir tengslum á milli eigna, verkbeiðna, verkbeiðniverka og fastafjármuna.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="1d8dd-110">Þú býrð til eign sem þú tengir fastafjármunum.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-110">You create an asset that you relate to a fixed asset.</span></span>

![Mynd 2](media/25-work-orders.png)

2. <span data-ttu-id="1d8dd-112">Þegar þú setur upp verkbeiðnigerðir á síðunni **Gerðir verkbeiðna** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Verkbeiðnigerðir**) býrðu til verkbeiðnigerð til að meðhöndla fjárfestingar.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="1d8dd-113">Sjá einnig [Verkbeiðnigerðir](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="1d8dd-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Mynd 3](media/26-work-orders.png)

3. <span data-ttu-id="1d8dd-115">Þegar þú setur upp verkflokka verkbeiðna á flipanum **Verkflokkur** á síðunni **Verkuppsetning verkbeiðni** (**Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verks**) býrðu til tengsl milli þeirrar verkbeiðnigerðar sem notuð er við fjárfestingar og verkefnahópsins sem stofnað var til vegna fjárfestinga á síðunni **Verkflokkar** í einingunni **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Uppsetning** > **Bókun** > **Verkefnahópar**).</span><span class="sxs-lookup"><span data-stu-id="1d8dd-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Mynd 4](media/27-work-orders.png)

4. <span data-ttu-id="1d8dd-117">Þegar þú býrð til verkbeiðni sem tengist fastri eign velur þú þá gerð verkbeiðni sem notuð er til að meðhöndla fjárfestingar, til dæmis **Fjárfesting**.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="1d8dd-118">Þegar verkbeiðni er búin til, er tengd tegund verkbeiðni sýnd á síðunni **Allar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Mynd 5](media/28-work-orders.png)

6. <span data-ttu-id="1d8dd-120">Þegar verkbeiðnin er búin til er verkið sem tengist verkbeiðninni búið til á síðunni **Öll verk** í einingunn **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Verk** > **Öll verk**).</span><span class="sxs-lookup"><span data-stu-id="1d8dd-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="1d8dd-121">Til að skoða upplýsingar sem tengjast verkefninu, veldu tengilinn í reitnum **Kenni verks** á flipanum **Almennt** á flýtiflipanum **Línulýsing** á upplýsingasíðunni **Allar verkbeiðnir** í einingunni **Eignastýring** (**Eignastýring** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir**).</span><span class="sxs-lookup"><span data-stu-id="1d8dd-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Mynd 6](media/29-work-orders.png)

7. <span data-ttu-id="1d8dd-123">Til að sjá yfirlit yfir verk sem eru tengd fastri eign skaltu velja **Fastar eignir** > **Fastar eignir** > **Fastar eignir** og síðan í reitnum **Númer fastrar eignar** velurðu tengilinn fyrir föstu eignina til að opna upplýsingaglugga.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="1d8dd-124">Stækkaðu gluggann **Tengdar upplýsingar** hægra megin á síðunni og veldu flýtiflipann **Tengd verk**.</span><span class="sxs-lookup"><span data-stu-id="1d8dd-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>

