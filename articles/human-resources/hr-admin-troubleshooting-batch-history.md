---
title: Auka afköst með sjálfvirkum hreinsunarverkum
description: Þessi grein útskýrir hvernig á að leysa nokkur árangursmál hjá Microsoft Dynamics 365 Human Resources með því að hreinsa upp sögu runuvinnslunnar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 97f6e310d3a69c870fe8ef03bd7a10cc7ab652e5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112967"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="b4cbf-103">Fínstilltu árangur með sjálfvirkum hreinsunarverkum</span><span class="sxs-lookup"><span data-stu-id="b4cbf-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="b4cbf-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="b4cbf-104">**Issue**</span></span>

<span data-ttu-id="b4cbf-105">Microsoft Dynamics 365 Human Resources getur upplifað vandamál við afköst ef saga runuvinnslu verður of stór.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="b4cbf-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="b4cbf-106">**Cause**</span></span>

<span data-ttu-id="b4cbf-107">Runuvinnslur sem keyra oft geta leitt til ósjálfbærs vaxtar í sögu runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="b4cbf-108">Þetta getur valdið vandamálum í afköstum.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-108">This can cause performance issues.</span></span> 

<span data-ttu-id="b4cbf-109">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="b4cbf-109">**Resolution**</span></span>

<span data-ttu-id="b4cbf-110">Tímasettu sjálfvirkt verkefni til að hreinsa úr sögu runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="b4cbf-111">Við mælum með að setja verkið upp til að keyra vikulega en það gæti þurft að keyra hreinsunina oftar eða sjaldnar, allt eftir umhverfi.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="b4cbf-112">Eftirfarandi aðferð inniheldur ráðlagðar stillingar okkar, en þú getur breytt þeim í samræmi við þarfir.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="b4cbf-113">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b4cbf-114">Á slánni **Leita** slærðu inn **Hreinsun á sögu runuvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Leita að hreinsun runuvinnsluferlis](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="b4cbf-116">Í **Sögutakmörkun (í dögum)** skaltu færa inn **30**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-116">In **History limit (days)**, enter **30**.</span></span>

   ![Stilltu sögutakmörkun í 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="b4cbf-118">Veldu **Keyra í bakgrunni** og veldu síðan **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Stilla endurtekningu](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="b4cbf-120">Undir **Skilgreina endurtekningu** stillirðu **Upphafsdag** og **Upphafstíma** til að eiga sér stað utan vinnutíma eða um helgar og velur síðan **ENGIN LOKADAGS.**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Skilgreindu upphafsdag og -tíma endurtekningar](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="b4cbf-122">Undir **ENDURTEKNINGARMYNSTUR** velurðu **Dagar** og stillir **ENDURTAKA EFTIR TILTEKIÐ BIL** á **7**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Stilltu hreinsun til að endurtaka vikulega](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="b4cbf-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-124">Select **OK**.</span></span>

8. <span data-ttu-id="b4cbf-125">Breyta öðrum breytum undir **Keyra í bakgrunni** eftir þörfum og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4cbf-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

