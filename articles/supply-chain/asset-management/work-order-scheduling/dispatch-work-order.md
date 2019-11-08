---
title: Senda verkbeiðni
description: Þetta efni útskýrir hvernig á að senda verkbeiðni í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 026b34934d6527416a4632d8e1aee76a8836dcb0
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652012"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="e4f8e-103">Senda verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="e4f8e-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e4f8e-104">Þú getur tímasett eina verkbeiðni eða verkbeiðnivinnslur fyrir einn starfskraft með því að nota aðgerðina **Senda**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="e4f8e-105">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e4f8e-106">Verkbeiðnin er valin af listanum.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="e4f8e-107">Á flipanum **Almennt** er smellt á **Senda**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="e4f8e-108">Í glugganum **Áætla verkbeiðni** velurðu starfskraftinn í reitnum **Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="e4f8e-109">Í reitinn **Áætlunartíma** er hægt að setja inn áætlaða vinnutíma ef áætlaður vinnutími er frábrugðinn spátímanum.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="e4f8e-110">Í reitnum **Áætlað upphaf** er hægt að breyta upphafsdegi og -tíma, ef þess er krafist.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="e4f8e-111">Ef áætlunarferlið á að fylgjast með takmörkunum afkastagetu varðandi tilföng sem eru þegar áætluð á aðrar vinnslur skal tryggja að skiptihnapparnir **Eign**, **Verkfæri** og **Starfskraftur** séu stilltir á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="e4f8e-112">Ef þú vilt sjá ítarlegar upplýsingar um áætlunarferlið skaltu velja **Já** á skiptihnappnum **Oflengd**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="e4f8e-113">Þetta þýðir að nákvæmar upplýsingar um reiknuð stig á verkbeiðninni eru sýndar í athugasemdakladda.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="e4f8e-114">Veldu **Já** á skipthnappnum **Hunsa áætlun** til að hunsa lokaða daga í dagatalinu (á við um eignir, starfskrafta og verkfæri).</span><span class="sxs-lookup"><span data-stu-id="e4f8e-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="e4f8e-115">Veldu **Já** á skiptihnappnum **Hunsa áætlaða framkvæmd** til að hunsa takmarkanir sem kunna að hafa verið valdar í verkbeiðni varðandi áætlun.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="e4f8e-116">Upplýsingar um uppsetningu á áætlaðri framkvæmd er að finna í kaflanum [Áætluð framkvæmd](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="e4f8e-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="e4f8e-117">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-117">Click **OK**.</span></span> <span data-ttu-id="e4f8e-118">Líftímastaða verkbeiðni er sjálfkrafa uppfærð í líftímastöðuna **Áætlað** sem er tilgreind í **Eignastýringu** > **Uppsetningu** > **Verkbeiðnum** > **Líftímalíkön**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="e4f8e-119">Myndin hér að neðan sýnir dæmi um sendingarval í glugganum **Áætla verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Mynd 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="e4f8e-121">Ef þú vilt eyða áætlun í vinnupöntun velurðu verkbeiðnina í **Allar verkbeiðnir** og smellir síðan á **Eyða áætlun** á flipanum **Almennt**. Mundu að uppfæra handvirkt líftímastöðu verkbeiðni ef þú eyðir áætluninni.</span><span class="sxs-lookup"><span data-stu-id="e4f8e-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

