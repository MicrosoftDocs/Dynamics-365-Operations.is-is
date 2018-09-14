--- 
title: "Setja upp sjálfvirka afstemmingu farms"
description: "Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 00412771c21c7f8ab0edc55b7d7121b7ec615415
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="8111a-103">Setja upp sjálfvirka afstemmingu farms</span><span class="sxs-lookup"><span data-stu-id="8111a-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8111a-104">Þessi verklýsing sýnir hvernig á að setja upp gögn fyrir sjálfvirka afstemmingu farms.</span><span class="sxs-lookup"><span data-stu-id="8111a-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="8111a-105">Þetta er yfirleitt gert af stjórnanda vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="8111a-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="8111a-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="8111a-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="8111a-107">Setja upp gerð farmbréfs</span><span class="sxs-lookup"><span data-stu-id="8111a-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="8111a-108">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > gerð farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="8111a-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="8111a-109">Farmbréfið skilgreinir hvernig farmbréf og reikninga flutningsaðila ætti að jafna þær.</span><span class="sxs-lookup"><span data-stu-id="8111a-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="8111a-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8111a-110">Click New.</span></span>
3. <span data-ttu-id="8111a-111">Sláið inn gildi í reitnum Farms uppskrift gerð.</span><span class="sxs-lookup"><span data-stu-id="8111a-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="8111a-112">Í svæðinu samsetning Vélar, slærðu inn 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span><span class="sxs-lookup"><span data-stu-id="8111a-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="8111a-113">Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.</span><span class="sxs-lookup"><span data-stu-id="8111a-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="8111a-114">Í svæðinu Vélaklasi, slærðu inn 'Microsoft.Dynamics.Ax.Tms.dll'.</span><span class="sxs-lookup"><span data-stu-id="8111a-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="8111a-115">Þetta er stöðluð Flutningsmáta stjórnun samsvarandi vél kóða safnið.</span><span class="sxs-lookup"><span data-stu-id="8111a-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="8111a-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8111a-116">Click New.</span></span>
7. <span data-ttu-id="8111a-117">Lýsingarsvæði, að velja gildið sem ættu að stemma á farmbréfið og reikning flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="8111a-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="8111a-118">Velja skal Já í svæðinu Jöfnun áskilin.</span><span class="sxs-lookup"><span data-stu-id="8111a-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="8111a-119">Ef þetta svæði var stillt á Já þetta merkir að gildið sem er valin í svæðinu Lýsingu verður að vera jöfn á farmbréfið og reikning flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="8111a-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="8111a-120">Ef það var stillt á Nei, svæðið má vera autt á eina af þeim.</span><span class="sxs-lookup"><span data-stu-id="8111a-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="8111a-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8111a-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="8111a-122">Setja upp úthlutanir á gerð farmbréfs</span><span class="sxs-lookup"><span data-stu-id="8111a-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="8111a-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8111a-123">Close the page.</span></span>
2. <span data-ttu-id="8111a-124">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > úthlutun á gerð farmbréfs.</span><span class="sxs-lookup"><span data-stu-id="8111a-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="8111a-125">Úthlutun á gerð farmbréfs er notuð til að tilgreina hvaða gerð farmbréfs er notað fyrir tiltekna flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="8111a-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="8111a-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8111a-126">Click New.</span></span>
4. <span data-ttu-id="8111a-127">Sláið inn eða veldu gildi í reitnum Hamur.</span><span class="sxs-lookup"><span data-stu-id="8111a-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="8111a-128">Sláið inn eða veldu gildi í reitnum Farmflytjandi.</span><span class="sxs-lookup"><span data-stu-id="8111a-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="8111a-129">Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="8111a-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="8111a-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8111a-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="8111a-131">Setja upp endurskoðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="8111a-131">Set up the audit master</span></span>
1. <span data-ttu-id="8111a-132">Fara í flutningsstjórnun > Uppsetningu > afstemmingu Farms > endurskoðunarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="8111a-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="8111a-133">Aðalgögn endurskoðunar skilgreinir mörk verðvikmarka fyrir farmgjöld sjálfvirka afstemmingu.</span><span class="sxs-lookup"><span data-stu-id="8111a-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="8111a-134">Hún tilgreinir með hversu mikið er upphæða á farmbréfið og flutningsaðila reiknings getur verið önnur og leyfa enn afstemmingu að eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="8111a-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="8111a-135">Hann skilgreinir einnig hvernig á að meðhöndla misræmi.</span><span class="sxs-lookup"><span data-stu-id="8111a-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="8111a-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8111a-136">Click New.</span></span>
3. <span data-ttu-id="8111a-137">Í reitinn Kenni endurskoðunarsniðmáts skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8111a-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="8111a-138">Í svæðinu farmflytjanda sendingar, velja sama farmflytjanda sem var áður.</span><span class="sxs-lookup"><span data-stu-id="8111a-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="8111a-139">Í reitnum gerð Farmbréfs skal velja þá gerð farmbréfs sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="8111a-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="8111a-140">Víkkið út hlutann Vikmörk.</span><span class="sxs-lookup"><span data-stu-id="8111a-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="8111a-141">Færið inn tölu í svæðinu Lágmarks vikmörk.</span><span class="sxs-lookup"><span data-stu-id="8111a-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="8111a-142">Færið inn tölu í svæðinu Hámarks vikmörk.</span><span class="sxs-lookup"><span data-stu-id="8111a-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="8111a-143">Víkkið út hlutann Niðurstaða.</span><span class="sxs-lookup"><span data-stu-id="8111a-143">Expand the Result section.</span></span>
10. <span data-ttu-id="8111a-144">Í reitinn Ástæðukóði ofgreiðslu skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="8111a-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="8111a-145">Ef upphæða sem eru mismunandi á farmbréfið og reikning flutningsaðila, tilgreina ofgreiðsla eða vangreiðsla ástæðukóða lykla sem á að skrá muninn á svo lengi sem mismunur er innan stig vikmarka.</span><span class="sxs-lookup"><span data-stu-id="8111a-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="8111a-146">Í reitinn Ástæðukóði vangreiðslu skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="8111a-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="8111a-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8111a-147">Close the page.</span></span>


