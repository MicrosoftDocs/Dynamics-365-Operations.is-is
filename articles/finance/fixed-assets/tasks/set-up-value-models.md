---
title: Setja upp virðislíkön
description: Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a528bd12552d5ce100027c9a789f6e1bdc597b66
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186855"
---
# <a name="set-up-value-models"></a><span data-ttu-id="1efe5-103">Setja upp virðislíkön</span><span class="sxs-lookup"><span data-stu-id="1efe5-103">Set up value models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1efe5-104">Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="1efe5-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="1efe5-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="1efe5-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="1efe5-106">Búa til bók</span><span class="sxs-lookup"><span data-stu-id="1efe5-106">Create a book</span></span>
1. <span data-ttu-id="1efe5-107">Fara í Eignir > Uppsetning > Bækur.</span><span class="sxs-lookup"><span data-stu-id="1efe5-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="1efe5-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1efe5-108">Click New.</span></span>
3. <span data-ttu-id="1efe5-109">Í reitinn Bók skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1efe5-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="1efe5-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="1efe5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1efe5-111">Þegar Reikna afskrift er valin verða tengdar bækur eigna teknar með í afskriftartillögur.</span><span class="sxs-lookup"><span data-stu-id="1efe5-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="1efe5-112">Ef hann er ekki valinn verða bókin ekki sjálfkrafa afskrifa.</span><span class="sxs-lookup"><span data-stu-id="1efe5-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="1efe5-113">Velja skal Já í Reikna út afskriftir reitnum.</span><span class="sxs-lookup"><span data-stu-id="1efe5-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="1efe5-114">Sláið inn eða veldu gildi í reitnum Afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="1efe5-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="1efe5-115">Önnur afskriftarregla er einnig þekkt sem umskiptingaraðferð afskriftar.</span><span class="sxs-lookup"><span data-stu-id="1efe5-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="1efe5-116">Afskriftatillögu verður skipta yfir í þessa forstillingu þegar önnur forstilling reiknar afskriftarupphæð sem er jöfn eða meiri en sjálfgefinn afskriftareglu.</span><span class="sxs-lookup"><span data-stu-id="1efe5-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="1efe5-117">Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="1efe5-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="1efe5-118">Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.</span><span class="sxs-lookup"><span data-stu-id="1efe5-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="1efe5-119">Ef Stofna afskriftaleiðréttingar með grunnleiðréttingum er valinn, afskriftaleiðréttingar sjálfkrafa stofnuð þegar virði eignar er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="1efe5-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="1efe5-120">Ef það er ekki valinn er mun uppfært virði eignarinnar aðeins hafa áhrif á afskriftaútreikninga fram á við.</span><span class="sxs-lookup"><span data-stu-id="1efe5-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="1efe5-121">Veldu Já í reitnum Stofna afskriftaleiðréttingar með grunnleiðréttingum</span><span class="sxs-lookup"><span data-stu-id="1efe5-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="1efe5-122">Að sjálfgefnu eru færslur eignabókar bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="1efe5-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="1efe5-123">Hægt er að gera bókun í fjárhag fyrir bók óvirka með því að stilla reitinn Bóka í fjárhag á nei.</span><span class="sxs-lookup"><span data-stu-id="1efe5-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="1efe5-124">Bækur sem bóka ekki í fjárhag eru vanalega notaðar fyrir skattskýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="1efe5-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="1efe5-125">Þetta gefur viðbótar sveigjanleika til að eyða sögulegum færslum fyrir eignabók þar sem þær hafa ekki verið bundnar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="1efe5-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="1efe5-126">Sjálfgefið bókunarlag fer á Núverandi lag ef bókin er bókuð í fjárhag, en Ekkert ef það er ekki bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="1efe5-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="1efe5-127">Uppfæra bókunarlag ef nauðsynlegt er fyrir þetta bók til að bóka í öðru lagi.</span><span class="sxs-lookup"><span data-stu-id="1efe5-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="1efe5-128">Sláið inn eða veldu gildi í reitnum dagatal.</span><span class="sxs-lookup"><span data-stu-id="1efe5-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="1efe5-129">Afleiddar afskriftabækur munu bóka færslur á mismunandi bækur í einu.</span><span class="sxs-lookup"><span data-stu-id="1efe5-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="1efe5-130">Færslur eru stofnaðar með aðalbókinni og á meðan á bókun stendur, er nákvæmt afrit færslunnar bókað í afleiddu bókina.</span><span class="sxs-lookup"><span data-stu-id="1efe5-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="1efe5-131">Ekki eru framkvæmdir endurreikningar með færslum afleiddrar bókar, svo ekki ætti að nota hana fyrir afskriftarfærslur.</span><span class="sxs-lookup"><span data-stu-id="1efe5-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="1efe5-132">Tengið bók við eignaflokk</span><span class="sxs-lookup"><span data-stu-id="1efe5-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="1efe5-133">Smella á eignaflokkar.</span><span class="sxs-lookup"><span data-stu-id="1efe5-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="1efe5-134">Færa inn eða veljið gildi í svæðinu eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="1efe5-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="1efe5-135">Í reitinn líftími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="1efe5-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="1efe5-136">Athugaðu að afskriftartímabils er reiknað eftir uppsetningu líftíma.</span><span class="sxs-lookup"><span data-stu-id="1efe5-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="1efe5-137">Er hægt að setja afskriftarreglan eins og krafist er hvað varðar skatta.</span><span class="sxs-lookup"><span data-stu-id="1efe5-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  

