---
title: Setja upp sjálfvirka afstemmingu farms
description: Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "357474"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="1db17-103">Setja upp sjálfvirka afstemmingu farms</span><span class="sxs-lookup"><span data-stu-id="1db17-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1db17-104">Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms.</span><span class="sxs-lookup"><span data-stu-id="1db17-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="1db17-105">Þetta er yfirleitt gert af stjórnanda vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="1db17-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="1db17-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="1db17-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="1db17-107">Setja upp gerð farmbréfs</span><span class="sxs-lookup"><span data-stu-id="1db17-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="1db17-108">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > gerð farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="1db17-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="1db17-109">Farmbréfið skilgreinir hvernig farmbréf og reikninga flutningsaðila ætti að jafna þær.</span><span class="sxs-lookup"><span data-stu-id="1db17-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="1db17-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1db17-110">Click New.</span></span>
3. <span data-ttu-id="1db17-111">Sláið inn gildi í reitnum Farms uppskrift gerð.</span><span class="sxs-lookup"><span data-stu-id="1db17-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="1db17-112">Sláðu inn 'Microsoft.Dynamics.Ax.Tms.dll‘ í reitinn Samsetning vélar.</span><span class="sxs-lookup"><span data-stu-id="1db17-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="1db17-113">Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.</span><span class="sxs-lookup"><span data-stu-id="1db17-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="1db17-114">Sláðu inn 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer‘ í reitinn Vélaklasi.</span><span class="sxs-lookup"><span data-stu-id="1db17-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="1db17-115">Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.</span><span class="sxs-lookup"><span data-stu-id="1db17-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="1db17-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1db17-116">Click New.</span></span>
7. <span data-ttu-id="1db17-117">Lýsingarsvæði, að velja gildið sem ættu að stemma á farmbréfið og reikning flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="1db17-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="1db17-118">Velja skal Já í svæðinu Jöfnun áskilin.</span><span class="sxs-lookup"><span data-stu-id="1db17-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="1db17-119">Ef þetta svæði var stillt á Já þetta merkir að gildið sem er valin í svæðinu Lýsingu verður að vera jöfn á farmbréfið og reikning flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="1db17-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="1db17-120">Ef það var stillt á Nei, svæðið má vera autt á eina af þeim.</span><span class="sxs-lookup"><span data-stu-id="1db17-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="1db17-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1db17-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="1db17-122">Setja upp úthlutanir á gerð farmbréfs</span><span class="sxs-lookup"><span data-stu-id="1db17-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="1db17-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1db17-123">Close the page.</span></span>
2. <span data-ttu-id="1db17-124">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > úthlutun á gerð farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="1db17-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="1db17-125">Úthlutun á gerð farmbréfs er notuð til að tilgreina hvaða gerð farmbréfs er notað fyrir tiltekna flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="1db17-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="1db17-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1db17-126">Click New.</span></span>
4. <span data-ttu-id="1db17-127">Sláið inn eða veldu gildi í reitnum Hamur.</span><span class="sxs-lookup"><span data-stu-id="1db17-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="1db17-128">Sláið inn eða veldu gildi í reitnum Farmflytjandi.</span><span class="sxs-lookup"><span data-stu-id="1db17-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="1db17-129">Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="1db17-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="1db17-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1db17-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="1db17-131">Setja upp endurskoðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="1db17-131">Set up the audit master</span></span>
1. <span data-ttu-id="1db17-132">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > endurskoðunarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="1db17-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="1db17-133">Aðalgögn endurskoðunar skilgreinir mörk verðvikmarka fyrir farmgjöld sjálfvirka afstemmingu.</span><span class="sxs-lookup"><span data-stu-id="1db17-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="1db17-134">Hún tilgreinir með hversu mikið er upphæða á farmbréfið og flutningsaðila reiknings getur verið önnur og leyfa enn afstemmingu að eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="1db17-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="1db17-135">Hann skilgreinir einnig hvernig á að meðhöndla misræmi.</span><span class="sxs-lookup"><span data-stu-id="1db17-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="1db17-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1db17-136">Click New.</span></span>
3. <span data-ttu-id="1db17-137">Í reitinn Kenni endurskoðunarsniðmáts skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1db17-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="1db17-138">Í svæðinu farmflytjanda sendingar, velja sama farmflytjanda sem var áður.</span><span class="sxs-lookup"><span data-stu-id="1db17-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="1db17-139">Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="1db17-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="1db17-140">Víkkið út hlutann Vikmörk.</span><span class="sxs-lookup"><span data-stu-id="1db17-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="1db17-141">Færið inn tölu í svæðinu Lágmarks vikmörk.</span><span class="sxs-lookup"><span data-stu-id="1db17-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="1db17-142">Færið inn tölu í svæðinu Hámarks vikmörk.</span><span class="sxs-lookup"><span data-stu-id="1db17-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="1db17-143">Víkkið út hlutann Niðurstaða.</span><span class="sxs-lookup"><span data-stu-id="1db17-143">Expand the Result section.</span></span>
10. <span data-ttu-id="1db17-144">Í reitinn Ástæðukóði ofgreiðslu skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="1db17-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="1db17-145">Ef upphæða sem eru mismunandi á farmbréfið og reikning flutningsaðila, tilgreina ofgreiðsla eða vangreiðsla ástæðukóða lykla sem á að skrá muninn á svo lengi sem mismunur er innan stig vikmarka.</span><span class="sxs-lookup"><span data-stu-id="1db17-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="1db17-146">Í reitinn Ástæðukóði vangreiðslu skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="1db17-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="1db17-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1db17-147">Close the page.</span></span>

