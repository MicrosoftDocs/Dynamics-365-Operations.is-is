---
title: Setja upp verktakamiða fyrir lánardrottna
description: Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport,  VendInvoiceDeclaration_IS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4795f6c442a03cdb34b4522b2dca2ca3a0b9eb83
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183700"
---
# <a name="set-up-an-invoice-declaration-for-vendors"></a><span data-ttu-id="e03a3-103">Setja upp verktakamiða fyrir lánardrottna</span><span class="sxs-lookup"><span data-stu-id="e03a3-103">Set up an invoice declaration for vendors</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e03a3-104">Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="e03a3-104">This procedure walks you through setting up the Icelandic invoice declaration.</span></span> <span data-ttu-id="e03a3-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="e03a3-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="import-invoice-declaration-ger-configurations"></a><span data-ttu-id="e03a3-106">Flytja inn GER-skilgreiningar verktakamiða</span><span class="sxs-lookup"><span data-stu-id="e03a3-106">Import invoice declaration GER configurations</span></span>
1. <span data-ttu-id="e03a3-107">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e03a3-107">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e03a3-108">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="e03a3-108">Click Set active.</span></span>
3. <span data-ttu-id="e03a3-109">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="e03a3-109">Click Repositories.</span></span>
4. <span data-ttu-id="e03a3-110">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="e03a3-110">Click Open.</span></span>
5. <span data-ttu-id="e03a3-111">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="e03a3-111">Click Show filters.</span></span>
    * <span data-ttu-id="e03a3-112">Vinsamlegast bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="e03a3-112">Please add a criterion to filter by the Configuration name and enter Vendor invoice declaration (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
6. <span data-ttu-id="e03a3-113">Nota eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="e03a3-113">Apply the following filters: %3</span></span>
7. <span data-ttu-id="e03a3-114">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="e03a3-114">Click Import.</span></span>
8. <span data-ttu-id="e03a3-115">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e03a3-115">Click Yes.</span></span>
9. <span data-ttu-id="e03a3-116">Bæta við síu</span><span class="sxs-lookup"><span data-stu-id="e03a3-116">Add filter</span></span>
    * <span data-ttu-id="e03a3-117">Bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn skýrslu verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="e03a3-117">Add a criterion to filter by the Configuration name and enter Vendor invoice declaration report (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
10. <span data-ttu-id="e03a3-118">Nota eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="e03a3-118">Apply the following filters: %3</span></span>
11. <span data-ttu-id="e03a3-119">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="e03a3-119">Click Import.</span></span>
12. <span data-ttu-id="e03a3-120">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e03a3-120">Click Yes.</span></span>

## <a name="enable-vendor-invoice-declaration"></a><span data-ttu-id="e03a3-121">Virkja reikningsskýrslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="e03a3-121">Enable vendor invoice declaration</span></span>
1. <span data-ttu-id="e03a3-122">Fara í Viðskiptaskuldir > Uppsetning > Verktakamiðar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="e03a3-122">Go to Accounts payable > Setup > Vendor invoice declaration.</span></span>
2. <span data-ttu-id="e03a3-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e03a3-123">Click New.</span></span>
3. <span data-ttu-id="e03a3-124">Í reitnum Reikningur skal slá inn 'SubC'.</span><span class="sxs-lookup"><span data-stu-id="e03a3-124">In the Invoice declaration field, type 'SubC'.</span></span>
4. <span data-ttu-id="e03a3-125">Í reitnum Lýsing skal slá inn ‚Undirverktaki‘.</span><span class="sxs-lookup"><span data-stu-id="e03a3-125">In the Description field, type 'Sub-contractor'.</span></span>
5. <span data-ttu-id="e03a3-126">Í svæðinu fyrir Skýrslugerðakóði skal slá inn '06'.</span><span class="sxs-lookup"><span data-stu-id="e03a3-126">In the Reporting code field, type '06'.</span></span>
6. <span data-ttu-id="e03a3-127">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="e03a3-127">Click New.</span></span>
7. <span data-ttu-id="e03a3-128">Færa skal inn 'Gjafakort' í svæðið Verktakamiðar.</span><span class="sxs-lookup"><span data-stu-id="e03a3-128">In the Invoice declaration field, type 'Gift'.</span></span>
8. <span data-ttu-id="e03a3-129">Færa skal inn 'Gjafakort‘ í reitinn Lýsing.</span><span class="sxs-lookup"><span data-stu-id="e03a3-129">In the Description field, type 'Gifts'.</span></span>
9. <span data-ttu-id="e03a3-130">Í svæðinu fyrir Skýrslugerðarkóða skal slá inn '34'.</span><span class="sxs-lookup"><span data-stu-id="e03a3-130">In the Reporting code field, type '34'.</span></span>
10. <span data-ttu-id="e03a3-131">Í reitnum Færslugerð skal velja ‚LA‘.</span><span class="sxs-lookup"><span data-stu-id="e03a3-131">In the Record type field, select 'LA'.</span></span>
11. <span data-ttu-id="e03a3-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e03a3-132">Click Save.</span></span>

