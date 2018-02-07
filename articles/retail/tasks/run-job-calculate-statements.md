--- 
title: " Skilgreina og keyra vinnslu til að reikna yfirlit"
description: "Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að stofna og reikna uppgjör fyrir valda verslun eða verslunarflokk."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc936cdba771d322676565c2615ad75649cc50b
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="d9de4-103"> Skilgreina og keyra vinnslu til að reikna yfirlit</span><span class="sxs-lookup"><span data-stu-id="d9de4-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d9de4-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að stofna og reikna uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="d9de4-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="d9de4-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="d9de4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d9de4-106">Fara á Öll vinnusvæði > fjárhagur smásöluverslana.</span><span class="sxs-lookup"><span data-stu-id="d9de4-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="d9de4-107">Smellt er á Reikna út uppgjör</span><span class="sxs-lookup"><span data-stu-id="d9de4-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="d9de4-108">Annað hvort velja ákveðna verslun, eða hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="d9de4-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d9de4-109">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="d9de4-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="d9de4-110">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="d9de4-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="d9de4-111">Veljið undir runuvinnslu, 'Já'.</span><span class="sxs-lookup"><span data-stu-id="d9de4-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="d9de4-112">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="d9de4-112">Click Recurrence.</span></span>
6. <span data-ttu-id="d9de4-113">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="d9de4-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="d9de4-114">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="d9de4-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="d9de4-115">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="d9de4-115">Select the No end date option.</span></span>
9. <span data-ttu-id="d9de4-116">Færa inn "Dagar" í svæðinu PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="d9de4-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="d9de4-117">Í reitinn Á, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="d9de4-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="d9de4-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d9de4-118">Click OK.</span></span>
12. <span data-ttu-id="d9de4-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d9de4-119">Click OK.</span></span>


