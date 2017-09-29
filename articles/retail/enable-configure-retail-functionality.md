---
title: "Frumstilla grunngögn í nýju Retail-umhverfi"
description: "Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ac4f651cd7e5df912ea2535eafd5e54c11377253
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="a446c-103">Frumstilla grunngögn í nýju Retail-umhverfi</span><span class="sxs-lookup"><span data-stu-id="a446c-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a446c-104">Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a446c-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a446c-105">Þegar smásölulausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla smásöluskilgreiningu til að stofna grunnskilgreiningargögn.</span><span class="sxs-lookup"><span data-stu-id="a446c-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="a446c-106">**Mikilvægt:** Áður en grunnstilling smásölu er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem setja verður upp verslanir fyrir smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="a446c-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="a446c-107">Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir smásölu.</span><span class="sxs-lookup"><span data-stu-id="a446c-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="a446c-108">Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar smásölu.</span><span class="sxs-lookup"><span data-stu-id="a446c-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="a446c-109">Ræsa Dynamics 365 for Retail-biðlara.</span><span class="sxs-lookup"><span data-stu-id="a446c-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="a446c-110">Smellt er á **Smásala** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Smásölufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="a446c-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="a446c-111">Smellið á **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="a446c-111">Click **Initialize**.</span></span>

<span data-ttu-id="a446c-112">Frumstilling stofnar eftirfarandi sjálfgefin skilgreiningargögn:</span><span class="sxs-lookup"><span data-stu-id="a446c-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="a446c-113">Vinnslur og undirvinnslur Retail Verkraðara</span><span class="sxs-lookup"><span data-stu-id="a446c-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="a446c-114">Skema smásölurásar</span><span class="sxs-lookup"><span data-stu-id="a446c-114">Retail channel schema</span></span>
-   <span data-ttu-id="a446c-115">Dreifingaráætlanir smásölu</span><span class="sxs-lookup"><span data-stu-id="a446c-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="a446c-116">Sjálfgefið útlit afgreiðsluskjás, sem inniheldur hnappahnit, myndir og þemu</span><span class="sxs-lookup"><span data-stu-id="a446c-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="a446c-117">Upplýsingar um tímabelti</span><span class="sxs-lookup"><span data-stu-id="a446c-117">Time zone information</span></span>
-   <span data-ttu-id="a446c-118">Aðgerðir í sölustað (POS)</span><span class="sxs-lookup"><span data-stu-id="a446c-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="a446c-119">Heimildir sölustaðar</span><span class="sxs-lookup"><span data-stu-id="a446c-119">POS permissions</span></span>
-   <span data-ttu-id="a446c-120">Skýrslur rásar</span><span class="sxs-lookup"><span data-stu-id="a446c-120">Channel reports</span></span>
-   <span data-ttu-id="a446c-121">Lýsigögn eiginda</span><span class="sxs-lookup"><span data-stu-id="a446c-121">Attribute metadata</span></span>
-   <span data-ttu-id="a446c-122">Sniðmát fyrir villuleit eininga</span><span class="sxs-lookup"><span data-stu-id="a446c-122">Entity validation templates</span></span>
-   <span data-ttu-id="a446c-123">Runuvinnsla til að hreinsa setuferil Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="a446c-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="a446c-124">Þar að auki er skráning sem er tengd við greiðslukortageirann (PCI) virk fyrir Dynamics 365 for Retail-gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="a446c-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="a446c-125">**Ábending:** Það er valkostur til að skilgreina Retail verkraðara sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="a446c-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="a446c-126">Þessi valkostur gerir kleift að endurstilla skilgreiningu Retail verkraðara á sjálfgefnar stillingar.</span><span class="sxs-lookup"><span data-stu-id="a446c-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="a446c-127">Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar smásölugagna.</span><span class="sxs-lookup"><span data-stu-id="a446c-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="a446c-128">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="a446c-128">Here are some examples:</span></span>

-   <span data-ttu-id="a446c-129">Smásölufæribreytur</span><span class="sxs-lookup"><span data-stu-id="a446c-129">Retail parameters</span></span>
-   <span data-ttu-id="a446c-130">Færibreytur Retail Verkraðara</span><span class="sxs-lookup"><span data-stu-id="a446c-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="a446c-131">Smásölurásir</span><span class="sxs-lookup"><span data-stu-id="a446c-131">Retail channels</span></span>
-   <span data-ttu-id="a446c-132">Afgreiðslukassar og tæki</span><span class="sxs-lookup"><span data-stu-id="a446c-132">Registers and devices</span></span>
-   <span data-ttu-id="a446c-133">Úrval</span><span class="sxs-lookup"><span data-stu-id="a446c-133">Assortments</span></span>





