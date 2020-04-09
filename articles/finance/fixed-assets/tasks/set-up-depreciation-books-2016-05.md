---
title: Uppsetning afskriftabóka
description: Þessi aðferð gengur í gegnum ferlið við að búa til nýja afskriftabók og tengja hana við fastafjárhóp.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154602"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="0add0-103">Uppsetning afskriftabóka</span><span class="sxs-lookup"><span data-stu-id="0add0-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0add0-104">Þessi aðferð gengur í gegnum ferlið við að búa til nýja afskriftabók og tengja hana við fastafjárhóp.</span><span class="sxs-lookup"><span data-stu-id="0add0-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="0add0-105">Stofna afskriftarbók</span><span class="sxs-lookup"><span data-stu-id="0add0-105">Create a depreciation book</span></span>
1. <span data-ttu-id="0add0-106">Fara í Eignir > Uppsetning > Afskriftarbækur.</span><span class="sxs-lookup"><span data-stu-id="0add0-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="0add0-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0add0-107">Click New.</span></span>
3. <span data-ttu-id="0add0-108">Færa inn gildi í svæðinu afskriftarbók.</span><span class="sxs-lookup"><span data-stu-id="0add0-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="0add0-109">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="0add0-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0add0-110">Merkja eða afmerkja gátreit Reikna afskrift.</span><span class="sxs-lookup"><span data-stu-id="0add0-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="0add0-111">Í reitnum afskriftarregla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0add0-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0add0-112">Í listanum skal finna og velja þá afskriftarregla sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0add0-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="0add0-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0add0-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0add0-114">Í reitnum önnur afskriftarregla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0add0-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0add0-115">Á listanum, skal velja viðeigandi afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="0add0-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="0add0-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0add0-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0add0-117">Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="0add0-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0add0-118">Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.</span><span class="sxs-lookup"><span data-stu-id="0add0-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="0add0-119">Merkja eða afmerkja gátreit Stofna afskriftaleiðréttingar með grunnleiðréttingar .</span><span class="sxs-lookup"><span data-stu-id="0add0-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="0add0-120">Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0add0-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0add0-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0add0-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="0add0-122">Tengið afskriftarbók við eignaflokkur</span><span class="sxs-lookup"><span data-stu-id="0add0-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="0add0-123">Smella á eignaflokkar.</span><span class="sxs-lookup"><span data-stu-id="0add0-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0add0-124">Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0add0-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0add0-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0add0-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0add0-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0add0-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0add0-127">Veljið valkost í svæðinu afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="0add0-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="0add0-128">Í reitinn líftími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="0add0-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0add0-129">Sjáðu að svæðisgildi afskriftartímabils er reiknaður eftir uppsetningu líftíma.</span><span class="sxs-lookup"><span data-stu-id="0add0-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

