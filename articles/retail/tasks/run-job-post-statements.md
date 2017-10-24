--- 
title: " Skilgreina og keyra vinnslu til að bóka yfirlit"
description: "Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="4d077-103"> Skilgreina og keyra vinnslu til að bóka yfirlit</span><span class="sxs-lookup"><span data-stu-id="4d077-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4d077-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="4d077-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="4d077-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="4d077-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4d077-106">Fara í Öll vinnusvæði > ..</span><span class="sxs-lookup"><span data-stu-id="4d077-106">Go to All workspaces > ..</span></span> <span data-ttu-id="4d077-107">> Fjárhagur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="4d077-107">> Retail store financials.</span></span>
2. <span data-ttu-id="4d077-108">Smellt er á Bóka uppgjör.</span><span class="sxs-lookup"><span data-stu-id="4d077-108">Click Post statements.</span></span>
    * <span data-ttu-id="4d077-109">Velja stigveldi fyrirtækis og síðan í fyrirtækishnútur, í trénu velja einstaka verslun eða hnút.</span><span class="sxs-lookup"><span data-stu-id="4d077-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="4d077-110">Annað hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="4d077-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4d077-111">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="4d077-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="4d077-112">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="4d077-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="4d077-113">Kanna eða afmerkja gátreit runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="4d077-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="4d077-114">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="4d077-114">Click Recurrence.</span></span>
6. <span data-ttu-id="4d077-115">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="4d077-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="4d077-116">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="4d077-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="4d077-117">Velja hvort á að ljúka endurtekningu eftir tiltekinn fjölda keyrslur á tiltekinni dagsetningu eða aldrei.</span><span class="sxs-lookup"><span data-stu-id="4d077-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="4d077-118">Velja síðan ýmsum valkostum til að skilgreina hversu oft eigi að keyra vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="4d077-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="4d077-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4d077-119">Click OK.</span></span>
9. <span data-ttu-id="4d077-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4d077-120">Click OK.</span></span>


