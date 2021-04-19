---
title: Stofna runu runueigindir fyrir afurð
description: Þessi verklýsing sýnir hvernig á að stofna runueigind, úthluta sjálfgefin gildissvið, og taka eigindina með í flokk.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5deb35028ee499633fb6b0bb5155df2fd91e643a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820107"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="23afc-103">Stofna runu runueigindir fyrir afurð</span><span class="sxs-lookup"><span data-stu-id="23afc-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23afc-104">Þessi verklýsing sýnir hvernig á að stofna runueigind, úthluta sjálfgefin gildissvið, og taka eigindina með í flokk.</span><span class="sxs-lookup"><span data-stu-id="23afc-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="23afc-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er the USP2 fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="23afc-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="23afc-106">Fara í Birgðastjórnun > Uppsetning > Runa > Runueigindir.</span><span class="sxs-lookup"><span data-stu-id="23afc-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="23afc-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23afc-107">Click New.</span></span>
3. <span data-ttu-id="23afc-108">Í reitinn Eigind skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23afc-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="23afc-109">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23afc-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23afc-110">Veljið gerðina 'Brot' í svæðinu gerð eigindar.</span><span class="sxs-lookup"><span data-stu-id="23afc-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="23afc-111">Þetta ferli notar gerðina brot til að virkja tugagildi.</span><span class="sxs-lookup"><span data-stu-id="23afc-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="23afc-112">Hægt er að velja aðrar gerðir eiginda.</span><span class="sxs-lookup"><span data-stu-id="23afc-112">You can select other attribute types.</span></span> <span data-ttu-id="23afc-113">Ef velja gerðina tölusetning verður að færa inn gildi í listanum tölusetning áður en hægt er að færa inn gildi í markreit.</span><span class="sxs-lookup"><span data-stu-id="23afc-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="23afc-114">Í reitinn Lágmark skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23afc-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="23afc-115">Í reitinn Hámark skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23afc-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="23afc-116">Í reitinn Hækka skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23afc-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="23afc-117">Í reitinn Mark skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23afc-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="23afc-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23afc-118">Click Save.</span></span>
11. <span data-ttu-id="23afc-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23afc-119">Close the page.</span></span>
12. <span data-ttu-id="23afc-120">Fara í Birgðastjórnun > Uppsetning > Runa > Runueigindaflokkar.</span><span class="sxs-lookup"><span data-stu-id="23afc-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="23afc-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23afc-121">Click New.</span></span>
14. <span data-ttu-id="23afc-122">Færa inn gildi í svæðinu eigindaflokkur.</span><span class="sxs-lookup"><span data-stu-id="23afc-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="23afc-123">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23afc-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="23afc-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23afc-124">Click Save.</span></span>
17. <span data-ttu-id="23afc-125">Smellið á eigindir Flokka.</span><span class="sxs-lookup"><span data-stu-id="23afc-125">Click Group attributes.</span></span>
18. <span data-ttu-id="23afc-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23afc-126">Click New.</span></span>
19. <span data-ttu-id="23afc-127">Í reitnum Eigind skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="23afc-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="23afc-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23afc-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="23afc-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="23afc-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23afc-130">Hægt er að taka eigind með í alla flokkana.</span><span class="sxs-lookup"><span data-stu-id="23afc-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="23afc-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23afc-131">Click Save.</span></span>
23. <span data-ttu-id="23afc-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23afc-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]