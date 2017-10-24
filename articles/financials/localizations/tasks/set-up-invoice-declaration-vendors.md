--- 
title: "Setja upp verktakamiða fyrir lánardrottinn (Ísland)"
description: "Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða."
author: mrolecki
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7ce7101270ae3e59a6484b2f0efe0bd06f4a7c45
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-an-invoice-declaration-for-vendors-iceland"></a><span data-ttu-id="91ce1-103">Setja upp verktakamiða fyrir lánardrottinn (Ísland)</span><span class="sxs-lookup"><span data-stu-id="91ce1-103">Set up an invoice declaration for vendors (Iceland)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91ce1-104">Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="91ce1-104">This procedure walks you through setting up the Icelandic invoice declaration.</span></span> <span data-ttu-id="91ce1-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="91ce1-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="import-invoice-declaration-ger-configurations"></a><span data-ttu-id="91ce1-106">Flytja inn GER-skilgreiningar verktakamiða</span><span class="sxs-lookup"><span data-stu-id="91ce1-106">Import invoice declaration GER configurations</span></span>
1. <span data-ttu-id="91ce1-107">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="91ce1-107">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="91ce1-108">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="91ce1-108">Click Set active.</span></span>
3. <span data-ttu-id="91ce1-109">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="91ce1-109">Click Repositories.</span></span>
4. <span data-ttu-id="91ce1-110">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="91ce1-110">Click Open.</span></span>
5. <span data-ttu-id="91ce1-111">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="91ce1-111">Click Show filters.</span></span>
    * <span data-ttu-id="91ce1-112">Vinsamlegast bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="91ce1-112">Please add a criterion to filter by the Configuration name and enter Vendor invoice declaration (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
6. <span data-ttu-id="91ce1-113">Notaðu eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="91ce1-113">Apply the following filters: %3</span></span>
7. <span data-ttu-id="91ce1-114">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="91ce1-114">Click Import.</span></span>
8. <span data-ttu-id="91ce1-115">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="91ce1-115">Click Yes.</span></span>
9. <span data-ttu-id="91ce1-116">Bæta við síu</span><span class="sxs-lookup"><span data-stu-id="91ce1-116">Add filter</span></span>
    * <span data-ttu-id="91ce1-117">Bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn skýrslu verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="91ce1-117">Add a criterion to filter by the Configuration name and enter Vendor invoice declaration report (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
10. <span data-ttu-id="91ce1-118">Notaðu eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="91ce1-118">Apply the following filters: %3</span></span>
11. <span data-ttu-id="91ce1-119">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="91ce1-119">Click Import.</span></span>
12. <span data-ttu-id="91ce1-120">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="91ce1-120">Click Yes.</span></span>

## <a name="enable-vendor-invoice-declaration"></a><span data-ttu-id="91ce1-121">Virkja reikningsskýrslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91ce1-121">Enable vendor invoice declaration</span></span>
1. <span data-ttu-id="91ce1-122">Fara í Viðskiptaskuldir > Uppsetning > Verktakamiðar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="91ce1-122">Go to Accounts payable > Setup > Vendor invoice declaration.</span></span>
2. <span data-ttu-id="91ce1-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="91ce1-123">Click New.</span></span>
3. <span data-ttu-id="91ce1-124">Í reitnum Reikningur skal slá inn 'SubC'.</span><span class="sxs-lookup"><span data-stu-id="91ce1-124">In the Invoice declaration field, type 'SubC'.</span></span>
4. <span data-ttu-id="91ce1-125">Í reitnum Lýsing skal slá inn ‚Undirverktaki‘.</span><span class="sxs-lookup"><span data-stu-id="91ce1-125">In the Description field, type 'Sub-contractor'.</span></span>
5. <span data-ttu-id="91ce1-126">Í svæðinu fyrir Skýrslugerðakóði skal slá inn '06'.</span><span class="sxs-lookup"><span data-stu-id="91ce1-126">In the Reporting code field, type '06'.</span></span>
6. <span data-ttu-id="91ce1-127">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="91ce1-127">Click New.</span></span>
7. <span data-ttu-id="91ce1-128">Færa skal inn 'Gjafakort' í svæðið Verktakamiðar.</span><span class="sxs-lookup"><span data-stu-id="91ce1-128">In the Invoice declaration field, type 'Gift'.</span></span>
8. <span data-ttu-id="91ce1-129">Færa skal inn 'Gjafakort‘ í reitinn Lýsing.</span><span class="sxs-lookup"><span data-stu-id="91ce1-129">In the Description field, type 'Gifts'.</span></span>
9. <span data-ttu-id="91ce1-130">Í svæðinu fyrir Skýrslugerðarkóða skal slá inn '34'.</span><span class="sxs-lookup"><span data-stu-id="91ce1-130">In the Reporting code field, type '34'.</span></span>
10. <span data-ttu-id="91ce1-131">Í reitnum Færslugerð skal velja ‚LA‘.</span><span class="sxs-lookup"><span data-stu-id="91ce1-131">In the Record type field, select 'LA'.</span></span>
11. <span data-ttu-id="91ce1-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="91ce1-132">Click Save.</span></span>


