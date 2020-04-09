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
ms.openlocfilehash: b30e387658fb6c4a8a3f2b0407c8022c4276c7d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140133"
---
# <a name="set-up-an-invoice-declaration-for-vendors"></a><span data-ttu-id="a01ee-103">Setja upp verktakamiða fyrir lánardrottna</span><span class="sxs-lookup"><span data-stu-id="a01ee-103">Set up an invoice declaration for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a01ee-104">Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="a01ee-104">This procedure walks you through setting up the Icelandic invoice declaration.</span></span> <span data-ttu-id="a01ee-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="a01ee-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="import-invoice-declaration-ger-configurations"></a><span data-ttu-id="a01ee-106">Flytja inn GER-skilgreiningar verktakamiða</span><span class="sxs-lookup"><span data-stu-id="a01ee-106">Import invoice declaration GER configurations</span></span>
1. <span data-ttu-id="a01ee-107">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a01ee-107">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a01ee-108">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="a01ee-108">Click Set active.</span></span>
3. <span data-ttu-id="a01ee-109">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="a01ee-109">Click Repositories.</span></span>
4. <span data-ttu-id="a01ee-110">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="a01ee-110">Click Open.</span></span>
5. <span data-ttu-id="a01ee-111">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="a01ee-111">Click Show filters.</span></span>
    * <span data-ttu-id="a01ee-112">Vinsamlegast bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="a01ee-112">Please add a criterion to filter by the Configuration name and enter Vendor invoice declaration (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
6. <span data-ttu-id="a01ee-113">Nota eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="a01ee-113">Apply the following filters: %3</span></span>
7. <span data-ttu-id="a01ee-114">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="a01ee-114">Click Import.</span></span>
8. <span data-ttu-id="a01ee-115">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="a01ee-115">Click Yes.</span></span>
9. <span data-ttu-id="a01ee-116">Bæta við síu</span><span class="sxs-lookup"><span data-stu-id="a01ee-116">Add filter</span></span>
    * <span data-ttu-id="a01ee-117">Bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn skýrslu verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="a01ee-117">Add a criterion to filter by the Configuration name and enter Vendor invoice declaration report (IS) or find the configuration in the list, select it and move to the next step.</span></span>  
10. <span data-ttu-id="a01ee-118">Nota eftirfarandi síur: %3</span><span class="sxs-lookup"><span data-stu-id="a01ee-118">Apply the following filters: %3</span></span>
11. <span data-ttu-id="a01ee-119">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="a01ee-119">Click Import.</span></span>
12. <span data-ttu-id="a01ee-120">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="a01ee-120">Click Yes.</span></span>

## <a name="enable-vendor-invoice-declaration"></a><span data-ttu-id="a01ee-121">Virkja reikningsskýrslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a01ee-121">Enable vendor invoice declaration</span></span>
1. <span data-ttu-id="a01ee-122">Fara í Viðskiptaskuldir > Uppsetning > Verktakamiðar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="a01ee-122">Go to Accounts payable > Setup > Vendor invoice declaration.</span></span>
2. <span data-ttu-id="a01ee-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a01ee-123">Click New.</span></span>
3. <span data-ttu-id="a01ee-124">Í reitnum Reikningur skal slá inn 'SubC'.</span><span class="sxs-lookup"><span data-stu-id="a01ee-124">In the Invoice declaration field, type 'SubC'.</span></span>
4. <span data-ttu-id="a01ee-125">Í reitnum Lýsing skal slá inn ‚Undirverktaki‘.</span><span class="sxs-lookup"><span data-stu-id="a01ee-125">In the Description field, type 'Sub-contractor'.</span></span>
5. <span data-ttu-id="a01ee-126">Í svæðinu fyrir Skýrslugerðakóði skal slá inn '06'.</span><span class="sxs-lookup"><span data-stu-id="a01ee-126">In the Reporting code field, type '06'.</span></span>
6. <span data-ttu-id="a01ee-127">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="a01ee-127">Click New.</span></span>
7. <span data-ttu-id="a01ee-128">Færa skal inn 'Gjafakort' í svæðið Verktakamiðar.</span><span class="sxs-lookup"><span data-stu-id="a01ee-128">In the Invoice declaration field, type 'Gift'.</span></span>
8. <span data-ttu-id="a01ee-129">Færa skal inn 'Gjafakort‘ í reitinn Lýsing.</span><span class="sxs-lookup"><span data-stu-id="a01ee-129">In the Description field, type 'Gifts'.</span></span>
9. <span data-ttu-id="a01ee-130">Í svæðinu fyrir Skýrslugerðarkóða skal slá inn '34'.</span><span class="sxs-lookup"><span data-stu-id="a01ee-130">In the Reporting code field, type '34'.</span></span>
10. <span data-ttu-id="a01ee-131">Í reitnum Færslugerð skal velja ‚LA‘.</span><span class="sxs-lookup"><span data-stu-id="a01ee-131">In the Record type field, select 'LA'.</span></span>
11. <span data-ttu-id="a01ee-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a01ee-132">Click Save.</span></span>

