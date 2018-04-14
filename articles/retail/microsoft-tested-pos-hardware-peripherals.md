---
title: "Jaðarbúnaður POS-vélbúnaðar"
description: "Retail Modern sölukerfi í skýinu (POS) og Cloud POS geta notað vítækt jaðartæki POS, með mörg viðmót og notkunarmöguleika til að uppfylla mismunandi viðskiptaaðstæður smásalans."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6ecfb0d6d3884bd8c96444613afed68547e141f1
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="eeac4-103">Jaðarbúnaður POS-vélbúnaðar</span><span class="sxs-lookup"><span data-stu-id="eeac4-103">POS hardware peripherals</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="eeac4-104">Retaoæ Modern sölukerfi í skýinu (POS) og Cloud POS geta notað vítækt jaðartæki POS, með mörg viðmót og notkunarmöguleika til að uppfylla mismunandi viðskiptaaðstæður smásalans.</span><span class="sxs-lookup"><span data-stu-id="eeac4-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="eeac4-105">Til að styðja við víðtækasta val á tækjum framleiðenda og gerða, notar POS staðlað viðmót eins og Ole fyrir Retail POS (OPOS), Windows tækisrekla, og Windows viðmót forrits fyrir þjónustustað (API).</span><span class="sxs-lookup"><span data-stu-id="eeac4-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="eeac4-106">Almennt, vinnur POS á þessar tæki svo lengi sem veittur er viðeigandi rekill.</span><span class="sxs-lookup"><span data-stu-id="eeac4-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="eeac4-107">Hins vegar, þar sem hver framleiðanda og forritari geta beitt þessum stöðlum á mismunandi hátt, eru oft mismunur í studdri getu eða hegðun.</span><span class="sxs-lookup"><span data-stu-id="eeac4-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="eeac4-108">Eftirfarandi listi inniheldur gerðir tækja, í hverri flokki, sem hafa verið prófaðar af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eeac4-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="eeac4-109">**OPOS-tæki**</span><span class="sxs-lookup"><span data-stu-id="eeac4-109">**OPOS devices**</span></span>

-   <span data-ttu-id="eeac4-110">Strikamerki – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="eeac4-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="eeac4-111">Kortalesari – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="eeac4-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="eeac4-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="eeac4-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="eeac4-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="eeac4-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="eeac4-114">Undirskriftartæki – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="eeac4-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="eeac4-115">Prentari – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="eeac4-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="eeac4-116">Peningaskúffur – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="eeac4-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="eeac4-117">Vigt – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="eeac4-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="eeac4-118">**Lyklaborð wedge Kortalesara**</span><span class="sxs-lookup"><span data-stu-id="eeac4-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="eeac4-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="eeac4-119">Magtek USB</span></span>

<span data-ttu-id="eeac4-120">**Greiðslustöð**</span><span class="sxs-lookup"><span data-stu-id="eeac4-120">**Payment terminal**</span></span>

-   <span data-ttu-id="eeac4-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="eeac4-121">Equinox L3500</span></span>
-   <span data-ttu-id="eeac4-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="eeac4-122">Verifone MX925</span></span>

<span data-ttu-id="eeac4-123">**Nettæki**</span><span class="sxs-lookup"><span data-stu-id="eeac4-123">**Network devices**</span></span>

-   <span data-ttu-id="eeac4-124">Prentari – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="eeac4-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="eeac4-125">Peningaskúffa – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="eeac4-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="eeac4-126">Greiðslustöð – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="eeac4-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="eeac4-127">**MPOS eingöngu direct IPC**</span><span class="sxs-lookup"><span data-stu-id="eeac4-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="eeac4-128">Strikamerki – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="eeac4-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="eeac4-129">Kortalesari – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="eeac4-129">MSR – Magtek PN - 21073075</span></span>





