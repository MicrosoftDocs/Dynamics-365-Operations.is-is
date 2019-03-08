---
title: Bókun á sölu á netinu og greiðslur
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "353495"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="8f172-103">Bókun á sölu á netinu og greiðslur</span><span class="sxs-lookup"><span data-stu-id="8f172-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8f172-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.</span><span class="sxs-lookup"><span data-stu-id="8f172-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="8f172-105">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="8f172-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8f172-106">Fara á Öll vinnusvæði > fjárhagur smásöluverslana.</span><span class="sxs-lookup"><span data-stu-id="8f172-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="8f172-107">Smellt er á Samstilla pantanir</span><span class="sxs-lookup"><span data-stu-id="8f172-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="8f172-108">Í svæðinu stigveldi Fyrirtækis, veljið 'Smásöluverslanir eftir Svæði'.</span><span class="sxs-lookup"><span data-stu-id="8f172-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="8f172-109">Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="8f172-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="8f172-110">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="8f172-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="8f172-111">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="8f172-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="8f172-112">Kanna eða afmerkja gátreit runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="8f172-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="8f172-113">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="8f172-113">Click Recurrence.</span></span>
7. <span data-ttu-id="8f172-114">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="8f172-114">Select the No end date option.</span></span>
8. <span data-ttu-id="8f172-115">Í reitinn Fjöldi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="8f172-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="8f172-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8f172-116">Click OK.</span></span>
10. <span data-ttu-id="8f172-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8f172-117">Click OK.</span></span>

