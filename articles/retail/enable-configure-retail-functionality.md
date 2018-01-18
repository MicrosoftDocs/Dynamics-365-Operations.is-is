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
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d3c81aaa675352eb679c1e1540f947c1d1da804b
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="6b534-103">Frumstilla grunngögn í nýju Retail-umhverfi</span><span class="sxs-lookup"><span data-stu-id="6b534-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="6b534-104">Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="6b534-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="6b534-105">Þegar smásölulausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla smásöluskilgreiningu til að stofna grunnskilgreiningargögn.</span><span class="sxs-lookup"><span data-stu-id="6b534-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="6b534-106">**Mikilvægt:** Áður en grunnstilling smásölu er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem setja verður upp verslanir fyrir smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="6b534-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="6b534-107">Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir smásölu.</span><span class="sxs-lookup"><span data-stu-id="6b534-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="6b534-108">Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar smásölu.</span><span class="sxs-lookup"><span data-stu-id="6b534-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="6b534-109">Ræsa Dynamics 365 for Retail-biðlara.</span><span class="sxs-lookup"><span data-stu-id="6b534-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="6b534-110">Smellt er á **Smásala** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Smásölufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="6b534-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="6b534-111">Smellið á **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="6b534-111">Click **Initialize**.</span></span>

<span data-ttu-id="6b534-112">Frumstilling stofnar eftirfarandi sjálfgefin skilgreiningargögn:</span><span class="sxs-lookup"><span data-stu-id="6b534-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="6b534-113">Vinnslur og undirvinnslur Retail Verkraðara</span><span class="sxs-lookup"><span data-stu-id="6b534-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="6b534-114">Skema smásölurásar</span><span class="sxs-lookup"><span data-stu-id="6b534-114">Retail channel schema</span></span>
-   <span data-ttu-id="6b534-115">Dreifingaráætlanir smásölu</span><span class="sxs-lookup"><span data-stu-id="6b534-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="6b534-116">Sjálfgefið útlit afgreiðsluskjás, sem inniheldur hnappahnit, myndir og þemu</span><span class="sxs-lookup"><span data-stu-id="6b534-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="6b534-117">Upplýsingar um tímabelti</span><span class="sxs-lookup"><span data-stu-id="6b534-117">Time zone information</span></span>
-   <span data-ttu-id="6b534-118">Aðgerðir í sölustað (POS)</span><span class="sxs-lookup"><span data-stu-id="6b534-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="6b534-119">Heimildir sölustaðar</span><span class="sxs-lookup"><span data-stu-id="6b534-119">POS permissions</span></span>
-   <span data-ttu-id="6b534-120">Skýrslur rásar</span><span class="sxs-lookup"><span data-stu-id="6b534-120">Channel reports</span></span>
-   <span data-ttu-id="6b534-121">Lýsigögn eiginda</span><span class="sxs-lookup"><span data-stu-id="6b534-121">Attribute metadata</span></span>
-   <span data-ttu-id="6b534-122">Sniðmát fyrir villuleit eininga</span><span class="sxs-lookup"><span data-stu-id="6b534-122">Entity validation templates</span></span>
-   <span data-ttu-id="6b534-123">Runuvinnsla til að hreinsa setuferil Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="6b534-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="6b534-124">Þar að auki er skráning sem er tengd við greiðslukortageirann (PCI) virk fyrir Dynamics 365 for Retail-gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="6b534-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="6b534-125">**Ábending:** Það er valkostur til að skilgreina Retail verkraðara sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="6b534-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="6b534-126">Þessi valkostur gerir kleift að endurstilla skilgreiningu Retail verkraðara á sjálfgefnar stillingar.</span><span class="sxs-lookup"><span data-stu-id="6b534-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="6b534-127">Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar smásölugagna.</span><span class="sxs-lookup"><span data-stu-id="6b534-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="6b534-128">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="6b534-128">Here are some examples:</span></span>

-   <span data-ttu-id="6b534-129">Smásölufæribreytur</span><span class="sxs-lookup"><span data-stu-id="6b534-129">Retail parameters</span></span>
-   <span data-ttu-id="6b534-130">Færibreytur Retail Verkraðara</span><span class="sxs-lookup"><span data-stu-id="6b534-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="6b534-131">Smásölurásir</span><span class="sxs-lookup"><span data-stu-id="6b534-131">Retail channels</span></span>
-   <span data-ttu-id="6b534-132">Afgreiðslukassar og tæki</span><span class="sxs-lookup"><span data-stu-id="6b534-132">Registers and devices</span></span>
-   <span data-ttu-id="6b534-133">Úrval</span><span class="sxs-lookup"><span data-stu-id="6b534-133">Assortments</span></span>





