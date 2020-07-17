---
title: Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum sem tengjast afköstum með Microsoft Dynamics 365 Human Resources með því að tímasetja langtímarunuvinnslu eftir vinnutíma.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500506"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="c62b1-103">Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="c62b1-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="c62b1-104">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="c62b1-104">Issue</span></span>

<span data-ttu-id="c62b1-105">Vandamál með afköst geta komið upp hjá Microsoft Dynamics 365 Human Resources ef langtímarunuvinnsla er keyrð á vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="c62b1-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="c62b1-106">Upplausn</span><span class="sxs-lookup"><span data-stu-id="c62b1-106">Resolution</span></span>

<span data-ttu-id="c62b1-107">Tímasetjið eftirfarandi runuvinnslur utan vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="c62b1-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="c62b1-108">Einnig er mælt með því að endurskoða tíðni runuvinnsla sem keyra oft.</span><span class="sxs-lookup"><span data-stu-id="c62b1-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="c62b1-109">Dragið úr endurtekningum á runuvinnslunni ef mögulegt.</span><span class="sxs-lookup"><span data-stu-id="c62b1-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="c62b1-110">Í mörgum tilfellum er sjálfgefin tíðni nægjanleg.</span><span class="sxs-lookup"><span data-stu-id="c62b1-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="c62b1-111">Eftirfarandi runuvinnslur ættu að keyra að næturlagi eða eftir vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="c62b1-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="c62b1-112">Gætið þess að athuga tímabeltið fyrir þessar endurteknar runuvinnslur.</span><span class="sxs-lookup"><span data-stu-id="c62b1-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="c62b1-113">Sumar runuvinnslur nota hugsanlega PST staðaltíma.</span><span class="sxs-lookup"><span data-stu-id="c62b1-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="c62b1-114">Runuvinnsla</span><span class="sxs-lookup"><span data-stu-id="c62b1-114">Batch job</span></span> | <span data-ttu-id="c62b1-115">Sjálfgefin endurtekning</span><span class="sxs-lookup"><span data-stu-id="c62b1-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="c62b1-116">Hreinsun runuvinnsluferils</span><span class="sxs-lookup"><span data-stu-id="c62b1-116">Batch job history cleanup</span></span> | <span data-ttu-id="c62b1-117">1 skipti á mánuði</span><span class="sxs-lookup"><span data-stu-id="c62b1-117">1 time per month</span></span> |
| <span data-ttu-id="c62b1-118">Flytja út hreinsun sviðsetningar</span><span class="sxs-lookup"><span data-stu-id="c62b1-118">Export staging cleanup</span></span> | <span data-ttu-id="c62b1-119">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="c62b1-119">1 time per day</span></span> |
| <span data-ttu-id="c62b1-120">Samstilling ósvaraðra beiðna Common Data Service-samþættingar</span><span class="sxs-lookup"><span data-stu-id="c62b1-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="c62b1-121">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="c62b1-121">1 time per day</span></span> |
| <span data-ttu-id="c62b1-122">Kerfisvinnsla gagnasamþjöppunar sem þarf að keyra reglulega utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="c62b1-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="c62b1-123">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="c62b1-123">1 time per day</span></span> |
| <span data-ttu-id="c62b1-124">Kerfisvinnsla endurbyggingar gagnagrunnsvísa sem þarf að keyra reglulega utan vinnutíma</span><span class="sxs-lookup"><span data-stu-id="c62b1-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="c62b1-125">1 skipti á dag</span><span class="sxs-lookup"><span data-stu-id="c62b1-125">1 time per day</span></span> |

1. <span data-ttu-id="c62b1-126">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c62b1-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c62b1-127">Í stikunni **Leita** skal leita að einni af ofangreindum runuvinnslum.</span><span class="sxs-lookup"><span data-stu-id="c62b1-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="c62b1-128">Veljið **Keyra í bakgrunni** og veljið síðan **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="c62b1-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Stilla endurtekningu](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="c62b1-130">Undir **Skilgreina endurtekningu** skal stilla **Upphafsdagsetningu** og **Upphafstíma** þannig að endurtekning gerist utan vinnutíma eða um helgar.</span><span class="sxs-lookup"><span data-stu-id="c62b1-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="c62b1-131">Veljið **Engin lokadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="c62b1-131">Select **No end date**.</span></span> 

   ![Skilgreindu upphafsdag og -tíma endurtekningar](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="c62b1-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c62b1-133">Select **OK**.</span></span>

6. <span data-ttu-id="c62b1-134">Ef þörf krefur skal breyta öðrum færibreytum undir **Keyra í bakgrunni** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c62b1-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c62b1-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c62b1-135">Additional resources</span></span>

[<span data-ttu-id="c62b1-136">Auka afköst með sjálfvirkum hreinsunarverkum</span><span class="sxs-lookup"><span data-stu-id="c62b1-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
