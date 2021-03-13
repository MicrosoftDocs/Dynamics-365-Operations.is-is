---
title: Viðhaldsáætlun
description: Þetta efni skýrir viðhaldsskema í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d235a3797b1acee9c92c3d81e8b4a20e1f7c5c75
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017956"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="8e3c7-103">Viðhaldsáætlun</span><span class="sxs-lookup"><span data-stu-id="8e3c7-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8e3c7-104">Viðhaldsskemað inniheldur lista yfir allar áætlaðar fyrirbyggjandi viðhaldsáætlanir, viðhaldsbeiðnir og viðhaldslotur sem gera skal. Sumum dagskrárlínum kann að hafa verið breytt í viðhaldsbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="8e3c7-105">Fjögur sýn á viðhaldsskema er aðeins mismunandi eftir því hvaða viðhaldsskemalínur þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="8e3c7-106">Valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="8e3c7-106">Menu item</span></span>                  | <span data-ttu-id="8e3c7-107">Efnisyfirlit</span><span class="sxs-lookup"><span data-stu-id="8e3c7-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3c7-108">Ítarleg viðhaldsáætlun</span><span class="sxs-lookup"><span data-stu-id="8e3c7-108">All maintenance schedule</span></span>       | <span data-ttu-id="8e3c7-109">Allar viðhaldsskemalínur eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="8e3c7-110">Eignaáætlunin mín</span><span class="sxs-lookup"><span data-stu-id="8e3c7-110">My asset schedule</span></span>        | <span data-ttu-id="8e3c7-111">Allar viðhaldsskemalínur sem innihalda eignir settar upp á virkum stöðum sem þú tengist sem starfsmaður (sett upp í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md)) eru sýndar á þessum lista.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="8e3c7-112">Opna áætlunarlínur viðhalds</span><span class="sxs-lookup"><span data-stu-id="8e3c7-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="8e3c7-113">Línur um viðhaldsskema með stöðunni „Stofnað“ - sem þýðir að þeim hefur enn ekki verið breytt í verkbeiðni eða þeim hent - eru sýndar á þessum lista.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="8e3c7-114">Opna viðhaldsáætlunarhópa</span><span class="sxs-lookup"><span data-stu-id="8e3c7-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="8e3c7-115">Línur fyrir viðhaldsskema sem tengjast verkpöntunarsafni eru sýndar á þessum lista.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="8e3c7-116">Ef viðhaldsskemalína er innifalin í nokkrum verkbeiðnisöfnum (sjá [Verkbeiðnisöfn](../work-orders/work-order-pools.md)) er sýnd ein skrá fyrir hvert safn í **Opna viðhaldsskemasöfn**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="8e3c7-117">Þetta er gert til að hámarka síunarvalkosti í verkbeiðnisöfnum.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="8e3c7-118">Til að opna viðhaldsskema:</span><span class="sxs-lookup"><span data-stu-id="8e3c7-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="8e3c7-119">Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Viðhaldsskema** > **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur** eða **Opna söfn viðhaldsáætlana**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="8e3c7-120">Til að uppfæra viðhaldsskema skaltu smella á **Viðhaldsáætlun** eða **Viðhaldslotur**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="8e3c7-121">Þú getur breytt viðhaldsskemalínu með því að velja hana og smella á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="8e3c7-122">Til dæmis geturðu auðveldlega uppfært þjónustustigið eða starfsmanninn sem ber ábyrgð á vinnslunni.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="8e3c7-123">Þú getur aðeins breytt viðhaldsskemalínum sem hafa ekki enn verið tengdir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="8e3c7-124">Þú getur eytt viðhaldsskemalínu með því að velja hana á listasíðunni og smella á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="8e3c7-125">Þú getur fleygt viðhaldsskemalínu með því að velja hana á listasíðunni og smella á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="8e3c7-126">Þessi aðgerð er gagnleg ef til dæmis eign er með 2.000 km viðhaldsáætlun og 10.000 km viðhaldsáætlun.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="8e3c7-127">Þá gætirðu viljað henda línunni sem búin var til úr viðhaldsáætluninni um 2.000 km þegar hún fellur saman við 10.000 km, 20.000 km, 30.000 km og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="8e3c7-128">Ef þú fargar viðhaldsskemalínu sem tengist viðhaldsáætlun birtist sú lína aldrei aftur þegar sú viðhaldsáætlun er áætluð.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="8e3c7-129">Þú getur valið fjölda viðhaldsskemalína í **Öll viðhaldsskemu** og smellt á **Verkbeiðnisafn**, ef þú vilt að allar valdar línur séu með í sama verkbeiðnisafni.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="8e3c7-130">Þú getur valið fjölda viðhaldsskemalína í **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur** eða **Opna viðhaldskemasöfn** og smellt á **Stilla áætlun** ef þú vilt gera sömu leiðréttingar á nokkrum línum.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="8e3c7-131">Þú getur breytt áætluðum upphafs- og lokadögum, þjónustustigi og ábyrgum starfsmannahópi eða ábyrgum viðhaldsstarfsmanni tengdum völdum viðhaldsskemalínum.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="8e3c7-132">Þegar lína fyrir viðhaldsskema hefur verið tengd verkbeiðni verður auðkenni verkbeiðni birt í reitnum **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="8e3c7-133">Í upplýsingaglugganum **Allar eignir** > flýtiflipanum **Viðhaldsáætlanir eigna** er hægt að velja viðhaldsáætlanir fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="8e3c7-134">Seinna, ef þú eyðir viðhaldsáætlunarlínu eða viðhaldslotu sem tengist eign í **Allar eignir**, eyðirðu einnig sjálfkrafa öllum viðhaldsskemalínum með stöðunni „Stofnað“ sem hafa verið stofnaðar út frá þeirri viðhaldsáætlun eða viðhaldsumferð.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="8e3c7-135">Sjá einnig [Stofna eign](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="8e3c7-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="8e3c7-136">Myndin hér að neðan sýnir listasíðuna **Öll viðhaldsskemu**.</span><span class="sxs-lookup"><span data-stu-id="8e3c7-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Mynd 1](media/16-preventive-maintenance.png)

