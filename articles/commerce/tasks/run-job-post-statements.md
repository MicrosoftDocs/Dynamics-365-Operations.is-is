---
title: Skilgreina og keyra vinnsluna til að bóka uppgjör
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09a47e268e271cf86e63ceff913435842f017bb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022885"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="47037-103">Skilgreina og keyra vinnsluna til að bóka uppgjör</span><span class="sxs-lookup"><span data-stu-id="47037-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="47037-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að bóka uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="47037-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="47037-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="47037-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="47037-106">Fara í Öll vinnusvæði > ..</span><span class="sxs-lookup"><span data-stu-id="47037-106">Go to All workspaces > ..</span></span> <span data-ttu-id="47037-107">> Fjármál verslunar.</span><span class="sxs-lookup"><span data-stu-id="47037-107">> Store financials.</span></span>
2. <span data-ttu-id="47037-108">Smelltu á Bóka uppgjör í runu.</span><span class="sxs-lookup"><span data-stu-id="47037-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="47037-109">Velja stigveldi fyrirtækis og síðan í fyrirtækishnútur, í trénu velja einstaka verslun eða hnút.</span><span class="sxs-lookup"><span data-stu-id="47037-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="47037-110">Annað hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="47037-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="47037-111">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="47037-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="47037-112">Smelltu á flipann Keyra í bakgrunni. ![Keyra í bakgrunni](../dev-itpro/media/runbackground.png "Keyra í bakgrunni")</span><span class="sxs-lookup"><span data-stu-id="47037-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="47037-113">Kanna eða afmerkja gátreit runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="47037-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="47037-114">![Runuvinnsla](../dev-itpro/media/batchprocessing.png "Runuvinnsla og endurtekning")</span><span class="sxs-lookup"><span data-stu-id="47037-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="47037-115">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="47037-115">Click Recurrence.</span></span>
6. <span data-ttu-id="47037-116">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="47037-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="47037-117">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="47037-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="47037-118">Velja hvort á að ljúka endurtekningu eftir tiltekinn fjölda keyrslur á tiltekinni dagsetningu eða aldrei.</span><span class="sxs-lookup"><span data-stu-id="47037-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="47037-119">Velja síðan ýmsum valkostum til að skilgreina hversu oft eigi að keyra vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="47037-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="47037-120">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="47037-120">Click OK.</span></span>
9. <span data-ttu-id="47037-121">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="47037-121">Click OK.</span></span>

