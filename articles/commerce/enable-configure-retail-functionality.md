---
title: Frumstilla grunngögn í nýju Retail-umhverfi
description: Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022951"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="9d1f8-103">Frumstilla grunngögn í nýju Retail-umhverfi</span><span class="sxs-lookup"><span data-stu-id="9d1f8-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d1f8-104">Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9d1f8-105">Þegar Commerce-lausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla Commerce-skilgreiningu til að stofna grunnskilgreiningargögn.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d1f8-106">Áður en grunnstilling Commerce er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem settar verða upp verslanir fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="9d1f8-107">Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="9d1f8-108">Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="9d1f8-109">Ræsið Commerce-biðlarann.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="9d1f8-110">Smelltu á **Retail og Commerce** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Commerce-færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="9d1f8-111">Smellið á **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-111">Click **Initialize**.</span></span>

<span data-ttu-id="9d1f8-112">Frumstilling stofnar eftirfarandi sjálfgefin skilgreiningargögn:</span><span class="sxs-lookup"><span data-stu-id="9d1f8-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="9d1f8-113">Vinnslur og undirvinnslur Commerce Verkraðara</span><span class="sxs-lookup"><span data-stu-id="9d1f8-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="9d1f8-114">Skema fyrir viðskiptarás</span><span class="sxs-lookup"><span data-stu-id="9d1f8-114">Commerce channel schema</span></span>
- <span data-ttu-id="9d1f8-115">Dreifingaráætlanir Commerce</span><span class="sxs-lookup"><span data-stu-id="9d1f8-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="9d1f8-116">Sjálfgefið útlit afgreiðsluskjás, sem inniheldur hnappahnit, myndir og þemu</span><span class="sxs-lookup"><span data-stu-id="9d1f8-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="9d1f8-117">Upplýsingar um tímabelti</span><span class="sxs-lookup"><span data-stu-id="9d1f8-117">Time zone information</span></span>
- <span data-ttu-id="9d1f8-118">Aðgerðir í sölustað (POS)</span><span class="sxs-lookup"><span data-stu-id="9d1f8-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="9d1f8-119">Heimildir sölustaðar</span><span class="sxs-lookup"><span data-stu-id="9d1f8-119">POS permissions</span></span>
- <span data-ttu-id="9d1f8-120">Skýrslur rásar</span><span class="sxs-lookup"><span data-stu-id="9d1f8-120">Channel reports</span></span>
- <span data-ttu-id="9d1f8-121">Lýsigögn eiginda</span><span class="sxs-lookup"><span data-stu-id="9d1f8-121">Attribute metadata</span></span>
- <span data-ttu-id="9d1f8-122">Sniðmát fyrir villuleit eininga</span><span class="sxs-lookup"><span data-stu-id="9d1f8-122">Entity validation templates</span></span>
- <span data-ttu-id="9d1f8-123">Runuvinnsla til að hreinsa setuferil Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="9d1f8-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="9d1f8-124">Þar að auki er skráning sem er tengd við greiðslu korts atvinnugrein (PCI) er virk fyrir Commerce-gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="9d1f8-125">Það er möguleiki á því að skilgreina verkröð Commerce sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="9d1f8-126">Þessi valkostur gerir kleift að endurstilla skilgreiningu Commerce verkraðara á sjálfgefnar stillingar.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="9d1f8-127">Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar Commerce-gagna.</span><span class="sxs-lookup"><span data-stu-id="9d1f8-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="9d1f8-128">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="9d1f8-128">Here are some examples:</span></span>

- <span data-ttu-id="9d1f8-129">Viðskiptafæribreytur</span><span class="sxs-lookup"><span data-stu-id="9d1f8-129">Commerce parameters</span></span>
- <span data-ttu-id="9d1f8-130">Færibreytur viðskiptaverkraðara</span><span class="sxs-lookup"><span data-stu-id="9d1f8-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="9d1f8-131">Commerce-rásir</span><span class="sxs-lookup"><span data-stu-id="9d1f8-131">Commerce channels</span></span>
- <span data-ttu-id="9d1f8-132">Afgreiðslukassar og tæki</span><span class="sxs-lookup"><span data-stu-id="9d1f8-132">Registers and devices</span></span>
- <span data-ttu-id="9d1f8-133">Úrval</span><span class="sxs-lookup"><span data-stu-id="9d1f8-133">Assortments</span></span>
