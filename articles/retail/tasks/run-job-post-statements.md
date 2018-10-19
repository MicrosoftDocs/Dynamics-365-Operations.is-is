--- 
title: "Skilgreina og keyra vinnsluna til að bóka uppgjör"
description: "Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="709e3-103">Skilgreina og keyra vinnsluna til að bóka uppgjör</span><span class="sxs-lookup"><span data-stu-id="709e3-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="709e3-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="709e3-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="709e3-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="709e3-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="709e3-106">Fara í Öll vinnusvæði > ..</span><span class="sxs-lookup"><span data-stu-id="709e3-106">Go to All workspaces > ..</span></span> <span data-ttu-id="709e3-107">> Fjárhagur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="709e3-107">> Retail store financials.</span></span>
2. <span data-ttu-id="709e3-108">Smellt er á Bóka uppgjör.</span><span class="sxs-lookup"><span data-stu-id="709e3-108">Click Post statements.</span></span>
    * <span data-ttu-id="709e3-109">Velja stigveldi fyrirtækis og síðan í fyrirtækishnútur, í trénu velja einstaka verslun eða hnút.</span><span class="sxs-lookup"><span data-stu-id="709e3-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="709e3-110">Annað hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="709e3-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="709e3-111">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="709e3-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="709e3-112">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="709e3-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="709e3-113">Kanna eða afmerkja gátreit runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="709e3-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="709e3-114">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="709e3-114">Click Recurrence.</span></span>
6. <span data-ttu-id="709e3-115">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="709e3-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="709e3-116">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="709e3-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="709e3-117">Velja hvort á að ljúka endurtekningu eftir tiltekinn fjölda keyrslur á tiltekinni dagsetningu eða aldrei.</span><span class="sxs-lookup"><span data-stu-id="709e3-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="709e3-118">Velja síðan ýmsum valkostum til að skilgreina hversu oft eigi að keyra vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="709e3-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="709e3-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="709e3-119">Click OK.</span></span>
9. <span data-ttu-id="709e3-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="709e3-120">Click OK.</span></span>


