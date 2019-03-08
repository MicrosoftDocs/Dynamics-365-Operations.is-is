---
title: Skilgreina og keyra vinnsluna til að reikna uppgjör
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að stofna og reikna uppgjör fyrir valda verslun eða verslunarflokk.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "365179"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="55823-103">Skilgreina og keyra vinnsluna til að reikna uppgjör</span><span class="sxs-lookup"><span data-stu-id="55823-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="55823-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að stofna og reikna uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="55823-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="55823-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="55823-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="55823-106">Fara á Öll vinnusvæði > fjárhagur smásöluverslana.</span><span class="sxs-lookup"><span data-stu-id="55823-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="55823-107">Smellt er á Reikna út uppgjör</span><span class="sxs-lookup"><span data-stu-id="55823-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="55823-108">Annað hvort velja ákveðna verslun, eða hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="55823-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="55823-109">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="55823-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="55823-110">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="55823-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="55823-111">Veljið undir runuvinnslu, 'Já'.</span><span class="sxs-lookup"><span data-stu-id="55823-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="55823-112">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="55823-112">Click Recurrence.</span></span>
6. <span data-ttu-id="55823-113">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="55823-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="55823-114">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="55823-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="55823-115">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="55823-115">Select the No end date option.</span></span>
9. <span data-ttu-id="55823-116">Færa inn "Dagar" í svæðinu PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="55823-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="55823-117">Í reitinn Á, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="55823-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="55823-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="55823-118">Click OK.</span></span>
12. <span data-ttu-id="55823-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="55823-119">Click OK.</span></span>

