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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8679a729dc17e3ee85468b459da3956a92160ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974061"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="9e38c-103">Afstemma farm handvirkt</span><span class="sxs-lookup"><span data-stu-id="9e38c-103">Reconcile freight manually</span></span>

<span data-ttu-id="9e38c-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="9e38c-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="9e38c-105">Þessi verklýsing sýnir hvernig afstemmingu farms handvirkt.</span><span class="sxs-lookup"><span data-stu-id="9e38c-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="9e38c-106">Þetta er yfirleitt gert af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="9e38c-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="9e38c-107">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="9e38c-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="9e38c-108">Veljið hleðslu til að afstemma</span><span class="sxs-lookup"><span data-stu-id="9e38c-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="9e38c-109">Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.</span><span class="sxs-lookup"><span data-stu-id="9e38c-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="9e38c-110">Hreinsa gátreitinn Fela sent og móttekið.</span><span class="sxs-lookup"><span data-stu-id="9e38c-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="9e38c-111">Velja farms sem hefur farmkenni 00006 á listanum.</span><span class="sxs-lookup"><span data-stu-id="9e38c-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="9e38c-112">Stofna reikning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="9e38c-112">Create a carrier invoice</span></span>
<span data-ttu-id="9e38c-113">Ef afstemmingu farms handvirkt og ekki sjálfkrafa mótteknir reikningar flutningsaðila, er hægt að stofna reikning á grundvelli farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="9e38c-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="9e38c-114">Smelltu á Tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9e38c-114">Click Related information.</span></span>
2. <span data-ttu-id="9e38c-115">Skoða upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="9e38c-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="9e38c-116">Smelltu á Stofna farmbréfsreikning.</span><span class="sxs-lookup"><span data-stu-id="9e38c-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="9e38c-117">Í reitinn Reikningur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e38c-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="9e38c-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e38c-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="9e38c-119">Afstemma reikning</span><span class="sxs-lookup"><span data-stu-id="9e38c-119">Reconcile the invoice</span></span>
<span data-ttu-id="9e38c-120">Til að stemma af farmflytjanda reiknings og til farmbréfs, er þetta gert línu fyrir lína.</span><span class="sxs-lookup"><span data-stu-id="9e38c-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="9e38c-121">Smelltu á Jafna farmbréf og reikninga.</span><span class="sxs-lookup"><span data-stu-id="9e38c-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="9e38c-122">Útvíkka hlutann Reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9e38c-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="9e38c-123">Útvíkkið hlutann Ójafnaðar upplýsingar farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="9e38c-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="9e38c-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9e38c-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9e38c-125">Smellt er á Jöfnun.</span><span class="sxs-lookup"><span data-stu-id="9e38c-125">Click Match.</span></span>
6. <span data-ttu-id="9e38c-126">Útvíkkið hlutann upplýsingar um jafnað farmbréf</span><span class="sxs-lookup"><span data-stu-id="9e38c-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="9e38c-127">Senda reikninginn til samþykkis</span><span class="sxs-lookup"><span data-stu-id="9e38c-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="9e38c-128">Smellið á Senda til samþykktar</span><span class="sxs-lookup"><span data-stu-id="9e38c-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="9e38c-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e38c-129">Close the page.</span></span>
3. <span data-ttu-id="9e38c-130">Hreinsa gátreitinn Fela samþykkt</span><span class="sxs-lookup"><span data-stu-id="9e38c-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="9e38c-131">Smellið á Reikningabók lánardrottna</span><span class="sxs-lookup"><span data-stu-id="9e38c-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="9e38c-132">Smellið til að elta tengilinn í reitnum tilvísunarnúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="9e38c-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="9e38c-133">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="9e38c-133">Click Lines.</span></span>

