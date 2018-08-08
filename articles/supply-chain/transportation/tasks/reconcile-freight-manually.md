--- 
title: "Afstemma farmbréf handvirkt"
description: "Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt."
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: eb6f53de5013e8d5ee50c606bac15599bc960da4
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="8399f-103">Afstemma farmbréf handvirkt</span><span class="sxs-lookup"><span data-stu-id="8399f-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8399f-104">Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt.</span><span class="sxs-lookup"><span data-stu-id="8399f-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="8399f-105">Þetta er yfirleitt gert af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="8399f-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="8399f-106">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="8399f-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="8399f-107">Veljið hleðslu til að afstemma</span><span class="sxs-lookup"><span data-stu-id="8399f-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="8399f-108">Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.</span><span class="sxs-lookup"><span data-stu-id="8399f-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="8399f-109">Hreinsa gátreitinn Fela sent og móttekið.</span><span class="sxs-lookup"><span data-stu-id="8399f-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="8399f-110">Velja farms sem hefur farmkenni 00006 á listanum.</span><span class="sxs-lookup"><span data-stu-id="8399f-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="8399f-111">Stofna reikning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="8399f-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="8399f-112">Ef afstemmingu farms handvirkt og ekki sjálfkrafa mótteknir reikningar flutningsaðila, er hægt að stofna reikning á grundvelli farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="8399f-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="8399f-113">Smelltu á Tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8399f-113">Click Related information.</span></span>
2. <span data-ttu-id="8399f-114">Skoða upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="8399f-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="8399f-115">Smelltu á Stofna farmbréfsreikning.</span><span class="sxs-lookup"><span data-stu-id="8399f-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="8399f-116">Í reitinn Reikningur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8399f-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="8399f-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8399f-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="8399f-118">Afstemma reikning</span><span class="sxs-lookup"><span data-stu-id="8399f-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="8399f-119">Til að stemma af farmflytjanda reiknings og til farmbréfs, er þetta gert línu fyrir lína.</span><span class="sxs-lookup"><span data-stu-id="8399f-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="8399f-120">Smelltu á Jafna farmbréf og reikninga.</span><span class="sxs-lookup"><span data-stu-id="8399f-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="8399f-121">Útvíkka hlutann Reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8399f-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="8399f-122">Útvíkkið hlutann Ójafnaðar upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="8399f-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="8399f-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="8399f-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8399f-124">Smellt er á Jöfnun.</span><span class="sxs-lookup"><span data-stu-id="8399f-124">Click Match.</span></span>
6. <span data-ttu-id="8399f-125">Útvíkkið hlutann upplýsingar um jafnað farmbréf</span><span class="sxs-lookup"><span data-stu-id="8399f-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="8399f-126">Senda reikninginn til samþykkis</span><span class="sxs-lookup"><span data-stu-id="8399f-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="8399f-127">Smellið á Senda til samþykktar</span><span class="sxs-lookup"><span data-stu-id="8399f-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="8399f-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8399f-128">Close the page.</span></span>
3. <span data-ttu-id="8399f-129">Hreinsa gátreitinn Fela samþykkt</span><span class="sxs-lookup"><span data-stu-id="8399f-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="8399f-130">Smellið á Reikningabók lánardrottna</span><span class="sxs-lookup"><span data-stu-id="8399f-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="8399f-131">Smellið til að elta tengilinn í reitnum tilvísunarnúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8399f-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="8399f-132">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="8399f-132">Click Lines.</span></span>


