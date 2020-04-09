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
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141201"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="ec612-103">Skilgreina og keyra vinnsluna til að reikna uppgjör</span><span class="sxs-lookup"><span data-stu-id="ec612-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec612-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu á runuvinnslum ítrekað til að stofna og reikna uppgjör fyrir valda verslun eða verslunarflokk.</span><span class="sxs-lookup"><span data-stu-id="ec612-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="ec612-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="ec612-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ec612-106">Opna Öll vinnusvæði > Fjármál verslunar.</span><span class="sxs-lookup"><span data-stu-id="ec612-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="ec612-107">Smellt er á Reikna út uppgjör</span><span class="sxs-lookup"><span data-stu-id="ec612-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="ec612-108">Annað hvort velja ákveðna verslun, eða hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="ec612-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ec612-109">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="ec612-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ec612-110">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="ec612-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="ec612-111">Veljið undir runuvinnslu, 'Já'.</span><span class="sxs-lookup"><span data-stu-id="ec612-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="ec612-112">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="ec612-112">Click Recurrence.</span></span>
6. <span data-ttu-id="ec612-113">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="ec612-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ec612-114">Í reitinn upphafstími skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="ec612-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="ec612-115">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="ec612-115">Select the No end date option.</span></span>
9. <span data-ttu-id="ec612-116">Færa inn "Dagar" í svæðinu PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="ec612-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="ec612-117">Í reitinn Á, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ec612-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="ec612-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ec612-118">Click OK.</span></span>
12. <span data-ttu-id="ec612-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ec612-119">Click OK.</span></span>

