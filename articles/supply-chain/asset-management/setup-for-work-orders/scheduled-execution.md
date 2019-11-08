---
title: Áætluð keyrsla
description: Þetta efni útskýrir tímasetta framkvæmd í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89e13179e17b7cf075d631bc65d82da5f24da624
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569847"
---
# <a name="scheduled-execution"></a><span data-ttu-id="828b0-103">Áætluð keyrsla</span><span class="sxs-lookup"><span data-stu-id="828b0-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="828b0-104">Þú getur notað þjónustustig fyrir verkbeiðni til að setja upp áætlaða framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="828b0-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="828b0-105">(Sjá nánari upplýsingar um þjónustustig í verkbeiðni [Þjónustustig og lýsing](service-level-and-description.md) .) Fyrirhuguð framkvæmd veitir sveigjanleika í verkáætlun fyrir viðhaldsstarfsmenn, vegna þess að þú getur sett upp ítarlegri eða minna nákvæmar kröfur um það bil sem ljúka skal verkbeiðni á.</span><span class="sxs-lookup"><span data-stu-id="828b0-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="828b0-106">Sem dæmi má nefna að viðhaldsstarfsmaður sem lýkur verki hraðar en gert var ráð fyrir í framleiðslustöð gæti farið í annað starf í nágrenninu sem áætlað var fyrir núverandi viku en ekki endilega fyrir núverandi dag.</span><span class="sxs-lookup"><span data-stu-id="828b0-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="828b0-107">Þessi aðferð gerir kleift að hámarka skipulagningu starfsmanna og verklok.</span><span class="sxs-lookup"><span data-stu-id="828b0-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="828b0-108">Tímasett framkvæmdaruppsetning, sem tengist verkbeiðnum, getur verið almenn eða sértæk.</span><span class="sxs-lookup"><span data-stu-id="828b0-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="828b0-109">Þú getur sett upp almennar línur sem eru ekki takmarkaðar við sérstakar gerðir verkbeiðni, eignagerðir og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="828b0-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="828b0-110">Að öðrum kosti er hægt að búa til áætlaðar framkvæmdalínur sem eiga við um tiltekna gerð verkbeiðni, eignagerð, gerð viðhaldsverks og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="828b0-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="828b0-111">Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Áætluð framkvæmd**.</span><span class="sxs-lookup"><span data-stu-id="828b0-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="828b0-112">Veldu **Nýtt** til að stofna áætlaða framkvæmdalínu.</span><span class="sxs-lookup"><span data-stu-id="828b0-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="828b0-113">Í reitunum **Virk staðsetning**, **Gerð verkbeiðni**, **Gerð eigna**, **Framleiðandi**, **Tegund**, **Tegundaflokkur viðhaldsverka**, **Gerð viðhaldsverks**, **Tegundaafbrigði af viðhaldsverka** og **Viðskipti** velurðu gildi eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="828b0-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="828b0-114">Í reitnum **Þjónustustig** velurðu þjónustustig verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="828b0-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="828b0-115">Ef þú skilur þennan reit eftir auðan, þá gerirðu almenna gerð áætlaðrar framkvæmdalínu.</span><span class="sxs-lookup"><span data-stu-id="828b0-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="828b0-116">Fyrir dæmi um almenna línu, sjá fyrstu skrána á myndinni sem hér fylgir.</span><span class="sxs-lookup"><span data-stu-id="828b0-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="828b0-117">Sú lína virkjar allar verkbeiðnir sem hafa ekkert þjónustustig verkbeiðni sem á að tímasetja fyrir tiltekinn dag og tíma.</span><span class="sxs-lookup"><span data-stu-id="828b0-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="828b0-118">Í reitnum **Áætluð framkvæmd** velurðu tímamillibilið.</span><span class="sxs-lookup"><span data-stu-id="828b0-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="828b0-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="828b0-119">Select **Save**.</span></span>

![Áætluð keyrsla](media/20-setup-for-work-orders.png)
