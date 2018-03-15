--- 
title: " Bóka netsölu og -greiðslur"
description: "Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu."
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2feaf580c7ae1fc53f9257f117576c99764c6ea0
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="de284-103"> Bóka netsölu og -greiðslur</span><span class="sxs-lookup"><span data-stu-id="de284-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="de284-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.</span><span class="sxs-lookup"><span data-stu-id="de284-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="de284-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="de284-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="de284-106">Fara á Öll vinnusvæði > fjárhagur smásöluverslana.</span><span class="sxs-lookup"><span data-stu-id="de284-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="de284-107">Smellt er á Samstilla pantanir</span><span class="sxs-lookup"><span data-stu-id="de284-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="de284-108">Í svæðinu stigveldi Fyrirtækis, veljið 'Smásöluverslanir eftir Svæði'.</span><span class="sxs-lookup"><span data-stu-id="de284-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="de284-109">Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="de284-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="de284-110">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="de284-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="de284-111">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="de284-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="de284-112">Kanna eða afmerkja gátreit runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="de284-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="de284-113">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="de284-113">Click Recurrence.</span></span>
7. <span data-ttu-id="de284-114">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="de284-114">Select the No end date option.</span></span>
8. <span data-ttu-id="de284-115">Í reitinn Fjöldi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="de284-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="de284-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="de284-116">Click OK.</span></span>
10. <span data-ttu-id="de284-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="de284-117">Click OK.</span></span>


