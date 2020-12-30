---
title: Afstemma farmbréf handvirkt
description: Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430707"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="1be66-103">Afstemma farm handvirkt</span><span class="sxs-lookup"><span data-stu-id="1be66-103">Reconcile freight manually</span></span>

<span data-ttu-id="1be66-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="1be66-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="1be66-105">Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1be66-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="1be66-106">Þetta er yfirleitt gert af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="1be66-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="1be66-107">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="1be66-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="1be66-108">Veljið hleðslu til að afstemma</span><span class="sxs-lookup"><span data-stu-id="1be66-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="1be66-109">Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.</span><span class="sxs-lookup"><span data-stu-id="1be66-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="1be66-110">Hreinsa gátreitinn Fela sent og móttekið.</span><span class="sxs-lookup"><span data-stu-id="1be66-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="1be66-111">Velja farms sem hefur farmkenni 00006 á listanum.</span><span class="sxs-lookup"><span data-stu-id="1be66-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="1be66-112">Stofna reikning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="1be66-112">Create a carrier invoice</span></span>
<span data-ttu-id="1be66-113">Ef afstemmingu farms handvirkt og ekki sjálfkrafa mótteknir reikningar flutningsaðila, er hægt að stofna reikning á grundvelli farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="1be66-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="1be66-114">Smelltu á Tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1be66-114">Click Related information.</span></span>
2. <span data-ttu-id="1be66-115">Skoða upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="1be66-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="1be66-116">Smelltu á Stofna farmbréfsreikning.</span><span class="sxs-lookup"><span data-stu-id="1be66-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="1be66-117">Í reitinn Reikningur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1be66-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="1be66-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1be66-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="1be66-119">Afstemma reikning</span><span class="sxs-lookup"><span data-stu-id="1be66-119">Reconcile the invoice</span></span>
<span data-ttu-id="1be66-120">Til að stemma af farmflytjanda reiknings og til farmbréfs, er þetta gert línu fyrir lína.</span><span class="sxs-lookup"><span data-stu-id="1be66-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="1be66-121">Smelltu á Jafna farmbréf og reikninga.</span><span class="sxs-lookup"><span data-stu-id="1be66-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="1be66-122">Útvíkka hlutann Reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1be66-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="1be66-123">Útvíkkið hlutann Ójafnaðar upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="1be66-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="1be66-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1be66-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="1be66-125">Smellt er á Jöfnun.</span><span class="sxs-lookup"><span data-stu-id="1be66-125">Click Match.</span></span>
6. <span data-ttu-id="1be66-126">Útvíkkið hlutann upplýsingar um jafnað farmbréf</span><span class="sxs-lookup"><span data-stu-id="1be66-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="1be66-127">Senda reikninginn til samþykkis</span><span class="sxs-lookup"><span data-stu-id="1be66-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="1be66-128">Smellið á Senda til samþykktar</span><span class="sxs-lookup"><span data-stu-id="1be66-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="1be66-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1be66-129">Close the page.</span></span>
3. <span data-ttu-id="1be66-130">Hreinsa gátreitinn Fela samþykkt</span><span class="sxs-lookup"><span data-stu-id="1be66-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="1be66-131">Smellið á Reikningabók lánardrottna</span><span class="sxs-lookup"><span data-stu-id="1be66-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="1be66-132">Smellið til að elta tengilinn í reitnum tilvísunarnúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="1be66-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="1be66-133">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="1be66-133">Click Lines.</span></span>

