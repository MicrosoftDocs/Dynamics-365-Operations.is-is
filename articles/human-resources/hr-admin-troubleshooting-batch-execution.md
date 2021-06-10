---
title: Endurstilla fastar runuvinnslur
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum með runuvinnslur sem ekki er unnið úr.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053516"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="1b5d7-103">Endurstilla fastar runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="1b5d7-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="1b5d7-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="1b5d7-104">Issue</span></span>

<span data-ttu-id="1b5d7-105">Microsoft Dynamics 365 Human Resources getur fundið vandamál við runuvinnslur sem er fastar í **Keyrir** eða **Hættir við** stöðu og lýkur ekki.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="1b5d7-106">Upplausn</span><span class="sxs-lookup"><span data-stu-id="1b5d7-106">Resolution</span></span>

<span data-ttu-id="1b5d7-107">Þegar runuvinnsla er föst í stöðunni **Í keyrslu** eða **Hættir við** er hægt að endurstilla stöðuna með því að þvinga á afturköllun vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="1b5d7-108">Eftir að hætt hefur verið við það er hægt að endurstilla runuvinnsluna með því að setja hana í stöðuna **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="1b5d7-109">Hún er svo aftur keyrð í næstu runuvinnslu á dagskrá.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="1b5d7-110">Á **Kerfisstjórnun** vinnusvæðinu skal velja **Tenglar** síðuna og svo **Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="1b5d7-111">Á **Runuvinnsla** listasíðunni skal velja verkið sem þarf að endurstilla.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="1b5d7-112">Á aðgerðaborðanum skal velja **Þvinga afturköllun** og staðfesta aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1b5d7-113">Aðgerðin **Þvinga afturköllun** er aðeins tiltæk þegar valin runuvinnsla er með stöðuna **Keyrir** eða **Hættir við** og engin runuvinnsla eða afturköllunarferli er í keyrslu fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="1b5d7-114">Á aðgerðaborðanum skal velja **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="1b5d7-115">Á síðunni **Velja nýja stöðu** skal velja **Í bið** og svo velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b5d7-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Velja nýja stöðu á runuvinnslu](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="1b5d7-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1b5d7-117">See also</span></span>

[<span data-ttu-id="1b5d7-118">Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="1b5d7-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="1b5d7-119">Auka afköst með sjálfvirkum hreinsunarverkum</span><span class="sxs-lookup"><span data-stu-id="1b5d7-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
