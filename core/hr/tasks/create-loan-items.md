--- 
title: "Stofna lánshluti"
description: "Lánshlutir eru færslur sem aðstoða við að rekja efnislegu vörurnar, eins og símar eða tölvur sem fyrirtækið lánar til starfsmanna."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="eded9-103">Stofna lánshluti</span><span class="sxs-lookup"><span data-stu-id="eded9-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eded9-104">Lánshlutir eru færslur sem aðstoða við að rekja efnislegu vörurnar, eins og símar eða tölvur sem fyrirtækið lánar til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="eded9-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="eded9-105">Hver efnislegt vara verður að hafa samsvarandi lánshlut.</span><span class="sxs-lookup"><span data-stu-id="eded9-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="eded9-106">Hvert skrá lánshluts ætti að lýsa hvað er verið að lána, hver er ábyrgur fyrir láni og fjölda daga sem hlutur getur verið í láni.</span><span class="sxs-lookup"><span data-stu-id="eded9-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="eded9-107">Hægt er að stofna marga lánshluti, eins og lykla, aðgangskort eða einkennisbúninga, á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="eded9-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="eded9-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="eded9-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="eded9-109">Stofna gerðir Lána</span><span class="sxs-lookup"><span data-stu-id="eded9-109">Create Loan types</span></span>
1. <span data-ttu-id="eded9-110">Farið í Mannauður > Starfsfólk > Lánshlutir > Gerðir lánshluta.</span><span class="sxs-lookup"><span data-stu-id="eded9-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="eded9-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="eded9-111">Click New.</span></span>
3. <span data-ttu-id="eded9-112">Í reitinn Gerð láns skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eded9-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="eded9-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="eded9-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eded9-114">Færið inn fjölda daga sem hlutir sem úthlutað er á þessa lánsgerð geta verið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="eded9-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="eded9-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="eded9-115">Click Save.</span></span>
7. <span data-ttu-id="eded9-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="eded9-116">Close the page.</span></span>
8. <span data-ttu-id="eded9-117">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="eded9-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="eded9-118">Stofna lánshluti</span><span class="sxs-lookup"><span data-stu-id="eded9-118">Create Loan items</span></span>
1. <span data-ttu-id="eded9-119">Farið í Mannauður > Starfsfólk > Lánshlutir > Lánshlutir.</span><span class="sxs-lookup"><span data-stu-id="eded9-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="eded9-120">Smellt er á stofna Lánshlutur</span><span class="sxs-lookup"><span data-stu-id="eded9-120">Click Create loan items.</span></span>
3. <span data-ttu-id="eded9-121">Í magn.</span><span class="sxs-lookup"><span data-stu-id="eded9-121">In the Qty.</span></span> <span data-ttu-id="eded9-122">færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="eded9-122">field, enter a number.</span></span>
4. <span data-ttu-id="eded9-123">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="eded9-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eded9-124">Í reitnum Gerð láns skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="eded9-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eded9-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="eded9-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="eded9-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="eded9-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eded9-127">Færa inn fjölda daga sem hlutur getur verið í láni.</span><span class="sxs-lookup"><span data-stu-id="eded9-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="eded9-128">Sjálfgefna gildið fyrir Áætlað skila svæði á síðunni Lánsbúnaður er reiknaður sem núgildandi dagsetning plús þessi tala.</span><span class="sxs-lookup"><span data-stu-id="eded9-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="eded9-129">Í reitnum Einstaklingur við stjórn skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="eded9-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="eded9-130">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="eded9-130">Click Select.</span></span>
11. <span data-ttu-id="eded9-131">Í reitinn upphafsgildi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="eded9-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="eded9-132">Í reitinn tímabil skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="eded9-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="eded9-133">Í reitinn snið skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="eded9-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="eded9-134">Til dæmis ef hæsta upphafsnúmer fyrir lánaða vöru er 10 þarf að færa inn tvö númeratákn í reitinn snið.</span><span class="sxs-lookup"><span data-stu-id="eded9-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="eded9-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="eded9-135">Click OK.</span></span>
15. <span data-ttu-id="eded9-136">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="eded9-136">Refresh the page.</span></span>


