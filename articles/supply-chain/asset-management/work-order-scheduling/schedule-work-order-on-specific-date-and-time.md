---
title: Áætla verkbeiðni á ákveðnum degi og tíma
description: Þetta efni útskýrir hvernig á að tímasetja verkbeiðni á tiltekinni dagsetningu og tíma í eignastjórnun.
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
ms.openlocfilehash: 0f818c4c3b669cc94e37cba1e3571c57b5c0dd1b
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887366"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="3bdca-103">Áætla verkbeiðni á ákveðnum degi og tíma</span><span class="sxs-lookup"><span data-stu-id="3bdca-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3bdca-104">Ef þarf að skipuleggja verkbeiðni á tilteknum degi *og* tíma er hægt að hnekkja stöðluðu skipulagningarferli í Eignastjórnun og búa til tiltekna áætlun fyrir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="3bdca-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="3bdca-105">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="3bdca-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3bdca-106">Í verkbeiðnilistanum skaltu smella á verkbeiðnikennið í dálkinum **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="3bdca-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="3bdca-107">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="3bdca-107">Click **Edit**.</span></span>

4. <span data-ttu-id="3bdca-108">Á flýtiflipanum **Haus verkbeiðni** skaltu setja upphafs- og lokadagsetningar og tíma í reitina **Vænt upphaf** og **Vænt lok**.</span><span class="sxs-lookup"><span data-stu-id="3bdca-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

![Mynd 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="3bdca-110">Á flipanum **Almennt** skaltu smella á **Tímasetja** til að nota staðlað tímasetningarferli eða smella á **Senda** ef þú vilt skipuleggja verkbeiðni til ákveðins starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="3bdca-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to schedule the work order to a specific worker.</span></span>

6. <span data-ttu-id="3bdca-111">Til að hnekkja fyrirliggjandi frátekna afkastagetu til að tryggja að verkbeiðni sé áætluð á væntu tímabili skaltu gera valið eins og sýnt er á myndinni hér að neðan í glugganum **Skipuleggja verkbeiðni** > kaflanum **Takmörkuð geta**.</span><span class="sxs-lookup"><span data-stu-id="3bdca-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="3bdca-112">Þetta þýðir að tímasetningarferlið mun hunsa núverandi frátekna afkastagetu þar sem verkbeiðnin verður að hefjast á áætluðum upphafstíma.</span><span class="sxs-lookup"><span data-stu-id="3bdca-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

![Mynd 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="3bdca-114">Smelltu á **Í lagi** til að hefja röðunina.</span><span class="sxs-lookup"><span data-stu-id="3bdca-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="3bdca-115">Ef tímasetningarferlið hefur í för með sér tvöfaldar bókanir sérðu skilaboð á skjánum og þú getur breytt tengdum verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="3bdca-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="3bdca-116">Til þess að tímasetja viðhaldsstarfsmann fyrir verkbeiðnina verður sá viðhaldsstarfsmaður að vera tiltækur á væntum upphafsdegi og -tíma.</span><span class="sxs-lookup"><span data-stu-id="3bdca-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="3bdca-117">Framboð starfskrafta er sett upp í [starfsmannadagatal](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="3bdca-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

