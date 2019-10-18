---
title: Verkbeiðnir og eignir
description: Þetta efni útskýrir verkbeiðnir og eignir í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250830"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="fed08-103">Verkbeiðnir og eignir</span><span class="sxs-lookup"><span data-stu-id="fed08-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="fed08-104">Í eignastýringu geta eignir verið tengdar fastafjármunum og þú getur búið til verkbeiðnir fyrir þessar eignir.</span><span class="sxs-lookup"><span data-stu-id="fed08-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="fed08-105">Ef þú notar þessa virkni geturðu fengið fullkomið yfirlit yfir fastafjármuni, tengd fjárfestingarverkefni og kostnaðinn sem skráður er á fjárfestingarverkefnin í einingunni **Verkefnisstjórnun og bókhald** og eininguna **Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="fed08-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="fed08-106">Reiturinn **Númer eignar** er aðeins fylltur út í vinnslugerð verkbeiðni ef gerðin „Fjárfesting“ er valin sem verkgerð í verkbeiðniverki.</span><span class="sxs-lookup"><span data-stu-id="fed08-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Mynd 1](media/24-work-orders.png)

<span data-ttu-id="fed08-108">Eftirfarandi aðferð lýsir tengslum á milli eigna, verkbeiðna, verkbeiðniverka og fastafjármuna.</span><span class="sxs-lookup"><span data-stu-id="fed08-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="fed08-109">Þú býrð til eign sem þú tengir fastafjármunum eins og sýnt er á myndinni hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="fed08-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Mynd 2](media/25-work-orders.png)

2. <span data-ttu-id="fed08-111">Þegar þú setur upp verkbeiðnigerðir (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Verkbeiðnigerðir**), þú býrð til verkbeiðnigerð til að meðhöndla fjárfestingar.</span><span class="sxs-lookup"><span data-stu-id="fed08-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="fed08-112">Sjá einnig [Verkbeiðnigerðir](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="fed08-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Mynd 3](media/26-work-orders.png)

3. <span data-ttu-id="fed08-114">Þegar þú setur upp verkhópa verkbeiðna (tengillinn **Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verks** > **Verkefnahópur**), þú býrð til tengsl milli þeirrar verkbeiðnigerðar sem notuð er við fjárfestingar og verkefnahópsins sem stofnað var til vegna fjárfestinga í einingunni **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Uppsetning** > **Bókun** > **Verkefnahópar**).</span><span class="sxs-lookup"><span data-stu-id="fed08-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Mynd 4](media/27-work-orders.png)

4. <span data-ttu-id="fed08-116">Þegar þú býrð til verkbeiðni sem snýr að varanlegum eignum velur þú þá gerð verkbeiðni sem notuð er til að meðhöndla fjárfestingar, til dæmis „Fjárfesting“.</span><span class="sxs-lookup"><span data-stu-id="fed08-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="fed08-117">Þegar verkbeiðni er búin til, er tengd tegund verkbeiðni sýnd í **Öllum verkbeiðnum**.</span><span class="sxs-lookup"><span data-stu-id="fed08-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Mynd 5](media/28-work-orders.png)

6. <span data-ttu-id="fed08-119">Þegar verkbeiðni er stofnuð er verkefnið sem tengist verkbeiðninni stofnað í **Verkefnisstjórnun og bókhald** > **Öll verkefni**.</span><span class="sxs-lookup"><span data-stu-id="fed08-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="fed08-120">Þú getur séð upplýsingar sem tengjast verkefninu með því að smella á tengilinn **Verkkenni** á verkbeiðninni (í **Eignastjórnun** opnarðu verkbeiðnina í smáatriðum > flýtiflipann **Línuupplýsingar** > flipann **Almennt** > reitnum **Verkkenni**).</span><span class="sxs-lookup"><span data-stu-id="fed08-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Mynd 6](media/29-work-orders.png)

7. <span data-ttu-id="fed08-122">Í **Fastafjármunir**, þú getur séð yfirlit yfir verkefnin sem tengjast fastafjármunum (**Fastafjármunir** > **Fastafjármunir** > **Fastafjármunir** > smelltu á eignina í reitnum **Númer eignar** > skoða innihaldið í glugganum **Tengdar upplýsingar** > hlutanum **Tilheyrandi verkefni**).</span><span class="sxs-lookup"><span data-stu-id="fed08-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

