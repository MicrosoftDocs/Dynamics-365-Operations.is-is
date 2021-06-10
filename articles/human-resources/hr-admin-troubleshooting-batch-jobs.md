---
title: Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum sem tengjast afköstum með Microsoft Dynamics 365 Human Resources með því að tímasetja langtímarunuvinnslu eftir vinnutíma.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053468"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="48baf-103">Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="48baf-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="48baf-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="48baf-104">Issue</span></span>

<span data-ttu-id="48baf-105">Vandamál með afköst geta komið upp hjá Microsoft Dynamics 365 Human Resources ef langtímarunuvinnsla er keyrð á vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="48baf-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="48baf-106">Upplausn</span><span class="sxs-lookup"><span data-stu-id="48baf-106">Resolution</span></span>

<span data-ttu-id="48baf-107">Tímasetjið eftirfarandi runuvinnslur utan vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="48baf-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="48baf-108">Einnig er mælt með því að endurskoða tíðni runuvinnsla sem keyra oft.</span><span class="sxs-lookup"><span data-stu-id="48baf-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="48baf-109">Dragið úr endurtekningum á runuvinnslunni ef mögulegt.</span><span class="sxs-lookup"><span data-stu-id="48baf-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="48baf-110">Í mörgum tilfellum er sjálfgefin tíðni nægjanleg.</span><span class="sxs-lookup"><span data-stu-id="48baf-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="48baf-111">Eftirfarandi runuvinnslur ættu að keyra að næturlagi eða eftir vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="48baf-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="48baf-112">Gætið þess að athuga tímabeltið fyrir þessar endurteknar runuvinnslur.</span><span class="sxs-lookup"><span data-stu-id="48baf-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="48baf-113">Sumar runuvinnslur nota hugsanlega PST staðaltíma.</span><span class="sxs-lookup"><span data-stu-id="48baf-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="48baf-114">Runuvinnsla</span><span class="sxs-lookup"><span data-stu-id="48baf-114">Batch job</span></span> | <span data-ttu-id="48baf-115">Sjálfgefin endurtekning</span><span class="sxs-lookup"><span data-stu-id="48baf-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="48baf-116">Hreinsun runuvinnsluferils</span><span class="sxs-lookup"><span data-stu-id="48baf-116">Batch job history cleanup</span></span> | <span data-ttu-id="48baf-117">1 skipti á mánuði</span><span class="sxs-lookup"><span data-stu-id="48baf-117">1 time per month</span></span> |
| <span data-ttu-id="48baf-118">Flytja út hreinsun sviðsetningar</span><span class="sxs-lookup"><span data-stu-id="48baf-118">Export staging cleanup</span></span> | <span data-ttu-id="48baf-119">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="48baf-119">1 time per day</span></span> |
| <span data-ttu-id="48baf-120">Samstilling ósvaraðra beiðna Common Data Service-samþættingar</span><span class="sxs-lookup"><span data-stu-id="48baf-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="48baf-121">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="48baf-121">1 time per day</span></span> |
| <span data-ttu-id="48baf-122">Kerfisvinnsla gagnasamþjöppunar sem þarf að keyra reglulega utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="48baf-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="48baf-123">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="48baf-123">1 time per day</span></span> |
| <span data-ttu-id="48baf-124">Kerfisvinnsla endurbyggingar gagnagrunnsvísa sem þarf að keyra reglulega utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="48baf-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="48baf-125">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="48baf-125">1 time per day</span></span> |

1. <span data-ttu-id="48baf-126">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="48baf-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="48baf-127">Í stikunni **Leita** skal leita að einni af ofangreindum runuvinnslum.</span><span class="sxs-lookup"><span data-stu-id="48baf-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="48baf-128">Veljið **Keyra í bakgrunni** og veljið síðan **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="48baf-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Stilla endurtekningu](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="48baf-130">Undir **Skilgreina endurtekningu** skal stilla **Upphafsdagsetningu** og **Upphafstíma** þannig að endurtekning gerist utan vinnutíma eða um helgar.</span><span class="sxs-lookup"><span data-stu-id="48baf-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="48baf-131">Veljið **Engin lokadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="48baf-131">Select **No end date**.</span></span> 

   ![Skilgreindu upphafsdag og -tíma endurtekningar](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="48baf-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="48baf-133">Select **OK**.</span></span>

6. <span data-ttu-id="48baf-134">Ef þörf krefur skal breyta öðrum færibreytum undir **Keyra í bakgrunni** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="48baf-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48baf-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="48baf-135">Additional resources</span></span>

[<span data-ttu-id="48baf-136">Auka afköst með sjálfvirkum hreinsunarverkum</span><span class="sxs-lookup"><span data-stu-id="48baf-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]